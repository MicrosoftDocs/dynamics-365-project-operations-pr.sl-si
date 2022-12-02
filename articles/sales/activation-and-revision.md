---
title: Aktiviranje in popravljanje projektne ponudbe
description: Ta članek vsebuje informacije o aktivaciji in pregledu ponudb v programu Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Aktiviranje in popravljanje projektne ponudbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Funkciji aktivacije in pregleda vam pomagata spremljati različice ponudb, ki temeljijo na projektih, v fazah ocenjevanja in pogajanj. Ko je osnutek ponudbe aktiviran, je na voljo samo za branje.

Funkciji aktivacije in pregleda vam omogočata izvajanje naslednjih opravil:

- Sprejem ali zavrnitev ponudb šele po aktivaciji.
- Preglejte ponudbo, da spremenite obstoječo ponudbo ali ustvarite novo različico.

> [!NOTE]
> Ko je funkcija za aktivacijo in pregled ponudb omogočena, je ni več mogoče onemogočiti.

Če želite vklopiti možnost aktivacije in pregleda ponudb, ki temeljijo na projektih, sledite tem korakom.

1. Odprite možnost **Nastavitve** \> **Parametri**.
1. Odprite zapis **Parametri**.
1. V podoknu za dejanja pod zavihkom **Nadzor funkcij** izberite možnost **Omogoči aktivacijo in pregled ponudb**.
1. V potrditvenem pogovornem oknu izberite **V redu**.
1. Čez nekaj trenutkov osvežite brskalnik. Zdaj bi morali biti na voljo funkciji za aktivacijo in pregled. Če sta ti funkciji omogočeni, se gumb **Omogoči aktivacijo in pregled ponudb** ne prikaže več v podoknu za dejanja.

## <a name="activating-a-quote"></a>Aktivacija ponudbe

Ko je funkcija za aktivacijo in pregled ponudb omogočena, gumba **Zaključi ponudbo kot uspešno** in **Zaključi ponudbo kot neuspešno** v podoknu za dejanja nista na voljo za osnutke ponudbe o projektu. Na voljo sta šele po aktivaciji ponudbe.

Aktivacija predstavlja stopnjo v postopku ponudbe, ko želite preprečiti nadaljnje spremembe ponudbe. Na tej stopnji se ponudba pošlje v notranji pregled ali stranki.

Gumba **Zaključi ponudbo kot uspešno** in **Zaključi ponudbo kot neuspešno** v podoknu za dejanja sta na voljo za aktivirane ponudbe. Odvisno od izida notranjega pregleda ali pregleda stranke lahko uporabite enega od teh gumbov, da zaprete aktivirano ponudbo. Z izbiro možnosti **Preglej ponudbo** se lahko pogajate in spreminjate aktivirane ponudbe.

## <a name="revising-a-quote"></a>Pregled ponudbe

Če morate spremeniti aktivirano ponudbo, izberite možnost **Preglej ponudbo**. Ponudba je zaključena in uporabljena je koda razloga **pregledano**. Nato se ustvari nova ponudba z enakim ID-jem in povečano številko pregleda. Vse podrobnosti iz prvotne ponudbe se kopirajo v novo ponudbo. Nova ponudba je v stanju osnutka in jo je mogoče po potrebi urediti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
