---
title: Spremembe funkcij iz aplikacije Project Service Automation v aplikacijo Project Operations
description: Ta članek ponuja pregled sprememb funkcij iz Project Service Automation v Dynamics 365 Project Operations.
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
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925370"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Spremembe funkcij iz aplikacije Project Service Automation v aplikacijo Project Operations

Nadgradnja iz Dynamics 365 Project Service Automation do Dynamics 365 Project Operations Lite bo dostavljen v treh fazah. Ta članek vsebuje informacije o večjih spremembah, ki jih lahko pričakujete, ko bo nadgradnja končana.

| Nadgradite dostavo | 1. faza <br>(januar 2022) | 2. faza <br>(aprilski val 2022) | 3. faza  |
|------------------|------------------------|---------------------------|---------------------------|
| Ni odvisnosti od strukture razčlenitve dela (WBS) za projekte. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS je vključen v trenutno podprte omejitve projektnih operacij. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS zunaj trenutno podprtih omejitev Project Operations, vključno s podporo za namizni odjemalca Project. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Upravljanje projektov

Najpomembnejše spremembe v uporabniški izkušnji bodo na področju načrtovanja projektov. Project Operations sprejema novo sodobno izkušnjo za upravljanje strukture razčlenitve dela (WBS) z izkoriščanjem zmogljivosti načrtovanja, ki jih zagotavlja [Projekt za splet](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Razlike v izkušnji pri načrtovanju

Naslednja tabela povzema razlike pri načrtovanju med avtomatizacijo projektnih storitev in projektnimi operacijami.

|  Načrtovanje     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Predloge projekta – zmožnost definiranja in uporabe predlog projektov, ko je projekt ustvarjen  |  &nbsp;    | :heavy_check_mark: |
| Integracija strukture razčlenitve projektnega dela (WBS) z namiznim odjemalcem   |    &nbsp;  | :heavy_check_mark: |
| Omejitve - Začnite ne prej kot, končajte najkasneje  | :heavy_check_mark: |   &nbsp;  |
| Mejniki – opravila z ničelnim trajanjem   | :heavy_check_mark:  |  &nbsp;  |
| Naloge, ki temeljijo na virih, bodo spoštovale razpoložljivost dodeljenih virov   | :heavy_check_mark: |  &nbsp;    |
| Urejanje po fazah – urejajte načrte in delajte vsak dan   |   &nbsp;  | :heavy_check_mark: |
| Samodejno/ročno razporejanje – uporabite mehanizem za načrtovanje projekta za samodejno ali ročno načrtovanje opravil |  &nbsp; | :heavy_check_mark:  |
| Urejanje velikih projektov neposredno v uporabniškem vmesniku: velikost načrtov, ki jih je mogoče urejati, ni omejena  | Omejitev 500 opravil  | :heavy_check_mark:       |
| Odstotek dokončanja - Označite napredek opravila   | :heavy_check_mark:  |  &nbsp;  |
| [Načini načrtovanja projekta](../project-management/scheduling-modes.md) - Projekt definirajte kot fiksne enote, fiksni napor ali fiksno trajanje | :heavy_check_mark: | &nbsp; |
| Časovna os – Zgradite in prilagodite pogled časovne osi za vizualizacijo podrobnosti razporeda in komunikacijo z zainteresiranimi stranmi. | :heavy_check_mark:  | &nbsp; |
| Naloge, ki jih poganja napor – Podpora motorja za razporejanje za načrtovanje opravila glede na napor  | :heavy_check_mark:  | &nbsp; |
| **Informacije o opravilu** pogovorno okno – shranite podrobnosti opravila v pogovornem oknu | :heavy_check_mark:  |  &nbsp;  |
| Povleci in spusti – izberite več opravil in spremenite njihov položaj na WBS | :heavy_check_mark: | &nbsp;  |
| Prilagodljivi trajni pogledi – Določite bolj natančne poglede atributov opravil   | :heavy_check_mark:  | &nbsp; |
| Razvrstite in filtrirajte WBS  | :heavy_check_mark:  | &nbsp; |
| Pogled na plošče za izvedbo projekta brez slapa  | :heavy_check_mark:   | &nbsp; |
| Pogled časovne osi – Interaktivni Ganttov grafikon, ki se uporablja za vizualizacijo in urejanje WBS   | :heavy_check_mark:  | &nbsp; |
| Bližnjice na tipkovnici – uporabite bližnjice na tipkovnici za običajne operacije, na primer zamik ali vstavljanje  | :heavy_check_mark:  |  &nbsp; |
| Razveljavitev na več ravneh – Izvedite analizo kaj-če, da v celoti razumete vpliv sprememb z razveljavitvijo in ponovno uporabo celotnega niza operacij | :heavy_check_mark: | &nbsp; |
| Izreži/Kopiraj/Prilepi – Sodelujte pri razvoju urnika s kopiranjem in lepljenjem podrobnosti urnika med aplikacijami  | :heavy_check_mark: | &nbsp; |
| Kontrolni seznami opravil – opravilu dodajte do 20 elementov kontrolnega seznama   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Načrtovanje projekta

The **Projekt** stran v Project Operations ima precejšnje število razlik v primerjavi z **Projekt** stran v Project Service Automation.

Naslednja dejanja so bila odstranjena iz **Projekti** stran kot del 1. faze nadgradnje:

  - **Odpri v programu MS Project**
  - **Ustvari predlogo**
  - **Odstrani povezavo s programom MS Project**

The **Projekt** stran v Project Operations vključuje naslednje nove zavihke.

- **Ocene materiala**
- **Nastavitev obračunavanja opravil**

The **Stanje** zavihek je bil odstranjen in **Stanje** polje je zdaj na **Povzetek** zavihek z načinom načrtovanja projekta.

   ![Posodobitve strani projekta.](media/projectform.png)

The **Urnik** zavihek je bil preimenovan v **Naloga** zavihek in ponuja novo izkušnjo načrtovanja projektov s Project za splet.

   ![Nov zavihek Projektna opravila.](media/tasktab.png)

## <a name="scheduling-modes"></a>Načini razporejanja

Project Operations je predstavil novo funkcijo, [Načini načrtovanja](../project-management/scheduling-modes.md). Vsi obstoječi projekti Project Service Automation bodo privzeto nastavljeni **Določeno trajanje** v projektnih operacijah. Vendar pa lahko privzeto vrednost za nove projekte upravljate tako, da obiščete **Nastavitve** > **Parametri** > **Parameter** > **Način urnika**.

   ![Nastavitve parametrov projekta za način urnika.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Meje načrtovanja projekta

Operacije projekta se za vse operacije načrtovanja projekta zanašajo na Project za splet. Project za splet upravlja strukturo razčlenitve dela z uporabo omejitev v naslednji tabeli.

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

## <a name="project-planning-extensibility-and-development"></a>Razširljivost in razvoj načrtovanja projekta

Ko nadgradite na Project Operations, morate uporabiti API-je za načrtovanje projektov za izvajanje operacij ustvarjanja, posodabljanja in brisanja na naslednjih entitetah:

|   Ime entitete           |   Logično ime entitete       |
|-------------------------|-----------------------------|
| Projekt                 | msdyn_project               |
| Projektno opravilo            | msdyn_projecttask           |
| Odvisnost projektnega opravila | msdyn_projecttaskdependency |
| Dodelitev vira     | msdyn_resourceassignment    |
| Vedro projekta          | msdyn_projectbucket         |
| Član projektne ekipe     | msdyn_projectteam           |

Če imate trenutno prilagoditve, ki vključujejo te entitete, glejte [Uporabite API-je načrtovanja projekta za izvajanje operacij z entitetami načrtovanja](../project-management/schedule-api-preview.md) za navodila za izvajanje.

## <a name="data-model-changes"></a>Spremembe podatkovnega modela

Kot del 1. faze nadgradnje pride do sprememb v podatkovnem modelu. Te spremembe so predvsem terenske spremembe obstoječih subjektov. V prvi fazi so subjekti, **msydn_project** in **msdyn_projectteam** so refaktoriranje prilagoditev. 

> [!IMPORTANT]
> Ta razdelek bo posodobljen z dodatnimi entitetami, ko bodo prihodnje faze nadgradnje zaključene.

Naslednja polja so bila zamenjana z novimi polji.

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
| msdyn_project     | msdyn_actualfeesales                         | Prikazuje skupni znesek dejanske prodaje honorarjev za projekt. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Prikazuje skupne dejanske stroške materiala na projektu. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Prikazuje skupno dejansko prodajo materiala na projektu. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Pogodbena vrstica, povezana s tem projektom. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | To je notranje sistemsko polje, ki se uporablja za **Kopiraj projekt** povezana s korelacijskim identifikatorjem. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | To je notranje sistemsko polje, ki se uporablja za **Kopiraj projekt** povezane z identifikatorjem seje. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Zadnja sinhronizacija xRM Global Revision Token iz storitve načrtovanja projekta. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokument Microsoft Project, ki pripada projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Seštevek načrtovanih stroškov materiala na projektu. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Agregat načrtovane prodaje materiala na projektu. Samo za uporabo v Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program, s katerim je povezan ta projekt. |
| msdyn_project     | msdyn_quotelineproject                       | Vrstica Citat, povezana s tem projektom. |
| msdyn_project     | msdyn_replaylogheader                        | Glava za dnevnike ponovnega predvajanja. |
| msdyn_project     | msdyn_schedulemode                           | Privzeti način razporejanja, ki se uporablja za vsa opravila v projektu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najzgodnejši začetni datum poljubnega opravila v projektu.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Član projektne skupine, od katerega je bil ta član projektne skupine kopiran. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Označuje, ali je treba ustvariti zahtevo po virih za na novo ustvarjenega generičnega člana ekipe.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status izbrisa člana skupine za sledenje, ali je bila v storitev načrtovanja projekta poslana zahteva za izbris in ali je uspešno poslala odgovor v pričakovanem časovnem oknu. |
| msdyn_projectteam | msdyn_effortcompleted                        | Spremlja trud, ki ga je član ekipe dosegel pri svojih nalogah. |
| msdyn_projectteam | msdyn_effortremaining                        | Sledi trudu, ki ga mora član ekipe še opraviti pri svojih nalogah. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Čakalna doba od trenutka, ko član ekipe pošlje zahtevo za izbris storitvi načrtovanja projekta, do trenutka, ko je član ekipe dejansko izbrisan dne Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Časovni žig za beleženje, ko je zahteva za izbris člana skupine poslana storitvi načrtovanja projekta. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Pokaže člana projektne ekipe, iz katerega je bil kopiran ta član projektne ekipe.  |

## <a name="project-templates"></a>Projektne predloge

Project Operations ne nudi podpore za predloge projektov. Vendar pa lahko veliko osnovne funkcionalnosti ponovite z uporabo [API za kopiranje projekta](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podpora za namizne dodatke

Podpora za namizni dodatek Microsoft Project ne bo na voljo v prvih dveh fazah nadgradnje. V 3. fazi bodo stranke, ki imajo projekte, večje od trenutno podprtih omejitev za Project za splet, lahko uporabljale namizni dodatek.

## <a name="editing-resource-assignment-contours"></a>Urejanje kontur dodelitve virov

Možnost urejanja kontur dodelitve sredstev bo na voljo, ko bo na voljo 2. faza nadgradnje.

## <a name="billing-and-pricing"></a>Zaračunavanje in cene

Naslednje nove funkcije so bile dodane v Project Operations. Te funkcije so aditivne narave in ne vplivajo na podatkovni model Project Service Automation.

- [Snemanje porabe materiala pri projektih in projektnih nalogah](../material/material-usage-log.md)
- [Upravljanje podizvajalcev](../pro/subcontracting/managing-subcontracts-overview.md)
- [Pogodbe za predplačila in honorarje](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status pogodbe, ki ne bo presegel in potrditve](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Zaračunavanje na podlagi nalog](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Zastarele komponente

Naslednje tabele dokumentirajo vsa opuščena polja, ki so po nadgradnji premaknjena v rešitev opuščenih komponent. Za več informacij in povezavo do rešitve glejte [Dynamics 365 Project Service Automation 3x za Project Operations 4x zastarele komponente](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>Podrobnosti o računu

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

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassification

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

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatuser

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

### <a name="salesorderdetail"></a>Podrobnosti o naročilu

| Polja                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

