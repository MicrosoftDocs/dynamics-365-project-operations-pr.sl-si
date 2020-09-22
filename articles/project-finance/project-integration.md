---
title: Integracija odjemalca Microsoft Project
description: Načrtovanje in vzdrževanje projektnega razporeda je lahko zapleteno, zato morajo vodje projektov uporabljati orodja, ki jim pomagajo pri izpolnjevanju te naloge. Integracija z odjemalcem Microsoft Project Client nudi podporo za odpiranje in upravljanje strukturirane členitve projektnega dela.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755856"
---
# <a name="microsoft-project-client-integration"></a>Integracija odjemalca Microsoft Project

[!include [banner](../includes/banner.md)]

Načrtovanje in vzdrževanje projektnega razporeda je lahko zapleteno, zato morajo vodje projektov uporabljati orodja, ki jim pomagajo pri izpolnjevanju te naloge. Integracija z odjemalcem Microsoft Project Client nudi podporo za odpiranje in upravljanje strukturirane členitve projektnega dela. Vodja projekta lahko objavi vse spremembe nazaj v strukturirano členitev projektnega dela rešitve Dynamics 365 Finance.

> [!NOTE]
> Če uporabljate julijsko posodobitev (različica 10.0.4), morate namestiti KB 4054797 in 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfiguracija dodatka odjemalca Microsoft Project Client
Če želite omogočiti integracijo z odjemalcem Microsoft Project Client, morate namestiti dodatek Microsoft Dynamics 365 v uporabnikovo odjemalsko aplikacijo Microsoft Project. To naredite tako, da odprete **Delovni prostor za upravljanje projektov**.

•   Kliknite **Konfiguriraj dodatek odjemalca projekta** v razdelku **Povezave** > **Nastavitev** delovnega prostora.

•   Kliknite **Odpri** in ob pozivu še **Zaženi**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Odpiranje in urejevanje obstoječega osnutka strukturirane členitve dela v odjemalcu Microsoft Project Client
Če ima projekt v rešitvi Dynamics 365 Finance že ustvarjeno strukturirano členitev dela, lahko strukturirano členitev dela odprete v aplikaciji Microsoft Project Client, kadar je ta v stanju osnutka. Če želite to možnost odpreti na strani **Projekt**, kliknite povezavo **Odpri v odjemalcu Microsoft Project** na zavihku **Načrt**. To stran lahko odprete tudi v aplikaciji Microsoft Project Client s klikom **Odpri** na zavihku **Microsoft Dynamics 365**. Na seznamu izberite možnost **Pravna oseba** in **Projekt**.

> [!NOTE]
> Če uporabljate Internet Explorer za svoj brskalnik, boste morali klikniti **Shrani**, da boste lahko datoteko ročno odprli iz mesta, kamor je prenesena. Ali pa kliknite **Shrani in odpri**, da odprete datoteko v odjemalcu Microsoft Project Client. Ne preimenujte datoteke med shranjevanjem.

Pred kakršnim koli urejanjem datoteke s pomočjo odjemalca Microsoft Project Client, jo morate najprej preveriti. Kliknite **Preveri** na zavihku **Microsoft Dynamics 365**. S tem boste drugim uporabnikom preprečili, da bi hkrati urejali strukturirano členitev dela znotraj rešitve Finance. Če želite po končanih popravkih objaviti strukturirano členitev dela, kliknite **Prijava** na zavihku **Microsoft Dynamics 365**.

Če je bila projektna skupina že dodana projektu v rešitvi Finance, se seznam virov zapolni s člani skupine. Če projektna skupina še ni dodana projektu, lahko izberete vire in sestavite skupino znotraj odjemalca Microsoft Project Client, tako da kliknete gumb **Viri** na zavihku **Microsoft Dynamics 365**. 

Spodaj navedeni podatki se bodo v okviru postopka prijave sinhronizirali nazaj v program Finance:

•   Naziv opravila

•   Datum začetka

•   Datum zaključka

•   Predhodniki

•   Imena virov

•   Kategorija

•   Kategorija vira

•   Delovni čas

•   Beležke

•   Prednost

> [!NOTE]
> Če v datoteko odjemalca Microsoft Project Client dodate druge stolpce, se ti ne bodo shranili v datoteko in ne bodo prikazani ob ponovnem odpiranju datoteke.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Ustvarjanje strukturirane členitve dela za obstoječi projekt z odjemalcem Microsoft Project Client
Če želite ustvariti novo strukturirano členitev dela z odjemalcem Microsoft Project Client, sledite spodaj navedenim korakom:


1.  Odprite odjemalca Microsoft Project Client.

2.  Na zavihku **Microsoft Dynamics 365** kliknite **Odpri**.

3.  Izberite možnost **Pravna oseba** za projekt.

4.  Izberite **Projekt**.

5.  Kliknite **Ogled** na zavihku **Microsoft Dynamics 365**.

6.  Ko ste pripravljeni na objavo v rešitvi Finance, kliknite **Prijava** na zavihku **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Zamenjava obstoječe strukturirane členitve dela za obstoječi projekt z odjemalcem Microsoft Project Client
Če želite ustvariti novo strukturirano členitev dela z odjemalcem Microsoft Project Client in zamenjati obstoječo strukturirano členitev dela za obstoječi projekt, sledite tem korakom:

1.  Odprite odjemalca Microsoft Project Client.

2.  Ustvarite razpored v odjemalcu Microsoft Project Client.

3.  Na zavihku **Microsoft Dynamics 365** kliknite **Shrani spremembe** > **Zamenjaj obstoječi projekt**.

4.  Izberite možnost **Pravna oseba** za projekt.

5.  Izberite **Projekt**.

6.  Kliknite **V redu**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Ustvarite nov projekt v odjemalcu Microsoft Project Client


1.  Odprite odjemalca Microsoft Project Client.

2.  Ustvarite razpored v odjemalcu Microsoft Project Client.

3.  Na zavihku **Microsoft Dynamics 365** kliknite **Shrani spremembe** > **Shrani v nov projekt**.

4.  Izberite možnost **Pravna oseba** za projekt.

5.  Po potrebi vnesite **ID projekta**.

6.  Vnesite **Ime projekta**.

7.  Izberite **Vrsto projekta**, **Projektno skupino** in **ID projektne pogodbe**. Lahko pa kliknete možnost **Novo** in ustvarite novo projektno pogodbo.

8.  Izberite **Koledar**, ki ga želite uporabiti za vire.

11. Kliknite **V redu**.
