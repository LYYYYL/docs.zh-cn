---
title: 4206 - UnlockInstanceException
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5a46dc5f-d517-4135-8905-25a42f01206b
caps.latest.revision: "2"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 349844edb44e547a666f10c8d210d120ebf5a39f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="4206---unlockinstanceexception"></a>4206 - UnlockInstanceException
## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|4206|  
|关键字|WFInstanceStore|  
|级别|错误|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>描述  
 指示在尝试解锁某一实例时遇到了异常。  
  
## <a name="message"></a>消息  
 尝试解除实例锁定时遇到异常 %1。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|描述|  
|--------------------|--------------------|-----------------|  
|ExceptionMessage|xs:string|来自 SQL 异常的消息。|  
|AppDomain|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
