---
title: "如何：在 DataContext 層級篩選"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 15505cd7-0df2-427a-9f86-e0f96f60ee2e
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: e7ff6bf048b5303565cd8c6c1c7448a47a89fc22
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/17/2018
---
# <a name="how-to-filter-at-the-datacontext-level"></a>如何：在 DataContext 層級篩選
您可以在 `EntitySets` 層級篩選 `DataContext`。 這類篩選會套用至所有使用該 <xref:System.Data.Linq.DataContext> 執行個體的查詢。  
  
## <a name="example"></a>範例  
 在下列範例中，會使用 <xref:System.Data.Linq.DataLoadOptions.AssociateWith%28System.Linq.Expressions.LambdaExpression%29?displayProperty=nameWithType> 以根據 `ShippedDate` 來篩選客戶的預先載入訂單。  
  
 [!code-csharp[DLinqQueryConcepts#10](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#10)]
 [!code-vb[DLinqQueryConcepts#10](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#10)]  
  
## <a name="see-also"></a>請參閱  
 [查詢概念](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
