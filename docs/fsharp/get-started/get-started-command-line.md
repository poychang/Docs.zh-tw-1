---
title: "開始使用 F # 的命令列工具"
description: "跨平台.NET Core CLI 與了解如何使用 F # 在 Windows、 MacOS （Linux） 的任何作業系統上。"
keywords: "Visual F#, F#, 函式程式設計, .NET, .NET Core"
author: cartermp
ms.author: phcart
ms.date: 06/14/2017
ms.topic: article
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 615db1ec-6ef3-4de2-bae6-4586affa9771
ms.openlocfilehash: 4820a8a306bd478429b497a8b7c70ff170c1c655
ms.sourcegitcommit: d095094e942eedf09530ea5636fbaf9029853027
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2017
---
# <a name="get-started-with-f-with-the-net-core-cli"></a>開始使用 F # 和.NET 核心 CLI

本文件涵蓋如何您可以使用 F # 的.NET Core CLI 開始 （Windows、 macOS 或 Linux） 的任何作業系統上。 它將會經歷建置在多專案方案中的使用主控台應用程式會呼叫類別庫。

## <a name="prerequisites"></a>必要條件

若要開始，您必須安裝[.NET Core 1.0 或更新版本的 SDK](https://dot.net/core)。 沒有需要解除安裝舊版的.NET Core SDK，因為它支援由並存安裝。

本文假設您知道如何使用命令列，並以慣用的文字編輯器。 如果您已不使用它， [Visual Studio Code](https://code.visualstudio.com)是絕佳的選項為 F # 的文字編輯器。 若要取得實用的功能，如 IntelliSense、 更佳語法反白顯示，以及更多，您可以下載[Ionide 延伸](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp)。

## <a name="building-a-simple-multi-project-solution"></a>建立簡單的多專案方案

開啟命令提示字元/終端機，並使用`dotnet new`命令以建立新的方案檔稱為`FSNetCore`:

```
dotnet new sln -o FSNetCore
```

只要命令完成，則會產生下列目錄結構：

```
FSNetCore
    ├── FSNetCore.sln
```

將目錄變更為*FSNetCore*然後開始將專案加入至方案資料夾。
 
### <a name="writing-a-class-library"></a>撰寫類別程式庫

使用`dotnet new`命令，建立類別庫專案中的**src**名為程式庫的資料夾。 

```bash
dotnet new lib -lang F# -o src/Library 
```

只要命令完成，則會產生下列目錄結構：

```
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

取代內容`Library.fs`為下列：

```fsharp
module Library

open Newtonsoft.Json

let getJsonNetJson value = 
    sprintf "I used to be %s but now I'm %s thanks to JSON.NET!" value  (JsonConvert.SerializeObject(value))
```

將 Newtonsoft.Json NuGet 套件加入至程式庫專案。

```bash
dotnet add src/Library/Library.fsproj package Newtonsoft.Json
```

新增`Library`專案加入`FSNetCore`方案中使用`dotnet sln add`命令：

```bash
dotnet sln add src/Library/Library.fsproj
```

還原 NuGet 相依性， `dotnet restore` ([請參閱附註](#dotnet-restore-note)) 並執行`dotnet build`建置專案。

### <a name="writing-a-console-application-which-consumes-the-class-library"></a>撰寫主控台應用程式耗用類別庫

使用`dotnet new`命令，請建立主控台應用程式中的**src**名為應用程式的資料夾。 

```bash
dotnet new console -lang F# -o src/App 
```

只要命令完成，則會產生下列目錄結構：

```
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        ├── App
        │   ├── App.fsproj
        │   ├── Program.fs
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

變更`Program.fs`至：

```fsharp
open System
open Library

[<EntryPoint>]
let main argv = 
    printfn "Nice command-line arguments! Here's what JSON.NET has to say about them:"

    argv
    |> Array.map getJsonNetJson
    |> Array.iter (printfn "%s")

    0 // return an integer exit code
```

將參考加入`Library`專案使用`dotnet add reference`。

```bash
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
```

新增`App`專案加入`FSNetCore`方案中使用`dotnet sln add`命令：

```bash
dotnet sln add src/App/App.fsproj
```

還原 NuGet 相依性， `dotnet restore` ([請參閱附註](#dotnet-restore-note)) 並執行`dotnet build`建置專案。

將目錄切換到`src/App`主控台專案並執行專案傳遞`Hello World`做為引數。

```bash
cd src/App
dotnet run Hello World
``` 

您應該會看到下列結果：

```
Nice command-line arguments! Here's what JSON.NET has to say about them:

I used to be Hello but now I'm ""Hello"" thanks to JSON.NET!
I used to be World but now I'm ""World"" thanks to JSON.NET!
```
<a name="dotnet-restore-note"></a>
[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]
