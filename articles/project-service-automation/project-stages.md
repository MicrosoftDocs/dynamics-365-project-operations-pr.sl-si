---
title: Stopnje projekta
description: Ta tema vsebuje informacije o stopnjah projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755770"
---
# <a name="project-stages"></a>Stopnje projekta 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Stopnje projekta so posodobljene tako, da odražajo stanje projekta med napredkom. Privzeti potek poslovnega procesa samodejno posodobi nekatere stopnje projekta, druge pa ročno posodobi vodja projekta. 

V privzetem poteku poslovnega procesa so določene te stopnje:

- Novo
- Ponudba
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
