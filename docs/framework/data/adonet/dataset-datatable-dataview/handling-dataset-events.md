---
title: "处理数据集事件"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 54edefe0-bc38-419b-b486-3d8a0c356f13
caps.latest.revision: "4"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: cfe9d9c9f1442d3577772dde1ff33a7807394019
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="handling-dataset-events"></a>处理数据集事件
<xref:System.Data.DataSet> 对象提供三个事件： <xref:System.ComponentModel.MarshalByValueComponent.Disposed>、 <xref:System.Data.DataSet.Initialized>和 <xref:System.Data.DataSet.MergeFailed>。  
  
## <a name="the-mergefailed-event"></a>MergeFailed 事件  
 `DataSet` 对象的最常用事件是 `MergeFailed`，当要合并的 `DataSet` 对象的架构发生冲突时，会引发该事件。 当目标和源 <xref:System.Data.DataRow> 有相同的主键值，且 <xref:System.Data.DataSet.EnforceConstraints%2A> 属性设置为 `true`时会发生这种情况。 例如，如果所合并表的主键列与两个 `DataSet` 对象中的表的相同，则将发生异常并引发 `MergeFailed` 事件。 传递给 <xref:System.Data.MergeFailedEventArgs> 事件的 `MergeFailed` 对象具有 <xref:System.Data.MergeFailedEventArgs.Conflict%2A> 属性（标识两个 `DataSet` 对象之间的架构冲突）和 <xref:System.Data.MergeFailedEventArgs.Table%2A> 属性（标识发生冲突的表的名称）。  
  
 下面的代码段演示如何为 `MergeFailed` 事件添加事件处理程序。  
  
```vb  
AddHandler workDS.MergeFailed, New MergeFailedEventHandler( _  
  AddressOf DataSetMergeFailed)  
  
Private Shared Sub DataSetMergeFailed(  _  
  sender As Object,args As MergeFailedEventArgs)  
  Console.WriteLine("Merge failed for table " & args.Table.TableName)  
  Console.WriteLine("Conflict = " & args.Conflict)  
End Sub  
```  
  
```csharp  
workDS.MergeFailed += new MergeFailedEventHandler(DataSetMergeFailed);  
  
private static void DataSetMergeFailed(  
  object sender, MergeFailedEventArgs args)  
{  
  Console.WriteLine("Merge failed for table " + args.Table.TableName);  
  Console.WriteLine("Conflict = " + args.Conflict);  
}  
```  
  
## <a name="the-initialized-event"></a>初始化事件  
 在 <xref:System.Data.DataSet.Initialized> 构造函数初始化 `DataSet` 的新实例后会发生 `DataSet`事件。  
  
 如果 <xref:System.Data.DataSet.IsInitialized%2A> 已完成初始化， `true` 属性会返回 `DataSet` ；否则，返回 `false`。 <xref:System.Data.DataSet.BeginInit%2A> 方法，它开始初始化 `DataSet`，将 <xref:System.Data.DataSet.IsInitialized%2A> 设置为 `false`。 <xref:System.Data.DataSet.EndInit%2A> 方法（用于结束 `DataSet`的初始化）将它设置为 `true`。 [!INCLUDE[vsprvs](../../../../../includes/vsprvs-md.md)] 设计环境使用这些方法初始化其他组件使用的 `DataSet` 。 通常不会在代码中使用这些方法。  
  
## <a name="the-disposed-event"></a>释放事件  
 `DataSet` 派生自 <xref:System.ComponentModel.MarshalByValueComponent> 类，该类可公开 <xref:System.ComponentModel.MarshalByValueComponent.Dispose%2A> 方法和 <xref:System.ComponentModel.MarshalByValueComponent.Disposed> 事件。 <xref:System.ComponentModel.MarshalByValueComponent.Disposed>事件添加事件处理程序以侦听组件上已释放的事件。 你可以使用<xref:System.ComponentModel.MarshalByValueComponent.Disposed>事件`DataSet`如果你想要执行的代码时<xref:System.ComponentModel.MarshalByValueComponent.Dispose%2A>调用方法。 <xref:System.ComponentModel.MarshalByValueComponent.Dispose%2A>释放使用的资源<xref:System.ComponentModel.MarshalByValueComponent>。  
  
> [!NOTE]
>  `DataSet`和`DataTable`对象继承自<xref:System.ComponentModel.MarshalByValueComponent>和支持<xref:System.Runtime.Serialization.ISerializable>以进行远程处理的接口。 这两个对象是唯一可远程处理的 ADO.NET 对象。 有关详细信息，请参阅 [Remote Objects](http://msdn.microsoft.com/en-us/515686e6-0a8d-42f7-8188-73abede57c58)。  
  
 有关可用时使用其他事件信息`DataSet`，请参阅[处理数据表事件](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/handling-datatable-events.md)和[处理 DataAdapter 事件](../../../../../docs/framework/data/adonet/handling-dataadapter-events.md)。  
  
## <a name="see-also"></a>另请参阅  
 [数据集、数据表和数据视图](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 [验证数据](http://msdn.microsoft.com/library/b3a9ee4e-5d4d-4411-9c56-c811f2b4ee7e)  
 [在 ADO.NET 中检索和修改数据](../../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [ADO.NET 托管提供程序和数据集开发人员中心](http://go.microsoft.com/fwlink/?LinkId=217917)
