---
title: Nadgradnja premislekov za sodobne odobritve
description: Članek zajema točke, ki bi jih skrbniki morali upoštevati, ko omogočijo funkcijo »Sodobne odobritve«.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931764"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Nadgradnja premislekov za sodobne odobritve 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Kot del izdaje 1. faze aprila 2022 bo funkcija »Sodobne odobritve« privzeto omogočena. Ta funkcionalnost izboljšuje zanesljivost logike odobritve in zagotavlja, da lahko ugotovite razlog v primeru napake logike odobritve.

Kot del te spremembe se posodobijo spremembe stanja za odobritve projektov. Stanje gre zdaj neposredno iz **Oddano** v **Odobreno**. Stanje **V čakanju** ni več na voljo za odobritve. Če želite ugotoviti, ali je odobritev v čakanju, preverite, ali je odobritev del nabora odobritev, in preglejte stanje priloženega nabora odobritev.

## <a name="before-you-upgrade"></a>Pred nadgradnjo

Pred nadgradnjo na sodobne odobritve se prepričajte, da nimate čakajočih odobritev. Funkcija »Sodobne odobritve« ne uporablja stanja **V čakanju**. Zato vse odobritve, ki so še vedno označene kot **V čakanju**, po nadgradnji ne bodo obdelane.

## <a name="after-you-upgrade"></a>Po nadgradnji

Ko nadgradite na sodobne odobritve, mora skrbnik preveriti, ali je tok za oblak, ki obdeluje odobritve, omogočen.

1. Vpis v [flow.microsoft.com](https://flow.microsoft.com)
2. V zgornjem desnem kotu strani preklopite svoje okolje na okolje, ki ste ga nadgradili.
3. Izberite možnost **Rešitve** za seznam rešitev, ki so nameščene v okolju.
4. Na seznamu rešitev izberite **Project Operations** ali **Project Service**.
5. Spremenite filter z **Vse** na **Tokovi za oblak**.
6. Preverite, ali je možnost **Project Service – ponavljajoče se načrtovanje naborov odobritev projekta** nastavljena na **Vklopljeno**. Če ni, izberite tok in nato možnost **Vklopi**.
7. Preglejte seznam **Sistemska opravila** v območju **Nastavitve** in tako preverite, ali se obdelava izvaja vsakih pet minut.

## <a name="short-term-rollback"></a>Kratkoročna povrnitev prejšnjega stanja

Če ne morete sprejeti sprememb ali če naletite na resno težavo s to funkcijo, se lahko začasno vrnete na prvotni tok odobritve, tako da izvedete naslednje korake:
1. Prijavite se v svoje okolje in preverite, ali ni čakajočih odobritev.
2. Odprite **Nastavitve** > **Parametri projekta**.
3. Izberite možnost **Nadzor funkcij** in nato **Sodobne odobritve**, da funkcijo izklopite.

## <a name="removing-the-feature-flag"></a>Odstranjevanje zastavice funkcije

V posodobitvi 2. faze oktobra 2022 bo možnost izklopa te funkcije odstranjena.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
