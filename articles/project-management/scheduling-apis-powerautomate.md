---
title: Uporaba API-jev razporeda projekta s storitvijo Power Automate
description: Ta članek ponuja vzorčni tok, ki uporablja vmesnike za programiranje aplikacij (API-je) razporejanja projektov.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404466"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Uporaba API-jev razporeda projekta s storitvijo Power Automate

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ta članek opisuje vzorčni tok, ki prikazuje, kako s storitvijo Microsoft Power Automate ustvariti celoten projektni načrt, kako ustvariti komplet postopkov in kako posodobiti entiteto. Primer prikazuje, kako ustvariti projekt, člana projektne ekipe, komplete postopkov, opravila projekta in dodelitve virov. Ta članek pojasnjuje tudi, kako posodobiti entiteto in izvesti komplet postopkov.

Sledi popoln seznam korakov, ki so dokumentirani v vzorčnem toku v tem članku:

1. [Ustvarjanje sprožilca PowerApps](#1)
2. [Ustvari projekt](#2)
3. [Inicializacija spremenljivke za člana ekipe](#3)
4. [Ustvarjanje splošnega člana ekipe](#4)
5. [Ustvarjanje kompleta postopkov](#5)
6. [Ustvarjanje vedra projekta](#6)
7. [Inicializacija spremenljivke za stanje povezave](#7)
8. [Inicializacija spremenljivke za število opravil](#8)
9. [Inicializacija spremenljivke za ID opravila projekta](#9)
10. [Naredi do](#10)
11. [Nastavitev opravila projekta](#11)
12. [Ustvarjanje opravila projekta](#12)
13. [Ustvarjanje dodelitve virov](#13)
14. [Opuščanje spremenljivke](#14)
15. [Preimenovanje opravila projekta](#15)
16. [Zagon kompleta postopkov](#16)

## <a name="assumptions"></a>Predpostavke

Ta članek predpostavlja, da imate osnovno znanje o platformi Dataverse, tokovih za oblake in vmesniku za programiranje aplikacij (API) razporejanja projekta. Za več informacij glejte razdelek [Sklici](#references) v nadaljevanju tega članka.

## <a name="create-a-flow"></a>Ustvari tok

### <a name="select-an-environment"></a>Izberite okolje

Toka Power Automate ne morete ustvarjati v vašem okolju.

1. Pojdite na <https://flow.microsoft.com> in se vpišite s poverilnicami skrbnika.
2. V zgornjem desnem kotu izberite **Okolja**.
3. Na seznamu izberite okolje, kjer je nameščena storitev Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Ustvarjanje rešitve

Za ustvarjanje [toka, ki upošteva rešitve](/power-automate/overview-solution-flows), sledite spodnjim korakom. Če ustvarite tok, ki upošteva rešitve, ga lahko lažje izvozite in pozneje uporabite.

1. V podoknu za krmarjenje izberite **Rešitve**.
2. Na strani **Rešitve** izberite **Nova rešitev**.
3. V pogovornem oknu **Nova rešitev** nastavite zahtevana polja in nato izberite **Ustvari**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1. korak: ustvarjanje sprožilca PowerApps

1. Na strani **Rešitve** izberite rešitev, ki ste jo ustvarili, nato izberite **Novo**
2. V levem podoknu izberite razdelek **Tokovi za oblak** \> **Avtomatizacija** \> **Tok za oblak** \> **Takojšnje**.
3. V polje **Ime toka** vnesite **Predstavitev toka API-ja razporejanja**.
4. Na seznamu **Izbira načina sprožitve poteka** izberite možnost **Power Apps**. Ko ustvarite sprožilec Power Apps, je logika odvisna od vas kot avtorja. V tem članku pustite vhodne parametre prazne za namene preskusa.
5. izberite **Ustvari**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. korak: ustvarjanje projekta

Za ustvarjanje vzorčnega projekta sledite spodnjim korakom.

1. V ustvarjenem toku izberite možnost **Nov korak**.

    ![Dodajanje novega koraka.](media/newstep.png)

2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.

    ![Izbira postopka.](media/chooseactiontab.png)

3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.

![Preimenovanje koraka.](media/renamestep.png)

4. Preimenujte korak **Ustvari projekt**.
5. V polju **Ime dejanja** izberite **msdyn\_CreateProjectV1**.
6. V polju **msdyn\_subject** izberite možnost **Dodajanje dinamične vsebine**.
7. V zavihku **Izraz** v polje funkcije vnesite **Ime projekta – utcNow()**.
8. Izberite **V redu**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3. korak: inicializacija spremenljivke za člana ekipe

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **inicializacija spremenljivke**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Inicializacija člana ekipe**.
5. V polje **Ime** vnesite **TeamMemberAction**.
6. V polju **Vrsta** izberite možnost **Niz**.
7. V polje **Vrednost** vnesite **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. korak: ustvarjanje splošnega člana ekipe

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Ustvarjanje člana ekipe**.
5. V polju **Ime dejanja** v pogovornem oknu **Dinamična vsebina** izberite možnost **TeamMemberAction**.
6. V polju **Parametri dejanja** vnesite naslednje informacije o parametrih.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Tukaj je razlaga parametrov:

    - **\@\@odata.type** – ime entitete. Vnesite na primer **»Microsoft.Dynamics.CRM.msdyn\_projectteam«**.
    - **msdyn\_projectteamid** – Primarni ključ ID-ja projektne ekipe. Vrednost je izraz globalnega enoličnega identifikatorja (GUID).   ID se ustvari iz zavihka izraza.

    - **msdyn\_project\@odata.bind** – ID projekta za projekt v lasti. Vrednost bo dinamična vsebina, ki izhaja iz odziva koraka »Ustvarjanje projekta«. Prepričajte se, da ste vnesli celotno pot in dodali dinamično vsebino med oklepaje. Narekovaji so obvezni. Vnesite na primer **»/msdyn\_projects(ADD DYNAMIC CONTENT)«**.
    - **msdyn\_name** – Ime člana ekipe. Vnesete lahko na primer **»ScheduleAPIDemoTM1«**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5. korak: ustvarjanje kompleta postopkov

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Ustvarjanje kompleta postopkov**.
5. V polju **Ime dejanja** izberite možnost dejanje po meri storitve Dataverse **msdyn\_CreateOperationSetV1**.
6. V polje **Opis** vnesite **ScheduleAPIDemoOperationSet**.
7. V polje **Projekt** vnesite **/msdyn\_projects(**.
8. V pogovornem oknu **Dinamična vsebina** izberite možnost **msdyn\_CreateProjectV1Response ProjectId**.
9. V polje **Projekt** vnesite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. korak: ustvarjanje vedra projekta

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **dodajanje nove vrstice**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Ustvarjanje vedra**.
5. V polju **Ime tabele** izberite možnost **Vedra projekta**.
6. V polje **Ime** vnesite **ScheduleAPIDemoBucket1**.
7. V polju **Projekt** v pogovornem oknu **Dinamična vsebina** izberite možnost **msdyn\_CreateProjectV1Response ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7. korak: inicializacija spremenljivke za stanje povezave

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **inicializacija spremenljivke**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Inicializacija stanja povezave**.
5. V polje **Ime** vnesite **linkstatus**.
6. V polju **Vrsta** izberite **Celo število**.
7. V polje **Vrednost** vnesite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8. korak: inicializacija spremenljivke za število opravil

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **inicializacija spremenljivke**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Inicializacija števila opravil**.
5. V polje **Ime** vnesite **število opravil**.
6. V polju **Vrsta** izberite **Celo število**.
7. V polje **Vrednost** vnesite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9. korak: inicializacija spremenljivke za ID opravila projekta

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **inicializacija spremenljivke**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Inicializacija ProjectTaskID**.
5. V polje **Ime** vnesite **število opravil**.
6. V polju **Vrsta** izberite možnost **Niz**.
7. V polje **Vrednost** v graditelju izrazov vnesite **guid()**.

## <a name="step-10-do-until"></a><a id="10"></a>10. korak: naredi do

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **naredi do**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. Nastavite prvo vrednost v pogojnem stavku na spremenljivko **število opravil** iz pogovornega okna **Dinamična vsebina**.
4. Pogoj nastavite na **manj od ali enako**.
5. Nastavite drugo vrednost v pogojnem stavku na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11. korak: nastavitev opravila projekta

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **nastavitev spremenljivke**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V novem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Nastavitev opravila projekta**.
5. V polju **Ime** izberite možnost **msdyn\_projecttaskid**.
6. V polje **Vrednost** v graditelju izrazov vnesite **guid()**.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. korak: ustvarjanje opravila projekta

Sledite tem korakom, če želite ustvariti opravilo projekta z edinstvenim ID-jem, ki pripada trenutnemu projektu in vedru projekta, ki ste ga ustvarili.

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V tem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Ustvarjanje opravila projekta**.
5. V polju **Ime dejanja** izberite **msdyn\_PssCreateV1**.
6. V polju **Entiteta** vnesite naslednje informacije o parametrih.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Tukaj je razlaga parametrov:

    - **\@\@odata.type** – ime entitete. Vnesite na primer **»Microsoft.Dynamics.CRM.msdyn\_projecttask«**.
    - **msdyn\_projecttaskid** – enolični ID opravila. Vrednost mora biti nastavljena na dinamično spremenljivko iz **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID projekta za projekt v lasti. Vrednost bo dinamična vsebina, ki izhaja iz odziva koraka »Ustvarjanje projekta«. Prepričajte se, da ste vnesli celotno pot in dodali dinamično vsebino med oklepaje. Narekovaji so obvezni. Vnesite na primer **»/msdyn\_projects(ADD DYNAMIC CONTENT)«**.
    - **msdyn\_subject** – katero koli ime opravila.
    - **msdyn\_projectbucket\@odata.bind** – projektno vedro z opravilom. Vrednost bo dinamična vsebina, ki izhaja iz odziva koraka »Ustvarjanje vedra«. Prepričajte se, da ste vnesli celotno pot in dodali dinamično vsebino med oklepaje. Narekovaji so obvezni. Vnesite na primer **»/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)«**.
    - **msdyn\_start** – dinamična vsebina za začetni datum. Jutrišnji dan bo na primer predstavljen kot **»addDays(utcNow(), 1)«**.
    - **msdyn\_scheduledstart** – razporejen začetni datum. Jutrišnji dan bo na primer predstavljen kot **»addDays(utcNow(), 1)«**.
    - **msdyn\_scheduleend** – razporejen končni datum. Izberite datum v prihodnosti. Navedite na primer **»addDays(utcNow(), 5)«**.
    - **msdyn\_LinkStatus** – stanje povezave. Vnesite na primer **»192350000«**.

7. V polju **OperationSetId** v pogovornem oknu **Dinamična vsebina** izberite možnost **msdyn\_CreateOperationSetV1Response**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13. korak: ustvarjanje dodelitve virov

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V tem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Ustvari dodelitev**.
5. V polju **Ime dejanja** izberite **msdyn\_PssCreateV1**.
6. V polju **Entiteta** vnesite naslednje informacije o parametrih.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. V polju **OperationSetId** v pogovornem oknu **Dinamična vsebina** izberite možnost **msdyn\_CreateOperationSetV1Response**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14. korak: opuščanje spremenljivke

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **opuščanje spremenljivke**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V polju **Ime** izberite **število opravil**.
4. V polje **Vrednost** vnesite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. korak: preimenovanje opravila projekta

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V tem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Preimenovanje opravila projekta**.
5. V polju **Ime dejanja** izberite **msdyn\_PssUpdateV1**.
6. V polju **Entiteta** vnesite naslednje informacije o parametrih.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. V polju **OperationSetId** v pogovornem oknu **Dinamična vsebina** izberite možnost **msdyn\_CreateOperationSetV1Response**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16. korak: zagon kompleta postopkov

1. V toku izberite možnost **Nov korak**.
2. V pogovornem oknu **Izbira postopka** v iskalno polje vnesite **izvedba nevezanega dejanja**. Nato v zavihku **Dejanja** na seznamu rezultatov izberite postopek.
3. V tem koraku izberite tri pike (**...**) in nato možnost **Preimenuj**.
4. Preimenujte korak **Izvedba kompleta postopkov**.
5. V polju **Ime dejanja** izberite **msdyn\_ExecuteOperationSetV1**.
6. V polju **OperationSetId** v pogovornem oknu **Dinamična vsebina** izberite možnost **msdyn\_CreateOperationSetV1Response OperationSetId**.

## <a name="references"></a>Sklici

- [Pregled, kako tokove integrirati s storitvijo Dataverse – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja](schedule-api-preview.md)
- [Pregled tokov za oblake – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pregled tokov, ki upoštevajo rešitve – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
