---
title: "元数据可扩展性"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: f92fcc76-0806-4c84-9d63-7aae0d3899de
caps.latest.revision: "3"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 36eb5940fa1d869948a94fcbbb1945aea1c534ac
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="metadata-extensibility"></a>元数据可扩展性
本节包含演示自定义元数据的示例。  
  
## <a name="in-this-section"></a>本节内容  
 [自定义安全元数据终结点](../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md)  
 演示如何实现具有非元数据交换绑定之一使用的安全的元数据终结点的服务以及如何配置[ServiceModel 元数据实用工具 (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)或客户端进行提取中的元数据此类元数据终结点。  
  
 [自定义 WSDL 发布](../../../../docs/framework/wcf/samples/custom-wsdl-publication.md)  
 演示如何在自定义 <xref:System.ServiceModel.Description.IWsdlExportExtension?displayProperty=nameWithType> 特性上实现 <xref:System.ServiceModel.Description.IContractBehavior?displayProperty=nameWithType>，以便在其他功能中将该特性的属性导出为 WSDL 批注。
