---
title: Odstranjene ali opuščene funkcije v aplikaciji Dynamics 365 Project Operations
description: Ta članek opisuje funkcije, ki so bile odstranjene ali za katere je predvidena odstranitev in aplikacije Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028349"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Odstranjene ali opuščene funkcije v aplikaciji Dynamics 365 Project Operations

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvajanje – posel do izstavitve predračuna in Project Operations za primere uporabe z naročili na zalogi/v proizvodnji_

Ta članek opisuje funkcije, ki so bile odstranjene ali za katere je predvidena odstranitev in aplikacije Dynamics 365 Project Operations.

- *Odstranjena* funkcija v izdelku ni več na voljo.
- *Opuščena* funkcija se ne razvija več in bo lahko odstranjena s prihodnjo posodobitvijo.

S pomočjo tega seznama boste lažje razmislili o navedenih odstranitvah in opustitvah glede na svoje načrte.

> [!NOTE]
> Podrobne informacije o predmetih v aplikacijah za finance in postopke najdete v razdelku [**Poročila tehničnih sklicev**](/dynamics/s-e/global/axtechrefrep_61). Primerjate lahko različne različice teh poročil, da izveste več o predmetih, ki so bili spremenjeni ali odstranjeni v vsaki različici aplikacij za finance in postopke.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Odstranjene ali opuščene funkcije v aplikaciji Project Operations, izdaja marca 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parameter upravljanja projektov in računovodstva »Vedno ustvari transakcijo prilagoditve«

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Transakcije prilagoditve so potrebne za namene spremljanja spremembe. Po opustitvi bo ta parameter skrit. Sistem bo vedno ustvaril transakcije prilagoditve, kot to počne trenutno, ko je parameter nastavljen na **Da**. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Project Operations za primere uporabe v proizvodnji/na zalogi |
| **Stanje** | Opuščeno: do 1. marca 2023 bomo skrili parameter in spremenili vedenje sistema, tako da bodo transakcije prilagoditev vedno ustvarjene. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parameter upravljanja projektov in računovodstva »Uporabi datum prilagoditve kot nov datum projekta«

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Ta parameter je bil prvotno uporabljen za omogočanje prilagoditev, ko je bilo proračunsko obdobje zaprto. Vendar pa ni več potreben, ker je mogoče računovodski datum transakcije spremeniti na prvi datum odprtega obdobja, če je konfiguriran. Datuma projekta ne smete spreminjati, ker predstavlja datum, ko je bila transakcija izvedena. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Project Operations za primere uporabe v proizvodnji/na zalogi |
| **Stanje** | Opuščeno: do 1. marca 2023 bomo skrili parameter in spremenili vedenje sistema, tako da datum projekta ne bo nikoli spremenjen pi prilagoditvah. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Potek dela zahteve vira v aplikaciji Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Opuščeno zaradi nizke uporabe in omejitev obsega transakcij. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Project Operations za primere uporabe v proizvodnji/na zalogi |
| **Stanje** | Opuščeno: do 1. marca 2023 bomo onemogočili možnost zahtevanja virov za projekt s potekom dela. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stran s predlogom računa za projekt brez pogleda glave in vrstic

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Opuščeno zaradi izboljšav strani, ki je bila predstavljena skupaj s ključem funkcije **Uporaba predloga računa za projekt in obrazcev dnevnika računa s pogledom glave in vrstic**. |
| **Zamenjava z drugo funkcijo?** | Da |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Project Operations za scenarije, ki temeljijo na proizvodnji/zalogi; Project Operations za scenarije, ki temeljijo na virih/nezalogi |
| **Stanje** | Opuščeno: do 1. marca 2023 bomo izklopili prejšnjo (podedovano) stran in privzeto vklopili ključ funkcije **Uporaba predloga računa za projekt in obrazcev dnevnika računa s pogledom glave in vrstic**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Odstranjene ali opuščene funkcije v aplikaciji Project Operations, izdaja decembra 2021

### <a name="collaboration-workspaces"></a>Delovni prostori za sodelovanje

[Ustvarjanje ali povezava delovnih prostorov za sodelovanje (projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Opuščeno zaradi nizke uporabe. Stranke, ki uporabljajo aplikacijo Project Operations za scenarije, ki temeljijo na virih/nezalogi, lahko izkoristijo funkcijo [Sodelovanje s skupinami Office](../project-management/collaboration-groups.md). |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija  |
| **Možnost uvajanja** | Project Operations za primere uporabe v proizvodnji/na zalogi |
| **Stanje** | Opuščeno: načrtujemo, da do 1. decembra 2022 načrtujemo ne bomo več podpirali delovnih prostorov za sodelovanje. |
