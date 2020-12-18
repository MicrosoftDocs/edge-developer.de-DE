---
description: Definiert die eigene Eigenschaft eines neuen Objekts aus einem Eigenschaftendeskriptor.
title: JsDefineProperty-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a35dd6214190fa558c50cbb743b0f2b92b5e00b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234100"
---
# <span data-ttu-id="1a675-103">JsDefineProperty Funktion</span><span class="sxs-lookup"><span data-stu-id="1a675-103">JsDefineProperty Function</span></span>

<span data-ttu-id="1a675-104">Definiert die eigene Eigenschaft eines neuen Objekts aus einem Eigenschaftendeskriptor.</span><span class="sxs-lookup"><span data-stu-id="1a675-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="1a675-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a675-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="1a675-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a675-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1a675-107">Das Objekt, das die Eigenschaft aufweist.</span><span class="sxs-lookup"><span data-stu-id="1a675-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="1a675-108">Die ID der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1a675-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="1a675-109">Der Eigenschaftendeskriptor.</span><span class="sxs-lookup"><span data-stu-id="1a675-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="1a675-110">Gibt an, ob die Eigenschaft definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1a675-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="1a675-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a675-111">Return Value</span></span>  
 <span data-ttu-id="1a675-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1a675-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1a675-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a675-113">Remarks</span></span>  
 <span data-ttu-id="1a675-114">Erfordert einen aktiven Skriptkontext.</span><span class="sxs-lookup"><span data-stu-id="1a675-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1a675-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a675-115">Requirements</span></span>  
 <span data-ttu-id="1a675-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1a675-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1a675-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a675-117">See Also</span></span>  
 [<span data-ttu-id="1a675-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="1a675-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
