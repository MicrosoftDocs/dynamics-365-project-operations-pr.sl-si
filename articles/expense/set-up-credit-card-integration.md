---
title: Nastavitev integracije kreditne kartice
description: Ta tema razlaga, kako delati s transakcijami s kreditnimi karticami, povezanimi s stroški.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996231"
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

Včasih je po uvozu transakcij s kreditno kartico morda treba nekatere transakcije izbrisati. To je lahko zato, ker so transakcije podvojene ali ker podatki morda niso točni. Skrbniki lahko uporabljajo funkcijo **»Izbriši transakcije s kreditno kartico«** za izbiro in brisanje transakcij s kreditnimi karticami, ki **niso priložene** poročilu o odhodkih. 

1. Odprite **Redna opravila** > **Izbriši transakcije s kreditnimi karticami**.
2. Izberite **Filter** in zagotovite informacije za identifikacijo zapisov, ki jih je treba vključiti.
3. Če želite izbrisati zapise, izberite **V redu**. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
