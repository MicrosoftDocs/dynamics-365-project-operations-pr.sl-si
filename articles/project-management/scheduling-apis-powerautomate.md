---
title: Uporaba API-jev razporeda projekta s storitvijo Power Automate
description: Ta članek ponuja vzorčni tok, ki uporablja vmesnike za programiranje aplikacij (API-je) razporeda projekta.
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

Ta članek opisuje vzorčni potek, ki prikazuje, kako ustvariti celoten načrt projekta z uporabo Microsoft Power Automate, kako ustvariti nabor operacij in kako posodobiti entiteto. Primer prikazuje, kako ustvariti projekt, člana projektne skupine, nabore operacij, projektne naloge in dodelitve virov. Ta članek tudi pojasnjuje, kako posodobiti entiteto in izvesti nabor operacij.

Sledi popoln seznam korakov, ki so dokumentirani v vzorčnem toku v tem članku:

1. [Ustvariti PowerApps sprožilec](#1)
2. [Ustvari projekt](#2)
3. [Inicializirajte spremenljivko za člana ekipe](#3)
4. [Ustvarite generičnega člana ekipe](#4)
5. [Ustvarite nabor operacij](#5)
6. [Ustvari vedro projekta](#6)
7. [Inicializirajte spremenljivko za status povezave](#7)
8. [Inicializirajte spremenljivko za število opravil](#8)
9. [Inicializirajte spremenljivko za ID naloge projekta](#9)
10. [Naredite do](#10)
11. [Postavite projektno nalogo](#11)
12. [Ustvari projektno nalogo](#12)
13. [Ustvarite dodelitev vira](#13)
14. [Zmanjšaj spremenljivko](#14)
15. [Preimenujte nalogo projekta](#15)
16. [Zaženite nabor operacij](#16)

## <a name="assumptions"></a>Predpostavke

Ta članek predvideva, da imate osnovno znanje o Dataverse platformo, tokove v oblaku in vmesnik za programiranje aplikacij (API) za razpored projekta. Za več informacij glejte [Reference](#references) razdelek kasneje v tem članku.

## <a name="create-a-flow"></a>Ustvari tok

### <a name="select-an-environment"></a>Izberite okolje

Ustvarite lahko Power Automate pretok v vašem okolju.

1. Pojdi do<https://flow.microsoft.com> in za prijavo uporabite skrbniške poverilnice.
2. V zgornjem desnem kotu izberite **Okolja**.
3. Na seznamu izberite okolje, kjer Dynamics 365 Project Operations je nameščen.

### <a name="create-a-solution"></a>Ustvarjanje rešitve

Sledite tem korakom, da ustvarite a [tok, ki se zaveda rešitve](/power-automate/overview-solution-flows). Če ustvarite tok, ki se zaveda rešitve, lahko tok lažje izvozite in ga pozneje uporabite.

1. V podoknu za krmarjenje izberite **Rešitve**.
2. Na **Rešitve** stran, izberite **Nova rešitev**.
3. V **Nova rešitev** pogovornem oknu, nastavite zahtevana polja in nato izberite **Ustvari**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1. korak: ustvarite a PowerApps sprožilec

1. Na **Rešitve** izberite rešitev, ki ste jo ustvarili, in nato izberite **Novo**.
2. V levem podoknu izberite **Oblačni tokovi** \> **Avtomatizacija** \> **Oblačni tok** \> **Instant**.
3. V **Ime toka** polje, vnesite **Razporedi tok predstavitve API-ja**.
4. V **Izberite, kako želite sprožiti ta tok** seznam, izberite **Power Apps**. Ko ustvarite a Power Apps sprožilec, logika je odvisna od vas kot avtorja. V tem članku pustite vhodne parametre prazne za namene testiranja.
5. izberite **Ustvari**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. korak: ustvarjanje projekta

Sledite tem korakom, da ustvarite vzorčni projekt.

1. V toku, ki ste ga ustvarili, izberite **Nov korak**.

    ![Dodajanje novega koraka.](media/newstep.png)

2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.

    ![Izbira operacije.](media/chooseactiontab.png)

3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.

![Preimenovanje koraka.](media/renamestep.png)

4. Preimenujte korak **Ustvari projekt**.
5. V **Ime dejanja** polje izberite **msdyn\_ CreateProjectV1**.
6. Pod **msdyn\_ predmet** polje izberite **Dodajte dinamično vsebino**.
7. Na **Izraz** zavihek, v funkcijsko polje vnesite **Ime projekta - utcNow()**.
8. Izberite **V redu**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3. korak: Inicializirajte spremenljivko za člana ekipe

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **inicializirati spremenljivko**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Član init ekipe**.
5. V **Ime** polje, vnesite **TeamMemberAction**.
6. V **Vrsta** polje izberite **Vrvica**.
7. V **Vrednost** polje, vnesite **msdyn\_ UstvariTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4. korak: Ustvarite splošnega člana ekipe

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Ustvari člana ekipe**.
5. Za **Ime dejanja** polje izberite **TeamMemberAction** v **Dinamična vsebina** pogovorno okno.
6. V **Parametri ukrepanja** polje vnesite naslednje informacije o parametru.

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

    - **\@\@ odata.type** – Ime entitete. Na primer, enter **"Microsoft.Dynamics.CRM.msdyn\_ projektna ekipa"**.
    - **msdyn\_ projectteamid** – Primarni ključ ID-ja projektne skupine. Vrednost je izraz globalnega enoličnega identifikatorja (GUID).   ID se ustvari iz zavihka izraza.

    - **msdyn\_ projekt\@ odata.bind** – ID projekta lastniškega projekta. Vrednost bo dinamična vsebina, ki izhaja iz odziva koraka "Ustvari projekt". Prepričajte se, da ste vnesli celotno pot in dodali dinamično vsebino med oklepaje. Narekovaji so obvezni. Na primer, enter **"/msdyn\_ projekti (DODAJ DINAMIČNO VSEBINO)"**.
    - **msdyn\_ ime** – Ime člana ekipe. Na primer, enter **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5. korak: Ustvarite nabor operacij

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Ustvari nabor operacij**.
5. V **Ime dejanja** izberite polje **msdyn\_ CreateOperationSetV1** Dataverse dejanje po meri.
6. V **Opis** polje, vnesite **ScheduleAPIDemoOperationSet**.
7. V **Projekt** polje, vnesite **/msdyn\_ projekti (**.
8. V **Dinamična vsebina** pogovornem oknu izberite **msdyn\_ CreateProjectV1Response ProjectId**.
9. V **Projekt** polje, vnesite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6. korak: Ustvarite projektno vedro

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **dodaj novo vrstico**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Ustvari vedro**.
5. V **Ime tabele** polje izberite **Projektna vedra**.
6. V **Ime** polje, vnesite **ScheduleAPIDemoBucket1**.
7. Za **Projekt** polje izberite **msdyn\_ CreateProjectV1Response ProjectId** v **Dinamična vsebina** pogovorno okno.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7. korak: Inicializirajte spremenljivko za status povezave

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **inicializirati spremenljivko**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Zaženi status povezave**.
5. V **Ime** polje, vnesite **status povezave**.
6. V **Vrsta** polje izberite **Celo število**.
7. V **Vrednost** polje, vnesite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8. korak: Inicializirajte spremenljivko za število nalog

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **inicializirati spremenljivko**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Init Število nalog**.
5. V **Ime** polje, vnesite **število nalog**.
6. V **Vrsta** polje izberite **Celo število**.
7. V **Vrednost** polje, vnesite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9. korak: Inicializirajte spremenljivko za ID naloge projekta

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **inicializirati spremenljivko**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Zaženi ProjectTaskID**.
5. V **Ime** polje, vnesite **število nalog**.
6. V **Vrsta** polje izberite **Vrvica**.
7. Za **Vrednost** polje, vnesite **guid()** v graditelju izrazov.

## <a name="step-10-do-until"></a><a id="10"></a> 10. korak: Naredite do

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **narediti dokler**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. Nastavite prvo vrednost v pogojnem stavku na **število nalog** spremenljivka iz **Dinamična vsebina** pogovorno okno.
4. Nastavite pogoj na **manj kot enako**.
5. Nastavite drugo vrednost v pogojnem stavku na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11. korak: Nastavite projektno nalogo

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **nastavite spremenljivko**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V novem koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Nastavite projektno nalogo**.
5. V **Ime** polje izberite **msdyn\_ projecttaskid**.
6. Za **Vrednost** polje, vnesite **guid()** v graditelju izrazov.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. korak: Ustvarite projektno nalogo

Sledite tem korakom, da ustvarite nalogo projekta, ki ima edinstven ID, ki pripada trenutnemu projektu in vedru projekta, ki ste ga ustvarili.

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Ustvari projektno nalogo**.
5. V **Ime dejanja** polje izberite **msdyn\_ PssCreateV1**.
6. V **Entiteta** polje vnesite naslednje informacije o parametru.

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

    - **\@\@ odata.type** – Ime entitete. Na primer, enter **"Microsoft.Dynamics.CRM.msdyn\_ projektna naloga"**.
    - **msdyn\_ projecttaskid** – Enolični ID naloge. Vrednost mora biti nastavljena na dinamično spremenljivko iz **msdyn\_ projecttaskid**.
    - **msdyn\_ projekt\@ odata.bind** – ID projekta lastniškega projekta. Vrednost bo dinamična vsebina, ki izhaja iz odziva koraka "Ustvari projekt". Prepričajte se, da ste vnesli celotno pot in dodali dinamično vsebino med oklepaje. Narekovaji so obvezni. Na primer, enter **"/msdyn\_ projekti (DODAJ DINAMIČNO VSEBINO)"**.
    - **msdyn\_ predmet** – Poljubno ime opravila.
    - **msdyn\_ projectbucket\@ odata.bind** – Projektno vedro, ki vsebuje naloge. Vrednost bo dinamična vsebina, ki izhaja iz odziva koraka »Ustvari vedro«. Prepričajte se, da ste vnesli celotno pot in dodali dinamično vsebino med oklepaje. Narekovaji so obvezni. Na primer, enter **"/msdyn\_ projektna vedra (DODAJ DINAMIČNO VSEBINO)"**.
    - **msdyn\_ začetek** – Dinamična vsebina za začetni datum. Na primer, jutrišnji dan bo predstavljen kot **"addDays(utcNow(), 1)"**.
    - **msdyn\_ načrtovani začetek** – Načrtovani začetni datum. Na primer, jutrišnji dan bo predstavljen kot **"addDays(utcNow(), 1)"**.
    - **msdyn\_ razpored** – Načrtovani končni datum. Izberite datum v prihodnosti. Na primer, navedite **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – Stanje povezave. Na primer, enter **"192350000"**.

7. Za **OperationSetId** polje izberite **msdyn\_ CreateOperationSetV1Response** v **Dinamična vsebina** pogovorno okno.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. korak: Ustvarite dodelitev vira

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Ustvari nalogo**.
5. V **Ime dejanja** polje izberite **msdyn\_ PssCreateV1**.
6. V **Entiteta** polje vnesite naslednje informacije o parametru.

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

7. Za **OperationSetId** polje izberite **msdyn\_ CreateOperationSetV1Response** v **Dinamična vsebina** pogovorno okno.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14. korak: Zmanjšajte spremenljivko

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **dekrementna spremenljivka**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V **Ime** polje izberite **število nalog**.
4. V **Vrednost** polje, vnesite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15. korak: Preimenujte nalogo projekta

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Preimenuj projektno nalogo**.
5. V **Ime dejanja** polje izberite **msdyn\_ PssUpdateV1**.
6. V **Entiteta** polje vnesite naslednje informacije o parametru.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Za **OperationSetId** polje izberite **msdyn\_ CreateOperationSetV1Response** v **Dinamična vsebina** pogovorno okno.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16. korak: Zaženite nabor operacij

1. V toku izberite **Nov korak**.
2. V **Izberite operacijo** pogovorno okno vnesite v iskalno polje **izvesti nevezano dejanje**. Nato na **Dejanja** izberite operacijo na seznamu rezultatov.
3. V koraku izberite elipso (**...**), in nato izberite **Preimenuj**.
4. Preimenujte korak **Izvedi niz operacij**.
5. V **Ime dejanja** polje izberite **msdyn\_ ExecuteOperationSetV1**.
6. Za **OperationSetId** polje izberite **msdyn\_ CreateOperationSetV1Response OperationSetId** v **Dinamična vsebina** pogovorno okno.

## <a name="references"></a>Sklici

- [Pregled, kako integrirati tokove z Dataverse -Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja](schedule-api-preview.md)
- [Pregled tokov oblakov -Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pregled tokov, ki se zavedajo rešitev -Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
