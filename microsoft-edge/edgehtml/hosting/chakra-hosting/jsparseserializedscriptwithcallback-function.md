---
description: Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt. Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.
title: JsParseSerializedScriptWithCallback-Funktion | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b145f01a5c3459100d8402beae63b7cff55db7b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234078"
---
# JsParseSerializedScriptWithCallback Funktion

Analysiert ein serialisiertes Skript und gibt eine Funktion zurück, die das Skript darstellt. Bietet die Möglichkeit, die Skript Quelle nur verzögert zu laden, wenn/wann dies erforderlich ist.  
  
## Syntax  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### Parameter  
 `scriptLoadCallback`  
 Der Rückruf wird aufgerufen, wenn der Quellcode des Skripts geladen werden muss.  
  
 `scriptUnloadCallback`  
 Rückruf, der aufgerufen wird, wenn das serialisierte Skript und der Quellcode nicht mehr benötigt werden.  
  
 `buffer`  
 Das serialisierte Skript.  
  
 `sourceContext`  
 Ein Cookie, das das Skript identifiziert, das von debugfähigen-Skript Kontexten verwendet werden kann.     Dieser Kontext wird an scriptLoadCallback und scriptUnloadCallback übergeben.  
  
 `sourceUrl`  
 Der Speicherort, aus dem das Skript kam.  
  
 `result`  
 Eine Funktion, die den Skriptcode darstellt.  
  
## Rückgabewert  
 Der Code `JsNoError` , wenn der Vorgang erfolgreich war, andernfalls ein Fehlercode.  
  
## Hinweise  
  
> [!NOTE]
>  Diese API steht noch nicht für Store-Apps zur Verfügung.  
  
 Erfordert einen aktiven Skriptkontext.  
  
 Die Laufzeit bleibt auf dem Puffer, bis alle Instanzen von Funktionen, die aus dem Puffer erstellt wurden, als Garbage Collection erfasst werden.  Anschließend wird scriptUnloadCallback aufgerufen, um den Anrufer darüber zu informieren, dass es sicher freigegeben werden kann.  
  
## Anforderungen  
 **Kopfzeile:** jsrt. h  
  
## Weitere Informationen  
 [Referenz (JavaScript-Laufzeit)](../chakra-hosting/reference-javascript-runtime.md)
