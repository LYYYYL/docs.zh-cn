---
title: "承载异常"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ad9e14f8-fa17-4d59-b365-fe0e7ec17c98
caps.latest.revision: "5"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: efc22d39838caae4500a0673f5f86c3285134002
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="hosting-exceptions"></a>承载异常
本主题列出了由承载生成的所有异常。  
  
## <a name="exception-list"></a>异常列表  
  
|资源代码|资源字符串|  
|-------------------|---------------------|  
|Hosting_AddressIsAbsoluteUri|不允许完整的 URI。 对于 ServiceHostingEnvironment.EnsureServiceAvailable API，不允许完整的 URI。 对相应的服务使用虚拟路径。|  
|Hosting_BuildProviderCouldNotCreateType|在服务编译期间，无法加载指定的 CLR 类型。 验证此类型可以定义在位于应用程序的源文件中\\\App_Code 目录中，在位于应用程序的已编译的程序集中包含\\\bin 目录中，或位于安装中的程序集全局程序集缓存。 类型名区分大小写。 如目录\\\App_Code 和\\\bin 必须位于应用程序的根目录。 \\\App_Code 和\\\bin 目录不能嵌套在子目录中。|
