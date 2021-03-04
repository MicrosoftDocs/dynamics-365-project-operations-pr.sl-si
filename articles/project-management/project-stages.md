---
title: Stopnje projekta
description: Ta tema vsebuje informacije o stopnjah projekta, ki so na voljo v storitvi Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127493"
---
# <a name="project-stages"></a>Stopnje projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Stopnje projekta so zasnovane tako, da odražajo stanje projekta med napredkom. Prilagoditve lahko uporabite za samodejno posodabljanje faz s poteki poslovnih procesov, storitvijo Power Automate ali razširitvami vtičnikov.

V privzetem poteku poslovnega procesa so določene te stopnje:

- Nova
- Citat
- Paket
- Dostavi
- Popolno
- Zaprto 

## <a name="new"></a>Nova

Ko ustvarite projekt, je stopnja projekta nastavljena na **Novo**. Če je bil projekt ustvarjen iz predloge, ima morda podatke o razporedu, ocenah in ekipi. V nasprotnem primeru je to oris projekta, preostale komponente pa morate vnesti sami.

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