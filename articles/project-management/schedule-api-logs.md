---
title: Dnevniki načrtovanja projekta
description: Ta tema ponuja informacije in vzorce, ki vam bodo pomagali uporabljati dnevnike načrtovanja projektov za sledenje napakam, ki so povezane s storitvijo načrtovanja projektov in API-ji za načrtovanje projektov.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589538"
---
# <a name="project-scheduling-logs"></a>Dnevniki načrtovanja projekta

_**Velja za:** Projektne operacije za scenarije, ki temeljijo na virih/brez zalog, uvedba Lite - obračunavanje s predračunom_, _za splet_

Microsoft Dynamics 365 Project Operations uporablja [Projekt za splet](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kot njegov primarni mehanizem za načrtovanje. Namesto uporabe standarda Microsoft Dataverse Programski vmesniki spletnih aplikacij (API), Project Operations uporablja nove API-je za načrtovanje projektov za ustvarjanje, posodabljanje in brisanje projektnih nalog, dodelitev virov, odvisnosti opravil, projektnih segmentov in članov projektnih skupin. Ko pa se operacije ustvarjanja, posodabljanja ali brisanja programsko izvajajo na entitetah strukture razčlenitve dela (WBS), lahko pride do napak. Za sledenje tem napakam in zgodovini operacij sta bila implementirana dva nova skrbniška dnevnika: **Operacijski komplet** in **Storitev načrtovanja projektov (PSS)**. Za dostop do teh dnevnikov pojdite na **Nastavitve** \> **Integracija urnika**.

Naslednja slika prikazuje podatkovni model za dnevnike načrtovanja projekta.

![Podatkovni model za dnevnike načrtovanja projekta.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Dnevnik nabora operacij

Dnevnik nabora operacij sledi izvedbi nabora operacij, ki se uporablja za izvajanje ene ali več operacij ustvarjanja, posodabljanja ali brisanja v paketu na projektih, projektnih nalogah, dodelitvah virov, odvisnosti opravil, projektnih vedrih ali članih projektne skupine. The **Delovanje v statusu** polje prikazuje splošno stanje niza operacij. Podrobnosti koristne obremenitve nabora operacij so zajete v povezanih zapisih podrobnosti nabora operacij.

### <a name="operation-set"></a>Operacijski komplet

Naslednja tabela prikazuje polja, ki so povezana z **Operacijski komplet** entiteta.

| Ime sheme            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum/čas, ko je bila nastavitev operacij končana ali neuspešna.                                                | CompletedOn            |
| msdyn_correlationid   | The **Id korelacije** vrednost zahteve.                                                                  | CorrelationId          |
| msdyn_description     | Opis kompleta operacij.                                                                        | Description            |
| msdyn_executedon      | Datum/čas, ko se je zapis izvajal.                                                                       | Izvedeno:            |
| msdyn_operationsetId  | Edinstveni identifikator primerkov entitete.                                                                   | OperationSet           |
| msdyn_Project         | Projekt, ki je povezan z operacijskim sklopom.                                                            | Projekt                |
| msdyn_projectid       | The **ID projekta** vrednost zahteve.                                                                      | ProjectId (opuščeno) |
| msdyn_projectName     | Ni na voljo.                                                                                              | Ni na voljo.         |
| msdyn_PSSErrorLog     | Enolični identifikator dnevnika napak storitve načrtovanja projektov, ki je povezan z nizom operacij. | Dnevnik napak za PSS          |
| msdyn_PSSErrorLogName | Ni na voljo.                                                                                              | Ni na voljo.         |
| msdyn_status          | Stanje niza operacij.                                                                             | Status                 |
| msdyn_statusName      | Ni na voljo.                                                                                              | Ni na voljo.         |
| msdyn_useraadid       | The Azure Active Directory (Azure AD) ID objekta uporabnika, ki mu pripada zahteva.                     | UserAADID              |

### <a name="operation-set-detail"></a>Podrobnosti nabora operacij

Naslednja tabela prikazuje polja, ki so povezana z **Podrobnosti nabora operacij** entiteta.

| Ime sheme                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializirano Dataverse polja za zahtevo.                                            | CdsPayload            |
| msdyn_entityname           | Ime subjekta za zahtevo.                                                     | EntityName            |
| msdyn_httpglagol             | Metoda zahteve.                                                                         | Glagol HTTP (opuščeno) |
| msdyn_httpverbName         | Ni na voljo.                                                                             | Ni na voljo.        |
| msdyn_operationset         | Enolični identifikator niza operacij, ki mu pripada zapis.                      | OperationSet          |
| msdyn_operationsetdetailId | Edinstveni identifikator primerkov entitete.                                                  | Podrobnost za OperationSet   |
| msdyn_operationsetName     | Ni na voljo.                                                                             | Ni na voljo.        |
| msdyn_operationtype        | Vrsta operacije podrobnosti nabora operacij.                                             | OperationType         |
| msdyn_operationtypeName    | Ni na voljo.                                                                             | Ni na voljo.        |
| msdyn_psspayload           | Zaporedna polja storitve načrtovanja projektov za zahtevo.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahteve.                                                       | ID zapisa             |
| msdyn_requestnumber        | Samodejno ustvarjena številka, ki označuje vrstni red, v katerem so bile zahteve prejete. | Številka zahteve        |

## <a name="project-scheduling-service-error-logs"></a>Dnevniki napak storitve načrtovanja projektov

Dnevniki napak storitve Project Scheduling Service zajemajo napake, ki se pojavijo, ko storitev načrtovanja projektov poskusi a **Shrani** oz **Odprto** delovanje. Obstajajo trije podprti scenariji, kjer se ustvarijo ti dnevniki:

- Dejanja, ki jih sproži uporabnik, kritično ne uspejo (na primer, dodelitve ni mogoče ustvariti zaradi manjkajočih privilegijev).
- Storitev načrtovanja projektov ne more programsko ustvariti, posodobiti, izbrisati ali izvesti nobene druge kaskadne operacije na entiteti.
- Uporabnik doživi napake, ko se zapis ne odpre (na primer, ko se odpre projekt ali se posodobijo podatki o članu ekipe).

### <a name="project-scheduling-service-log"></a>Dnevnik storitve načrtovanja projektov

Naslednja tabela prikazuje polja, ki so vključena v dnevnik storitve načrtovanja projektov.

| Ime sheme          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Klicni sklad izjeme.                                               | Klicni sklad     |
| msdyn_correlationid | ID korelacije napake.                                               | CorrelationId  |
| msdyn_errorcode     | Polje, ki se uporablja za shranjevanje Dataverse kodo napake ali kodo napake HTTP. | Koda napake     |
| msdyn_HelpLink      | Povezava do javne dokumentacije pomoči.                                       | Povezava do pomoči      |
| msdyn_log           | Dnevnik storitve načrtovanja projektov.                                   | Dnevnik            |
| msdyn_project       | Projekt, ki je povezan z dnevnikom napak.                             | Projekt        |
| msdyn_projectName   | Ime projekta, če bo koristna obremenitev niza operacij ohranjena. | Ni na voljo. |
| msdyn_psserrorlogId | Edinstveni identifikator primerkov entitete.                                     | Dnevnik napak za PSS  |
| msdyn_SessionId     | ID seje projekta.                                                        | ID seje     |

## <a name="error-log-cleanup"></a>Čiščenje dnevnika napak

Privzeto je mogoče tako dnevnike napak storitve Project Scheduling Service kot dnevnik nabora operacij očistiti vsakih 90 dni. Vsi zapisi, ki so starejši od 90 dni, bodo izbrisani. Vendar pa s spremembo vrednosti **msdyn_StateOperationSetAge** polje na **Parametri projekta** strani, lahko skrbniki prilagodijo razpon čiščenja tako, da je med 1 in 120 dnevi. Na voljo je več načinov za spreminjanje te vrednosti:

- Prilagodite **Parameter projekta** entiteto z ustvarjanjem strani po meri in dodajanjem **Starost zastarelih operacij** polje.
- Uporabite odjemalsko kodo, ki uporablja [Komplet za razvoj programske opreme WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Uporabite kodo SDK za storitve, ki uporablja SDK Xrm **updateRecord** metoda (referenca odjemalskega API-ja) v aplikacijah, ki jih poganja model. Power Apps vključuje opis in podprte parametre za **updateRecord** metoda.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
