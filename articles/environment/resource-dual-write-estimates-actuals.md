---
title: Ocene projekta in integracija dejanskih vrednosti
description: Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za ocene in dejanske vrednosti projektov.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577210"
---
# <a name="project-estimates-and-actuals-integration"></a>Ocene projekta in integracija dejanskih vrednosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za ocene in dejanske vrednosti projektov.

## <a name="project-estimates"></a>Projektne ocene

Ocene projektnega dela, stroškov in materiala se izdelajo in vzdržujejo v Microsoft Dataverse in sinhronizirano z aplikacijami Finance in Operations za računovodske namene. Operacije ustvarjanja, posodabljanja in brisanja niso podprte v aplikacijah Finance in Operations.

Ustvarjanje ocen zahteva veljavno konfiguracijo računovodstva za projekt. Projekti, ki so povezani s podrobnostmi pogodbe, morajo imeti veljaven profil stroškov in prihodkov projekta, določen v pravilih profila stroškov in prihodkov projekta. Za več informacij glejte [Konfiguracija vodenja računov za plačljive projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Ocene dela

Ocene dela ustvari vodja projekta ali upravitelj virov, ki projektnemu opravilu dodeli tudi splošni ali poimenovani vir. Zapise o dodeljevanju virov lahko pregledate na zavihku **Dodelitev virov** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o dodelitvi sredstev v Dataverse ustvarite zapise urnih napovedi v aplikacijah Finance in Operations z uporabo **Integracijski subjekt Project Operations za ocene ur (msdyn\_ dodelitve sredstev)**.

   ![Integracija ocen dela.](./Media/DW4LaborEstimates.png)

Dvojno zapisovanje sinhronizira zapise o dodeljevanju virov v pripravljalno tabelo (**ProjCDSEstimateHoursImport**), nato pa s poslovno logiko ustvari in posodobi zapise napovedi ur (**ProjForecastEmpl**).

Računovodja projekta pregleda zapise ur napovedi, ustvarjene v aplikacijah Finance in Operations, tako da obiščete **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Načrtujte** > **Urne napovedi**.

## <a name="expense-estimates"></a>Ocena stroškov

Ocene stroškov ustvari vodja projekta na zavihku **Ocene stroškov** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o oceni stroškov so shranjeni v entiteti **Vrstica ocene** v storitvi Dataverse. Ti zapisi ocene imajo razred transakcije, **Stroški** in so sinhronizirani z zapisi napovedi stroškov v aplikacijah Finance in Operations **Integracijski subjekt Project Operations za ocene stroškov (msdyn\_ ocene)**.

   ![Integracija ocen stroškov.](./Media/DW4ExpenseEstimates.png)

Dvojno zapisovanje sinhronizira zapise o ocenah stroškov v pripravljalno tabelo (**ProjCDSEstimateExpenseImport**), nato pa s poslovno logiko ustvari in posodobi zapise napovedi stroškov (**ProjForecastCost**). Vrstice ocen ločeno shranijo zapise o oceni prodaje in oceni stroškov. Poslovna logika v aplikacijah Finance in Operations zapolni en sam zapis napovedi izdatkov z uporabo te podrobnosti v uprizoritveni tabeli.

Računovodja projekta lahko pregleda zapise napovedi stroškov v aplikacijah Finance in Operations, tako da obiščete **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Načrtujte** > **Napovedi stroškov**.

## <a name="material-estimates"></a>Ocene materiala

Ocene materiala ustvari vodja projekta na zavihku **Ocene materiala** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o oceni materiala so shranjeni v entiteti **Vrstica ocene** v storitvi Dataverse. Ti zapisi ocene imajo razred transakcije, **Material** in so sinhronizirani z zapisi napovedi postavk v aplikacijah Finance in Operations **Projektna integracijska tabela za ocene materiala (msdyn\_ ocene)**.

   ![Integracija ocen materiala.](./Media/DW4MaterialEstimates.png)

Dvojno zapisovanje sinhronizira zapise o ocenah materiala v pripravljalno tabelo **ProjForecastSalesImpor**, nato pa s poslovno logiko ustvari in posodobi zapise napovedi elementa (**ForecastSales**). Vrstice ocen ločeno shranijo zapise o oceni prodaje in oceni stroškov. Poslovna logika v aplikacijah Finance in Operations zapolni en zapis napovedi postavke s tem podrobnostm v uprizoritveni tabeli.

Računovodja projekta lahko pregleda zapise napovedi postavk v aplikacijah Finance in Operations, tako da obiščete **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Načrtujte** > **Napovedi artiklov**.

## <a name="project-actuals"></a>Dejanske vrednosti projekta

Dejanske vrednosti projekta so ustvarjene v storitvi Dataverse, glede na čas, stroške, material in dejavnost obračunavanja. Entiteta Dataverse vključuje vse operativne atribute teh transakcij, vključno s količino, lastno ceno, prodajno ceno in projektom. Za več informacij glejte [Dejanske vrednosti](../actuals/actuals-overview.md). Dejanski zapisi se sinhronizirajo z aplikacijami Finance in Operations z uporabo preslikave tabele z dvojnim zapisovanjem **Dejanski podatki o integraciji projektnih operacij (msdyn\_ dejansko stanje)** za nadaljnje računovodstvo.

   ![Integracija dejanskih vrednosti.](./Media/DW4Actuals.png)

Preslikava tabele **Dejanske vrednosti integracije za Project Operations** sinhronizira vse zapise iz entitete **Dejanske vrednosti** v storitvi Dataverse z atributom **Preskoči sinhronizacijo (samo za interno uporabo)**, nastavljenim na **Neresnično**. Ta vrednost atributa je pri ustvarjanju zapisa samodejno nastavljena v storitvi Dataverse. Primeri, ko je ta atribut nastavljen na **Resnično** so naslednji:

  - Dejanske stroške projekta za transakcije med podjetji. Za več informacij glejte [Ustvarjanje transakcij med podjetji](../project-accounting/create-intercompany-transactions.md). Ti zapisi so preskočeni, ker sistem ponovno ustvari dejanske stroške projekta v aplikacijah Finance in Operations, ko je knjižen račun med podjetji.
  - Negativni zapis neobračunane prodaje, ustvarjen ob potrditvi predračuna. Ti zapisi so preskočeni, ker podknjiga projekta v aplikacijah Finance in Operations ne razveljavi zapisa neobračunane prodaje pri izdajanju računov, ampak spremeni status v v celoti zaračunan.

Preslikava tabele za dvojno zapisovanje sinhronizira zapise o dejanskih stroških s pripravljalno tabelo **ProjCDSActualsImport**. Te zapise obdela občasni postopek **Uvoz iz pripravljalne tabele** pri ustvarjanju vrstic dnevnika integracij za Project Operations in vrstic predlogov za račune projekta. Za več informacij glejte [Dnevnik integracij za Project Operations](../project-accounting/project-operations-integration-journal.md).

Storitev Dataverse zajema tudi povezave med dejanskimi transakcijami projekta v entiteti **Povezava transakcije**. Za več informacij glejte [Povezava dejanskih vrednosti z izvirnimi zapisi](../actuals/linkingactuals.md). Povezave med dejanskimi transakcijami se sinhronizirajo tudi z aplikacijami Finance in Operations z uporabo preslikave tabele z dvojnim zapisovanjem, **Integracijska entiteta za projektno transakcijo Odnosi (msdyn\_ transakcijske povezave)**. Te zapise uporabi občasni postopek **Uvoz iz pripravljalne tabele** pri ustvarjanju vrstic dnevnika integracij za Project Operations in vrstic predlogov za račune projekta.

Knjiženje dnevnika integracij za Project Operations in predloga za račune projekta sproži posodobitev v ustreznih zapisih v pripravljalni tabeli **ProjCDSActualsImport**. Sistem zajema in beleži naslednje atribute računovodstva za dejanske transakcije:

- Znesek računovodske valute
- Menjalni tečaj
- Številka bona
- Znesek prometnega davka

Preslikava tabele **Dejanske vrednosti integracije za Project Operations** s temi podatki posodablja ustrezne zapise o dejanskih vrednostih v storitvi Dataverse.
