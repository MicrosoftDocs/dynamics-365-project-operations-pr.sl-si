---
title: 'Novosti pri izdaji: April 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji aplikacije Microsoft Dynamics 365 Project Operations aprila 2022 za scenarije, ki temeljijo na virih/nezalogi.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110904"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: April 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.41.0.45. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.26

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

Kategorije za nabavo se lahko uporabijo v naročilnicah projektov in računi dobaviteljev na čakanju. Za več informacij glejte razdelek [Uporaba kategorij za nabavo z naročilnicami projektov in računi dobaviteljev na čakanju](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V naslednji tabeli so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz maja 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| -------------- | ------------------- | ------------|
| Entiteta msdyn\_projectvendorinvoicelines za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations | 1.0.0.4 | Ta tabela podpira uporabo kategorij za nabavo z naročilnicami in računi dobaviteljev na čakanju. |

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| ------------ | ---------------- | -------------- |
| Čas in strošek | 2573900 | Funkcija **Sodobna odobritev** mora biti privzeto omogočena. |
| Zaračunavanje in cene | 2603313 | Odpravljena je napaka podvojenega zapisa, ki je preprečevala dodajanje ponudb in podrobnosti pogodbe, ki vsebujejo izdelek. |
| Uvajanje in konfiguracija | 2611368 | Stranke lahko z uporabo sodobnega oblikovalnika aplikacij v rešitev dodajo do pet entitet po meri. |
| Čas in strošek | 2628285 | Odpravljena je težava, ki je vplivala na možnost nastavitve pravilne kategorije vira med uvozom časovnega vnosa. |
| Upravljanje priložnosti| 2628815 | Posodobite omejitev znakov v opisu podrobnosti vrstice ponudbe, da se bo ujemala z omejitvijo znakov predmeta opravila, tako da bo uvoz uspel za opravila, kjer je predmet daljši od 100 znakov. |
| Čas in strošek| 2629547 | Polje **Oddal(-a)** za odobritve projekta mora kazati na uporabnika, ki je oddal zapis. |
| Čas in strošek| 2629865 | Polje **Kopiranje kategorije** pri opravilih, ko so projekti kopirani. |
| Čas in strošek| 2636463 | Popravljeni filtri na odobritvah v obrazcih sodobnih odobritev. |
| Načrtovanje in sledenje projektov | 2648300 | Odpravljena je težava, ki preprečuje spremembo lastnika projekta. |
| Zaračunavanje in cene | 2563000 | Vrstice dnevnika za neobračunano prodajo, kjer se valuta razlikuje od valute pogodbe, ne smejo biti dovoljene. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektov in računovodstvo v okoljih aplikacij Dynamics 365 Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
