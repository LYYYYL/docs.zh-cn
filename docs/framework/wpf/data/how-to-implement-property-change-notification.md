---
title: "如何：实现属性更改通知"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- notifications of change [WPF]
- data binding [WPF], property change notifications
- change notifications [WPF]
- properties [WPF], change notifications
ms.assetid: 30b59d9e-8c3a-4349-aa82-4be837e841cf
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 6674628acd4ea6b18f98a0ab5e20935220595de5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-implement-property-change-notification"></a>如何：实现属性更改通知
若要支持<xref:System.Windows.Data.BindingMode.OneWay>或<xref:System.Windows.Data.BindingMode.TwoWay>绑定，从而使你的绑定目标属性，以便自动反映绑定源 （例如具有预览窗格中，当用户编辑窗体时自动更新），动态更改您的类需要提供相应的属性更改通知。 此示例演示如何创建一个类以实现<xref:System.ComponentModel.INotifyPropertyChanged>。  
  
## <a name="example"></a>示例  
 若要实现<xref:System.ComponentModel.INotifyPropertyChanged>则需要声明<xref:System.ComponentModel.INotifyPropertyChanged.PropertyChanged>事件并创建`OnPropertyChanged`方法。 然后，对于每个需要更改通知的属性，只要进行了更新，就可以调用 `OnPropertyChanged`。  
  
 [!code-csharp[SimpleBinding#PersonClass](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Person.cs#personclass)]
 [!code-vb[SimpleBinding#PersonClass](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SimpleBinding/VisualBasic/Person.vb#personclass)]  
  
 若要查看如何的示例`Person`类可以用于支持<xref:System.Windows.Data.BindingMode.TwoWay>绑定，请参阅[控制文本框文本更新后，源](../../../../docs/framework/wpf/data/how-to-control-when-the-textbox-text-updates-the-source.md)。  
  
## <a name="see-also"></a>另请参阅  
 [绑定源概述](../../../../docs/framework/wpf/data/binding-sources-overview.md)  
 [数据绑定概述](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [操作说明主题](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
