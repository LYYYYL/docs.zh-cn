---
title: "如何：使用钢笔绘制矩形"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- rectangles [Windows Forms], drawing
- pens [Windows Forms], drawing rectangles
ms.assetid: 54a7fa14-3ad8-4d64-b424-2a12005b250c
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 032f53ffe3bccd329b3e2eea4fbf13949f35c3cd
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-use-a-pen-to-draw-rectangles"></a>如何：使用钢笔绘制矩形
若要绘制的矩形，你需要<xref:System.Drawing.Graphics>对象和一个<xref:System.Drawing.Pen>对象。 <xref:System.Drawing.Graphics>对象提供<xref:System.Drawing.Graphics.DrawRectangle%2A>方法，与<xref:System.Drawing.Pen>对象存储在行中，如颜色和宽度的功能。  
  
## <a name="example"></a>示例  
 下面的示例绘制一个具有在其左上角的矩形 （10，10）。 矩形的宽度为 100，50 的高度。 第二个参数传递给<xref:System.Drawing.Pen.%23ctor%2A>构造函数指示钢笔的宽度为 5 个像素。  
  
 当绘制矩形时，触笔上居中显示矩形的边界。 因为钢笔的宽度为 5，在该矩形两端均为绘制的 5 个像素宽，因此绘制 1 个像素在边界本身，2 个像素绘制内，和 2 个像素绘制在外部。 钢笔对齐方式的更多详细信息，请参阅[如何： 设置钢笔的宽度和对齐方式](../../../../docs/framework/winforms/advanced/how-to-set-pen-width-and-alignment.md)。  
  
 下图显示生成的矩形。 虚线显示其中矩形将绘制如果钢笔的宽度过一个像素。 矩形的左上角的放大的视图显示密集的黑色线条位于这些虚线。  
  
 ![钢笔](../../../../docs/framework/winforms/advanced/media/pens1.gif "pens1")  
  
 [!code-csharp[System.Drawing.UsingAPen#21](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.UsingAPen#21](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>编译代码  
 前面的示例专用于 Windows 窗体，它需要 <xref:System.Windows.Forms.PaintEventArgs>`e`，后者是 <xref:System.Windows.Forms.Control.Paint> 事件处理程序的参数。  
  
## <a name="see-also"></a>另请参阅  
 [使用笔绘制直线和形状](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
