---
title: "泛型型別參數 (C# 程式設計手冊)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- generics [C#], type parameters
- type parameters [C#]
ms.assetid: a03b0ab2-0606-4b41-b7bf-e64d5bb4d18f
caps.latest.revision: "23"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: b32db7eb6e7788167e110a91726e9dbfe19f31ba
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="generic-type-parameters-c-programming-guide"></a>泛型型別參數 (C# 程式設計手冊)
在泛型型別或方法定義中，當型別參數具現化泛型型別的變數時，它們是用戶端指定之特定類型的預留位置。 泛型類別，例如[泛型簡介](../../../csharp/programming-guide/generics/introduction-to-generics.md)中所列的 `GenericList<T>`，不能以現況使用，因為它其實不是類型，更像是類型的藍圖。 若要使用 `GenericList<T>`，用戶端程式碼必須在角括弧內指定型別引數，宣告並具現化建構的類型。 此特定類別的型別引數可以是由編譯器辨識出的任何類型。 您可以建立任何數目的建構類型執行個體，每一個使用不同的型別引數，如下所示：  
  
 [!code-csharp[csProgGuideGenerics#7](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_1.cs)]  
  
 這些 `GenericList<T>` 執行個體的每一個中，類別中出現的每個 `T`，在執行階段都會被型別引數取代。 透過這個替代，我們已經使用單一類別定義建立了三個類型安全且有效率的不同物件。 如需 CLR 如何執行此替代的詳細資訊，請參閱[執行階段中的泛型](../../../csharp/programming-guide/generics/generics-in-the-run-time.md)。  
  
## <a name="type-parameter-naming-guidelines"></a>型別參數命名方針  
  
-   **務必**使用描述性的名稱命名泛型型別參數，除非單一字母名稱足以表明，而且描述性名稱不會新增值。  
  
     [!code-csharp[csProgGuideGenerics#8](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_2.cs)]  
  
-   單一字母型別參數的類型**請考慮**使用 T 做為型別參數名稱。  
  
     [!code-csharp[csProgGuideGenerics#9](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_3.cs)]  
  
-   描述性型別參數名稱前面**務必**加上 "T"。  
  
     [!code-csharp[csProgGuideGenerics#10](../../../csharp/programming-guide/generics/codesnippet/CSharp/generic-type-parameters_4.cs)]  
  
-   **請考慮**在參數名稱中指出放在型別參數上的條件約束。 例如，參數的條件約束為 `ISession` 可能稱為 `TSession`。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Collections.Generic>  
 [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
 [泛型](../../../csharp/programming-guide/generics/index.md)  
 [C++ 範本和 C# 泛型之間的差異](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)
