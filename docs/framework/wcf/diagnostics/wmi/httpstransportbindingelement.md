---
title: HttpsTransportBindingElement
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e78aa8c6-b53b-4105-a900-d3e7a39670f2
caps.latest.revision: "8"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 24bd5d0241a638e942f6dfbe5c7afa75dd72e14b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="httpstransportbindingelement"></a>HttpsTransportBindingElement
HttpsTransportBindingElement  
  
## <a name="syntax"></a>语法  
  
```  
class HttpsTransportBindingElement : HttpTransportBindingElement  
{  
  boolean RequireClientCertificate;  
};  
```  
  
## <a name="methods"></a>方法  
 HttpsTransportBindingElement 类未定义任何方法。  
  
## <a name="properties"></a>属性  
 HttpsTransportBindingElement 类具有下列属性：  
  
### <a name="requireclientcertificate"></a>RequireClientCertificate  
 数据类型：Boolean  
  
 访问类型：只读  
  
 一个值，指示是否需要进行 SSL 客户端身份验证。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement>
