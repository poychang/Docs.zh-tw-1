---
title: "如何：從 Windows Form DomainUpDown 控制項中移除項目"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DomainUpDown control [Windows Forms], removing items from
- spin button control [Windows Forms], removing items
ms.assetid: e70f5cbc-b497-41a9-975a-344c00e56ed2
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 17972aa9cb1626793ab04d317bb66d2774899cfc
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-remove-items-from-windows-forms-domainupdown-controls"></a>如何：從 Windows Form DomainUpDown 控制項中移除項目
您可以移除 Windows Form 中的項目<xref:System.Windows.Forms.DomainUpDown>藉由呼叫控制項<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A>或<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A>方法<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection>類別。 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A>方法移除特定的項目，雖然<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A>方法中移除項目依其位置。  
  
### <a name="to-remove-an-item"></a>若要移除項目  
  
-   使用<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A>方法<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection>類別依名稱移除項目。  
  
    ```vb  
    DomainUpDown1.Items.Remove("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Remove("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Remove("noodles");  
    ```  
  
     -或-  
  
-   使用<xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A>方法，以移除項目依其位置。  
  
    ```vb  
    ' Removes the first item in the list.  
    DomainUpDown1.Items.RemoveAt(0)  
    ```  
  
    ```csharp  
    // Removes the first item in the list.  
    domainUpDown1.Items.RemoveAt(0);  
    ```  
  
    ```cpp  
    // Removes the first item in the list.  
    domainUpDown1->Items->RemoveAt(0);  
    ```  
  
## <a name="see-also"></a>請參閱  
 <xref:System.Windows.Forms.DomainUpDown>  
 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A?displayProperty=nameWithType>  
 [DomainUpDown 控制項](../../../../docs/framework/winforms/controls/domainupdown-control-windows-forms.md)  
 [DomainUpDown 控制項概觀](../../../../docs/framework/winforms/controls/domainupdown-control-overview-windows-forms.md)
