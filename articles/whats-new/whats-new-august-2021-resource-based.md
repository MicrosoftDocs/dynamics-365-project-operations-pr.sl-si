---
title: Novosti za avgust 2021 – storitev Project Operations za scenarije, ki temeljijo na virih/pomanjkanju zaloge
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v avgustovski (2021) izdaji storitve Project Operations za scenarije, ki temeljijo na virih/pomanjkanju zaloge.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501391"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za avgust 2021 – storitev Project Operations za scenarije, ki temeljijo na virih/pomanjkanju zaloge

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

   - Project Operations v različici okolja 4.13.0.152. storitve Microsoft Dataverse.
   - Upravljanje projektov in računovodstvo v različici okolja 10.0.20 storitve Dynamics 365 Finance.

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- **Nabori odobritev**: Nabori odobritev združujejo zahteve za odobritev časa, stroškov ali uporabe materiala v manjše podmnožice postopkov. To združevanje omogoča, da so odobritve obdelane v določenem vrstnem redu glede na projekt, poleg tega pa omogoča tudi ponovne poizkuse in oblikovanje zaporedja. Z združevanjem zahtev se povečata zanesljivost in sledljivost obdelave velikega števila odobritev. Več informacij najdete v razdelku [Nabori odobritev](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations.

Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivna različica za preslikovanje se prikaže na strani **Dvojno zapisovanje**, in sicer v stolpcu **Različica**. Novo različico za preslikovanje aktivirajte tako, da izberete možnost **Različica preslikave tabele**, ko ste izbrali najnovejšo različico, pa jo shranite. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težave, upoštevajte navodila iz razdelka [Težava z manjkajočimi stolpci tabele v preslikavi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v vodniku za odpravljanje težav pri dvojnem zapisovanju.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in cene | 2295625 | Ime mejnika je treba kopirati iz razporeda za izstavljanje računov v podrobnosti o vrstici računa. |
| Zaračunavanje in cene | 2316323 | Za scenarije, ki temeljijo na virih, v aplikaciji Project Operations ni dovoljeno urejanje popusta na predračunu. |
| Upravljanje priložnosti | 2338619 | Pravili poslovanja **Priložnost** in **Ponudba** morata biti sproženi samo na straneh. |
| Upravljanje virov | 2316523 | Pri uporabi funkcije **Pošlji zahtevo** iz zahteve za vir, ki ima priloženo vlogo, se ne sme prikazati napaka. |
| Upravljanje virov | 2326885 | Ustvarjanje zahtevanega pogoja za vir v sklopu projekta ne bi smelo prikazati napake. |
| Čas in strošek | 2335584 | Opuščen potek opravila v vnosu časa. |
| Čas in strošek | 2336884 | Gumb za časovni vnos **Kopiraj teden** mora delovati tudi za druge uporabnike, ne le za trenutnega. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pregled upravljanja projektov in računovodstva v storitvi Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Pot in stroški | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nepravilni zneski transakcij dobavitelja in transakcij prometnega davka so objavljeni, ko pri transakciji s kreditno kartico nastane strošek. |
| Pot in stroški | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Napačno izpolnjene so vrstice, ki se pojavijo po tem, ko je ustvarjen dnevnik plačil. |
| Pot in stroški | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nepravilni zneski transakcij prometnega davka so objavljeni, ko pri transakciji s kreditno kartico nastane strošek. |
| Pot in stroški | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Brisanje vrstice stroškov lahko traja dlje časa. |
| Vodenje računov projekta | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistem ne podpira nastavitve neprekinjenega zaporedja števil, ko objavite oceno po uporabi KB 4619395. |
| Vodenje računov projekta | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Objava računov dobavitelja morda ne bo uspešna, pri čemer se bo prikazalo sporočilo o napaki: »Transakcije na kuponu niso izravnane po 17. 5. 2021. (računovodska valuta: 0,00 – valuta za poročanje: 0,01)« |
