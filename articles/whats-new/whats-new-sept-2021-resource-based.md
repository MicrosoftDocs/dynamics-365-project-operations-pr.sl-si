---
title: Novosti za september 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji storitve Project Operations za scenarije, ki temeljijo na virih/nezalogi, za september 2021.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547174"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za september 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

   - Project Operations v različici okolja 4.14.0.99. storitve Microsoft Dataverse.
   - Upravljanje projektov in računovodstvo v različici okolja 10.0.20 storitve Dynamics 365 Finance.

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivna različica za preslikovanje se prikaže na strani **Dvojno zapisovanje**, in sicer v stolpcu **Različica**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pride do težav med zagonom preslikave, sledite navodilom v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodnika za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Čas in strošek | 1811407 | Prilagoditev varnostne vloge odobritelja projekta za odobritve vnosa stroška. |
| Čas in strošek | 1811438 | Prilagoditev varnostne vloge odobritelja projekta za preklic odobritve časovnega vnosa. |
| Čas in strošek | 2370126 | Posodobljeni ikoni **Projektno opravilo** in **Vloga** v entiteti **Časovni vnos**. |
| Čas in strošek | 2379879 | Popravljena funkcija **Kopiraj teden** v časovnem vnosu ob uporabi storitve Dynamics 365 za telefone. |
| Zaračunavanje in oblikovanje cen | 2371906 | Skupni znesek predračuna ne sme biti prilagodljiv v storitvi Project Operations za uvedbe, ki temeljijo na virih. |
| Zaračunavanje in oblikovanje cen | 2385802 | Odpravljena napaka, do katere pride z negativnimi dejanskimi urami, ko so skupne vrednosti za projekt osvežene. |
| Zaračunavanje in oblikovanje cen | 2389675 | Izboljšano delovanje potrditve predračuna. Entiteta dolgotrajnih poslov mora upoštevati dejavnost, ki je obvezna za zapisovanje rezultatov potrditve za računovodstvo. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pregled upravljanja projektov in računovodstva v storitvi Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Pot in stroški | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Zneski za transakcije dobavitelja in prometnega davka, ki so knjiženi iz stroška, ki je bil ustvarjen iz transakcije kreditne kartice, so nepravilni. |
| Pot in stroški | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Ustvarjene so napačne vrstice poravnave, ko je generiran dnevnik plačila. |
| Pot in stroški | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Zneski za transakcije prometnega davka, ki so knjiženi iz stroška, ki je bil ustvarjen iz transakcije kreditne kartice, so nepravilni. |
| Pot in stroški | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Brisanje vrstice stroškov lahko traja dlje časa. |
| Vodenje računov projekta | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Ko uporabite KB 4619395, sprememba zaporedja števil na **Neprekinjeno** ni podprta in ko objavite oceno, pride do naslednje napake »Sistem ne podpira nastavitve 'Neprekinjeno' zaporedja števil Proj_X«. |
| Vodenje računov projekta | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Knjiženje računa dobavitelja morda ni uspešno zaradi naslednjega sporočila o napaki: »Transakcije za kupon nimajo stanja kot na dan 17. 5. 2021. (računovodska valuta: 0,00 – valuta za poročanje: 0,01).« |
