---
title: "如何：添加数据服务引用（WCF 数据服务）"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework-oob
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: WCF Data Services, configuring
ms.assetid: 62c6f318-3ee1-433a-b7a3-efa234c3034c
caps.latest.revision: "2"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: a8fb075bdb17f0d562d752bc4125141bb0bb2ab9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-add-a-data-service-reference-wcf-data-services"></a>如何：添加数据服务引用（WCF 数据服务）
你可以使用**添加服务引用**对话框在 Visual Studio 中添加对引用[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]。 这使您可以更轻松地在使用 Visual Studio 开发的客户端应用程序中访问数据服务。 完成此过程后，会基于从数据服务获取的元数据生成数据类。 有关详细信息，请参阅[生成数据服务客户端库](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)。  
  
### <a name="to-add-a-data-service-reference"></a>添加数据服务引用  
  
1.  （可选）如果数据服务不是解决方案的一部分，且未运行，请启动数据服务，并记下数据服务的 URI。  
  
2.  右键单击客户端项目，然后选择**添加服务引用**。  
  
3.  如果数据服务当前解决方案的一部分，请单击**发现**。  
  
     - 或 -  
  
     在**地址**文本框中，键入数据服务的基 URL 如`http://localhost:1234/Northwind.svc`，然后单击**转**。  
  
4.  单击“确定”。  
  
     这样会添加一个新的代码文件，该文件包含用于访问作为对象的数据服务资源并与其交互的数据类。  
  
## <a name="see-also"></a>另请参阅  
 [快速入门](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)
