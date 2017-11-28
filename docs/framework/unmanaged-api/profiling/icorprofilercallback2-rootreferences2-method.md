---
title: "ICorProfilerCallback2::RootReferences2 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback2.RootReferences2
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback2::RootReferences2
helpviewer_keywords:
- RootReferences2 method [.NET Framework profiling]
- ICorProfilerCallback2::RootReferences2 method [.NET Framework profiling]
ms.assetid: 55a2f907-d216-42eb-8f2f-e5d59c2eebd6
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 8a0b2e23ba586e7a20ed11de6433b2d87cbe7219
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallback2rootreferences2-method"></a><span data-ttu-id="e8a50-102">ICorProfilerCallback2::RootReferences2 方法</span><span class="sxs-lookup"><span data-stu-id="e8a50-102">ICorProfilerCallback2::RootReferences2 Method</span></span>
<span data-ttu-id="e8a50-103">垃圾回收发生后，请通知有关根引用探查器。</span><span class="sxs-lookup"><span data-stu-id="e8a50-103">Notifies the profiler about root references after a garbage collection has occurred.</span></span> <span data-ttu-id="e8a50-104">此方法是扩展的[icorprofilercallback:: Rootreferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="e8a50-104">This method is an extension of the [ICorProfilerCallback::RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8a50-105">语法</span><span class="sxs-lookup"><span data-stu-id="e8a50-105">Syntax</span></span>  
  
```  
HRESULT RootReferences2(  
    [in] ULONG  cRootRefs,  
    [in, size_is(cRootRefs)] ObjectID rootRefIds[],  
    [in, size_is(cRootRefs)] COR_PRF_GC_ROOT_KIND rootKinds[],  
    [in, size_is(cRootRefs)] COR_PRF_GC_ROOT_FLAGS rootFlags[],  
    [in, size_is(cRootRefs)] UINT_PTR rootIds[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8a50-106">参数</span><span class="sxs-lookup"><span data-stu-id="e8a50-106">Parameters</span></span>  
 `cRootRefs`  
 <span data-ttu-id="e8a50-107">[in]中的元素数`rootRefIds`， `rootKinds`， `rootFlags`，和`rootIds`数组。</span><span class="sxs-lookup"><span data-stu-id="e8a50-107">[in] The number of elements in the `rootRefIds`, `rootKinds`, `rootFlags`, and `rootIds` arrays.</span></span>  
  
 `rootRefIds`  
 <span data-ttu-id="e8a50-108">[in]对象 Id，其中每个引用的静态对象或在堆栈上的对象的数组。</span><span class="sxs-lookup"><span data-stu-id="e8a50-108">[in] An array of object IDs, each of which references either a static object or an object on the stack.</span></span> <span data-ttu-id="e8a50-109">中的元素`rootKinds`数组提供信息来分类中的相应元素`rootRefIds`数组。</span><span class="sxs-lookup"><span data-stu-id="e8a50-109">Elements in the `rootKinds` array provide information to classify corresponding elements in the `rootRefIds` array.</span></span>  
  
 `rootKinds`  
 <span data-ttu-id="e8a50-110">[in]数组[COR_PRF_GC_ROOT_KIND](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-root-kind-enumeration.md)指示垃圾回收根的类型的值。</span><span class="sxs-lookup"><span data-stu-id="e8a50-110">[in] An array of [COR_PRF_GC_ROOT_KIND](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-root-kind-enumeration.md) values that indicate the type of the garbage collection root.</span></span>  
  
 `rootFlags`  
 <span data-ttu-id="e8a50-111">[in]数组[COR_PRF_GC_ROOT_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-root-flags-enumeration.md)描述垃圾回收根的属性的值。</span><span class="sxs-lookup"><span data-stu-id="e8a50-111">[in] An array of [COR_PRF_GC_ROOT_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-root-flags-enumeration.md) values that describe the properties of a garbage collection root.</span></span>  
  
 `rootIds`  
 <span data-ttu-id="e8a50-112">[in]值为整数，其中包含有关垃圾回收根，具体取决于的值的其他信息的该点的 UINT_PTR 数组`rootKinds`参数。</span><span class="sxs-lookup"><span data-stu-id="e8a50-112">[in] An array of UINT_PTR values that point to an integer that contains additional information about the garbage collection root, depending on the value of the `rootKinds` parameter.</span></span>  
  
 <span data-ttu-id="e8a50-113">如果类型的根是堆栈，则根 ID 将包含的变量的函数。</span><span class="sxs-lookup"><span data-stu-id="e8a50-113">If the type of the root is a stack, the root ID is for the function that contains the variable.</span></span> <span data-ttu-id="e8a50-114">如果该根 ID 为 0，该函数将是一个未命名的函数，是 CLR 的内部。</span><span class="sxs-lookup"><span data-stu-id="e8a50-114">If that root ID is 0, the function is an unnamed function that is internal to the CLR.</span></span> <span data-ttu-id="e8a50-115">如果根的类型为句柄，则根 ID 可供垃圾回收句柄。</span><span class="sxs-lookup"><span data-stu-id="e8a50-115">If the type of the root is a handle, the root ID is for the garbage collection handle.</span></span> <span data-ttu-id="e8a50-116">对于其他根类型，该 ID 是不透明值，应当忽略。</span><span class="sxs-lookup"><span data-stu-id="e8a50-116">For the other root types, the ID is an opaque value and should be ignored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e8a50-117">备注</span><span class="sxs-lookup"><span data-stu-id="e8a50-117">Remarks</span></span>  
 <span data-ttu-id="e8a50-118">`rootRefIds`， `rootKinds`， `rootFlags`，和`rootIds`数组是并行数组。</span><span class="sxs-lookup"><span data-stu-id="e8a50-118">The `rootRefIds`, `rootKinds`, `rootFlags`, and `rootIds` arrays are parallel arrays.</span></span> <span data-ttu-id="e8a50-119">也就是说， `rootRefIds[i]`， `rootKinds[i]`， `rootFlags[i]`，和`rootIds[i]`都涉及相同的根。</span><span class="sxs-lookup"><span data-stu-id="e8a50-119">That is, `rootRefIds[i]`, `rootKinds[i]`, `rootFlags[i]`, and `rootIds[i]` all concern the same root.</span></span>  
  
 <span data-ttu-id="e8a50-120">同时`RootReferences`和`RootReferences2`调用以通知探查器。</span><span class="sxs-lookup"><span data-stu-id="e8a50-120">Both `RootReferences` and `RootReferences2` are called to notify the profiler.</span></span> <span data-ttu-id="e8a50-121">探查器将通常实现一种方法或另一个，但不是同时，因为传入的信息`RootReferences2`是传入的超集`RootReferences`。</span><span class="sxs-lookup"><span data-stu-id="e8a50-121">Profilers will normally implement one method or the other, but not both, because the information passed in `RootReferences2` is a superset of that passed in `RootReferences`.</span></span>  
  
 <span data-ttu-id="e8a50-122">中的条目可以`rootRefIds`为零，这意味着相应的根引用为 null，并且未引用托管堆上的对象。</span><span class="sxs-lookup"><span data-stu-id="e8a50-122">It is possible for entries in `rootRefIds` to be zero, which implies that the corresponding root reference is null and does not refer to an object on the managed heap.</span></span>  
  
 <span data-ttu-id="e8a50-123">通过返回的对象 Id`RootReferences2`不是有效在回调过程，因为垃圾回收可能正处于将对象从旧地址移至新的地址。</span><span class="sxs-lookup"><span data-stu-id="e8a50-123">The object IDs returned by `RootReferences2` are not valid during the callback itself, because the garbage collection might be in the middle of moving objects from old addresses to new addresses.</span></span> <span data-ttu-id="e8a50-124">因此，探查器不应在 `RootReferences2` 调用期间尝试检查对象。</span><span class="sxs-lookup"><span data-stu-id="e8a50-124">Therefore, profilers should not attempt to inspect objects during a `RootReferences2` call.</span></span> <span data-ttu-id="e8a50-125">当[icorprofilercallback2:: Garbagecollectionfinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md)是调用，所有对象都已移到其新位置，可以安全地检查。</span><span class="sxs-lookup"><span data-stu-id="e8a50-125">When [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) is called, all objects have been moved to their new locations and can be safely inspected.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8a50-126">要求</span><span class="sxs-lookup"><span data-stu-id="e8a50-126">Requirements</span></span>  
 <span data-ttu-id="e8a50-127">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8a50-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8a50-128">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e8a50-128">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e8a50-129">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8a50-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8a50-130">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8a50-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8a50-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8a50-131">See Also</span></span>  
 [<span data-ttu-id="e8a50-132">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="e8a50-132">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="e8a50-133">ICorProfilerCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="e8a50-133">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)