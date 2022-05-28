---
title: Odstranjene ali zastarele funkcije v Dynamics 365 Project Operations
description: Ta tema opisuje funkcije, ki so bile odstranjene ali načrtovane za odstranitev iz Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601590"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Odstranjene ali zastarele funkcije v Dynamics 365 Project Operations

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvajanje – posel do izstavitve predračuna in Project Operations za primere uporabe z naročili na zalogi/v proizvodnji_

Ta tema opisuje funkcije, ki so bile odstranjene ali načrtovane za odstranitev iz Dynamics 365 Project Operations.

- *Odstranjena* funkcija v izdelku ni več na voljo.
- *Opuščena* funkcija se ne razvija več in bo lahko odstranjena s prihodnjo posodobitvijo.

S pomočjo tega seznama boste lažje razmislili o navedenih odstranitvah in opustitvah glede na svoje načrte.

> [!NOTE]
> Podrobne informacije o predmetih v aplikacijah Finance in Operations lahko najdete v [**Tehnična referenčna poročila**](/dynamics/s-e/global/axtechrefrep_61). Primerjate lahko različne različice teh poročil, da izveste o predmetih, ki so bili spremenjeni ali odstranjeni v vsaki različici aplikacij Finance in Operations.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcije, odstranjene ali opuščene v izdaji Project Operations marca 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Vodenje projekta in računovodstvo parameter "Vedno ustvari prilagoditveno transakcijo".

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Transakcije prilagoditve so potrebne za namene revizije. Po prenehanju veljavnosti bo ta parameter skrit. Sistem bo vedno ustvaril prilagoditvene transakcije, tako kot trenutno, ko je parameter nastavljen na **da**. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za scenarije proizvodnje/zaloge |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo skrili parameter in spremenili vedenje sistema, tako da bodo transakcije prilagajanja vedno ustvarjene. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Vodenje in računovodstvo projekta "Uporabi datum prilagoditve kot nov datum projekta".

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Ta parameter je bil prvotno uporabljen za omogočanje prilagoditev, ko je bil proračunsko obodbje zaprt. Vendar to ni več potrebno, ker se lahko datum obračuna transakcije spremeni na prvi datum odprtega obdobja, če je konfiguriran. Datuma projekta ne smete spreminjati, ker predstavlja datum, ko je prišlo do transakcije. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za scenarije proizvodnje/zaloge |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo skrili parameter in spremenili vedenje sistema, tako da se datum projekta ob prilagoditvah nikoli ne spremeni. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Potek dela zahteve za vire v projektnih operacijah za scenarije, ki temeljijo na zalogi/proizvodnji

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Zastarelo zaradi nizke uporabe in omejitev obsega transakcij. |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za scenarije proizvodnje/zaloge |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo onemogočili možnost zahtevanja sredstev za projekt z uporabo poteka dela. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stran predloga računa projekta brez pogleda glave in vrstic

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Zastarelo zaradi izboljšav strani, ki je bila uvedena skupaj z **Uporabite predlog računov projekta in obrazce dnevnika računov s pogledom Glava in vrstice** funkcijski ključ. |
| **Zamenjava z drugo funkcijo?** | Da |
| **Zadevna področja izdelkov** | Aplikacija |
| **Možnost uvajanja** | Projektne operacije za scenarije proizvodnje/zaloge; Projektne operacije za scenarije z viri/brez zalog |
| **Stanje** | Zastarelo: do 1. marca 2023 bomo izklopili prejšnjo (podedovano) stran in vklopili **Uporabite predlog računov projekta in obrazce dnevnika računov s pogledom Glava in vrstice** funkcijska tipka privzeto. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcije, odstranjene ali opuščene v izdaji Project Operations decembra 2021

### <a name="collaboration-workspaces"></a>Delovni prostori za sodelovanje

[Ustvarite ali povežite z delovnim prostorom za sodelovanje (projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razlog za opustitev/odstranitev** | Zastarelo zaradi nizke uporabe. Stranke, ki uporabljajo Project Operations za scenarije virov/brez zalog, lahko izkoristijo vzvod [Sodelovanje s pisarniškimi skupinami](../project-management/collaboration-groups.md). |
| **Zamenjava z drugo funkcijo?** | No |
| **Zadevna področja izdelkov** | Aplikacija  |
| **Možnost uvajanja** | Projektne operacije za scenarije proizvodnje/zaloge |
| **Stanje** | Zastarelo: do 1. decembra 2022 načrtujemo, da ne bomo več podpirali delovnih prostorov za sodelovanje. |
