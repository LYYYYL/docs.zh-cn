---
title: "如何：启用数据服务结果分页（WCF 数据服务）"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework-oob
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords: paging output [WCF Data Services]
ms.assetid: 9a316cbd-9612-4482-a541-a10bc78b2635
caps.latest.revision: "2"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 6bf267cdc4ab3ec3bdc82a3da52cef21ef1d6b2b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-enable-paging-of-data-service-results-wcf-data-services"></a>如何：启用数据服务结果分页（WCF 数据服务）
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] 使您能够限制由数据服务查询返回的实体数。 页限制在初始化服务时调用的方法中定义，并可为每个实体集单独设置页限制。  
  
 启用分页后，源中的最后一项包含指向下一页数据的链接。 有关详细信息，请参阅[配置数据服务](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md)。  
  
 本主题介绍如何修改数据服务以启用返回的 `Customers` 和 `Orders` 实体集的分页。 本主题中的示例使用 Northwind 示例数据服务。 在完成时创建此服务[WCF 数据服务快速入门](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)。  
  
### <a name="how-to-enable-paging-of-returned-customers-and-orders-entity-sets"></a>如何启用返回的 Customers 和 Orders 实体集的分页  
  
-   在数据服务的代码中，用下列代码替换 `InitializeService` 函数中的占位符代码：  
  
     [!code-csharp[Astoria Northwind Service#DataServiceConfigPaging](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind service/cs/northwind.svc.cs#dataserviceconfigpaging)]
     [!code-vb[Astoria Northwind Service#DataServiceConfigPaging](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind service/vb/northwind.svc.vb#dataserviceconfigpaging)]  
  
## <a name="see-also"></a>另请参阅  
 [加载延迟的内容](../../../../docs/framework/data/wcf/loading-deferred-content-wcf-data-services.md)  
 [如何： 加载分页结果](../../../../docs/framework/data/wcf/how-to-load-paged-results-wcf-data-services.md)
