---
title: "ICorDebugChain::GetActiveFrame 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugChain.GetActiveFrame
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugChain::GetActiveFrame
helpviewer_keywords:
- ICorDebugChain::GetActiveFrame method [.NET Framework debugging]
- GetActiveFrame method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 36887017-670b-4f21-b406-8fab956f84a3
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 7498e031b74bd904b908342b663e4421432e6d95
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugchaingetactiveframe-method"></a>ICorDebugChain::GetActiveFrame 方法
取得作用中 (也就是最新) 鏈結上的框架。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
#### <a name="parameters"></a>參數  
 `ppFrame`  
 [out]ICorDebugFrame 物件，表示使用中的位址指標 (也就是最新) 鏈結上的框架。  
  
## <a name="remarks"></a>備註  
 如果沒有受管理的堆疊框架，則`ppFrame`設為 null。  
  
 如果找不到使用中畫面格，則呼叫會成功並`ppFrame`將會是 null。 使用中框架將會無法使用鏈結 CHAIN_ENTER_UNMANAGED，因為起始，因為 CHAIN_CLASS_INIT 起始部分鏈結。 請參閱 CorDebugChainReason 列舉。  
  
## <a name="requirements"></a>需求  
 **平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** CorDebug.idl、 CorDebug.h  
  
 **程式庫：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
