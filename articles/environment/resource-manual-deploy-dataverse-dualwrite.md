---
title: Ročna uvedba aplikacije Project Operations Dataverse s podporo za dvojno zapisovanje
description: Ta tema vsebuje informacije o tem, kako ročno uvesti aplikacijo Project Operations Dataverse tako, da bo podpirala dvojno zapisovanje.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274028"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Ročna uvedba aplikacije Project Operations Dataverse s podporo za dvojno zapisovanje

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema vsebuje informacije o tem, kako aplikacijo Microsoft Dynamics 365 Project Operations ročno uvesti v storitev Microsoft Dataverse tako, da bo podpirala dvojno zapisovanje. Če so izpolnjene določene zahteve, Aplikacija Project Operations zazna konfiguracijo okolja in nudi dodatno podporo za dvojno zapisovanje.

Če ste sledili navodilom v tej temi, lahko med uvajanjem prek Microsoft Dynamics Lifecycle Services (LCS) preskočite uvajanje integracije Microsoft Power Platform (pred tem poznane kot okolje storitve Common Data Service).

Postopek uvajanja aplikacije Project Operations v Dataverse z omogočeno podporo za dvojno zapisovanje je sestavljen iz štirih korakov:

1. [Ustvarjenje novega okolja v storitvi Dataverse s podporo za dvojno zapisovanje](#create).
2. [Dodajanje pogojev za dvojno zapisovanje v okolje](#prerequisites).
3. [Dodajanje aplikacije Project Operations v storitvi Dataverse](#dataverse).
4. [Povezava okolij](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Ustvarjenje novega okolja v storitvi Dataverse s podporo za dvojno zapisovanje

Če želite zaključiti postopek, se morate vpisati kot skrbnik.

1. Odprite [skrbniško središče Power Platform](https://admin.powerplatform.com) in se vpišite kot skrbnik.
2. Ustvarite novo okolje in ga poimenujte.
3. Izberite vrsto okolja. Če ste se prijavili za preskusno različico, izberite **Preskusna različica (na podlagi naročnine)**.
4. Potrdite območje uvajanja.
5. Omogočite možnost **Ustvarjenje zbirke podatkov za to okolje**. 
6. Potrdite jezik ter potrdite, da se valuta ujema z valuto aplikacije Finance and Operations.
7. Omogočite možnost **Aplikacije Dynamics 365** in potrdite, da je polje **Samodejno uvedi te aplikacije** nastavljeno na **Brez**.
8. Dodajte varnostno skupino, če je to zahtevano.
9. Izberite **Shrani**, da ustvarite okolje.
10. Počakajte, da se uvajanje zaključi in da okolje vstopi v stanje **Pripravljeno**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Dodajanje pogojev za dvojno zapisovanje v okolje

Podpora za dvojno zapisovanje vsebuje dodatna polja, dodana ključnim entitetam, kot je entiteta **Podjetje**. Če podporo za dvojno zapisovanje vključujete v obstoječe okolje, bo za to, da jo omogočite, morda potrebna posodobitev podatkov. Za informacije o tem, kako uporabiti metodo ponovnega vzorčenja podatkov, si oglejte možnost [Uporaba metode ponovnega vzorčenja podatkov podjetja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Za več informacij o dvojnem zapisovanju si oglejte [Sistemske zahteve za dvojno zapisovanje](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Zaključite postopek dodajanja pogojev za dvojno zapisovanje v okolje.

1. Odprite okolje, ki ste ga ustvarili, in pojdite v razdelek **Viri** \> **Aplikacija Dynamics 365**.
2. Na seznamu aplikacije izberite možnost **Osnovna rešitev za dvojno zapisovanje** in jo namestite.
3. Počakajte, da se namestitev zaključi. Nato na seznamu aplikacije izberite možnost **Rešitev za organiziranje aplikacije za dvojno zapisovanje** in jo namestite.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Dodajanje aplikacije Project Operations v storitvi Dataverse

Ta postopek lahko zaključite samo, če ste zaključili prejšnje postopke, še preden ste namestili aplikacijo Project Operations. Med namestitvijo sistem analizira konfiguracijo okolja in doda podporo za dvojno zapisovanje, če je to zahtevano.

1. Odprite okolje, ki ste ga ustvarili, in pojdite v razdelek **Viri** \> **Aplikacija Dynamics 365**.
2. Na seznamu aplikacije izberite **Microsoft Dynamics 365 Project Operations** in ga namestite.

## <a name="link-your-environments"></a><a name="link"></a>Povezava okolij

Ko je okolje Dataverse uvedeno, lahko v aplikaciji Finance and Operations nastavite povezavo. Upoštevajte korake v razdelku [Uporaba čarovnika za dvojno zapisovanje z namenom povezave okolij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
