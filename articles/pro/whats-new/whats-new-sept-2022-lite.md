---
title: Novosti za september 2022 – poenostavljeno uvajanje storitve Project Operations
description: V tem članku so informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta septembra 2022 Dynamics 365 Project Operations enostavna uvedba.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621378"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novosti za september 2022 – poenostavljeno uvajanje storitve Project Operations

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse različica okolja 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

| Območje funkcij | Ime funkcije | Več informacij |
| --- | --- | --- |
| Upravljanje priložnosti | **Revizija in aktivacija ponudb**<br>Project Operations prinaša popolno podporo prodajnemu procesu. Projektne ponudbe je mogoče aktivirati, da predstavljajo stanje, v katerem je ponudba samo za branje in je v pregledu. Aktivirane ponudbe je mogoče spremeniti, da se ustvarijo nove ponudbe, ki imajo povečano številko revizije. Aktivirane projektne ponudbe ali revizije ponudb je mogoče zapreti kot zmagovalne ali izgubljene. | [Aktiviranje in popravljanje projektne ponudbe](/dynamics365/project-operations/sales/activation-and-revision) |
| Zaračunavanje in oblikovanje cen | **Neplačila cene glede na časovni pas**<br>Project Operations je uvedel koncept agnostičnega datuma glede na časovni pas za vse dejanske podatke projekta. Novo polje, **Datum transakcije**, je zdaj na voljo v vrsticah dnevnika in dejanskih podatkih in bo uporabljen za shranjevanje datuma, ko je prišlo do transakcije, vendar brez pretvorbe tega datuma v koordinirani univerzalni čas. Ta datum bo uporabljen za nadaljnje postopke, kot sta neplačilo cene in ustvarjanje računov. | <p>[Določite stopnje stroškov za ocene in dejanske vrednosti na podlagi projekta](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Določite prodajne cene za ocene in dejanske vrednosti na podlagi projekta](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Zaračunavanje in oblikovanje cen | **Preglasitve cen z datumom veljavnosti v Project Operations**<br>Preglasitve cen z datumom veljavnosti omogočajo preglasitev ali spremembo določenih cen v ceniku. | [Preglasitve cen z datumom veljavnosti](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Čas in strošek | **Globalni odobritelj**<br>Ta funkcija omogoča neodvisnega prodajalca programske opreme (ISV) in centralizirano odobritev, ne glede na status projekta ali člana ekipe v projektu. | [Varnost in odobritve](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2754422 | Ocene materiala in stroškov se ne prenesejo v Dynamics 365 Finance, ko so projekti kopirani v Dataverse. |
| Čas in strošek | 2787409 | Neveljavni odobritelj lahko odobri vnos časa, ki ni projekt. |
| Upravljanje priložnosti | 2788907 | Posodobljeno sporočilo o napaki pri preverjanju edinstvenosti za vrstice naročila, ki vključujejo zastavice. |
| Čas in strošek | 2842253 | Obravnava ničelne izjeme za odobritev časa. |
| Zaračunavanje in oblikovanje cen | 2844181 | Neuspešno pridobivanje ID-ja korelacije blokira ustvarjanje računa. |
| Zaračunavanje in oblikovanje cen | 2876628 | QLD, CLD – Ocena razrešitve cenika bi morala uporabljati podedovana polja datumskega obsega cenika. |
| Podizvajanje | 2893222 | Če za linijo podizvajalca ni določena nobena vloga, bi moralo biti mogoče to linijo izbrati pri članu skupine za katero koli vlogo. |
