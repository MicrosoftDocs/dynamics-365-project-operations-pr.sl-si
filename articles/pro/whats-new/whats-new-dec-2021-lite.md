---
title: Novosti za december 2021 – poenostavljeno uvajanje aplikacije Project Operations
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji poenostavljenega uvajanja aplikacije Project Operations za december 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914100"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novosti za december 2021 – poenostavljeno uvajanje aplikacije Project Operations

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.27.0.195, 4.27.0.242, 4.27.0.244 storitve Dataverse


## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

### <a name="subcontract-management"></a>Upravljanje podizvajalskih pogodb 

- [Podizvajalski člani projektne ekipe](../subcontracting/subcontracting-project-team-members.md): vodja projekta lahko ustvari imenovane ali splošne člane ekipe s podizvajalskimi pogodbami in podrobnostmi podizvajalske pogodbe, da vpliva na zaposlovanje in ocenjevanje.
- [Možnosti podizvajalske pogodbe za člane projektne ekipe](../subcontracting/subcon-options.md): pri izbiranju osebja za imenovane ali splošne člane projektne ekipe lahko vodja projekta pregleda obstoječe podizvajalske pogodbe ali ustvari nove podizvajalske pogodbe za enega ali več članov projektne ekipe. 
- [Ocena stroškov podizvajalskih dodelitev virov](../subcontracting/costing-subcon-ra.md): ocena stroškov projekta bo upoštevala podizvajalske dodelitev virov, stroške pa bo izračunala na podlagi nabavnih cenikov, povezanih s podizvajalskimi pogodbami. 
- [Konfiguracija plošče za načrtovanje za prikaz pogodbenih delavcev in podizvajalskih zmogljivosti](../subcontracting/configure-sb-subcon.md): ploščo za načrtovanje v aplikaciji Project Operations je zdaj mogoče konfigurirati za iskanje in predlaganje pogodbenega delavca, vrste virov, ki jih je mogoče rezervirati, in podizvajalske zmogljivosti skupaj z zaposlenimi. To konfiguracijo je mogoče uporabiti pri iskanju virov znotraj konteksta zaposlovanja za določeno projektno zahtevo ali pri iskanju izven konteksta projektne zahteve.
- [Zaposlovanje za projekt s pogodbenimi delavci in podizvajalskimi zmogljivostmi](../subcontracting/staffing-cw.md): pogodbene delavce je zdaj mogoče rezervirati za projekte, ki izkoriščajo izkušnje plošče za načrtovanje.
- [Beleženje časa, stroškov in porabe materiala na projektih za komponente podizvajalcev](../subcontracting/recording-subcon-actuals.md): pogodbeni delavci lahko beležijo čas in stroške, člani projektne ekipe pa lahko beležijo tudi porabo materialov, kupljenih s podizvajalsko pogodbo na projektu. To bo povzročilo beleženje natančnih stroškov pri projektih, ki uporabljajo kupljeno zmogljivost ali materiale.
- [Prehodi stanja na podizvajalsko pogodbo](../subcontracting/subcon-states.md): podizvajalske pogodbe je mogoče potrditi za dokončanje pogajanj z dobaviteljem, zaključiti za oznako zaključka dobave ali preklicati za oznako prekinitve pogodbe z dobaviteljem pred zaključkom dobave.

### <a name="task-planning"></a>Načrtovanje opravila
- Izboljšano odpravljanje težav za skrbnike sistema. Ko uporabnik ne more odpreti projekta, lahko skrbnik pregleda napake, ki niso povezane z licenco in jih ustvari aplikacija Project for the Web v [Dnevnikih razporejanja projekta](../../project-management/schedule-api-logs.md).
- [Uporabite kontrolne sezname opravil v aplikaciji Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). V aplikaciji Microsoft Project for the Web lahko opravilu dodate kontrolni seznam, da sledite določenim elementom.

## <a name="quality-updates"></a>Posodobitve kakovosti

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Načrtovanje in sledenje | 2392596 | API-ji za načrtovanje zdaj omogočajo posodobitve za polja **Preostali obseg dela**, **Dokončan obseg dela** in **Odstotek dokončanja**. |
| Načrtovanje in sledenje | 2478497 | Polja **Številka dejavnosti** in **ID opravila** za API-je razporejanja so lahko ob vnosu prazna, ker jih bo sistem izpolnil s samodejnim številčenjem.|
| Čas in strošek | 2468135 | Število ponovnih poskusov odobritve se zmanjša s pet na tri. |
| Čas in strošek | 2468188 | Odpravili smo težavo z besedilom dnevnika, ki presega največjo dolžino v atributu **notetext** za entiteto **Opomba**. |
