---
description: Ruft die externen Daten Informationen eines Objekts für indizierte Eigenschaften ab.
title: JsGetIndexedPropertiesExternalData-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233582"
---
# <span data-ttu-id="bfbd6-103">JsGetIndexedPropertiesExternalData Funktion</span><span class="sxs-lookup"><span data-stu-id="bfbd6-103">JsGetIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="bfbd6-104">Ruft die externen Daten Informationen eines Objekts für indizierte Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="bfbd6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfbd6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="bfbd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfbd6-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bfbd6-107">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="bfbd6-108">Der externe Datenspeicher für die indizierten Eigenschaften des Objekts.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="bfbd6-109">Der Arrayelementtyp in externen Daten.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="bfbd6-110">Die Anzahl der Arrayelemente in externen Daten.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="bfbd6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfbd6-111">Return Value</span></span>  
 <span data-ttu-id="bfbd6-112">Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bfbd6-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfbd6-113">Remarks</span></span>  
 <span data-ttu-id="bfbd6-114">Diese API wird nur im Microsoft Edge-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfbd6-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="bfbd6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfbd6-115">Requirements</span></span>  
 <span data-ttu-id="bfbd6-116">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bfbd6-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bfbd6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bfbd6-117">See Also</span></span>  
 [<span data-ttu-id="bfbd6-118">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="bfbd6-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
