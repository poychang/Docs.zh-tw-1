---
title: "平行 LINQ (PLINQ)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: PLINQ, overview
ms.assetid: 3d4d0cd3-bde4-490b-99e7-f4e41be96455
caps.latest.revision: "17"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c0028d3d8c30bbc7f0592a4462ca1eeb80c8b1f9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="parallel-linq-plinq"></a>平行 LINQ (PLINQ)
Parallel LINQ (PLINQ) 是平行實作的 LINQ to Objects。 PLINQ 當成擴充方法的實作一組完整的 LINQ 標準查詢運算子<xref:System.Linq>命名空間以及有其他運算子的平行作業。 PLINQ 結合了 LINQ 語法簡單易懂的特性以及平行程式設計的威力。 和以工作平行程式庫為目標的程式碼一樣，PLINQ 查詢會根據主機電腦的能力來以並行程度縮放。  
  
 在許多情況下，PLINQ 可以更有效率地使用主機電腦上的所有可用核心，來大幅增加 LINQ to Objects 查詢的速度。 提升效能可為桌面帶來高效能的計算能力。  
  
## <a name="in-this-section"></a>本章節內容  
 [PLINQ 簡介](../../../docs/standard/parallel-programming/introduction-to-plinq.md)  
  
 [認識 PLINQ 中的加速](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md)  
  
 [PLINQ 中的順序保留](../../../docs/standard/parallel-programming/order-preservation-in-plinq.md)  
  
 [PLINQ 中的合併選項](../../../docs/standard/parallel-programming/merge-options-in-plinq.md)  
  
 [如何：建立並執行簡單的 PLINQ 查詢](../../../docs/standard/parallel-programming/how-to-create-and-execute-a-simple-plinq-query.md)  
  
 [操作說明：控制 PLINQ 查詢中的順序](../../../docs/standard/parallel-programming/how-to-control-ordering-in-a-plinq-query.md)  
  
 [操作說明：結合平行和循序 LINQ 查詢](../../../docs/standard/parallel-programming/how-to-combine-parallel-and-sequential-linq-queries.md)  
  
 [操作說明：處理 PLINQ 查詢中的例外狀況](../../../docs/standard/parallel-programming/how-to-handle-exceptions-in-a-plinq-query.md)  
  
 [操作說明：取消 PLINQ 查詢](../../../docs/standard/parallel-programming/how-to-cancel-a-plinq-query.md)  
  
 [操作說明：撰寫自訂 PLINQ 彙總函式](../../../docs/standard/parallel-programming/how-to-write-a-custom-plinq-aggregate-function.md)  
  
 [操作說明：在 PLINQ 中指定執行模式](../../../docs/standard/parallel-programming/how-to-specify-the-execution-mode-in-plinq.md)  
  
 [操作說明：在 PLINQ 中指定合併選項](../../../docs/standard/parallel-programming/how-to-specify-merge-options-in-plinq.md)  
  
 [操作說明：使用 PLINQ 逐一查看檔案目錄](../../../docs/standard/parallel-programming/how-to-iterate-file-directories-with-plinq.md)  
  
 [操作說明：測量 PLINQ 查詢效能](../../../docs/standard/parallel-programming/how-to-measure-plinq-query-performance.md)  
  
 [PLINQ 資料範例](../../../docs/standard/parallel-programming/plinq-data-sample.md)  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Linq.ParallelEnumerable>  
 [平行程式設計](../../../docs/standard/parallel-programming/index.md)  
 [LINQ (Language-Integrated Query)](http://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)
