---
title: Nastavitev integracije kreditne kartice
description: Ta članek razlaga, kako delati s transakcijami s kreditnimi karticami, povezanimi s stroški.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924515"
---
# <a name="set-up-credit-card-integration"></a>Nastavitev integracije kreditne kartice

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Transakcije s kreditnimi karticami, povezane s stroški, lahko nastavite tako, da se samodejno uvozijo po ponavljajočem se urniku. Lahko pa transakcije uvozite tudi ročno, kot so potrebne. Transakcije s kreditnimi karticami se uvažajo prek podatkovne entitete za transakcije s kreditnimi karticami.

## <a name="import-credit-card-transactions"></a>Uvoz transakcij s kreditnimi karticami

Če želite uvoziti transakcije s kreditno kartico, sledite tem korakom:

1. Na strani **Transakcije s kreditnimi karticami** izberite **Uvoz transakcij**. Če prvič odpirate upravljanje podatkov, mora sistem posodobiti seznam podatkovnih entitet, preden lahko nadaljujete.
2. V polje **Ime** vnesite edinstven opis za uvozno opravilo.
3. V polju **Izvorna oblika zapisa podatkov** izberite obliko zapisa datoteke, ki vsebuje transakcije s kreditno kartico za uvoz.
4. Izberite **Naloži**, nato pa poiščite in izberite datoteko za uvoz.
5. Ko je datoteka naložena, preverite preslikavo datoteke transakcij s kreditnimi karticami in stolpce podatkovne entitete transakcij s kreditnimi karticami, tako da izberete povezavo **Prikaz zemljevida** na ploščici. Če obstajajo napake pri preslikavi ali če morate spremeniti preslikavo, naredite spremembe preslikave bodisi iz zavihka **Upodobitev preslikave** ali zavihka **Podrobnosti preslikave**.
6. Za avtomatizacijo transakcij s kreditnimi karticami izberite **Ustvari ponavljajoči se podatkovni posel**. Nato lahko nastavite ponavljanje, ki opredeljuje, kako pogosto naj se transakcije s kreditnimi karticami uvozijo. Ko končate, izberite **V redu**.
7. Če želite izbrano datoteko uvoziti zdaj, izberite **Uvozi**.
8. Če med uvozom pride do napak, si lahko ogledate dnevnik izvajanja ali podatke za pripravljanje, da vidite napake, ki jih morate popraviti, da zagotovite uspešen uvoz.

> [!NOTE]
> Če morate uvoziti več oblik zapisa datotek, morate za vsako vrsto zapisa ustvariti ločena opravila za uvoz.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Prerazporeditev transakcij s kreditnimi karticami za zaposlene, katerih zaposlitev se je končala

Ko je zapis zaposlenega ukinjen, je zaposlenčev račun za domenske storitve Active Directory (AD DS) onemogočen. Vendar pa lahko še obstajajo aktivne transakcije s kreditnimi karticami, ki jih je treba predložiti kot stroške in povrniti. Na strani **Transakcije s kreditnimi karticami** lahko zaposlenemu dodelite katero koli transakcijo s kreditno kartico, pri kateri je bila možnost povezanega zaposlenega prekinjena.

Izberite eno ali več transakcij s kreditnimi karticami in nato izberite **Prerazporeditev transakcij**. Nato lahko izberete drugega zaposlenega, ki mu dodelite transakcije s kreditnimi karticami. Ko so transakcije s kreditnimi karticami prerazporejene, jih lahko izberete za poročilo o stroških in plačate prek običajnega procesa za povračilo po poročilu o stroških.

## <a name="delete-credit-card-transactions"></a>Izbrišite transakcije s kreditnimi karticami 

Včasih je po uvozu transakcij s kreditno kartico morda treba nekatere transakcije izbrisati. To je lahko zato, ker so transakcije podvojene ali ker podatki niso točni. Skrbniki lahko uporabljajo funkcijo **»Izbriši transakcije s kreditno kartico«** za izbiro in brisanje transakcij s kreditnimi karticami, ki **niso priložene** poročilu o odhodkih. 

1. Odprite **Redna opravila** > **Izbriši transakcije s kreditnimi karticami**.
2. Izberite **Filter** in zagotovite informacije za identifikacijo zapisov, ki jih je treba vključiti.
3. Če želite izbrisati zapise, izberite **V redu**. 

## <a name="storing-credit-card-numbers"></a>Shranjevanje številk kreditnih kartic

Za shranjevanje številk kreditnih kartic so na voljo tri možnosti. Številke kreditnih kartic so shranjene na strani **Parametri upravljanja stroškov**.

- **Preprečitev vnosa številke kartice** – številke kreditnih kartic niso shranjene.
- **Razpršene številke kartic (shranjevanje zadnjih štirih številk)** – zadnje štiri številke kreditnih kartic so shranjene v šifrirani obliki.
- **Shranjevanje številk kartic** – številke kreditnih kartic so shranjene v nešifrirani obliki. Ta možnost ni v skladu s standardom za varnost podatkov (DSS) panoge plačilnih kartic (PCI). Za zagotavljanje skladnosti organizacije s predpisi PCI DSS, bi se zato morali njeni skrbniki odločiti, da ne številk kreditnih kartic ne bodo shranjevali ali da bodo shranjevali razpršene številke kartic.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
