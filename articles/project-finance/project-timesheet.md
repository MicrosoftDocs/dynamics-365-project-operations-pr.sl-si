---
title: Mobilna aplikacija Project Timesheet
description: Ta tema vsebuje informacije o mobilni aplikaciji Microsoft Dynamics 365 Project Timesheet. Mobilna aplikacija Project Timesheet omogoča uporabnikom, da oddajo časovne liste za projekte in jih odobrijo prek mobilne naprave.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: e2eb387f-5bb3-419c-953b-3bbc2f050059
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 6cd4629e9380fbe3d1839ba31a819c9057d1258c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755820"
---
# <a name="project-timesheet-mobile-application"></a>Mobilna aplikacija Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pregled

Mobilna aplikacija Microsoft Dynamics 365 Project Timesheet omogoča uporabnikom, da oddajo časovne liste za projekte in jih odobrijo prek mobilne naprave (naprave iPhone ali Android). Ta mobilna aplikacija vključuje funkcionalnost časovnih listov iz območja vodenja projekta in računovodstva rešitve Dynamics 365 Finance, s čimer izboljša produktivnost in učinkovitost uporabnika ter omogoča pravočasni vnos časa in odobritev časovnih listov projekta.

## <a name="download-and-install-the-mobile-app"></a>Prenos in namestitev mobilne aplikacije

Iz trgovine z aplikacijami si za svojo napravo prenesite in namestite mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet za naprave Android ali iPhone.

## <a name="enable-the-app"></a>Omogočanje aplikacije 

V rešitvi Finance mora biti omogočena mobilna aplikacija Project Timesheet. Če želite omogočiti funkcionalnost, pojdite na **Vodenje projekta in računovodski parametri \> Časovni list** in izberite **Omogočanje parametra za Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Prijava v mobilno aplikacijo

1.  Zaženite aplikacijo v mobilni napravi.

2.  Vnesite URL za rešitev Finance.

3.  Ko se prvič prijavite, boste pozvani k vnosu uporabniškega imena in gesla. Vnesite svoje poverilnice.

4.  Prijavljeni boste v privzeto podjetje.

## <a name="submit-a-project-timesheet"></a>Pošiljanje časovnega lista projekta

V aplikaciji lahko ustvarite časovni razpored projekta in ga pošljete. Nov časovni list lahko razvijete na podatkih iz prejšnjega časovnega lista, shranjenih vrstic ali projektnih nalog. Če ste določeni za pooblaščenca, lahko vnesete časovni list za drugega delavca. Če želite ustvariti časovni list kot pooblaščenec, izberite gumb **Meni** in nato ime vira.

Stran s časovnim listom bo ustvarila nov časovni list za obdobje časovnega lista, ki temelji na trenutnem datumu. Prikazan bo delovni teden. Če obdobje časovnega lista zajema več tednov, lahko na zavihkih delovnega tedna izberete drug delovni teden.
Če obstaja časovni list za trenutni datum, bo prikazan. Če želite ustvariti nov časovni list v drugem obdobju časovnega lista, izberite gumb **Meni** in nato **Nov časovni list**.

Informacije o projektu lahko vnesete tako, da kliknete dejanje **Dodaj čas** ali **Kopiraj čas iz**. Dejanje **Kopiraj čas iz** kopira podatke o vrstici projekta, ne kopira pa ur. Meni **Kopiraj čas iz** vključuje naslednje možnosti:

- **Kopiraj iz obstoječega časovnega lista** – kopiranje vrstic časovnega lista iz obstoječega časovnega lista.

- **Kopiraj iz priljubljenih** – ustvarjanje novih vrstic časovnega lista z uporabo nastavitev za časovni list, ki ste jih izbrali kot priljubljene.

- **Kopiraj iz naloge** – ustvarjanje novih vrstic časovnega lista iz dodeljenih projektov.

Prikazane informacije o projektu so odvisne od mobilnih parametrov, ki ste jih določili na strani **Vodenje projekta in računovodski parametri**.

V polju **Pravna oseba** izberite pravno osebo, za katero ste izvedli projektno delo. Polje **Pravna oseba** je na voljo samo, če je za vašo pravno osebo omogočena podpora za časovni list med podjetji.

Za časovni list izberite stranko, ki je povezana s projektom. V prvotni izdaji za naprave Android, vnos po stranki ni podprt, saj je najprej treba izbrati projekt. Če ste najprej izbrali projekt, se polje **Stranka** samodejno izpolni.

V polju **Projekt** izberite projekt, za katerega želite vnesti čas. Polje **Stranka** se samodejno izpolni.

Iskanje strank in projektov omogoča iskanje med strankami in projekti.

Izberite zahtevane podatke v poljih **Kategorija**, **Dejavnost**, **Lastnost vrstice**, **Skupina prometnega davka** in **Skupina prometnega davka za izdelek**. Ta polja je mogoče preglasiti.

Polje **Lastnost vrstice** bo nastavljeno na privzeto vrednost, ki temelji na vodenju projekta in računovodskih parametrih. Če so projekt/kategorija in parametri kategorije/vira omogočeni, bo vrednost polja **Lastnost vrstice** nastavljena na privzeto vrednost, ki ste jo določili za to preverjanje veljavnosti. Če projekt/kategorija in parametri kategorije/vira niso omogočeni, bo vrednost polja **Lastnost vrstice** nastavljena na privzeto glede na polje **Omogoči privzeto lastnost vrstice** na strani **Vodenje projekta in računovodski parametri**. vrednost polja **Lastnost vrstice** je mogoče preglasiti.

Če želite dodati čas, izberite dan. Vnesite število ur, ki ste jih opravili vsak dan.

Če želite dodati komentarje o urah, ki jih vnašate, kliknite **Dodaj komentarje** in nato vnesite komentarje za notranje občinstvo, javno občinstvo ali oboje.
Notranje komentarje si lahko ogledajo vodje projektov. Komentarji strank so vključeni v računih.

Če želite vrstico shraniti med priljubljene, potrdite polje in kliknite **Shrani med priljubljene**.

Finančna razsežnost in podpora za priloge nista na voljo v mobilni aplikaciji.

Za izpolnjevanje časovnega list nadaljujte z dodajanjem zahtevanih projektnih vrstic.

Kliknite **Pošlji**, da pošljete časovni list v potek dela za odobritev.

## <a name="review-timesheets"></a>Pregled časovnih listov

Seznam časovnih listov, ki jih je treba pregledati, je na voljo v meniju. Ta možnost je na voljo samo, če ste določeni za potrjevalca poteka dela. Podprta sta odobritev glave in vrstic. Odobritev ravni vrstice ponuja možnost označevanja ene ali več vrstic za odobritev. Po pregledu podatkov o časovnem listu kliknite **Odobri**, **Pooblasti** ali **Nazaj** za nadaljevanje poteka dela.
