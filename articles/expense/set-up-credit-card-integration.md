---
title: Nastavitev integracije kreditne kartice
description: V tej temi je pojasnjeno, kako uvoziti in vzdrževati transakcije s kreditnimi karticami, povezane s stroški.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120878"
---
# <a name="set-up-credit-card-integration"></a>Nastavitev integracije kreditne kartice

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Transakcije s kreditnimi karticami, povezane s stroški, lahko nastavite tako, da se samodejno uvozijo po ponavljajočem se urniku. Lahko pa transakcije uvozite tudi ročno, kot so potrebne. Transakcije s kreditnimi karticami se uvažajo prek podatkovne entitete za transakcije s kreditnimi karticami.

## <a name="import-credit-card-transactions"></a>Uvoz transakcij s kreditnimi karticami

1. Na strani **Transakcije s kreditnimi karticami** izberite **Uvoz transakcij**. Če prvič odpirate upravljanje podatkov, mora sistem posodobiti seznam podatkovnih entitet, preden lahko nadaljujete.
2. V polje **Ime** vnesite enolični opis opravila uvoza.
3. V polju **Izvorna oblika zapisa podatkov** izberite obliko zapisa datoteke, ki vsebuje transakcije s kreditno kartico za uvoz.
4. Izberite **Naloži**, nato pa poiščite in izberite datoteko za uvoz.
5. Ko je datoteka naložena, preverite preslikavo datoteke transakcij s kreditnimi karticami in stolpce podatkovne entitete transakcij s kreditnimi karticami, tako da izberete povezavo **Prikaz zemljevida** na ploščici. Če obstajajo napake pri preslikavi ali če morate spremeniti preslikavo, naredite spremembe preslikave bodisi iz zavihka **Upodobitev preslikave** ali zavihka **Podrobnosti preslikave**.
6. Za avtomatizacijo transakcij s kreditnimi karticami izberite **Ustvari ponavljajoči se podatkovni posel**. Nato lahko nastavite ponavljanje, ki opredeljuje, kako pogosto naj se transakcije s kreditnimi karticami uvozijo. Ko končate, izberite **V redu**.
7. Če želite izbrano datoteko uvoziti zdaj, izberite **Uvozi**.
8. Če med uvozom pride do napak, si lahko ogledate dnevnik izvajanja ali podatke o pripravi, da vidite napake, ki jih morate odpraviti, da zagotovite uspešen uvoz.

> [!NOTE]
> Če morate uvoziti več oblik zapisov datotek, morate za vsako vrsto oblike zapisa ustvariti ločen posel za uvoz.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Prerazporeditev transakcij s kreditnimi karticami za zaposlene, katerih zaposlitev se je končala

Ko je zapis zaposlenega ukinjen, je zaposlenčev račun za domenske storitve Active Directory (AD DS) onemogočen. Vendar pa lahko še obstajajo aktivne transakcije s kreditnimi karticami, ki jih je treba predložiti kot stroške in povrniti. Na strani **Transakcije s kreditnimi karticami** lahko prerazporedite zaposlenega za katero koli transakcijo s kreditno kartico, kjer se je zaposlitev povezanega zaposlenega končala.

Izberite eno ali več transakcij s kreditnimi karticami in nato izberite **Prerazporeditev transakcij**. Nato lahko izberete drugega zaposlenega, ki mu dodelite transakcije s kreditnimi karticami. Ko so transakcije s kreditnimi karticami prerazporejene, jih lahko izberete za poročilo o stroških in plačate prek običajnega procesa za povračilo po poročilu o stroških.
