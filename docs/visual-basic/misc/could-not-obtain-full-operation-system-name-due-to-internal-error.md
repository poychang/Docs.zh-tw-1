---
title: "由於內部錯誤，無法取得完整作業系統名稱"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: c67d47126718c3d90d853add61b7d06aaf84fc70
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/21/2017
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a>由於內部錯誤，無法取得完整作業系統名稱
由於內部錯誤，無法取得完整作業系統名稱。 這可能是因為目前電腦上沒有 WMI 存在所造成。  
  
 呼叫 `My.Computer.Info.OSFullName` 屬性失敗。 如果目前電腦上未安裝 Windows Management Instrumentation (WMI)，就可能會發生這項失敗。  
  
## <a name="to-correct-this-error"></a>更正這個錯誤  
  
1.  將包圍呼叫的 `Try...Catch` 區塊加入 `My.Computer.Info.OSFullName` 屬性中。  
  
2.  如需 WMI 及其安裝它的詳細資訊，請移至，並搜尋"Windows Management Instrumentation Core"。  
  
## <a name="see-also"></a>請參閱  
 [My.Computer.Info.OSFullName](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)  
 [例外狀況和 Visual Basic 中的錯誤處理](http://msdn.microsoft.com/en-us/3e351e73-cf23-40ab-8b60-05794160529e)  
 [Try...Catch...Finally 陳述式](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
