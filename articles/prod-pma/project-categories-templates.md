---
title: Sinhronizirajte kategorije stroškov projekta med financami in operacijami ter Project Service Automation
description: Ta članek opisuje predloge in osnovna opravila, ki se uporabljajo za sinhronizacijo kategorij stroškov projekta med njimi Microsoft Dynamics 365 Finance in Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8eba7defb93bd880db4b0e8fe425d07312cf5cb9
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028953"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sinhronizirajte kategorije stroškov projekta med financami in operacijami ter Project Service Automation

[!include[banner](../includes/banner.md)]

Ta članek opisuje predloge in osnovna opravila, ki se uporabljajo za sinhronizacijo kategorij stroškov projekta med Dynamics 365 Finance in Dynamics 365 Project Service Automation.

> [!NOTE]
> - V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.
> - Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.
> - Če uporabljate različico Enterprise 7.3.0, boste po namestitvi KB 4132657 in KB 4132660 lahko predloge uporabili za integracijo projektnih opravil, kategorij stroškov transakcij, ocen delovnih ur, ocen stroškov in dejanskih vrednosti ter konfiguriranje zaklepanja funkcionalnosti. Če morate ponastaviti računovodsko porazdeljevanje, priporočamo, da namestite tudi KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Pretok podatkov za rešitvi Project Service Automation in Finance

Rešitev za integracijo rešitve Project Service Automation in Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance. Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok podatkov o kategorijah transakcij stroškov projekta med rešitvama Finance in Project Service Automation.

Če so kategorije stroškov projekta upravljane v rešitvi Finance, gre potek integracije od rešitve Finance do Project Service Automation. ID-ji integracije kategorij stroškov projekta se nato posodobijo s sinhronizacijo od rešitve Project Service Automation do rešitve Finance.

Če so kategorije stroškov projekta upravljane v rešitvi Project Service Automation, gre potek integracije od rešitve Project Service Automation do rešitve Finance. Kategorije projektov morajo biti konfigurirane v rešitvi Finance, preden se izvede sinhronizacija s programom Project Service Automation. Nato sinhronizirajte še enkrat iz rešitve Finance v Project Service Automation in nato še iz Project Service Automation v Finance. Na ta način boste zagotovili, da bodo kategorije povezane in ne bodo obstajali dvojniki.

> [!NOTE]
> Kategorije stroškov projekta se običajno upravljajo v rešitvi Finance. Če pa niso ali če so kategorije stroškov že bile ustvarjene v rešitvi Project Service Automation, morate najprej izvesti sinhronizacijo s predlogo Kategorije transakcij stroškov projekta (PSA v Fin in Ops). Nato sinhronizirajte s predlogo Kategorije transakcij stroškov projekta (Fin in Ops v PSA). Nato morate še enkrat zagnati sinhronizacijo iz rešitve Project Service Automation v Finance.
>
> Če sinhronizirate najprej iz rešitve Project Service Automation, morajo biti pred začetkom sinhronizacije v programu Finance izpolnjene naslednje zahteve:
>
> - Kategorija v skupni rabi, ki se ujema s kategorijo projekta, ki je nastavljena v rešitvi Project Service Automation, mora obstajati in biti omogočena tako za **Projekt** kot za **Stroški**.
> - Za vsako pravno osebo v rešitvi Finance, za katero je treba izvesti integracijo, morajo obstajati naslednje kategorije projektov:
>
>     - **Kategorija projekta** obstaja. 
>     - **Uporaba v stroških** je omogočena.
>     - **Dejavnost v dnevniku** je omogočena.
>     - **Vrsta transakcije** je nastavljena na **Stroški**.

Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.

[![Podatkovni tok za integracijo rešitve Project Service Automation z rešitvijo Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sinhronizacija kategorije stroškov projekta iz rešitve Finance v Project Service Automation

### <a name="template-and-task"></a>Predloga in opravilo

Za dostop do predloge v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.

Spodnja predloga in temeljno opravilo se uporabljata za sinhronizacijo kategorij stroškov projekta iz rešitve Finance v Project Service Automation:

- **Ime predloge v Integraciji podatkov:** Kategorije transakcij stroškov projekta (Fin in Ops v PSA)
- **Ime opravila v projektu:** Sinhronizacija kategorij s PSA

### <a name="entity-set"></a>Nabor entitet

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integracijska entiteta za kategorije | Kategorije transakcij     |

### <a name="entity-flow"></a>Potek entitete

Kategorije stroškov projekta se upravljajo v rešitvi Finance in sinhronizirajo v rešitev Project Service Automation kot kategorije transakcij.

### <a name="power-query"></a>Power Query

Ko sinhronizirate s storitvijo Project Service Automation, morate uporabiti Microsoft Power Query za Excel, da nastavite vrsto obračunavanja v kategoriji transakcije. Predloga kategorij transakcij stroškov projekta (Fin in Ops v PSA) vsebuje privzeti stolpec in preslikavo. Če ustvarite lastno predlogo, morate dodati pogojni stolpec v Power Query. Upoštevajte ta navodila.

1. Kliknite puščico, da odprete preslikavo opravila kategorij stroškov projekta v predlogi Kategorije transakcij stroškov projekta (Fin in Ops v PSA).
2. Kliknite na **Napredna poizvedba in filtriranje** povezava za odpiranje Power Query.
2. Izberite **Dodaj pogojni stolpec**.
3. Vnesite ime za nov stolpec, na primer **BillingType**.
4. Vnesite naslednji pogoj: **če CATEGORYID ni enak nič, potem je 19235001, sicer pa nič**.
5. Kliknite **V redu** za stolpec.
6. Novi stolpec preslikajte na stran za preslikavo.

Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Finance v Project Service Automation.

[![Preslikava predloge za kategorijo stroškov projekta v rešitev Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sinhronizacija kategorije stroškov projekta iz rešitve Project Service Automation v Finance

### <a name="template-and-task"></a>Predloga in opravilo

Spodnja predloga in temeljno opravilo se uporabljata za sinhronizacijo kategorij stroškov projekta iz rešitve Project Service Automation v Finance:

- **Ime predloge v Integraciji podatkov:** Kategorije transakcij stroškov projekta (PSA v Fin in Ops)
- **Ime opravila v projektu:** Sinhronizacija kategorij s Fin Ops

### <a name="entity-set"></a>Nabor entitet

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Kategorije transakcij     | Integracijska entiteta za kategorije |

### <a name="entity-flow"></a>Potek entitete

Kategorije stroškov projekta se upravljajo v rešitvi Finance in sinhronizirajo v rešitev Project Service Automation kot kategorije transakcij. S povratno sinhronizacijo v rešitev Finance se posodobi kategorija projekta v rešitvi Finance z ID-jem integracije iz rešitve Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov.

> [!NOTE]
> Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.

[![Preslikava predloge Project Service Automation v rešitev Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]