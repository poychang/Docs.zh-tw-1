---
title: "PrintDialog 元件概觀 (Windows Form)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: PrintDialog
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], about PrintDialog component
ms.assetid: 8327b8ac-1017-4b5e-a88b-fea9dd56999c
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 0b90d94165de6985b43d47809ae57bfcae204f0b
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/22/2017
---
# <a name="printdialog-component-overview-windows-forms"></a>PrintDialog 元件概觀 (Windows Form)
Windows Form [PrintDialog](../../../../docs/framework/winforms/controls/printdialog-component-windows-forms.md)元件是預先設定的對話方塊，用來選取印表機、 選擇要列印的頁面以及決定 Windows 架構應用程式中的其他列印相關設定。 使用它做為印表機和列印相關設定選擇的簡單解決方案，就不需設定您自己的對話方塊。 您可以讓使用者列印文件中的許多部分： 列印全部、 列印選取的頁面範圍或列印選取的範圍。 藉由標準 Windows 對話方塊，建立使用者可立即熟悉基本功能的應用程式。 <xref:System.Windows.Forms.PrintDialog>元件繼承自<xref:System.Windows.Forms.CommonDialog>類別。  
  
## <a name="working-with-the-component"></a>使用元件  
 使用<xref:System.Windows.Forms.CommonDialog.ShowDialog%2A>方法，以在執行階段顯示的對話方塊。 這個元件有與其中一個列印工作的屬性 (<xref:System.Drawing.Printing.PrintDocument>類別) 或個別的印表機設定 (<xref:System.Drawing.Printing.PrinterSettings>類別)。 任一種，接著，會共用由多部印表機。  
  
 當加入至表單，<xref:System.Windows.Forms.PrintDialog>元件會出現在 Windows Form 設計工具底部的紙匣。  
  
## <a name="see-also"></a>請參閱  
 <xref:System.Windows.Forms.PrintDialog>  
 [PrintDialog 元件](../../../../docs/framework/winforms/controls/printdialog-component-windows-forms.md)
