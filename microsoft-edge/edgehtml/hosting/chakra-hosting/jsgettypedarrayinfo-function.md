---
description: Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.
title: JsGetTypedArrayInfo-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234117"
---
# <span data-ttu-id="899a4-103">JsGetTypedArrayInfo Funktion</span><span class="sxs-lookup"><span data-stu-id="899a4-103">JsGetTypedArrayInfo Function</span></span>

<span data-ttu-id="899a4-104">Ruft häufig verwendete Eigenschaften eines typisierten Arrays ab.</span><span class="sxs-lookup"><span data-stu-id="899a4-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="899a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="899a4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="899a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="899a4-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="899a4-107">Die typisierte Arrayinstanz.</span><span class="sxs-lookup"><span data-stu-id="899a4-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="899a4-108">Der Typ des Arrays.</span><span class="sxs-lookup"><span data-stu-id="899a4-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="899a4-109">Der `ArrayBuffer` Backstore des Arrays.</span><span class="sxs-lookup"><span data-stu-id="899a4-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="899a4-110">Der Offset in Bytes vom Anfang des arrayBuffer, auf den das Array verweist.</span><span class="sxs-lookup"><span data-stu-id="899a4-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="899a4-111">Die Anzahl der Bytes im Array.</span><span class="sxs-lookup"><span data-stu-id="899a4-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="899a4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="899a4-112">Return Value</span></span>  
 <span data-ttu-id="899a4-113">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="899a4-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="899a4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="899a4-114">Remarks</span></span>  
 <span data-ttu-id="899a4-115">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="899a4-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="899a4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="899a4-116">Requirements</span></span>  
 <span data-ttu-id="899a4-117">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="899a4-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="899a4-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="899a4-118">See Also</span></span>  
 [<span data-ttu-id="899a4-119">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="899a4-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
