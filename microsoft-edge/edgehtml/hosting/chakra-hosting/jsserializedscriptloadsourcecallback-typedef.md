---
description: Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden. Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234311"
---
# <span data-ttu-id="ec9b1-104">JsSerializedScriptLoadSourceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="ec9b1-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>

<span data-ttu-id="ec9b1-105">Wird von der Common Language Runtime aufgerufen, um den Quellcode des serialisierten Skripts zu laden.</span><span class="sxs-lookup"><span data-stu-id="ec9b1-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="ec9b1-106">Der Aufrufer muss den skriptpuffer gültig halten, bis `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="ec9b1-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="ec9b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec9b1-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="ec9b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec9b1-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="ec9b1-109">Der Kontext, der an oder übergeben wurde `JsParseSerializedScriptWithCallback` `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="ec9b1-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="ec9b1-110">Das Skript wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec9b1-110">The script returned.</span></span>  
  
## <span data-ttu-id="ec9b1-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec9b1-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="ec9b1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec9b1-112">Requirements</span></span>  
 <span data-ttu-id="ec9b1-113">**Kopfzeile:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ec9b1-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ec9b1-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec9b1-114">See Also</span></span>  
 [<span data-ttu-id="ec9b1-115">Referenz (JavaScript-Laufzeit)</span><span class="sxs-lookup"><span data-stu-id="ec9b1-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
