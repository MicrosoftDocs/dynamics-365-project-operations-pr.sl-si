---
title: Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov
description: Ta tema vsebuje informacije o nastavitvi in konfiguracij preslikav za dvojno zapisovanje za Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986556"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za entitete nastavitev in konfiguracije.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektne pogodbe, podrobnosti pogodbe in projekti

Projektne pogodbe, pogodbene vrstice in projekti so ustvarjeni v storitvi Dataverse in sinhronizirani z aplikacijami Finance and Operations za dodatno računovodstvo. Zapise v teh entitetah je mogoče ustvariti in izbrisati samo v storitvi Dataverse. Vendar pa je mogoče atribute računovodstva, kot so privzete vrednosti skupine davkov od prodaje in finančne razsežnosti, dodati tem zapisom v aplikacijah Finance and Operations.

  ![Koncepti integracije projektne pogodbe.](./media/1ProjectContract.jpg)

Storitev Dataverse sledi prodajnim dejavnostim za možne stranke, priložnostim in ponudbam in jih ne sinhronizira z aplikacijama Finance and Operations, ker s to dejavnostjo ni povezano nadaljnje računovodstvo.

Funkcionalnost projektne pogodbe v storitvi Dataverse ustvari zapis projektne pogodbe v aplikacijah Finance and Operations s preslikavo tabele **Glave projektnih pogodb (salesorders)**. Če shranite projektno pogodbo v storitvi Dataverse, prav tako začnete ustvarjati zapis entitete stranke projektne pogodbe. Ta zapis je sinhroniziran v aplikacijah Finance and Operations s preslikavo tabele **Vir financiranja projekta (msdyn\_projectcontractssplitbillingrules)**. Ta preslikava prav tako sinhronizira tudi dodajanja, posodobitve in brisanja strank projektne pogodbe. Odstotni deleži izstavitve računa za delitev med strankami projektnih pogodb se upravljajo samo v storitvi Dataverse in niso sinhronizirani z aplikacijami Finance and Operations.

Ko je projektna pogodba ustvarjena v storitvi Dataverse, lahko računovodja projekta posodobi atribute računovodstva za to projektno pogodbo v aplikacijah Finance and Operations v razdelku **Upravljanje projektov in računovodstvo** > **Projektne pogodbe** > **Nastavitev** > **Prikaži privzeto računovodstvo**. Računovodja lahko pregleda operativne atribute projektne pogodbe, kot sta zahtevani datum dobave in znesek pogodbe tako, da v aplikacijah Finance and Operations izbere ID projektne pogodbe, ki odpre ustrezen zapis o projektni pogodbi v storitvi Dataverse.

Entiteta projekta je sinhronizirana z aplikacijami Finance and Operations s preslikavo tabele **Projekti V2 (msdyn\_projects)**. Računovodja projekta lahko izvede ta dejanja:

  - Projekte lahko pregledate v aplikacijah Finance and Operations v razdelku **Upravljanje projektov in računovodstvo** > **Vsi projekti**. 
  - Atribute računovodstva za projekt lahko posodobite v aplikacijah Finance and Operations v razdelku **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Nastavitev** > **Prikaži privzeto računovodstvo**.  
  - Operativne atribute projekta, kot sta predvideni začetni in končni datum, lahko pregledate tako, da v aplikacijah Finance and Operations izberete ID projekta, ki odpre ustrezen zapis projekta v storitvi Dataverse.

Projekt je povezan s projektno pogodbo prek entitete **Podrobnosti projektne pogodbe**.

Podrobnosti projektne pogodbe v storitvi Dataverse ustvari pravilo obračunavanja projektne pogodbe v aplikacijah Finance and Operations s preslikavo tabele **Podrobnosti projektne pogodbe (salesorderdetails)**. Način obračunavanja določa vrsto pravila za izstavitev računa za projektno pogodbo v aplikacijah Finance and Operations:

  - Podrobnosti projektne pogodbe z načinom obračunavanja časa in materiala ustvarjajo vrsto pravila za obračunavanje časa in materiala.
  - Podrobnosti pogodbe z načinom obračunavanja »Fiksna cena« ustvarijo pravilo mejnika obračunavanja.

Računovodja projekta lahko podrobnosti projektne pogodbe pregleda v aplikacijah Finance and Operations v razdelku **Upravljanje projektov in računovodstvo** > **Projektne pogodbe** > **Nastavitev** > **Prikaži privzeto računovodstvo** na zavihku **Podrobnosti pogodbe**. Na tem zavihku lahko računovodja nastavi tudi privzete finančne razsežnosti za podrobnosti pogodbe z načinom obračunavanja »Fiksna cena«.

## <a name="billing-milestones"></a>Mejniki obračunavanja

Podrobnosti projektne pogodbe, ki uporabljajo način obračunavanja »Fiksna cena«, se fakturirajo prek mejnikov obračunavanja. Mejniki obračunavanja se sinhronizirajo s transakcijami za kupca projekta v aplikacijah Finance and Operations s preslikavo tabele **Mejniki podrobnosti pogodbe za integracijo za Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integracija mejnikov obračunavanja.](./media/2Milestones.jpg)

Računovodja lahko pregleda transakcije na računu in prilagodi atribute računovodstva za te transakcije tako, da se pomakne v razdelek **Pregled upravljanja projektov in računovodstva** > **Projektne pogodbe** > **Vzdrževanje** > **Transakcije za kupca** ali **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Vzdrževanje** > **Transakcije za kupca**.

Ko prvič ustvarite mejnik obračunavanja za določeno podrobnost projektne pogodbe, sistem samodejno ustvari projekt s predvidenimi prihodki s fiksno ceno za projekt, povezan s to podrobnostjo pogodbe. Projekte s predvidenimi prihodki s fiksno ceno je mogoče pregledati v razdelku **Upravljanje projektov in računovodstvo** > **Projekti s predvidenimi prihodki s fiksno ceno**.

### <a name="project-tasks"></a>Projektna opravila

Opravila projekta so sinhronizirana z aplikacijami Finance and Operations prek preslikave tabele **Opravila projekta (msdyn\_projecttasks)** samo za referenčne namene. Ustvarjanje, posodabljanje in brisanje postopkov ni podprto prek aplikacij Finance and Operations.

  ![Integracija opravil projekta.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Viri projekta

Entiteta **Vloge virov projekta** je sinhronizirana z aplikacijami Finance and Operations s preslikavo tabele **Vloge virov projekta za vsa podjetja (bookableresourcecategories)** samo za referenčne namene. Ker vloge virov v storitvi Dataverse niso določene za podjetje, sistem samodejno ustvari ustrezne zapise o vlogah virov za določeno podjetje v aplikacijah Finance and Operations za vse pravne osebe, vključene v obseg integracije za dvojno zapisovanje.

![Integracija vlog virov.](./media/5Resources.jpg)

Viri projekta v aplikaciji Project Operations so vzdrževani v storitvi Dataverse in niso sinhronizirani z aplikacijami Finance and Operations.

### <a name="transaction-categories"></a>Kategorije transakcij

Kategorije transakcij so vzdrževane v storitvi Dataverse in sinhronizirane z aplikacijami Finance and Operations s preslikavo tabele **Kategorije projektnih transakcij (msdyn\_transactioncategories)**. Po sinhronizaciji zapisa kategorije transakcij sistem samodejno ustvari štiri zapise skupnih kategorij. Vsak zapis ustreza vrsti transakcije v aplikacijah Finance and Operations in jih poveže z zapisom kategorije transakcij.

![Integracija kategorije transakcij.](./media/4TransactionCategories.jpg)

Uporaba kategorij transakcij za ocene in dejanske vrednosti zahteva, da računovodja projekta ali sistemski skrbnik ustvari ustrezne kategorije projektov v vsaki pravni osebi. Za več informacij glejte [Konfiguracija kategorij projekta](../project-accounting/configure-project-categories.md).
