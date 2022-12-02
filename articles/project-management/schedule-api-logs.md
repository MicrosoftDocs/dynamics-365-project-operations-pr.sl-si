---
title: Dnevniki načrtovanja projekta
description: Ta članek zagotavlja informacije in vzorce, ki vam bodo pomagali pri uporabi dnevnikov razporejanja projektov za sledenje napakam, ki so povezane s storitvijo razporejanja projektov in API-ji za razporejanje projektov.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923715"
---
# <a name="project-scheduling-logs"></a>Dnevniki načrtovanja projekta

_**Velja za:** aplikacija Project Operations za okoliščine, ki temeljijo na virih/nezalogi, poenostavljeno uvajanje – posel do izstavitve predračuna_, _storitev Project for the Web_

Microsoft Dynamics 365 Project Operations kot primarni mehanizem za razporejanje uporablja [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5). Project Operations namesto standardnih spletnih vmesnikov za programiranje aplikacij (API) Microsoft Dataverse uporablja nove API-je za razporejanje projektov za ustvarjanje, posodabljanje in brisanje opravil projekta, dodelitev virov, odvisnosti od opravil, projektnih veder in članov projektnih ekip. Ko pa se postopki ustvarjanja, posodabljanja ali brisanja programsko izvajajo na entitetah strukturirane razčlenitve dela (SČD), lahko pride do napak. Za sledenje tem napakam in zgodovini postopkov sta bila implementirana dva nova skrbniška dnevnika: **Komplet postopkov** in **Storitev razporejanja projektov (PSS)**. Do teh dnevnikov lahko dostopate v razdelku **Nastavitve** \> **Integracija urnika**.

Naslednja slika prikazuje podatkovni model za dnevnike razporejanja projektov.

![Podatkovni model za dnevnike razporejanja projektov.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Dnevnik kompleta postopkov

Dnevnik kompleta postopkov sledi izvajanju kompleta postopkov, ki se uporablja za zagon ene ali več postopkov ustvarjanja, posodabljanja ali brisanja v paketu na projektih, projektnih opravilih, dodelitvah virov, odvisnostih opravil, projektnih vedrih ali članih projektne ekipe. Polje **Postopek v stanju** prikazuje splošno stanje kompleta postopkov. Podrobnosti koristnih vrednosti kompleta postopkov so zajete v povezanih zapisih podrobnosti kompleta postopkov.

### <a name="operation-set"></a>Komplet postopkov

Spodnja tabela prikazuje polja, ki se nanašajo na entiteto **Komplet postopkov**.

| Ime sheme            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum/ura, ko je bil komplet postopkov dokončan ali neuspel.                                                | CompletedOn            |
| msdyn_correlationid   | Vrednost **correlationId** zahteve.                                                                  | CorrelationId          |
| msdyn_description     | Opis kompleta postopkov.                                                                        | Description            |
| msdyn_executedon      | Datum/ura zagona zapisa                                                                       | Izvedeno:            |
| msdyn_operationsetId  | Enolični identifikator primerkov entitete.                                                                   | OperationSet           |
| msdyn_Project         | Projekt, ki je povezan s kompletom postopkov.                                                            | Projekt                |
| msdyn_projectid       | Vrednost **projectId** zahteve.                                                                      | ProjectId (opuščeno) |
| msdyn_projectName     | Ni na voljo.                                                                                              | Ni na voljo.         |
| msdyn_PSSErrorLog     | Enolični identifikator dnevnika napak storitve razporejanja projektov, ki je povezan s kompletom postopkov. | Dnevnik napak za PSS          |
| msdyn_PSSErrorLogName | Ni na voljo.                                                                                              | Ni na voljo.         |
| msdyn_status          | Stanje kompleta postopkov.                                                                             | Status                 |
| msdyn_statusName      | Ni na voljo.                                                                                              | Ni na voljo.         |
| msdyn_useraadid       | ID predmeta Azure Active Directory (Azure AD) uporabnika, ki mu pripada ta zahteva.                     | UserAADID              |

### <a name="operation-set-detail"></a>Podrobnosti kompleta postopkov

Spodnja tabela prikazuje polja, ki se nanašajo na entiteto **Podrobnosti kompleta postopkov**.

| Ime sheme                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializirana polja Dataverse za zahtevo.                                            | CdsPayload            |
| msdyn_entityname           | Ime entitete za zahtevo.                                                     | EntityName            |
| msdyn_httpverb             | Način zahteve.                                                                         | Glagol HTTP (opuščeno) |
| msdyn_httpverbName         | Ni na voljo.                                                                             | Ni na voljo.        |
| msdyn_operationset         | Enolični identifikator za komplet postopkov, ki mu pripada ta zapis.                      | OperationSet          |
| msdyn_operationsetdetailId | Enolični identifikator primerkov entitete.                                                  | Podrobnost za OperationSet   |
| msdyn_operationsetName     | Ni na voljo.                                                                             | Ni na voljo.        |
| msdyn_operationtype        | Vrsta postopka podrobnosti kompleta postopkov.                                             | OperationType         |
| msdyn_operationtypeName    | Ni na voljo.                                                                             | Ni na voljo.        |
| msdyn_psspayload           | Serializirana polja storitve razporejanja projektov za zahtevo.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahteve.                                                       | ID zapisa             |
| msdyn_requestnumber        | Samodejno ustvarjena številka, ki se uporablja za določanje vrstnega reda, v katerem so bile prejete zahteve. | Številka zahteve        |

## <a name="project-scheduling-service-error-logs"></a>Dnevniki napak storitve razporejanja projektov

Dnevniki napak storitve razporejanja projektov zajamejo napake, do katerih pride, ko storitev razporejanja projektov poskusi izvesti postopek **Shrani** ali **Odpri**. Obstajajo trije podprti scenariji, v katerih so ustvarjeni ti dnevniki:

- Pri dejanjih, ki jih sproži uporabnik, pride do kritične napake (na primer, dodelitve ni mogoče ustvariti zaradi manjkajočih privilegijev).
- Storitev razporejanja projektov ne more programsko ustvariti, posodobiti, izbrisati ali izvesti katerega koli drugega kaskadnega postopka na entiteti.
- Uporabnik naleti na napake, ko se zapis ne odpre (na primer, ko se odpre projekt ali se posodobijo informacije o članu ekipe).

### <a name="project-scheduling-service-log"></a>Dnevnik storitve razporejanja projektov

Spodnja tabela prikazuje polja, ki so vključena v dnevnik storitve razporejanja projektov.

| Ime sheme          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Klicni sklad izjeme.                                               | Klicni sklad     |
| msdyn_correlationid | ID korelacije za napako.                                               | CorrelationId  |
| msdyn_errorcode     | Polje, ki se uporablja za shranjevanje kode napake Dataverse ali kode napake HTTP. | Koda napake     |
| msdyn_HelpLink      | Povezava do javne dokumentacije s pomočjo.                                       | Povezava do pomoči      |
| msdyn_log           | Dnevnik iz storitve razporejanja projektov.                                   | Dnevnik            |
| msdyn_project       | Projekt, ki je povezan z dnevnikom napak.                             | Projekt        |
| msdyn_projectName   | Ime projekta, če bo koristna vsebina kompleta postopkov ohranjena. | Ni na voljo. |
| msdyn_psserrorlogId | Enolični identifikator primerkov entitete.                                     | Dnevnik napak za PSS  |
| msdyn_SessionId     | ID seje projekta.                                                        | ID seje     |

## <a name="error-log-cleanup"></a>Čiščenje dnevnika napak

Privzeto je mogoče dnevnike napak storitve razporejanja projektov in dnevnik kompleta postopkov počistiti vsakih 90 dni. Vsi zapisi o napakah, ki so starejši od 90 dni, bodo izbrisani. Vendar pa lahko skrbniki s spremembo vrednosti polja **msdyn_StateOperationSetAge** na strani **Parametri projekta** prilagodijo obseg čiščenja med 1 in 120 dnevi. Na voljo je več načinov za spreminjanje te vrednosti:

- Prilagodite entiteto **Parameter projekta** tako, da ustvarite stran po meri in dodate polje **Starost zastarelega kompleta postopkov**.
- Uporabite kodo odjemalca, ki uporablja [Komplet za razvoj programske opreme WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Uporabite kodo Service SDK, ki uporablja način Xrm SDK **updateRecord** (sklic API-ja odjemalca) v aplikacijah, ki temeljijo na modelu. Power Apps vključuje opis in podprte parametre za način **updateRecord**.

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
