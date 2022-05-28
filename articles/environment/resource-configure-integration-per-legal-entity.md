---
title: Konfiguracija integracije storitve Project Operations po pravnih osebah
description: Ta tema vsebuje informacije o nastavitvi integracije po pravnih osebah v storitvi Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585858"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfiguracija integracije storitve Project Operations po pravnih osebah 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema vsebuje postopna navodila za konfiguracijo aplikacije Dynamics 365 Project Operations za pravno osebo.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Omogoči funkcijske tipke v Dynamics 365 Finance

Izvedite naslednje korake, da omogočite zahtevane funkcije.

1. V Dynamics 365 Finance pojdite na **Upravljanje funkcij** delovni prostor.
2. Pri možnosti **Seznam funkcij** poiščite in omogočite naslednje funkcije:
  
    - **Omogočanje več podrobnosti pogodbe za projekt**
    - **Omogočite operacije projekta na Dynamics 365 Customer Engagement**

> [!NOTE]
> Če **ključi funkcij** niso navedeni, preverite, ali vaša različica storitve za finance izpolnjuje najmanjše zahteve glede različice (različica aplikacije 10.0.13 z vsemi posodobitvami kakovosti ali novejša različica). Izberite **Preveri, ali so na voljo posodobitve**, da osvežite seznam funkcij.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Opredelitev scenarija za uvajanje storitve Project Operations za pravno osebo

Projektne operacije lahko omogočite na Dynamics 365 Customer Engagement na ravni pravne osebe. Za scenarije, ki temeljijo na virih/brez zalog, imate lahko eno pravno osebo, ki uporablja Operacije projekta na Dynamics 365 Customer Engagement. V istem okolju imate lahko še eno pravno osebo, ki uporablja Project Operations za scenarije z naročili na zalogi/v proizvodnji.

1. V Dynamics 365 Finance pojdite na **Vodenje projektov in računovodstvo** > **Nastaviti** > **Globalno vodenje projektov in računovodski parametri**.
2. Na seznamu razpoložljivih pravnih oseb izberite subjekte, pri katerih bo omogočeno več pogodbenih vrstic in funkcije Projektne operacije na Dynamics 365 Customer Engagement. Ne izberite pravnih oseb, ki bodo uporabljale Project Operations za scenarije z naročili na zalogi/v proizvodnji.

> [!NOTE]
> Pravno osebo je mogoče izbrati le, če nima obstoječih projektov.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfiguracija parametrov za vodenje projektov in računovodstvo

Vsaka pravna oseba, ki uporablja projektne operacije na Dynamics 365 Customer Engagement, potrebuje nabor privzetih parametrov. Ti parametri so nastavljeni na zavihku **Project Operations** na strani **Vodenje projektov in računovodski parametri**. Parametri so naslednji:

  - **Privzete vrednosti vrste obračunavanja**: Project Operations uporablja fiksni nabor privzetih vrednosti vrste obračunavanja, ki jih je treba preslikati v lastnosti vrstic storitve za finance. Ustvarite zapis za vsako vrsto obračunavanja: **Ni določeno**, **Se zaračuna**, **Se ne zaračuna**, **Brezplačno** in **Ni na voljo**.
  - **Privzete vrednosti za kategorije projektov**: izberite privzete kategorije projektov, ki se bodo uporabljale za vsako vrsto transakcije. Te privzete vrednosti se bodo uporabljale pri možnosti **Dnevnik integracij za Project Operations** in pri ocenah, kjer za dejanske vrednosti projekta ni določena nobena kategorija transakcij.
  - **Napovedi**: izberite model napovedi, ki se bo uporabljal za oceno časa in stroškov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]