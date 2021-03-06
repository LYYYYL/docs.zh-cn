---
title: "演练：在 WPF 中承载 ActiveX 控件"
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
- ActiveX controls [WPF interoperability]
- hosting ActiveX controls [WPF]
ms.assetid: 1931d292-0dd1-434f-963c-dcda7638d75a
caps.latest.revision: "30"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 25944b3dd28c0bce2646c06ec424b54acc8b8a1e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="walkthrough-hosting-an-activex-control-in-wpf"></a>演练：在 WPF 中承载 ActiveX 控件
若要启用改进与浏览器交互，你可以使用[!INCLUDE[TLA#tla_actx](../../../../includes/tlasharptla-actx-md.md)]控制在你[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-基于应用程序。 本演练演示如何可以承载[!INCLUDE[TLA#tla_wmp](../../../../includes/tlasharptla-wmp-md.md)]作为上的控件[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]页。  
  
 本演练涉及以下任务：  
  
-   创建项目。  
  
-   创建 ActiveX 控件。  
  
-   承载在 WPF 页上的 ActiveX 控件。  
  
 完成本演练后，你将了解如何使用[!INCLUDE[TLA#tla_actx](../../../../includes/tlasharptla-actx-md.md)]控制在你[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-基于应用程序。  
  
## <a name="prerequisites"></a>先决条件  
 你需要以下组件来完成本演练：  
  
-   [!INCLUDE[TLA#tla_wmp](../../../../includes/tlasharptla-wmp-md.md)]在计算机上安装其中[!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)]安装。  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)]。  
  
## <a name="creating-the-project"></a>创建项目  
  
#### <a name="to-create-and-set-up-the-project"></a>创建并设置项目  
  
1.  创建一个名为的 WPF 应用程序项目`HostingAxInWpf`。  
  
2.  将 Windows 窗体控件库项目添加到解决方案中，并将项目`WmpAxLib`。  
  
3.  在 WmpAxLib 项目中，将添加到名为 wmp.dll 的 Windows Media Player 程序集的引用。  
  
4.  打开**工具箱**。  
  
5.  在中右击**工具箱**，然后单击**选择项**。  
  
6.  单击**COM 组件**选项卡上，选择**Windows Media Player**控件，，然后单击**确定**。  
  
     Windows Media Player 控件添加到**工具箱**。  
  
7.  在解决方案资源管理器，右键单击**UserControl1**文件，，然后单击**重命名**。  
  
8.  名称更改为`WmpAxControl.vb`或`WmpAxControl.cs`，取决于语言。  
  
9. 如果系统提示你重命名所有引用时，请单击**是**。  
  
## <a name="creating-the-activex-control"></a>创建 ActiveX 控件  
 [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)]自动生成<xref:System.Windows.Forms.AxHost>包装类[!INCLUDE[TLA#tla_actx](../../../../includes/tlasharptla-actx-md.md)]控制时将控件添加到设计图面。 以下过程创建名为 AxInterop.WMPLib.dll 托管程序集。  
  
#### <a name="to-create-the-activex-control"></a>若要创建 ActiveX 控件  
  
1.  在 Windows 窗体设计器中打开 WmpAxControl.vb 或 WmpAxControl.cs。  
  
2.  从**工具箱**，将 Windows Media Player 控件添加到设计图面。  
  
3.  在属性窗口中，将 Windows Media Player 控件的值设置<xref:System.Windows.Forms.Control.Dock%2A>属性<xref:System.Windows.Forms.DockStyle.Fill>。  
  
4.  生成 WmpAxLib 控件库项目。  
  
## <a name="hosting-the-activex-control-on-a-wpf-page"></a>承载在 WPF 页上的 ActiveX 控件  
  
#### <a name="to-host-the-activex-control"></a>若要承载 ActiveX 控件  
  
1.  在 HostingAxInWpf 项目中，添加对生成的引用[!INCLUDE[TLA2#tla_actx](../../../../includes/tla2sharptla-actx-md.md)]互操作性程序集。  
  
     此程序集名为 AxInterop.WMPLib.dll，并且已添加到 WmpAxLib 项目的调试文件夹中，导入 Windows Media Player 控件时。  
  
2.  添加到名为 WindowsFormsIntegration.dll 的 WindowsFormsIntegration 程序集的引用。  
  
3.  添加对的引用[!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]名为 System.Windows.Forms.dll 的程序集。  
  
4.  在 WPF 设计器中打开 MainWindow.xaml。  
  
5.  名称<xref:System.Windows.Controls.Grid>元素`grid1`。  
  
     [!code-xaml[HostingAxInWpf#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingAxInWpf/CSharp/HostingAxInWpf/window1.xaml#1)]  
  
6.  在设计视图或 XAML 视图中，选择<xref:System.Windows.Window>元素。  
  
7.  在属性窗口中，单击**事件**选项卡。  
  
8.  双击<xref:System.Windows.FrameworkElement.Loaded>事件。  
  
9. 插入以下代码以处理<xref:System.Windows.FrameworkElement.Loaded>事件。  
  
     此代码创建的实例<xref:System.Windows.Forms.Integration.WindowsFormsHost>控件，添加的实例`AxWindowsMediaPlayer`控件作为其子级。  
  
     [!code-csharp[HostingAxInWpf#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingAxInWpf/CSharp/HostingAxInWpf/window1.xaml.cs#11)]
     [!code-vb[HostingAxInWpf#11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HostingAxInWpf/VisualBasic/HostingAxInWpf/window1.xaml.vb#11)]  
  
10. 按 F5 生成并运行该应用程序。  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [WPF 设计器](http://msdn.microsoft.com/en-us/c6c65214-8411-4e16-b254-163ed4099c26)  
 [演练：在 WPF 中托管 Windows 窗体复合控件](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)  
 [演练：在 Windows 窗体中承载 WPF 复合控件](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
