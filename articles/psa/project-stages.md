---
title: Vrste stopenj projekta
description: Ta tema vsebuje informacije o stopnjah projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996906"
---
# <a name="project-stage-types"></a>Vrste stopenj projekta 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Stopnje projekta so zasnovane tako, da odražajo stanje projekta med napredkom. Prilagoditve lahko uporabite za samodejno posodabljanje faz s poteki poslovnih procesov, storitvijo Power Automate ali razširitvami vtičnikov.

V privzetem poteku poslovnega procesa so določene te stopnje:

- Nova
- Citat
- Načrt
- Dostava
- Dokončano
- Zaprto 

## <a name="new"></a>Novo

Ko ustvarite projekt, je stopnja projekta nastavljena na **Novo**. Če je bil projekt ustvarjen iz predloge, ima morda podatke o razporedu, ocenah in ekipi. V nasprotnem primeru je to samo oris projekta, preostale komponente pa morate vnesti sami.

## <a name="quote"></a>Ponudba

Ko povežete projekt s ponudbo ali ga ustvarite iz ponudbe, je stanje projekta nastavljeno na **Ponudba**, pri čemer se posodobita tudi predvidena začetni in končni datum. Ko je projekt na stopnji **Ponudba**, so na zavihku **Prodaja** na strani **Entiteta projekta** prikazane podrobnosti ponudbe.

## <a name="plan"></a>Načrt

Ko je ponudba, ki je povezana s projektom, sprejeta, in se projekt premakne na stopnjo **Pogodba**, se stopnja projekta posodobi na stopnjo **Načrt**. Ko je projekt na stopnji **Načrt**, so na strani **Entiteta projekta** prikazane podrobnosti pogodbe.

## <a name="deliver"></a>Dostava

Ko je načrt projekta dokončan in ste pripravljeni na zagon projekta, mora vodja projekta posodobiti stopnjo projekta na **Dostava**, da pokaže, da se je projekt začel.

## <a name="complete"></a>Dokončano 

Ko je delo za projekt končano, lahko vodja projekta posodobi stopnjo na **Dokončano**. Ko vodja projekta posodobi stopnjo projekta na **Dokončano**, to pomeni, da je delo 100-odstotno dokončano, vendar je projekt še vedno odprt, tako da je mogoče zabeležiti vse čakajoče časovne vnose ali vnose stroškov.

## <a name="close"></a>Zaprto

Ko so za projekt zabeležene vse transakcije, lahko vodja projekta posodobi stopnjo na **Zaprto**. Na tej točki ni več mogoče beležiti transakcij in projekt je nastavljen na način samo za branje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]