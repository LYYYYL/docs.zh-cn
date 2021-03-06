---
title: "如何：在 XAML 中使用特殊字符"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Unicode UTF-8 file format
- UTF-8 file format
- characters [WPF], special
- typography [WPF], special characters
- special characters [WPF]
ms.assetid: a57776d1-f353-4794-afa0-bfa3c712ed1c
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 308b2152f98286ba532a15e5491b5d1a25aa66dd
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-use-special-characters-in-xaml"></a>如何：在 XAML 中使用特殊字符
在中创建的标记文件[!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)]自动保存在[!INCLUDE[TLA#tla_unicode](../../../../includes/tlasharptla-unicode-md.md)]utf-8 文件格式，这意味着大部分特殊字符，如重音符号进行正确编码。 但是，有一组常用特殊字符的处理方式不同。 这些特殊字符遵循[!INCLUDE[TLA#tla_w3c](../../../../includes/tlasharptla-w3c-md.md)][!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)]编码标准。  
  
 下表显示这组特殊字符的编码语法：  
  
|字符|语法|描述|  
|---------------|------------|-----------------|  
|<|`<`|小于符号。|  
|>|`>`|大于符号。|  
|&|`&`|& 符号。|  
|"|`"`|双引号。|  
  
> [!NOTE]
>  如果你创建的标记文件，使用文本编辑器中，如[!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)]记事本，你必须保存在文件[!INCLUDE[TLA#tla_unicode](../../../../includes/tlasharptla-unicode-md.md)]以保持任何 utf-8 文件格式编码的特殊字符。  
  
 以下示例演示创建标记时如何在文本中使用特殊字符。  
  
## <a name="example"></a>示例  
 [!code-xaml[SpecialCharsSnippets#SpecialCharsSnippet1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SpecialCharsSnippets/CS/Window1.xaml#specialcharssnippet1)]
