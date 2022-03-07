---
title: Ocene projekta in integracija dejanskih vrednosti
description: Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za ocene in dejanske vrednosti projektov.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006311"
---
# <a name="project-estimates-and-actuals-integration"></a>Ocene projekta in integracija dejanskih vrednosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za ocene in dejanske vrednosti projektov.

## <a name="project-estimates"></a>Projektne ocene

Ocene dela, stroškov in materiala za projekt so ustvarjene in vzdrževane v storitvi Microsoft Dataverse in sinhronizirajo z aplikacijami Finance and Operations za računovodske namene. Ustvarjanje, posodabljanje in brisanje postopkov ni podprto prek aplikacij Finance and Operations.

Ustvarjanje ocen zahteva veljavno konfiguracijo računovodstva za projekt. Projekti, ki so povezani s podrobnostmi pogodbe, morajo imeti veljaven profil stroškov in prihodkov projekta, določen v pravilih profila stroškov in prihodkov projekta. Za več informacij glejte [Konfiguracija vodenja računov za plačljive projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Ocene dela

Ocene dela ustvari vodja projekta ali upravitelj virov, ki projektnemu opravilu dodeli tudi splošni ali poimenovani vir. Zapise o dodeljevanju virov lahko pregledate na zavihku **Dodelitev virov** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o dodeljevanju virov v storitvi Dataverse ustvarijo zapise napovedi ur dela v aplikacijah Finance and Operations z možnostjo **Entiteta za integracijo za oceno ur v storitvi Project Operations (msdyn\_resourceassignments)**.

   ![Integracija ocen dela.](./Media/DW4LaborEstimates.png)

Dvojno zapisovanje sinhronizira zapise o dodeljevanju virov v pripravljalno tabelo (**ProjCDSEstimateHoursImport**), nato pa s poslovno logiko ustvari in posodobi zapise napovedi ur (**ProjForecastEmpl**).

Računovodja projekta pregleda zapise o napovedanih urah, ustvarjenih v aplikacijah Finance and Operations, v razdelku **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Načrt** > **Napovedi ur**.

## <a name="expense-estimates"></a>Ocena stroškov

Ocene stroškov ustvari vodja projekta na zavihku **Ocene stroškov** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o oceni stroškov so shranjeni v entiteti **Vrstica ocene** v storitvi Dataverse. Ti zapisi o oceni imajo razred transakcije **Strošek** in so sinhronizirani z zapisi o napovedi stroškov v aplikacijah Finance and Operations z možnostjo **Entiteta za integracijo za oceno stroškov v storitvi Project Operations (msdyn\_estimatelines)**.

   ![Integracija ocen stroškov.](./Media/DW4ExpenseEstimates.png)

Dvojno zapisovanje sinhronizira zapise o ocenah stroškov v pripravljalno tabelo (**ProjCDSEstimateExpenseImport**), nato pa s poslovno logiko ustvari in posodobi zapise napovedi stroškov (**ProjForecastCost**). Vrstice ocen ločeno shranijo zapise o oceni prodaje in oceni stroškov. Poslovna logika v aplikacijah Finance and Operations zapolni en zapis napovedi stroškov z uporabo te podrobnosti v pripravljalni tabeli.

Računovodja projekta lahko pregleda zapise napovedi stroškov, ustvarjenih v aplikacijah Finance and Operations, v razdelku **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Načrt** > **Napovedi stroškov**.

## <a name="material-estimates"></a>Ocene materiala

Ocene materiala ustvari vodja projekta na zavihku **Ocene materiala** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o oceni materiala so shranjeni v entiteti **Vrstica ocene** v storitvi Dataverse. Ti zapisi o oceni imajo razred transakcije **Material** in so sinhronizirani z zapisi o napovedi elementa v aplikacijah Finance and Operations z možnostjo **Tabela integracije projekta za ocene materiala (msdyn\_estimatelines)**.

   ![Integracija ocen materiala.](./Media/DW4MaterialEstimates.png)

Dvojno zapisovanje sinhronizira zapise o ocenah materiala v pripravljalno tabelo **ProjForecastSalesImpor**, nato pa s poslovno logiko ustvari in posodobi zapise napovedi elementa (**ForecastSales**). Vrstice ocen ločeno shranijo zapise o oceni prodaje in oceni stroškov. Poslovna logika v aplikacijah Finance and Operations zapolni en zapis napovedi elementa z uporabo te podrobnosti v pripravljalni tabeli.

Računovodja projekta lahko pregleda zapise napovedi elementa, ustvarjenih v aplikacijah Finance and Operations, v razdelku **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Načrt** > **Napovedi elementa**.

## <a name="project-actuals"></a>Dejanske vrednosti projekta

Dejanske vrednosti projekta so ustvarjene v storitvi Dataverse, glede na čas, stroške, material in dejavnost obračunavanja. Entiteta Dataverse vključuje vse operativne atribute teh transakcij, vključno s količino, lastno ceno, prodajno ceno in projektom. Za več informacij glejte [Dejanske vrednosti](../actuals/actuals-overview.md). Zapisi o dejanskih vrednosti se sinhronizirajo z aplikacijami Finance and Operations s preslikavo tabele za dvojno zapisovanje **Dejanske vrednosti integracije za Project Operations (msdyn\_actuals)** za nadaljnje računovodstvo.

   ![Integracija dejanskih vrednosti.](./Media/DW4Actuals.png)

Preslikava tabele **Dejanske vrednosti integracije za Project Operations** sinhronizira vse zapise iz entitete **Dejanske vrednosti** v storitvi Dataverse z atributom **Preskoči sinhronizacijo (samo za interno uporabo)**, nastavljenim na **Neresnično**. Ta vrednost atributa je pri ustvarjanju zapisa samodejno nastavljena v storitvi Dataverse. Primeri, ko je ta atribut nastavljen na **Resnično** so naslednji:

  - Dejanske stroške projekta za transakcije med podjetji. Za več informacij glejte [Ustvarjanje transakcij med podjetji](../project-accounting/create-intercompany-transactions.md). Ti zapisi so preskočeni, ker sistem v aplikacijah Finance and Operations znova ustvari dejanske stroške projekta, ko je knjižen račun dobavitelja med podjetji.
  - Negativni zapis neobračunane prodaje, ustvarjen ob potrditvi predračuna. Ti zapisi so preskočeni, ker v aplikacijah Finance and Operations pomožna poslovna knjiga projekta ne razveljavi zapisa neobračunane prodaje pri izdaji računov, vendar zamenja stanje v »Zaračunano v celoti«.

Preslikava tabele za dvojno zapisovanje sinhronizira zapise o dejanskih stroških s pripravljalno tabelo **ProjCDSActualsImport**. Te zapise obdela občasni postopek **Uvoz iz pripravljalne tabele** pri ustvarjanju vrstic dnevnika integracij za Project Operations in vrstic predlogov za račune projekta. Za več informacij glejte [Dnevnik integracij za Project Operations](../project-accounting/project-operations-integration-journal.md).

Storitev Dataverse zajema tudi povezave med dejanskimi transakcijami projekta v entiteti **Povezava transakcije**. Za več informacij glejte [Povezava dejanskih vrednosti z izvirnimi zapisi](../actuals/linkingactuals.md). Povezave med dejanskimi transakcijami so tudi sinhronizirane z aplikacijami Finance and Operations s preslikavo tabele za dvojno zapisovanje **Entiteta za integracijo za odnose projektne transakcije (msdyn\_transactionconnections)**. Te zapise uporabi občasni postopek **Uvoz iz pripravljalne tabele** pri ustvarjanju vrstic dnevnika integracij za Project Operations in vrstic predlogov za račune projekta.

Knjiženje dnevnika integracij za Project Operations in predloga za račune projekta sproži posodobitev v ustreznih zapisih v pripravljalni tabeli **ProjCDSActualsImport**. Sistem zajema in beleži naslednje atribute računovodstva za dejanske transakcije:

- Znesek računovodske valute
- Menjalni tečaj
- Številka bona
- Znesek prometnega davka

Preslikava tabele **Dejanske vrednosti integracije za Project Operations** s temi podatki posodablja ustrezne zapise o dejanskih vrednostih v storitvi Dataverse.
