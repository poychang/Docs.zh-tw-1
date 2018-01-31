---
title: "-errorreport (C# 編譯器選項)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords: /errorreport
helpviewer_keywords:
- -errorreport compiler option [C#]
- errorreport compiler option [C#]
- /errorreport compiler option [C#]
ms.assetid: bd0e7493-b79d-4369-9c3f-ba26ebdfbedf
caps.latest.revision: "35"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 6d2fcb3f0bf4491de23b70c8beebf7ae495b2aa0
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2018
---
# <a name="-errorreport-c-compiler-options"></a>-errorreport (C# 編譯器選項)
此選項提供將 C# 編譯器內部錯誤回報給 Microsoft 的便利方式。  
  
> [!NOTE]
>  在 Windows Vista 和 Windows Server 2008 上，您為 Visual Studio 建立的錯誤報告設定不會覆寫透過 Windows 錯誤報告 (WER) 所做的設定。 WER 設定一律優先於 Visual Studio 錯誤報告設定。  
  
## <a name="syntax"></a>語法  
  
```console  
-errorreport:{ none | prompt | queue | send }  
```  
  
## <a name="arguments"></a>引數  
 **none**  
 將不會收集有關內部編譯器錯誤的報告，也不會將報告傳送給 Microsoft。  
  
 **提示**  
 提示您在收到內部編譯器錯誤時傳送報告。 **提示**是您在開發環境中編譯應用程式的預設值。  
  
 **queue**  
 佇列錯誤報告。 當您使用系統管理認證登入時，您可以報告自上次登入後的任何失敗。 系統提示您傳送錯誤報告的頻率，最多三天一次。 **佇列**是您在命令列編譯應用程式的預設值。  
  
 **傳送**  
 自動向 Microsoft 傳送內部編譯器錯誤報告。 若要啟用此選項，您必須先同意 Microsoft 資料收集原則。 第一次在電腦上指定 **-errorreport:send** 時，編譯器訊息會請您參考包含 Microsoft 資料收集原則的網站。  
    
## <a name="remarks"></a>備註  
 編譯器無法處理原始程式碼檔案時，就會出現編譯器內部錯誤 (ICE)。 發生 ICE 時，編譯器不會產生輸出檔或任何有用的診斷，無法讓您修正程式碼。  
  
 在舊版中，當您收到 ICE 時，我們鼓勵您連絡 Microsoft 產品支援服務回報問題。 您可以使用 **-errorreport** 向 Visual C# 小組提供 ICE 資訊。 您的錯誤報告有助於改善未來的編譯器版本。  
  
 使用者能否傳送報告，取決於電腦和使用者原則權限。  
  
 如需錯誤偵錯工具的詳細資訊，請參閱 [Dr. Watson for Windows (Drwtsn32.exe) 工具的說明](https://support.microsoft.com/help/308538/description-of-the-dr--watson-for-windows-drwtsn32-exe-tool)。  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 開發環境中設定這個編譯器選項  
  
1.  開啟專案的 [屬性] 頁面。 如需詳細資訊，請參閱[專案設計工具、建置頁 (C#)](/visualstudio/ide/reference/build-page-project-designer-csharp)。  
  
2.  按一下 [建置] 屬性頁面。  
  
3.  按一下 [ **進階** ] 按鈕。  
  
4.  修改**報告編譯器內部錯誤**屬性。  
  
 如需如何以程式設計方式設定這個編譯器選項的詳細資訊，請參閱 <xref:VSLangProj80.CSharpProjectConfigurationProperties3.ErrorReport%2A>。  
  
## <a name="see-also"></a>請參閱  
 [C# 編譯器選項](../../../csharp/language-reference/compiler-options/index.md)
