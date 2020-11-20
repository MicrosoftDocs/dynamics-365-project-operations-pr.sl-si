---
title: Konfiguracija integracije storitve Project Operations po pravnih osebah
description: Ta tema vsebuje informacije o nastavitvi integracije po pravnih osebah v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122903"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfiguracija integracije storitve Project Operations po pravnih osebah 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema pojasnjuje korake, potrebne za konfiguracijo storitve Dynamics 365 Project Operations po pravnih osebah.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Omogočanje ključev funkcij v storitvi Dynamics 365 Finance

Izvedite naslednje korake, da omogočite zahtevane funkcije.

1. V storitvi Dynamics 365 Finance izberite delovni prostor **Upravljanje funkcij**.
2. Pri možnosti **Seznam funkcij** poiščite in omogočite naslednje funkcije:
  
    - **Omogočanje več podrobnosti pogodbe za projekt**
    - **Omogočanje storitve Project Operations za Dynamics 365 Customer Engagement**

> [!NOTE]
> Če **ključi funkcij** niso navedeni, preverite, ali vaša različica storitve za finance izpolnjuje najmanjše zahteve glede različice (različica aplikacije 10.0.13 z vsemi posodobitvami kakovosti ali novejša različica). Izberite **Preveri, ali so na voljo posodobitve**, da osvežite seznam funkcij.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Opredelitev scenarija za uvajanje storitve Project Operations za pravno osebo

Project Operations lahko omogočite v storitvi Dynamics 365 Customer Engagement na ravni pravne osebe. V storitvi Project Operations lahko uporabljate eno pravno osebo v okviru storitve Dynamics 365 Customer Engagement za scenarije, ki temeljijo na viru/nezalogi. V istem okolju imate lahko še eno pravno osebo, ki uporablja Project Operations za scenarije z naročili na zalogi/v proizvodnji.

1. V storitvi Dynamics 365 Finance odprite **Vodenje projektov in računovodstvo** > **Nastavitev** > **Globalno vodenje projektov in računovodski parametri**.
2. Na seznamu razpoložljivih pravnih oseb izberite entitete, v katerih je vključenih več podrobnosti pogodbe in bodo omogočene funkcije Dynamics 365 Customer Engagement za Project Operations. Ne izberite pravnih oseb, ki bodo uporabljale Project Operations za scenarije z naročili na zalogi/v proizvodnji.

> [!NOTE]
> Pravno osebo je mogoče izbrati le, če nima obstoječih projektov.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfiguracija parametrov za vodenje projektov in računovodstvo

Vsaka pravna oseba, ki uporablja Project Operations v okviru storitve Dynamics 365 Customer Engagement, potrebuje nabor privzetih parametrov. Ti parametri so nastavljeni na zavihku **Project Operations** na strani **Vodenje projektov in računovodski parametri**. Parametri so naslednji:

  - **Privzete vrednosti vrste obračunavanja**: Project Operations uporablja fiksni nabor privzetih vrednosti vrste obračunavanja, ki jih je treba preslikati v lastnosti vrstic storitve za finance. Ustvarite zapis za vsako vrsto obračunavanja: **Ni določeno**, **Se zaračuna**, **Se ne zaračuna**, **Brezplačno** in **Ni na voljo**.
  - **Privzete vrednosti za kategorije projektov**: izberite privzete kategorije projektov, ki se bodo uporabljale za vsako vrsto transakcije. Te privzete vrednosti se bodo uporabljale pri možnosti **Dnevnik integracij za Project Operations** in pri ocenah, kjer za dejanske vrednosti projekta ni določena nobena kategorija transakcij.
  - **Napovedi**: izberite model napovedi, ki se bo uporabljal za oceno časa in stroškov.
