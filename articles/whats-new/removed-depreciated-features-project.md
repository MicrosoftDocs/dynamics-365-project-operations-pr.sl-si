---
title: Odstranjene ali zastarele funkcije v Dynamics 365 Project Operations
description: Ta članek opisuje funkcije, ki so bile odstranjene ali načrtovane za odstranitev iz Dynamics 365 Project Operations.
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
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Odstranjene ali zastarele funkcije v Dynamics 365 Project Operations

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvajanje – posel do izstavitve predračuna in Project Operations za primere uporabe z naročili na zalogi/v proizvodnji_

Ta članek opisuje funkcije, ki so bile odstranjene ali načrtovane za odstranitev iz Dynamics 365 Project Operations.

- *Odstranjena* funkcija v izdelku ni več na voljo.
- *Opuščena* funkcija se ne razvija več in bo lahko odstranjena s prihodnjo posodobitvijo.

S pomočjo tega seznama boste lažje razmislili o navedenih odstranitvah in opustitvah glede na svoje načrte.

> [!NOTE]
> Podrobne informacije o predmetih v aplikacijah za finance in poslovanje najdete v [**Tehnična referenčna poročila**](/dynamics/s-e/global/axtechrefrep_61). Primerjate lahko različne različice teh poročil, da izveste več o predmetih, ki so bili spremenjeni ali odstranjeni v vsaki različici aplikacij za finance in poslovanje.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcije, odstranjene ali zastarele v izdaji Project Operations marca 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Vodenje projektov in računovodstvo Parameter "Vedno ustvari transakcijo popravka".

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Transakcije popravkov so potrebne za namene revizije. Po opustitvi bo ta parameter skrit. Sistem bo vedno ustvaril prilagoditvene transakcije, tako kot to počne trenutno, ko je parameter nastavljen na **ja** |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za proizvodne/založene scenarije |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo skrili parameter in spremenili vedenje sistema, tako da bodo transakcije prilagoditev vedno ustvarjene. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Vodenje projekta in računovodstvo Parameter »Uporabi datum prilagoditve kot nov datum projekta«.

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Ta parameter je bil prvotno uporabljen za omogočanje prilagoditev, ko je bil proračunsko obodbje zaprt. Vendar pa ni več potreben, ker je mogoče obračunski datum transakcije spremeniti na prvi datum odprtega obdobja, če je konfiguriran. Datuma projekta ne smete spreminjati, ker predstavlja datum, ko je prišlo do transakcije. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za proizvodne/založene scenarije |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo skrili parameter in spremenili vedenje sistema, tako da se datum projekta pri prilagoditvah nikoli ne spremeni. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Delovni tok zahteve za vir v projektnih operacijah za scenarije, ki temeljijo na zalogi/produkciji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Zastarelo zaradi nizke uporabe in omejitev obsega transakcij. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za proizvodne/založene scenarije |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo onemogočili možnost zahtevanja virov za projekt z uporabo poteka dela. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stran s predlogom računa za projekt brez pogleda glave in vrstic

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Opuščeno zaradi izboljšav strani, ki je bila predstavljena skupaj z **Uporabite predlog računa za projekt in obrazce dnevnika računa s pogledom glave in vrstic** ključ funkcije. |
| **Zamenjava z drugo funkcijo?** | Da |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za proizvodne/založene scenarije; Projektne operacije za scenarije virov/nezaloženih |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo izklopili prejšnjo (podedovano) stran in vklopili **Uporabite predlog računa za projekt in obrazce dnevnika računa s pogledom glave in vrstic** funkcijski ključ privzeto. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcije, odstranjene ali zastarele v izdaji Project Operations decembra 2021

### <a name="collaboration-workspaces"></a>Delovni prostori za sodelovanje

[Ustvarite ali povežite delovni prostor za sodelovanje (projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Zastarelo zaradi majhne uporabe. Stranke, ki uporabljajo Project Operations za vire/nezaložene scenarije, lahko izkoristijo [Sodelovanje z Office Groups](../project-management/collaboration-groups.md). |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija  |
| **Možnost uvajanja** | Projektne operacije za proizvodne/založene scenarije |
| **Stanje** | Zastarelo: Do 1. decembra 2022 načrtujemo, da ne bomo več podpirali delovnih prostorov za sodelovanje. |
