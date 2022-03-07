---
title: Zajem računa s tehnologijo OCR
description: Ta tema vsebuje informacije o obdelavi z optičnim prepoznavanjem znakov (OCR) za potrdila.
author: suvaidya
ms.date: 11/10/2021
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
ms.openlocfilehash: 4dc1628a0dde0551aaf3bc10af628ef57881d85e
ms.sourcegitcommit: a51f40c905874103040708be2188c04ab0716c38
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798060"
---
# <a name="capture-a-receipt-using-ocr"></a>Zajem računa s tehnologijo OCR

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

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

      - Izberite **Ustvari**, da ustvarite ročno vneseno transakcijo stroška in izpolnite vrednosti, ki so izvlečene iz potrdila.
      - Če izberete **Išči ujemanje**, sistem poskuša poiskati ujemanje obstoječega stroška s potrdilom.

## <a name="installation"></a>Namestitev

Če želite uporabiti te napredne zmožnosti stroškov, namestite dodatek Expense Management Service za Microsoft Dynamics 365 Finance in vklopite funkcije v svojem primeru. Do dodatka lahko dostopate iz svojega projekta v Microsoft Dynamics storitvah življenjskega cikla (LCS).

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
- Še vedno lahko odprete prejšnjo stran **Poročila o stroških**, tako da obiščete **Upravljanje stroškov > Moji stroški > Poročila o stroških**.
- Poteki dela in morebitne odobritve vas še vedno vodijo na obstoječo stran s poročili o stroških.
- Prejemki bodo obdelani prek Microsoft Azure Cognitive Services, metapodatki pa bodo ekstrahirani in dodani.
- Dodana je možnost, ki omogoča ustvarjanje poročila o stroških, ki vključuje ujemajoča se nepovezana potrdila.
- Možnost, ki je dodana v poročila o stroških, vam omogoča, da iz potrdila ustvarite vrstico stroška ali poskušate poiskati ujemanje obstoječega potrdila z obstoječo vrstico stroška.

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

**Ali Microsoft za svoje modele uporablja moje podatke?**

Ne, Microsoft je za storitev obdelave potrdil zgradil splošni model strojnega učenja. Ta model ne temelji na potrdilih, ki jih naložite.

**Kje je na voljo in obdelana ta funkcija?**

Razpoložljivost te funkcije v različnih regijah je navedena v naslednji tabeli. Če vaša regija trenutno ni podprta, pošljite zahtevo za prednostno razpoložljivost storitve OCR v vaši regiji. 

| Regija | Podprto                         |
|--------|-----------------------------------|
| ZDA    | Da                               |
| Kanada    | Da                               |
| Združeno kraljestvo     | Da                               |
| AUS    | Da                               |
| EU     | Delno. Samo angleški računi. |
| Azija   | No                                |
| Japonska  | No                                |
| Afrika | No                                |

**Kam gredo moja potrdila?**

Storitev Finance pri Cognitive Services izvleče podatke polja. Cognitive Services ohrani kopijo potrdila do 24 ur med izvajanjem obdelave. Po končani obdelavi rešitev Cognitive Services potrdilo odstrani. Potrdila so še vedno shranjena v storitvi Finance.

Za več informacij glejte [Omogočanje razumevanja potrdil z novo zmožnostjo prepoznavalnika obrazcev](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
