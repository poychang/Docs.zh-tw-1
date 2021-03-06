---
title: "using static 指示詞 (C# 參考)"
ms.date: 03/10/2017
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords: using static directive [C#]
ms.assetid: 8b8f9e34-c75e-469b-ba85-6f2eb4090314
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5838bede475cf2ad1b72518770241e86206a06bb
ms.sourcegitcommit: 7e99f66ef09d2903e22c789c67ff5a10aa953b2f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2017
---
# <a name="using-static-directive-c-reference"></a>using static 指示詞 (C# 參考)

`using static` 指示詞指定了一種類型，讓您不需要指定類型名稱，即可存取其靜態成員。 它的語法為：

```csharp
using static <fully-qualified-type-name>
```

其中 *fully-qualified-type-name* 是不需要指定類型名稱，即可參考其靜態成員之類型的名稱。 如果您未提供完整類型名稱 (完整命名空間名稱及類型名稱)，C# 會產生編譯器錯誤 CS0246：「找不到類型或命名空間名稱 '<type-name>'」。

`using static` 指示詞會套用至任何具有靜態成員的類型，即使該類型同時具有執行個體成員也一樣。 不過，執行個體成員只能透過類型執行個體叫用。

`using static` 指示詞是在 C# 6 中引進。

## <a name="remarks"></a>備註
 
一般而言，當您呼叫靜態成員時，您會提供類型名稱及成員名稱。 重複輸入相同的類型名稱來叫用類型的成員，可能會導致冗長且難以理解的程式碼。 例如，`Circle` 類別的下列定義參考了 <xref:System.Math> 類別的一些成員。
  
[!code-csharp[using-static#1](../../../../samples/snippets/csharp/language-reference/keywords/using/using-static1.cs#1)]

`using static` 指示詞可避免每次參考成員時都必須明確參考 <xref:System.Math> 類別，因此所產生的程式碼會更簡潔：

[!code-csharp[using-static#2](../../../../samples/snippets/csharp/language-reference/keywords/using/using-static2.cs#1)]

`using static` 只會匯入指定的類型中宣告的可存取靜態成員和巢狀類型。  不會匯入繼承的成員。  您可以使用 using 靜態指示詞從任何具名類型匯入，包括 Visual Basic 模組。  如果 F# 最上層函式出現在中繼資料中，作為具名類型的靜態成員，其名稱是有效的 C# 識別項，則可以匯入 F# 函式。  
  
 `using static` 讓您在可供擴充方法查閱使用的指定類型中宣告擴充方法。  不過，擴充方法的名稱不會匯入程式碼中未限定參考的範圍。  
  
 在相同編譯單位或命名空間中透過不同 `using static` 指示詞從不同的類型匯入、具有相同名稱的方法會形成方法群組。  這些方法群組內的多載解析會遵循一般的 C# 規則。  
  
## <a name="example"></a>範例

下列範例使用 `using static` 指示詞來提供 <xref:System.Console>、<xref:System.Math> 和 <xref:System.String> 類別的靜態成員，而不需要指定其類型名稱。

[!code-csharp[using-static#3](../../../../samples/snippets/csharp/language-reference/keywords/using/using-static3.cs)]

在此範例中，`using static` 指示詞也可能已套用至 <xref:System.Double> 類型。 這會使它可以呼叫<xref:System.Double.TryParse(System.String,System.Double@)>方法，而不指定型別名稱。 不過，這會建立難以閱讀的程式碼，因為您必須檢查 `using static` 陳述式，以判斷呼叫了哪一個數字類型的 `TryParse` 方法。

## <a name="see-also"></a>請參閱

[using 指示詞](using-directive.md)   
[C# 參考](../../../csharp/language-reference/index.md)   
[C# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
[使用命名空間](../../../csharp/programming-guide/namespaces/using-namespaces.md)   
[命名空間關鍵字](../../../csharp/language-reference/keywords/namespace-keywords.md)   
[命名空間](../../../csharp/programming-guide/namespaces/index.md)   
