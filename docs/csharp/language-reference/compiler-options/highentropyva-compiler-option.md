---
title: "-highentropyva（C# 编译器选项）"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords: /highentropyva
helpviewer_keywords:
- /highentropyva compiler option [C#]
- -highentropyva compiler option [C#]
- highentropyva compiler option [C#]
ms.assetid: eaf409b3-384e-49dd-9417-62453658f421
caps.latest.revision: "8"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 5746caed8c1bf61038c97a49987c4c168eef9f3f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="highentropyva-c-compiler-options"></a>/highentropyva（C# 编译器选项）
**/highentropyva** 编译器选项可向 Windows 内核提供下列信息：特定的可执行文件是否支持高熵地址空间布局随机化 (ASLR)。  
  
## <a name="syntax"></a>语法  
  
```console  
/highentropyva[+ | -]  
```  
  
## <a name="arguments"></a>参数  
 `+` &#124; `-`  
 此选项指定 64 位可执行文件或由 [/platform:anycpu](../../../csharp/language-reference/compiler-options/platform-compiler-option.md) 编译器选项标记的可执行文件支持高熵虚拟地址空间。 默认情况下，此选项处于禁用状态。 通过 **/highentropyva+** 或 **/highentropyva** 启用它。  
  
## <a name="remarks"></a>备注  
 当随机化进程的地址空间布局包含在 ASLR 中时，**/highentropyva** 选项允许 Windows 内核的兼容版本使用更高程度的熵。 使用更高程度的熵意味着，可向内存区域（例如堆栈或堆）分配更多的地址。 因此，猜测特定内存区域的位置会更加困难。  
  
 指定 **/highentropyva** 编译器选项时，目标可执行文件及其依赖的任何模块在作为 64 位进程运行时，必须能够处理大于 4 GB 的指针值。
