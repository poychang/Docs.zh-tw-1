---
title: "無法寫入記錄檔，因為如果寫入，可用磁碟空間會減少到 ReservedSpace 值以下"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vbrApplicationLog_ReservedSpaceEncroached
ms.assetid: 95832e70-4ecc-47aa-90c1-f35c4d468151
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 486f27efe5da0a5d663e7bdae9d5789df4add4e7
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/21/2017
---
# <a name="unable-to-write-to-log-file-because-writing-to-it-would-reduce-free-disk-space-below-reservedspace-value"></a>無法寫入記錄檔，因為如果寫入，可用磁碟空間會減少到 ReservedSpace 值以下
<xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> 類別無法寫入記錄檔，因為：  
  
-   可用磁碟空間數量 (以位元組為單位) 小於 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A> 屬性的值  
  
     —且—  
  
-   <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A> 屬性的值是 <xref:Microsoft.VisualBasic.Logging.DiskSpaceExhaustedOption.ThrowException>。  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1.  封存現有的記錄檔並將其從電腦中移除，讓 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> 物件可以建立新的記錄檔。  
  
2.  將 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A> 屬性的值變更為較小的數字，以保留較少的磁碟空間。  
  
3.  將 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A> 屬性設定為 <xref:Microsoft.VisualBasic.Logging.DiskSpaceExhaustedOption.DiscardMessages> ，以在可用磁碟空間不足時，捨棄訊息而不發出警告。  
  
## <a name="see-also"></a>請參閱  
 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.ReserveDiskSpace%2A>  
 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.DiskSpaceExhaustedBehavior%2A>  
 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener>  
 [My.Application.Log](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)  
 [My.Application.Info.DirectoryPath](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
