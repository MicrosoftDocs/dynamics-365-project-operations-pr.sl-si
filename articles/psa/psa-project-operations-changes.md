---
title: Spremembe funkcij iz aplikacije Project Service Automation v aplikacijo Project Operations
description: Ta članek ponuja pregled sprememb funkcij iz aplikacije Project Service Automation v Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459947"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Spremembe funkcij iz aplikacije Project Service Automation v aplikacijo Project Operations

Nadgradnja iz Dynamics 365 Project Service Automation v Dynamics 365 Project Operations Lite bo opravljena v treh fazah. Ta članek vsebuje informacije o večjih spremembah, ki jih lahko pričakujete, ko bo nadgradnja končana.

| Izvedba nadgradnje | 1. faza <br>(januar 2022) | 2. faza <br>(november 2022) | 3. faza  |
|------------------|------------------------|---------------------------|---------------------------|
| Brez odvisnosti od strukturirane členitve dela (SČD) za projekte. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| SČD je vključena v trenutno podprte omejitve aplikacije Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| SČD zunaj trenutno podprtih omejitev aplikacije Project Operations, vključno s podporo za Project desktop client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Upravljanje projektov

Najpomembnejše spremembe uporabniške izkušnje bodo na področju načrtovanja projektov. Project Operations uvede novo sodobno izkušnjo za upravljanje strukturirane členitve dela (SČD) z izkoriščanjem zmogljivosti načrtovanja, ki jih zagotavlja [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Razlike v izkušnjah načrtovanja

Naslednja tabela povzema razlike v načrtovanju med aplikacijama Project Service Automation in Project Operations.

|  Načrtovanje     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Predloge projektov – zmožnost določanja in uporabe predlog projektov, ko je projekt ustvarjen  |  &nbsp;    | :heavy_check_mark: |
| Integracija strukturirane členitve projektnega dela (SČD) z namiznim odjemalcem   |    &nbsp;  | :heavy_check_mark: |
| Omejitve – ne začnite prej, ne končajte pozneje  | :heavy_check_mark: |   &nbsp;  |
| Mejniki – opravila z ničelnim trajanjem   | :heavy_check_mark:  |  &nbsp;  |
| Opravila, ki temeljijo na virih, bodo upoštevala razpoložljivost dodeljenih virov   | :heavy_check_mark: |  &nbsp;    |
| Urejanje po fazah – urejanje načrtov in delo po dnevih   |   &nbsp;  | :heavy_check_mark: |
| Samodejno/ročno načrtovanje – uporaba mehanizma za načrtovanje projekta za samodejno ali ročno načrtovanje opravil |  &nbsp; | :heavy_check_mark:  |
| Urejanje velikih projektov neposredno v uporabniškem vmesniku: velikost načrtov, ki jih je mogoče urejati, ni omejena  | Omejitev 500 opravil  | :heavy_check_mark:       |
| Odstotek dokončanja – označi napredek opravila   | :heavy_check_mark:  |  &nbsp;  |
| [Načini razporedov projektov](../project-management/scheduling-modes.md) – opredelitev projekta kot fiksne enote, fiksni obseg dela ali fiksno trajanje | :heavy_check_mark: | &nbsp; |
| Časovnica – gradnja in prilagoditev pogleda časovnice za vizualizacijo podrobnosti razporeda in komuniciranje z zainteresiranimi skupinami. | :heavy_check_mark:  | &nbsp; |
| Opravila, ki temeljijo na obsegu dela – podpora mehanizma za načrtovanje za načrtovanje opravila, ki temelji na obsegu dela  | :heavy_check_mark:  | &nbsp; |
| Pogovorno okno **Informacije o opravilu** – shranjevanje podrobnosti opravila s pogovornim oknom | :heavy_check_mark:  |  &nbsp;  |
| Povleci in spusti – izbira več opravil in sprememba njihovega položaja na SČD | :heavy_check_mark: | &nbsp;  |
| Prilagodljivi trajni pogledi – določanje bolj zrnatih pogledov atributov opravil   | :heavy_check_mark:  | &nbsp; |
| Razvrstitev in filtriranje SČD  | :heavy_check_mark:  | &nbsp; |
| Pogled plošč za izvedbo projekta brez modela »slap«  | :heavy_check_mark:   | &nbsp; |
| Pogled časovnice – interaktivni Ganttov grafikon, ki se uporablja za vizualizacijo in urejanje SČD   | :heavy_check_mark:  | &nbsp; |
| Bližnjice na tipkovnici – uporaba bližnjic na tipkovnici za običajne postopke, kot sta zamik ali vstavljanje  | :heavy_check_mark:  |  &nbsp; |
| Večstopenjska razveljavitev – izvedba analize »kaj če« za razumevanje vpliva sprememb z razveljavitvijo in ponovno uporabo celotnega niza postopkov | :heavy_check_mark: | &nbsp; |
| Izreži/Kopiraj/Prilepi – sodelovanje pri razvoju razporeda s kopiranjem in lepljenjem podrobnosti razporeda med aplikacijami  | :heavy_check_mark: | &nbsp; |
| Kontrolni seznami opravil – dodajanje do 20 elementov kontrolnega seznama opravilu   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Načrtovanje projekta

Stran **Projekt** v aplikaciji Project Operations ima veliko razlik v primerjavi s stranjo **Projekt** v storitvi Project Service Automation.

Naslednja dejanja so bila odstranjena s strani **Projekti** kot del nadgradnje 1. faze:

  - **Odpri v programu MS Project**
  - **Ustvari predlogo**
  - **Odstrani povezavo s programom MS Project**

Stran **Projekt** v aplikaciji Project Operations vključuje naslednje nove zavihke.

- **Ocene materiala**
- **Nastavitev obračunavanja opravil**

Zavihek **Stanje** je bil odstranjen in polje **Stanje** je zdaj v zavihku **Povzetek** z načinom načrtovanja projekta.

   ![Posodobitve strani »Projekt«.](media/projectform.png)

Zavihek **Razpored** je bil preimenovan v zavihek **Opravilo** in predstavlja novo izkušnjo načrtovanja projekta s storitvijo Project for the Web.

   ![Novi zavihek »Opravila projekta«.](media/tasktab.png)

## <a name="scheduling-modes"></a>Načini razporejanja

Aplikacija Project Operations je predstavila novo funkcijo [Načini načrtovanja](../project-management/scheduling-modes.md). Vsi obstoječi projekti storitve Project Service Automation bodo privzeto nastavljeni na **Fiksno trajanje** v aplikaciji Project Operations. Vendar pa lahko privzeto za nove projekte upravljate tako, da odprete razdelek **nastavitve** > **Parametri** > **Parameter** > **Način načrtovanja**.

   ![Nastavitve parametrov projekta za način načrtovanja.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Omejitve načrtovanja projekta

Aplikacija Project Operations se zanaša na Project for the Web za vse postopke načrtovanja projekta. Project for the Web upravlja strukturirano členitev dela z uporabo omejitev v naslednji tabeli.

| **Polje**                                          | **Omejitev**             |
|----------------------------------------------------|-----------------------|
| Največje skupno število opravil za projekt                  | 500                   |
| Največje skupno trajanje projekta               | 3650 dni (10 let)  |
| Največje skupno število virov za projekt              | 300                   |
| Največje skupno število povezav (samo naslednik) za projekt | 600                   |
| Največje skupno število polj po meri za projekt          | 10                    |
| Najvišja raven hierarhije                            | 10 ravni             |
| Največje število povezav (naslednik + predhodnik)            | 20                    |
| Najdaljše trajanje listnega opravila                      | 1250 dni             |
| Najdaljše trajanje opravila povzetka                 | 3650 dni (10 let)  |
| Največje število virov, dodeljenih opravilu               | 20 virov          |
| Podprto datumsko obdobje za opravilo                    | 1. 1. 2000–31. 12. 2149 |
| Elementi kontrolnega seznama                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Razširljivost in razvoj načrtovanja projektov

Ko nadgradite na Project Operations, morate uporabiti API-je za načrtovanje projektov za izvajanje postopkov ustvarjanja, posodabljanja in brisanja na naslednjih entitetah:

|   Ime entitete           |   Logično ime entitete       |
|-------------------------|-----------------------------|
| Projekt                 | msdyn_project               |
| Projektno opravilo            | msdyn_projecttask           |
| Odvisnost projektnega opravila | msdyn_projecttaskdependency |
| Dodelitev vira     | msdyn_resourceassignment    |
| Vedro projekta          | msdyn_projectbucket         |
| Član projektne ekipe     | msdyn_projectteam           |

Če imate trenutno prilagoditve, ki vključujejo te entitete, glejte [Uporaba API-jev za načrtovanje projekta za izvajanje postopkov s pomočjo entitet načrtovanja](../project-management/schedule-api-preview.md) za navodila za izvajanje.

## <a name="data-model-changes"></a>Spremembe podatkovnega modela

Spremembe podatkovnega modela so del 1. faze nadgradnje. Te spremembe so predvsem spremembe polj obstoječih entitet. V 1. fazi sta entiteti **msydn_project** in **msdyn_projectteam** so prenovi prilagoditev. 

> [!IMPORTANT]
> Ta razdelek bo posodobljen z dodatnimi entitetami, ko bodo zaključene prihodnje faze nadgradnje.

Naslednja polja so bila nadomeščena z novimi polji.

|   Entity          |   Staro logično ime   |   Novo logično ime    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Dodana so naslednja polja.

|   Entity          |   Logično ime                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Pokaže združeno dejansko vrednost za projekt. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Pokaže združene dejanske stroške materiala za projekt. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Pokaže združene dejanske stroške materiala za projekt. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Podrobnosti pogodbe, povezane s tem projektom. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | To je polje notranjega sistema, ki se uporablja za dejanje **Kopiraj projekt**, povezano z identifikatorjem korelacije. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | To je polje notranjega sistema, ki se uporablja za dejanje **Kopiraj projekt**, povezano z identifikatorjem seje. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Zadnja sinhronizacija globalnega revizijskega žetona xRM iz storitve načrtovanja projektov. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokument Microsoft Project, ki pripada projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Združena načrtovana vrednost materiala za projekt. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Združena načrtovana prodaja materiala za projekt. Samo za uporabo v storitvi Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program, s katerim je povezan ta projekt. |
| msdyn_project     | msdyn_quotelineproject                       | Vrstica ponudbe, povezana s tem projektom. |
| msdyn_project     | msdyn_replaylogheader                        | Glava za dnevnike ponovnih predvajanj. |
| msdyn_project     | msdyn_schedulemode                           | Privzeti način načrtovanja, uporabljen za vsa opravila v projektu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najzgodnejši začetni datum poljubnega opravila v projektu.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Član projektne ekipe, iz katerega je bil kopiran ta član projektne ekipe. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Označuje, ali naj se ustvari zahteva za vir za novoustvarjenega generičnega člana ekipe.  |
| msdyn_projectteam | msdyn_deletestatus                           | Stanje izbrisa člana skupine za sledenje, ali je bila v storitev načrtovanja projektov poslana zahteva za izbris in ali storitev uspešno in v pričakovanem časovnem obdobju pošlje nazaj odgovor. |
| msdyn_projectteam | msdyn_effortcompleted                        | Sledi obsegu dela, ki ga izvede član ekipe pri dodeljenih nalogah. |
| msdyn_projectteam | msdyn_effortremaining                        | Sledi obsegu dela, ki ga mora član ekipe še izvesti pri dodeljenih nalogah. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Čakalna doba od trenutka, ko član ekipe pošlje zahtevo za brisanje storitvi načrtovanja projektov, do trenutka, ko je član ekipe dejansko izbrisan v Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Časovni žig za beleženje, kdaj je zahteva za izbris člana ekipe poslana v storitev načrtovanja projektov. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Pokaže člana projektne ekipe, iz katerega je bil kopiran ta član projektne ekipe.  |

## <a name="project-templates"></a>Projektne predloge

Project Operations ne nudi podpore za projektne predloge. Vendar pa lahko velik del osnovne funkcije ponovite z uporabo [API-jev za kopiranje projekta](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podpora za namizne dodatke

Podpora za namizni dodatek Microsoft Project ne bo na voljo v prvih dveh fazah nadgradnje. V 3. fazi bodo stranke, ki imajo projekte večje od trenutno podprtih omejitev storitve Project for the Web, lahko uporabljale namizni dodatek.

## <a name="editing-resource-assignment-contours"></a>Urejanje krivulj dodelitve virov

Možnost urejanja krivulj dodelitve virov bo na voljo, ko bo na voljo 2. faza nadgradnje.

## <a name="billing-and-pricing"></a>Zaračunavanje in cene

V aplikacijo Project Operations so bile dodane naslednje nove funkcije. Te funkcije se lahko dodajajo in ne vplivajo na podatkovni model Project Service Automation.

- [Beleženje uporabe materiala v projektih in projektnih opravilih](../material/material-usage-log.md)
- [Upravljanje podizvajalskih pogodb](../pro/subcontracting/managing-subcontracts-overview.md)
- [Pogodbe za predplačila in honorarje](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Stanje in veljavnosti pogodbe »Ni dovoljeno preseči«](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Obračunavanje na podlagi opravil](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Opuščene komponente

Naslednje tabele dokumentirajo vsa opuščena polja, ki so po nadgradnji premaknjena v rešitev za opuščene komponente. Za več informacij in povezavo do rešitve glejte [Dynamics 365 Project Service Automation 3x v Project Operations 4x opuščene komponente](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

