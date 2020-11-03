---
title: Ujemanje potrdila s stroškom z uporabo OCR
description: Ta tema vsebuje informacije o obdelavi z optičnim prepoznavanjem znakov (OCR) za potrdila.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084721"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Ujemanje potrdila s stroškom z uporabo OCR

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Vnos stroškov je bil izboljšan z uvedbo obdelave z optičnim prepoznavanjem znakov (OCR) za potrdila. Ta funkcionalnost je namenjena izboljšanju uporabniške izkušnje pri ustvarjanju poročil o stroških.

## <a name="key-features"></a>Najpomembnejše funkcije

- Sistem izvleče ime trgovca, datum in skupni znesek iz potrdil.
- Sistem bo poskušal izvesti ujemanje nepovezanih potrdil z nepovezanimi transakcijami stroškov.
- Iz potrdil lahko ustvarite ročno vnesene transakcije stroškov.

## <a name="attach-receipts-to-an-expense-report"></a>Prilaganje potrdil poročilu o stroških

Za samodejno prilaganje potrdil, ki vključujejo transakcije s kreditnimi karticami, ko je ustvarjeno poročilo o stroških, izvedite naslednje korake.

  1. Odprite delovni prostor **Upravljanje stroškov**.
  2. Na zavihku **Potrdila** preverite, ali obstajajo nepovezana potrdila. Potrdila lahko naložite tudi na zavihek **Potrdila**.
  3. Na zavihku **Stroški** preverite, ali obstajajo nepovezani stroški. Običajno skrbnik stroškov uvozi te stroške od ponudnika kreditne kartice.
  4. Izberite **Novo poročilo o stroških**. Opazite lahko, da lahko zdaj vključite stroške in potrdila, ko ustvarite poročilo o stroških. Če dodate stroške in potrdila, se sproži samodejno ujemanje potrdil s stroški.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Ustvarjanje ali ujemanje potrdil za poročilo o stroških
Če želite ustvariti strošek ali poiskati ujemanje stroška s potrdila, izvedite naslednje korake.

  1. Na poročilu o stroških na zavihku **Potrdila** priložite potrdilo z izbiro možnosti **Dodaj potrdila**.
  2. Pod naloženo sliko potrdila opazite možnosti **Ustvari** in **Išči ujemanje**.

      - Izberite **Ustvari** , da ustvarite ročno vneseno transakcijo stroška in izpolnite vrednosti, ki so izvlečene iz potrdila.
      - Če izberete **Išči ujemanje** , sistem poskuša poiskati ujemanje obstoječega stroška s potrdilom.

## <a name="installation"></a>Namestitev

Če želite uporabiti te napredne zmožnosti stroškov, namestite dodatek za storitev upravljanja stroškov za Microsoft Dynamics 365 Finance in vklopite funkcije v svojem primerku. Do dodatka lahko dostopate iz svojega projekta v Microsoft Dynamics Lifecycle Services (LCS).

1. Prijavite se v LCS in odprite želeno okolje.
2. Odprite **Vse podrobnosti**.
3. Izberite **Vzdrževanje** ali se pomaknite navzdol do hitrega dostopa **Dodatki za okolje**.
4. Izberite **Namestitev novega dodatka**.
5. Izberite **Storitev za upravljanje stroškov**.
6. Sledite navodilom za namestitev ter sprejmite pogoje in določila.
7. Izberite **Namesti**.

V delovnem prostoru **Upravljanje funkcij** vklopite naslednje funkcije:

- Prenovljena poročila o stroških
- Samodejno iskanje ujemanja in ustvarjanje stroška s potrdila

Ko vklopite te funkcije, se zgodijo naslednja dejanja:

- Obstoječi delovni prostor **Upravljanje stroškov** se nadomesti z novim delovnim prostorom.
- Dodana je nova postavka menija za vidljivost polja stroška.
- Še vedno lahko odprete prejšnjo stran **Poročila o stroških** , tako da obiščete **Upravljanje stroškov > Moji stroški > Poročila o stroških**.
- Poteki dela in morebitne odobritve vas še vedno vodijo na obstoječo stran s poročili o stroških.
- Potrdila bodo obdelana prek Microsoft Azure Cognitive Services ter metapodatki bodo izvlečeni in dodani.
- Dodana je možnost, ki omogoča ustvarjanje poročila o stroških, ki vključuje ujemajoča se nepovezana potrdila.
- Možnost, ki je dodana v poročila o stroških, vam omogoča, da iz potrdila ustvarite vrstico stroška ali poskušate poiskati ujemanje obstoječega potrdila z obstoječo vrstico stroška.

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

**Ali Microsoft za svoje modele uporablja moje podatke?**

Ne, Microsoft je za storitev obdelave potrdil zgradil splošni model strojnega učenja. Ta model ne temelji na potrdilih, ki jih naložite.

**Kje je na voljo in obdelana ta funkcija?**

Trenutno so podprte Združene države Amerike.

**Kam gredo moja potrdila?**

Storitev Finance pri Cognitive Services izvleče podatke polja. Cognitive Services ohrani kopijo potrdila do 24 ur med izvajanjem obdelave. Po končani obdelavi rešitev Cognitive Services potrdilo odstrani. Potrdila so še vedno shranjena v storitvi Finance.

Za več informacij glejte [Omogočanje razumevanja potrdil z novo zmožnostjo prepoznavalnika obrazcev](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
