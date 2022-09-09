---
title: Aktivirajte in popravite projektno ponudbo
description: Ta članek vsebuje informacije o aktiviranju in pregledovanju ponudb v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410393"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktivirajte in popravite projektno ponudbo

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Zmožnosti aktiviranja in revizije vam pomagajo spremljati različice za ponudbe, ki temeljijo na projektu, med fazami ocenjevanja in pogajanj. Ko je osnutek ponudbe aktiviran, postane samo za branje.

Zmožnosti aktivacije in revizije vam omogočajo izvajanje naslednjih nalog:

- Dobite ali izgubite ponudbe šele po aktivaciji.
- Popravite ponudbo, da spremenite obstoječo ponudbo ali ustvarite novo različico.

> [!NOTE]
> Ko je funkcija za aktivacijo in revizijo ponudb omogočena, je ni več mogoče onemogočiti.

Če želite vklopiti možnost aktiviranja in pregleda projektnih ponudb, sledite tem korakom.

1. Pojdi do **nastavitve** \> **Parametri**.
1. Odprite **Parametri** zapis.
1. V podoknu z dejanji na **Nadzor funkcij** zavihek izberite **Omogoči aktivacijo in revizijo ponudb**.
1. V potrditvenem pogovornem oknu izberite **V redu**.
1. Po nekaj trenutkih osvežite brskalnik. Zdaj bi morale biti na voljo možnosti za aktiviranje in revizijo. Vedeli boste, da so te zmožnosti omogočene, če **Omogoči aktivacijo in revizijo za ponudbe** gumb se ne prikaže več v podoknu z dejanji.

## <a name="activating-a-quote"></a>Aktiviranje ponudbe

Ko je funkcija za aktivacijo in revizijo ponudb omogočena, se **Zapri citat kot zmagal** in **Zapri citat kot izgubljen** gumbi v podoknu z dejanji niso na voljo za ponudbe osnutka projekta. Na voljo so šele po aktiviranju ponudbe.

Aktivacija predstavlja fazo v procesu ponudbe, ko želite preprečiti nadaljnje spremembe ponudbe. V tej fazi se ponudba pošlje v interni pregled ali stranki.

The **Zapri citat kot zmagal** in **Zapri citat kot izgubljen** gumbi v podoknu z dejanji so na voljo za aktivirane ponudbe. Odvisno od rezultata notranjega pregleda ali pregleda stranke lahko uporabite enega od teh gumbov, da zaprete aktivirano ponudbo. Z izbiro lahko izvedete pogajanja in spremembe o aktiviranih ponudbah **Popravi ponudbo**.

## <a name="revising-a-quote"></a>Popravljanje ponudbe

Če morate spremeniti aktivirano ponudbo, izberite **Popravi ponudbo**. Ponudba je zaključena in **revidirano** uporabljena je koda vzroka. Nato se ustvari nova ponudba z enakim ID-jem in povečano številko revizije. Vse podrobnosti iz prvotne ponudbe se kopirajo v novo ponudbo. Nova ponudba je v stanju osnutka in jo je mogoče po potrebi urediti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
