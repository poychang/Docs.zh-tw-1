---
title: DbProviderFactory
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2a8e2640-3a49-42a1-a3a9-b43026907ae1
caps.latest.revision: "3"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 3e42682a466d778a83981cd6dd0d9daeecef8822
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/17/2018
---
# <a name="dbproviderfactories"></a>DbProviderFactory
<xref:System.Data.Common> 命名空間 (Namespace) 提供類別 (Class)，可用於建立 <xref:System.Data.Common.DbProviderFactory> 執行個體 (Instance) 以使用特定的資料來源。 當您建立 <xref:System.Data.Common.DbProviderFactory> 執行個體並將資料提供者相關資訊傳遞給它時，`DbProviderFactory` 可以根據所提供的資訊來決定要傳回的正確強型別 (Strongly Typed) 物件。  
  
 從 .NET Framework 版本 4 開始，資料提供者 (例如：<xref:System.Data.Odbc>, <xref:System.Data.OleDb>、<xref:System.Data.SqlClient> 及 <xref:System.Data.OracleClient>) 不會再列於 machine.config 檔案中，但自訂提供者會繼續列於該檔案中。  
  
## <a name="in-this-section"></a>本節內容  
 [處理站模型概觀](../../../../docs/framework/data/adonet/factory-model-overview.md)  
 提供 Factory 設計模式和程式設計介面的概觀。  
  
 [取得 DbProviderFactory](../../../../docs/framework/data/adonet/obtaining-a-dbproviderfactory.md)  
 示範如何列出已安裝的資料提供者，以及如何從 <xref:System.Data.Common.DbConnection> 建立 `DbProviderFactory`。  
  
 [DbConnection、DbCommand 和 DbException](../../../../docs/framework/data/adonet/dbconnection-dbcommand-and-dbexception.md)  
 示範如何建立 <xref:System.Data.Common.DbCommand> 和 <xref:System.Data.Common.DbDataReader>，以及如何使用 <xref:System.Data.Common.DbException> 處理資料錯誤。  
  
 [使用 DbDataAdapter 修改資料](../../../../docs/framework/data/adonet/modifying-data-with-a-dbdataadapter.md)  
 示範如何使用具有 <xref:System.Data.Common.DbCommandBuilder> 的 <xref:System.Data.Common.DbDataAdapter> 擷取及修改資料。  
  
## <a name="see-also"></a>請參閱  
 [在 ADO.NET 中擷取和修改資料](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [ADO.NET Managed 提供者和 DataSet 開發人員中心](http://go.microsoft.com/fwlink/?LinkId=217917)
