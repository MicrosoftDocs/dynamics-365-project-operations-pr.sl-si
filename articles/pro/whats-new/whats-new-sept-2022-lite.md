---
title: Novosti za september 2022 – poenostavljeno uvajanje storitve Project Operations
description: V tem članku so na voljo informacije o posodobitvah kakovosti, ki so na razpolago v septembrski (2022) izdaji poenostavljenega uvajanja aplikacije Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634873"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novosti za september 2022 – poenostavljeno uvajanje storitve Project Operations

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.46.0.60. storitve Dataverse

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

| Območje funkcij | Ime funkcije | Več informacij |
| --- | --- | --- |
| Upravljanje priložnosti | **Revizija in aktivacija ponudb**<br>Project Operations prinaša popolno podporo prodajnemu procesu. Projektne ponudbe lahko aktivirate, da predstavljajo stanje, kjer je ponudba na voljo samo za branje in je v pregledu. Aktivirane ponudbe lahko revidirate, da se ustvarijo nove ponudbe, ki imajo povečano številko revizije. Aktivirane projektne ponudbe ali revizije ponudbe lahko zaprete kot »pridobljeno« ali »izgubljeno«. | [Aktiviranje in popravljanje projektne ponudbe](/dynamics365/project-operations/sales/activation-and-revision) |
| Zaračunavanje in oblikovanje cen | **Privzeto oblikovanje cen glede na neznani časovni pas**<br>Aplikacija Project Operations je uvedla koncept neznanega datuma glede na časovni pas za vse dejanske vrednosti projekta. Novo polje, **Datum transakcije**, je zdaj na voljo v vrsticah dnevnika in dejanskih vrednostih ter bo uporabljeno za shranjevanje datuma, ko je bila transakcija izvedena, vendar brez pretvorbe tega datuma v usklajen univerzalni čas. Ta datum bo uporabljen za nadaljnje procese, kot sta privzeto nastavljanje cene in ustvarjanje računov. | <p>[Določitev mer stroškov za ocene in dejanske vrednosti, ki temeljijo na projektih](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Določitev prodajnih cen za ocene in dejanske vrednosti, ki temeljijo na projektu](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Zaračunavanje in oblikovanje cen | **Preglasitve cen, ki začnejo veljati na določen datum, v aplikaciji Project Operations**<br>Funkcija preglasitve cen, ki začnejo veljati na določen datum, omogoča način za preglasitev ali spremembo določenih cen v ceniku. | [Preglasitve cen, ki začnejo veljati na določen datum](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Čas in strošek | **Globalni odobritelj**<br>Ta funkcija omogoča neodvisnega razvijalca programske opreme (ISV) in centralizirano odobritev, ne glede na stanje projekta ali člana ekipe v projektu. | [Varnost in odobritve](/dynamics365/project-operations/approvals/approvals-security) |
|Načrtovanje in sledenje projektov|**Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja** </br> </br>API za urejanje krivulj dodelitve virov omogoča razvijalcem, da programsko določijo trud osebe, ki je dodelila opravilo, v katerem koli podprtem časovnem obdobju za bolj natančno načrtovanje truda v časovnih fazah.|[Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2754422 | Ocene materiala in stroškov ne tečejo v aplikacijo Dynamics 365 Finance, ko so projekti kopirani v okolje Dataverse. |
| Čas in strošek | 2787409 | Neveljavni odobritelj lahko odobri vnos časa, ki ne temelji na projektu. |
| Upravljanje priložnosti | 2788907 | Posodobljeno sporočilo o napaki pri preverjanju edinstvenosti za vrstice naročila, ki vključujejo zastavice. |
| Čas in strošek | 2842253 | Obravnava izjeme z vrednostjo »null« za odobritev časa. |
| Zaračunavanje in oblikovanje cen | 2844181 | Neuspelo pridobivanje ID-ja korelacije blokira ustvarjanje računa. |
| Zaračunavanje in oblikovanje cen | 2876628 | QLD, CLD – ocena razrešitve cenika bi morala uporabljati podedovana polja obsega datuma za cenik. |
| Podizvajalske pogodbe | 2893222 | Če za podrobnosti podizvajalske pogodbe ni določena nobena vloga, bi moralo biti mogoče to vrstico izbrati pri članu ekipe za katero koli vlogo. |
