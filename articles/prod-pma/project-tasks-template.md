---
title: Sinhronizacija opravil projekta neposredno iz rešitve Project Service Automation v Finance and Operations
description: Ta tema opisuje predlogo in temeljno opravilo, ki se uporabljata za sinhronizacijo opravil projekta neposredno iz rešitve Microsoft Dynamics 365 Project Service Automation v Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084738"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinhronizacija opravil projekta neposredno iz rešitve Project Service Automation v Finance and Operations

[!include[banner](../includes/banner.md)]

Ta tema opisuje predlogo in temeljno opravilo, ki se uporabljata za sinhronizacijo opravil projekta neposredno iz rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.

> [!NOTE]
> - V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.
> - Če uporabljate različico Enterprise 7.3.0, boste po namestitvi KB 4132657 in KB 4132660 lahko predloge uporabili za integracijo projektnih opravil, kategorij stroškov transakcij, ocen delovnih ur, ocen stroškov in dejanskih vrednosti ter konfiguriranje zaklepanja funkcionalnosti. Če morate ponastaviti računovodsko porazdeljevanje, priporočamo, da namestite tudi KB 4131710.
> - Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Pretok podatkov za Project Service Automation v Finance

Rešitev za integracijo rešitve Project Service Automation v rešitev Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance. Predloga za integracijo, ki je na voljo s funkcijo za integracijo podatkov, omogoča pretok podatkov o opravilih projekta iz rešitve Project Service Automation v Finance.

Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.

[![Pretok podatkov za integracijo rešitve Project Service Automation v Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Predloga in opravilo

Za dostop do predloge v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt** , da izberete javne predloge.

Naslednja predloga in temeljno opravilo se uporabljata za sinhronizacijo opravil projekta iz rešitve Project Service Automation v Finance:

- **Ime predloge v integraciji podatkov:** opravila projekta (PSA v Fin in Ops)
- **Ime opravila v projektu:** opravila projekta

Preden lahko pride do sinhronizacije opravil projekta, morate sinhronizirati projektne pogodbe in projekte.

## <a name="entity-set"></a>Nabor entitet

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Opravila projekta              | Integracijska entiteta za opravilo projekta |

## <a name="entity-flow"></a>Potek entitete

Ocene opravil projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot napovedi dejavnosti projekta.

## <a name="prerequisites-and-mapping-setup"></a>Predpogoji in nastavitev preslikave

Preden lahko pride do sinhronizacije opravil projekta, morate sinhronizirati projektne pogodbe in projekte.

## <a name="power-query"></a>Power Query

Če je ta pogoj izpolnjen, morate za filtriranje podatkov uporabiti rešitev Microsoft Power Query for Excel:

- V opravilu projekta imate zapise, povezane z viri.

Če morate uporabiti rešitev Power Query, upoštevajte navodila:

- Predloga opravil projekta (PSA v Fin in Ops) ima privzeti filter, ki iz opravila projekta izključi zapise, povezane z viri, tako, da filter v možnosti **IsLineTask** nastavi na **Napačno**. Če ustvarite svojo predlogo, morate dodati ta filter.

## <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.

[![Preslikava predloge](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)