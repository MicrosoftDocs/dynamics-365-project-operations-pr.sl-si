---
title: Različice preslikave dvojnega zapisovanja za Project Operations
description: Ta tema zagotavlja seznam preslikav za dvojno zapisovanje, ki jih potrebuje aplikacija Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b24a20d47eefa43b2e4e184a377decdb280d436d
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025794"
---
# <a name="project-operations-dual-write-map-versions"></a>Različice preslikave dvojnega zapisovanja za Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Za uporabo Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, je treba, da se v okolju izvaja nabor preslikav za dvojno zapisovanje. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Zahtevane preslikave: osnovna rešitev za organiziranje z dvojnim zapisovanjem

Naslednje preslikave so predpogoj za rešitev Project Operations. Zaženite preslikave, navedene v spodnji tabeli, in vse povezane preslikave tabel v vašem okolju.

| Preslikava tabele | Začetna sinhronizacija |
| --- | --- |
| Knjiga (msdyn_ledgers) | Zahteva začetno sinhronizacijo za preslikavo tabele in vse predpogoje. Za začetno sinhronizacijo so glavne aplikacije Finance and Operations. |
| Pravne osebe (cdm_companies) | Ni potrebno. Sistem samodejno zapolni to entiteto, ko so okolja povezana z dvojnim zapisovanjem. |
| Stranke V3 (računi) | Ni potrebno za omogočanje uporabe. |
| Dobavitelji V2 (msdyn_vendors) | Ni potrebno za omogočanje uporabe. |

1. Na seznamu preslikav izberite preslikavo »Glavna knjiga **(msdyn\_ledgers)**« z vsemi zahtevami in izberite potrditveno polje **Začetna sinhronizacija**. V polju **Glavni za začetno sinhronizacijo** izberite **aplikacije Finance and Operations** za preslikavo glavne knjige in zahtevane preslikave. Izberite **Zaženi**.

![Sinhronizacija preslikave knjige](media/DW6.png)

2. Izvedite iste korake za vse preostale preslikave tabel, navedene v zgornji tabeli. Pri izvajanju teh preslikav ne izberite potrditvenega polja **Začetna sinhronizacija**.

## <a name="project-operations-dual-write-maps"></a>Preslikave za dvojno zapisovanje za Project Operations

Naslednje preslikave so obvezne za rešitev Project Operations. Naštete so različice preslikave dvojnega zapisovanja, prva je posodobitev aplikacije Project Operations v maju 2021, različica 4.10.0.186.

| **Preslikava entitete** | **Najnovejša različica** | **Začetna sinhronizacija** |
| --- | --- | --- |
| Entiteta za integracijo za odnose projektne transakcije (msdyn\_transactionconnections) | 1.0.0.0 | Ni potrebno za omogočanje uporabe. |
| Glave projektnih pogodb (prodajni nalogi) | 1.0.0.1 | Ni potrebno za omogočanje uporabe. |
| Podrobnosti pogodbe (salesorderdetails) | 1.0.0.0 | Ni potrebno za omogočanje uporabe. |
| Vir financiranja projekta (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Ni potrebno za omogočanje uporabe. |
| Integracije tabele aplikacije Project Operations za ocene materiala (msdyn\_estimatelines) | 1.0.0.0 | Ni potrebno za omogočanje uporabe. |
| Predlogi za račune projekta V2 (računi) | 1.0.0.3 | Ni potrebno za omogočanje uporabe. |
| Dejanske vrednosti integracije za Project Operations (msdyn_actuals) | 1.0.0.14 | Ni potrebno za omogočanje uporabe. |
| Mejniki podrobnosti pogodbe o integraciji storitve Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Ni potrebno za omogočanje uporabe. |
| Entiteta za integracijo za oceno stroškov v storitvi Project Operations (msdyn_estimateslines) | 1.0.0.2 | Ni potrebno za omogočanje uporabe. |
| Entiteta za integracijo za oceno ur v storitvi Project Operations (msdyn_resourceassignments) | 1.0.0.5 | Ni potrebno za omogočanje uporabe. |
| Entiteta za izvoz kategorije stroškov projekta pri integraciji storitve Project Operations (msdyn_expensecategories) | 1.0.0.1 | Ni potrebno za omogočanje uporabe. |
| Entiteta za izvoz stroškov projekta pri integraciji storitve Project Operations (msdyn_expenses) | 1.0.0.2 | Ni potrebno za omogočanje uporabe. |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Ni potrebno za omogočanje uporabe. |
| Entiteta za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Ni potrebno za omogočanje uporabe. |
| Vloge virov podjetja za vsa podjetja (bookableresourcecategories) | 1.0.0.1 | Zahteva začetno sinhronizacijo preslikave tabele za sinhronizacijo vlog virov vodje projekta in članov ekipe, ki so zapolnjene v okolju Dynamics 365 Dataverse med omogočanjem uporabe. Storitev Dataverse je glavni vir za začetno sinhronizacijo. |
| Opravila projekta (msdyn_projecttasks) | 1.0.0.4 | Ni potrebno za omogočanje uporabe. |
| Kategorije projektnih transakcij (msdyn_transactioncategories) | 1.0.0.0 | Ni potrebno za omogočanje uporabe. |
| Projekti V2 (msdyn_projects) | 1.0.0.2 | Ni potrebno za omogočanje uporabe. |

Za izvajanje navedenih preslikav izvedite naslednje korake.

1. Omogočite vloge virov projekta za preslikavo tabele **vsa podjetja (bookableresourcecategories)**, saj ta preslikava zahteva začetno sinhronizacijo. V polju **Glavni za začetno sinhronizacijo** izberite možnost **Common Data Service**. 

 ![Sinhronizacija preslikave tabele vloge virov](media/6ResourceInitialSync.jpg)

 Počakajte, da je stanje preslikave **Izvajanje**, preden se pomaknete na naslednji korak.

2. Izberite vse preostale zahtevane preslikave. Filtrirate jih lahko na seznamu preslikav dvojnega zapisovanja tako, da v zgornjem desnem kotu v iskanje vnesete ključno besedo **Projekt**. Izberete lahko več preslikav in jih zaženete. Za več informacij glejte [Upravljanje več preslikav tabele](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Poskrbite, da omogočite in zaženete povezane preslikave entitet.

### <a name="project-operations-dual-write-map-versions"></a>Različice preslikave dvojnega zapisovanja za Project Operations

Vedno zaženite najnovejšo različico preslikave v svojem okolju. Nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno, če obstaja kateri od naslednjih pogojev:

- Preslikava ni aktivirana.
- Najnovejša različica preslikave ni aktivirana. 
- Povezane preslikave tabel niso aktivirane.

Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Novo različico preslikave lahko aktivirate tako, da izberete možnost **Različice preslikave tabele**, izberete najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, boste morali spremembe znova uporabiti. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
