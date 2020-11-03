---
title: Obdelava potrdila o stroških
description: Ta tema vsebuje informacije o obdelavi z optičnim prepoznavanjem znakov (OCR) za potrdila. Ta funkcija je namenjena izboljšanju uporabniške izkušnje pri ustvarjanju poročil o stroških v storitvi Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084914"
---
# <a name="expense-receipt-processing"></a>Obdelava potrdila o stroških

[!include [banner](../includes/banner.md)]

Vnos stroškov je bil izboljšan z uvedbo obdelave z optičnim prepoznavanjem znakov (OCR) za potrdila. Ta funkcija je namenjena izboljšanju uporabniške izkušnje pri ustvarjanju poročil o stroških.

## <a name="key-features"></a>Najpomembnejše funkcije

- Ime trgovca, datum in skupni znesek se izvlečejo iz potrdil.
- Funkcija poskuša izvesti ujemanje nepovezanih potrdil z nepovezanimi transakcijami stroškov.
- Uporabniki lahko ročno vnesejo transakcije stroškov iz potrdil.

## <a name="usage-examples"></a>Primeri uporabe

Za samodejno prilaganje potrdil, ki vključujejo transakcije s kreditnimi karticami, ko je ustvarjeno poročilo o stroških, storite naslednje:

  1. Odprite delovni prostor **Upravljanje stroškov**.
  2. Na zavihku **Potrdila** preverite, ali obstajajo nepovezana potrdila. Potrdila lahko naložite tudi na zavihek **Potrdila**.
  3. Na zavihku **Stroški** preverite, ali obstajajo nepovezani stroški. Običajno skrbnik stroškov uvozi te stroške od ponudnika kreditne kartice.
  4. Izberite **Novo poročilo o stroških**. Opazite lahko, da lahko zdaj vključite stroške in potrdila, ko ustvarite poročilo o stroških. Če dodate stroške in potrdila, se sproži samodejno ujemanje potrdil s stroški.

Če želite ustvariti strošek ali poiskati ujemanje stroška s potrdila, storite naslednje:

  1. Na poročilu o stroških na zavihku **Potrdila** priložite potrdilo z izbiro možnosti **Dodaj potrdila**.
  2. Pod naloženo sliko potrdila opazite možnosti **Ustvari** in **Išči ujemanje**.

      - Izberite **Ustvari** , da ustvarite ročno vneseno transakcijo stroška in izpolnite vrednosti, ki so izvlečene iz potrdila.
      - Če izberete **Išči ujemanje** , sistem poskuša poiskati ujemanje obstoječega stroška s potrdilom.

## <a name="installation"></a>Namestitev

Ta funkcija deluje v kombinaciji s funkcijo **Preoblikovana poročila o stroških** za poenostavljeno izkušnjo s stroški. Ta funkcija je na voljo samo za okolja Tier 2+, in sicer preskusna in produkcijska okolja.

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

Za več informacij o preoblikovani funkciji poročil o stroških glejte [Preoblikovana poročila o stroških](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

**Ali Microsoft za svoje modele uporablja moje podatke?**

Ne, Microsoft je za storitev obdelave potrdil zgradil splošni model strojnega učenja. Ta model ne temelji na potrdilih, ki jih naložite.

**Kje je na voljo in obdelana ta funkcija?**

Trenutno so podprte Združene države Amerike.

**Kam gredo moja potrdila?**

Storitev Finance pri Cognitive Services izvleče podatke polja. Cognitive Services ohrani kopijo potrdila do 24 ur med izvajanjem obdelave. Po končani obdelavi rešitev Cognitive Services potrdilo odstrani. Potrdila so še vedno shranjena v storitvi Finance.

Za več informacij glejte [Omogočanje razumevanja potrdil z novo zmožnostjo prepoznavalnika obrazcev](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
