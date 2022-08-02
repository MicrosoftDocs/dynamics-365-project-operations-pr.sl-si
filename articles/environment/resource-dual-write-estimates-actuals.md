---
title: Ocene projekta in integracija dejanskih vrednosti
description: Ta članek vsebuje informacije o integraciji dvojnega zapisovanja projektnih operacij za ocene in dejanske vrednosti projekta.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029100"
---
# <a name="project-estimates-and-actuals-integration"></a>Ocene projekta in integracija dejanskih vrednosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek vsebuje informacije o integraciji dvojnega zapisovanja projektnih operacij za ocene in dejanske vrednosti projekta.

## <a name="project-estimates"></a>Projektne ocene

Ocene projektnega dela, stroškov in materiala se ustvarijo in vzdržujejo v Microsoft Dataverse in sinhroniziran z aplikacijami za finance in poslovanje za računovodske namene. Operacije ustvarjanja, posodabljanja in brisanja niso podprte prek aplikacij za finance in operacije.

Ustvarjanje ocen zahteva veljavno konfiguracijo računovodstva za projekt. Projekti, ki so povezani s podrobnostmi pogodbe, morajo imeti veljaven profil stroškov in prihodkov projekta, določen v pravilih profila stroškov in prihodkov projekta. Za več informacij glejte [Konfiguracija vodenja računov za plačljive projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Ocene dela

Ocene dela ustvari vodja projekta ali upravitelj virov, ki projektnemu opravilu dodeli tudi splošni ali poimenovani vir. Zapise o dodeljevanju virov lahko pregledate na zavihku **Dodelitev virov** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o dodelitvi virov v Dataverse ustvarite zapise urnih napovedi v aplikacijah za finance in poslovanje z uporabo **Integracijska entiteta Project Operations za ocene ur (msdyn\_ dodelitve virov)**.

   ![Integracija ocen dela.](./Media/DW4LaborEstimates.png)

Dvojno zapisovanje sinhronizira zapise o dodeljevanju virov v pripravljalno tabelo (**ProjCDSEstimateHoursImport**), nato pa s poslovno logiko ustvari in posodobi zapise napovedi ur (**ProjForecastEmpl**).

Računovodja projekta pregleda zapise predvidenih ur, ustvarjene v aplikacijah za finance in poslovanje, tako da obišče **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Načrtujte** > **Urne napovedi**.

## <a name="expense-estimates"></a>Ocena stroškov

Ocene stroškov ustvari vodja projekta na zavihku **Ocene stroškov** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o oceni stroškov so shranjeni v entiteti **Vrstica ocene** v storitvi Dataverse. Ti ocenjevalni zapisi imajo razred transakcije, **Stroški** in so sinhronizirani z zapisi napovedi stroškov v aplikacijah za finance in poslovanje z uporabo **Enota integracije projektnih operacij za ocene stroškov (msdyn\_ ocene)**.

   ![Integracija ocen stroškov.](./Media/DW4ExpenseEstimates.png)

Dvojno zapisovanje sinhronizira zapise o ocenah stroškov v pripravljalno tabelo (**ProjCDSEstimateExpenseImport**), nato pa s poslovno logiko ustvari in posodobi zapise napovedi stroškov (**ProjForecastCost**). Vrstice ocen ločeno shranijo zapise o oceni prodaje in oceni stroškov. Poslovna logika v aplikacijah za finance in operacije zapolni en sam zapis napovedi stroškov z uporabo te podrobnosti v uprizoritveni tabeli.

Računovodja projekta lahko pregleda zapise napovedi stroškov v aplikacijah za finance in poslovanje tako, da obišče **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Načrtujte** > **Napovedi stroškov**.

## <a name="material-estimates"></a>Ocene materiala

Ocene materiala ustvari vodja projekta na zavihku **Ocene materiala** na strani **Podrobnosti projekta** v storitvi Dataverse. Zapisi o oceni materiala so shranjeni v entiteti **Vrstica ocene** v storitvi Dataverse. Ti zapisi ocen imajo razred transakcije, **Material** in so sinhronizirani z zapisi napovedi postavk v aplikacijah za finance in poslovanje z uporabo **Projektna integracijska tabela za ocene materiala (msdyn\_ ocene)**.

   ![Integracija ocen materiala.](./Media/DW4MaterialEstimates.png)

Dvojno zapisovanje sinhronizira zapise o ocenah materiala v pripravljalno tabelo **ProjForecastSalesImpor**, nato pa s poslovno logiko ustvari in posodobi zapise napovedi elementa (**ForecastSales**). Vrstice ocen ločeno shranijo zapise o oceni prodaje in oceni stroškov. Poslovna logika v aplikacijah za finance in operacije zapolni en sam zapis napovedi postavke z uporabo te podrobnosti v uprizoritveni tabeli.

Računovodja projekta lahko pregleda zapise napovedi postavk v aplikacijah za finance in poslovanje tako, da obišče **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Načrtujte** > **Napovedi artiklov**.

## <a name="project-actuals"></a>Dejanske vrednosti projekta

Dejanske vrednosti projekta so ustvarjene v storitvi Dataverse, glede na čas, stroške, material in dejavnost obračunavanja. Entiteta Dataverse vključuje vse operativne atribute teh transakcij, vključno s količino, lastno ceno, prodajno ceno in projektom. Za več informacij glejte [Dejanske vrednosti](../actuals/actuals-overview.md). Dejanski zapisi se sinhronizirajo z aplikacijami za finance in poslovanje z uporabo preslikave tabele z dvojnim pisanjem **Dejanski podatki o integraciji projektnih operacij (msdyn\_ dejansko stanje)** za nadaljnje računovodstvo.

   ![Integracija dejanskih vrednosti.](./Media/DW4Actuals.png)

Preslikava tabele **Dejanske vrednosti integracije za Project Operations** sinhronizira vse zapise iz entitete **Dejanske vrednosti** v storitvi Dataverse z atributom **Preskoči sinhronizacijo (samo za interno uporabo)**, nastavljenim na **Neresnično**. Ta vrednost atributa je pri ustvarjanju zapisa samodejno nastavljena v storitvi Dataverse. Primeri, ko je ta atribut nastavljen na **Resnično** so naslednji:

  - Dejanske stroške projekta za transakcije med podjetji. Za več informacij glejte [Ustvarjanje transakcij med podjetji](../project-accounting/create-intercompany-transactions.md). Ti zapisi so preskočeni, ker sistem znova ustvari dejanski strošek projekta v aplikacijah za finance in operacije, ko je objavljen račun dobavitelja med podjetji.
  - Negativni zapis neobračunane prodaje, ustvarjen ob potrditvi predračuna. Ti zapisi so preskočeni, ker podknjiga projekta v aplikacijah za finance in operacije ne razveljavi nezaračunanega prodajnega zapisa pri fakturiranju, ampak spremeni status v fakturirano v celoti.

Preslikava tabele za dvojno zapisovanje sinhronizira zapise o dejanskih stroških s pripravljalno tabelo **ProjCDSActualsImport**. Te zapise obdela občasni postopek **Uvoz iz pripravljalne tabele** pri ustvarjanju vrstic dnevnika integracij za Project Operations in vrstic predlogov za račune projekta. Za več informacij glejte [Dnevnik integracij za Project Operations](../project-accounting/project-operations-integration-journal.md).

Storitev Dataverse zajema tudi povezave med dejanskimi transakcijami projekta v entiteti **Povezava transakcije**. Za več informacij glejte [Povezava dejanskih vrednosti z izvirnimi zapisi](../actuals/linkingactuals.md). Povezave med dejanskimi transakcijami so prav tako sinhronizirane z aplikacijami za finance in poslovanje z uporabo preslikave tabele z dvojnim pisanjem, **Integracijska entiteta za projektno transakcijo Odnosi (msdyn\_ transakcijske povezave)**. Te zapise uporabi občasni postopek **Uvoz iz pripravljalne tabele** pri ustvarjanju vrstic dnevnika integracij za Project Operations in vrstic predlogov za račune projekta.

Knjiženje dnevnika integracij za Project Operations in predloga za račune projekta sproži posodobitev v ustreznih zapisih v pripravljalni tabeli **ProjCDSActualsImport**. Sistem zajema in beleži naslednje atribute računovodstva za dejanske transakcije:

- Znesek računovodske valute
- Menjalni tečaj
- Številka bona
- Znesek prometnega davka

Preslikava tabele **Dejanske vrednosti integracije za Project Operations** s temi podatki posodablja ustrezne zapise o dejanskih vrednostih v storitvi Dataverse.
