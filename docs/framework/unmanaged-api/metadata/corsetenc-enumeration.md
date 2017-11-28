---
title: "CorSetENC 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorSetENC
api_location: mscoree.dll
api_type: COM
f1_keywords: CorSetENC
helpviewer_keywords: CorSetENC enumeration [.NET Framework metadata]
ms.assetid: fe4150e8-071d-43fb-8e06-c3c616dbeed2
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 85a909d92be8bfdb9ada709b54cf252183ff411e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="corsetenc-enumeration"></a><span data-ttu-id="5f8d3-102">CorSetENC 枚举</span><span class="sxs-lookup"><span data-stu-id="5f8d3-102">CorSetENC Enumeration</span></span>
<span data-ttu-id="5f8d3-103">包含一些值，用于在元数据生成期间影响行为。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-103">Contains values used to influence behavior during the generation of metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f8d3-104">语法</span><span class="sxs-lookup"><span data-stu-id="5f8d3-104">Syntax</span></span>  
  
```  
typedef enum CorSetENC {  
  
    MDSetENCOn                  = 0x00000001,  
    MDSetENCOff                 = 0x00000002,  
  
    MDUpdateENC                 = 0x00000001,  
    MDUpdateFull                = 0x00000002,  
    MDUpdateExtension           = 0x00000003,  
    MDUpdateIncremental         = 0x00000004,  
    MDUpdateDelta               = 0x00000005,  
    MDUpdateMask                = 0x00000007  
  
} CorSetENC;  
```  
  
## <a name="members"></a><span data-ttu-id="5f8d3-105">成员</span><span class="sxs-lookup"><span data-stu-id="5f8d3-105">Members</span></span>  
  
|<span data-ttu-id="5f8d3-106">成员</span><span class="sxs-lookup"><span data-stu-id="5f8d3-106">Member</span></span>|<span data-ttu-id="5f8d3-107">描述</span><span class="sxs-lookup"><span data-stu-id="5f8d3-107">Description</span></span>|  
|------------|-----------------|  
|`MDSetENCOn`|<span data-ttu-id="5f8d3-108">已过时。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-108">Obsolete.</span></span>|  
|`MDSetENCOff`|<span data-ttu-id="5f8d3-109">已过时。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-109">Obsolete.</span></span>|  
|`MDUpdateENC`|<span data-ttu-id="5f8d3-110">指示可以更新元数据，而不能移动标记。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-110">Indicates that whereas metadata can be updated, tokens cannot be moved.</span></span>|  
|`MDUpdateFull`|<span data-ttu-id="5f8d3-111">指示可以在更新过程移动标记。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-111">Indicates that tokens can be moved during updates.</span></span>|  
|`MDUpdateExtension`|<span data-ttu-id="5f8d3-112">指示更新可以包含仅的新增功能。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-112">Indicates that updates can consist only of additions.</span></span> <span data-ttu-id="5f8d3-113">令牌不能移动。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-113">Tokens cannot be moved.</span></span>|  
|`MDUpdateIncremental`|<span data-ttu-id="5f8d3-114">指示为增量编译。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-114">Indicates that compilation is incremental.</span></span>|  
|`MDUpdateDelta`|<span data-ttu-id="5f8d3-115">指示应保存该仅更改了元数据。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-115">Indicates that only changed metadata should be saved.</span></span>|  
|`MDUpdateMask`|<span data-ttu-id="5f8d3-116">包括`MDUpdateENC`，`MDUpdateFull`和`MDUpdateIncremental`。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-116">Includes `MDUpdateENC`, `MDUpdateFull` and `MDUpdateIncremental`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5f8d3-117">要求</span><span class="sxs-lookup"><span data-stu-id="5f8d3-117">Requirements</span></span>  
 <span data-ttu-id="5f8d3-118">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f8d3-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f8d3-119">**标头：** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="5f8d3-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="5f8d3-120">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f8d3-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f8d3-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f8d3-121">See Also</span></span>  
 [<span data-ttu-id="5f8d3-122">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="5f8d3-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)