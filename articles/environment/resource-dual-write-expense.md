---
title: Integracija upravljanja stroškov
description: Ta članek ponuja informacije o integraciji poročila o stroških v Project Operations z uporabo dvojnega pisanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64c318dc1915a9a87b6ae3c6b8a2aa6d3c9cd36
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924634"
---
# <a name="expense-management-integration"></a>Integracija upravljanja stroškov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek vsebuje informacije o integraciji poročil o stroških v Project Operations [polna razporeditev stroškov](../expense/expense-overview.md) z uporabo dvojnega pisanja.

## <a name="expense-categories"></a>Kategorije stroškov

Pri popolni uvedbi stroškov se kategorije stroškov ustvarijo in vzdržujejo v aplikacijah Finance in Operations. Če želite ustvariti novo kategorijo stroškov, izvedite naslednje korake:

1. V storitvi Microsoft Dataverse ustvarite kategorijo **transakcije**. Integracija dvojnega pisanja bo sinhronizirala to kategorijo transakcij z aplikacijami Finance in Operations. Za več informacij glejte [Konfiguracija kategorij projekta](/dynamics365/project-operations/project-accounting/configure-project-categories) in [Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov](resource-dual-write-setup-integration.md). Kot rezultat te integracije sistem ustvari štiri skupne zapise kategorij v aplikacijah Finance in Operations.
2. V aplikaciji Finance se pomaknite v razdelek **Upravljanje stroškov** > **Nastavitev** > **Skupne kategorije** in izberite skupno kategorijo z razredom transakcije **Strošek**. Parameter **Lahko se uporablja v stroških** na **Resnično** in določite vrsto stroškov, ki jih želite uporabiti.
3. Z zapisom skupne kategorije ustvarite novo kategorijo stroškov tako, da v razdelku **Upravljanje stroškov** > **Nastavitev** > **Kategorije stroškov** izberete **Novo**. Ko je zapis shranjen, dvojno zapisovanje uporabi preslikavo tabele, **Entiteta za izvor kategorij stroškov projekta za integracijo aplikacije Project Operations (msdyn\_expensecategories)**, za sinhronizacijo zapisa v storitev Dataverse.

  ![Integracija kategorije stroškov.](./media/DW6ExpenseCategories.png)

Kategorije stroškov v aplikacijah Finance in Operations so specifične za podjetje ali pravno osebo. V storitvi Dataverse so na voljo ločeni, ustrezni zapisi, določeni za pravne osebe. Ko vodja projekta oceni stroške, ne more izbrati kategorij stroškov, ustvarjenih za projekt, ki je v lasti drugega podjetja kot podjetje, ki je lastnik projekta, pri katerem delajo. 

## <a name="expense-reports"></a>Poročila o stroških

Poročila o stroških so ustvarjena in odobrena v aplikacijah Finance in Operations. Za več informacij glejte [Ustvarjanje in obdelava poročil o stroških v aplikaciji Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Ko vodja projekta odobri poročilo o stroških, je knjižen v glavni knjigi. V aplikaciji Project Operations so vrstice poročila o stroških, povezane s projektom, objavljene s posebnimi pravili knjiženja:

  - Stroški, povezani s projektom (vključno z nevračljivim davkom), se ne knjižijo takoj na račun stroškov projekta v glavni knjigi, ampak se knjižijo na račun za integracijo stroškov. Ta račun je konfiguriran na zavihku **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Vodenje projektov in računovodski parametri**, **Project Operations v aplikaciji Dynamics 365 Customer Engagement**.
  - Dvojno zapisovanje sinhronizira v storitev Dataverse z preslikavo tabele **Entiteta za izvoz stroškov projekta integracije za Project Operations (msdyn\_expenses)**.
  - Pomožna poslovna knjiga za davke, dobavitelje in druga finančna knjiženja so zabeležena, kot je ustrezno v času knjiženja poročila o stroških.

  ![Integracija poročila o stroških.](./media/DW6ExpenseReports.png)

Ko je zapis zapisan v entiteto **Strošek** v storitvi Dataverse, sistem sproži avtomatiziran postopek odobritve zapisa. Po potrebi lahko v storitvi Dataverse stanje avtomatiziranega postopka odobritve preverite tako, da odprete razdelek **Napredne nastavitve** > **Sistem** > **Sistemska opravila**. Po končani odobritvi se v entiteti **Dejanske vrednosti** ustvarijo zapisi razreda transakcije stroška.

Dejanske vrednosti, povezane s stroški, so nato obdelane s preslikavo tabele za dvojno zapisovanje **Dejanske vrednosti integracije za Project Operations (msdyn\_actuals)**. Za več informacij si preberite razdelek [Ocene in dejanske vrednosti projekta](resource-dual-write-estimates-actuals.md).

Občasni postopek **Uvoz iz pripravljalne tabele** ustvari vrstice dnevnika, povezane s poročilom o stroških, v dnevniku integracij za Project Operations. Protikonto privzeto velja za račun za integracijo stroškov. Dnevnik integracije knjiženja počisti saldo konta za transakcijo stroškov in znesek stroškov premakne na račun stroškov projekta. Prav tako sistem ustvarja transakcije pomožne poslovne knjige za namene izdajanja računov in prepoznavanja prihodkov.
