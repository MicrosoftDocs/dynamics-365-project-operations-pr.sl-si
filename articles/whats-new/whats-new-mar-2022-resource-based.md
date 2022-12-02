---
title: Novosti v marcu 2022 – Project Operations za primere uporabe z viri/brez zalog
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v marčevski izdaji (2022) aplikacije Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910926"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v marcu 2022 – Project Operations za primere uporabe z viri/brez zalog

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.30.0.99. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.25

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

Dnevnice so zdaj podprte v novem in prenovljenem sodobnem delovnem prostoru za stroške. Podjetja, ki uporabljajo dnevnice, lahko omogočijo to funkcijo, da uporabnikom omogočijo enostaven način oddaje in povrnitve dnevnic. Več informacij najdete v razdelku [Stroški dnevnic](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Na naslednjem seznamu so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz marca 2022.

| **Preslikava entitete** | **Posodobljena različica** | **Pripombe** |
| --- | --- | --- |
| Entiteta msdyn\_projectvendorinvoicelines za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations | 1.0.0.3 | Preslikave so posodobljene za uskladitev z entiteto vrstice računa dobavitelja v okolju Dataverse. <br>Ne aktivirajte različice za preslikavo 1.0.0.4. Za uporabo v kombinaciji z okoljem Finance različice 10.0.26 bo na voljo v naslednji mesečni posodobitvi. |

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Čas in strošek | 2388011 | Pokažite komentarje zavrnitve predlagateljem vnosa časa med množično odobritvijo. |
| Načrtovanje in sledenje projektov | 2495294 | Podrobnosti projekta ne smete urejati na strani **Podrobnosti opravila**. |
| Zaračunavanje in cene | 2499605 | Mejniki pogodbe, ki so ustvarjeni iz mejnikov ponudb, so nepravilno označeni kot samo za branje. |
| Načrtovanje in sledenje projektov | 2506050 | Komplet postopkov ostane na čakanju eno uro, če ni nobene spremembe za shranjevanje. Komplet je nato lažno označen kot **Neuspel**, medtem ko moral biti takoj dokončan. |
| Zaračunavanje in cene | 2507401 | Privzete pogodbene enote so v projektih nepravilno vnesene zaradi nepravilnega predpomnjenja. |
| Zaračunavanje in cene | 2541660 | **Preverjanje veljavnosti izdelave prodajnega naloga** v dvojnem zapisovanju bi moralo biti namenjeno samo naročilom, ki temeljijo na projektu. |
| Zaračunavanje in cene | 2552745 | Davek ni razdeljen med stranke, ki so nastavile pravila za razdeljeno obračunavanje. |
| Zaračunavanje in cene | 2558859 | Izboljšana sporočila o napakah, ko so nastavljene razsežnosti cen. |
| Zaračunavanje in cene | 2558933 | **Uvoz iz ocen projekta** ne uspe, ko je vrednost **msdyn\_project** dodana kot cenovna razsežnost. |
| Zaračunavanje in cene | 2559101 | Brisanje parametrov projekta ni blokirano in povzroča težave. |
| Upravljanje priložnosti | 2570390 | Vtičnik za dvojno zapisovanje na ponudbah, naročilih in priložnostih vsili vrsto računa **Stranka**, tudi če ta vrsta računa ni pravilna. |
| Zaračunavanje in cene | 2586097 | Dejanski stroški deljenega obračunavanja se ne razveljavijo, ko je projekt odstranjen iz podrobnosti projektne pogodbe. |
| Zaračunavanje in cene | 2589619 | Davek na material, ki ni v katalogu, se prenese na neobračunane dejanske vrednosti prodaje in na račun. |
| Upravljanje priložnosti | 2594015 | Ponudbe za stranke, ki imajo plačilne pogoje **Net60**, ni mogoče zapreti kot pridobljeno. |
| Načrtovanje in sledenje projektov | 2595841 | Uporabniki v aplikaciji Project for the Web prejmejo sporočilo o napaki o manjkajoči vrednosti **msdyn\_actualstart**, ko ustvarijo novo zahtevo za vir. |
| Čas in strošek | 2602511 | Polje **Zavrnil(-a)** za vnos časa kaže vrednost **Sistem** namesto imenovanega uporabnika kot zavrnitelja. |
| Čas in strošek | 2602528 | Odobritelj projekta lahko odobri čas za projekte, kjer ni naveden kot odobritelj. |
| Zaračunavanje in cene | 2608550 | Popravek računa je mogoče potrditi tudi, če na izvirniku ni sprememb. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektov in računovodstvo v okoljih aplikacij Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Med aplikacijama Finance in Project Operations je prišlo do neujemanja v dovoljeni dolžini polja **ID kategorije**. |
| Upravljanje projektov in računovodstvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projektov z nespremenljivo ceno ni mogoče izločiti, ko je polje **O izdaji računov za kupce** nastavljeno na **Poslovni izid** in se uporablja načelo **Delež napredka**. |
| Upravljanje projektov in računovodstvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nepravilna privzeta skupina prometnega davka je vnesena iz nastavitve projekta v vrsticah stroškov v dnevniku integracije aplikacije Project Operations. |
| Upravljanje projektov in računovodstvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | V integriranem uvajanju z aplikacijo Project Operations ne morete urejati razsežnosti glave predloga računa za projekt. |
| Upravljanje projektov in računovodstvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Računi medpodjetnih dobaviteljev ne smejo biti integrirani z okoljem Dataverse. |
| Upravljanje projektov in računovodstvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Valuta stanja strank in valuta poročanja se ne ujemata. |
| Upravljanje projektov in računovodstvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Račun za projekt lahko knjižite, tudi če je stranka na čakanju za vse račune. |
| Upravljanje projektov in računovodstvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Gumb **Izbriši vse vrstice** v predlogih računa projekta, ki imajo pogleda **Glava** in **Vrstice**. |
| Upravljanje projektov in računovodstvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Ko knjižite račun dobavitelja, se pojavi naslednja napaka: »Datum obračuna za račun mora biti v istem obračunskem letu kot povezano naročilo. Zaženite proces naročilnice ob koncu leta ali spremenite datum na tekoče obračunsko leto.« |
| Pot in stroški | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Potrjena cena za projekt se ne sprosti po sprostitvi zahteve za pot s potrjeno ceno. |
| Pot in stroški | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Ko oddate poročilo o stroških, se pojavi naslednja napaka: »Sled sklada: podjetje ne obstaja.« |
| Pot in stroški | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Privzeti **ID projekta** se ne vnese v poročila o stroških, ko je v projektu izbran parameter **Zahteva dejavnosti za dnevnik**. |
| Pot in stroški | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Gumb **Stroški knjiženja** v aplikaciji Project Operations ne deluje pravilno za primere uporabe z viri/brez zalog. |
| Pot in stroški | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Prišlo je do težave s **Stopnjo na prevoženo razdaljo** za poročilo o stroških prevožene razdalje, ki vključuje potnike. |
| Pot in stroški | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stopnje stroška na prevoženo razdalje za zaposlene niso pravilno seštete, če se v kategoriji stroškov **Stopnje prevožene razdalje** uporabljata dve različni vrsti vozil. |
| Pot in stroški | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Iskanje za polje **Projekt** v vrstici zahteve za pot ne vrne pravilnega seznama projektov. |
| Pot in stroški | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Prevožena razdalja v pregledu** prikaže opozorilo na poročilih o stroških. |
| Pot in stroški | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Storitev optičnega prepoznavanja znakov (OCR) na potrdilih ne deluje zaradi težave z URL-jem storitve OCR za stroške. |
| Pot in stroški | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ko je funkcija **Sposobnost hitrega razčlenjevanja ponavljajočih se stroškov** omogočena, se zneski v vrsticah razčlenitve v poročilih o stroških spremenijo vsakič, ko se odpre stran **Razčlenitev**. |
| Pot in stroški | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Poročila o stroških ne morete izbrisati, če ima vmesni seznam več kot enega odobritelja. |

## <a name="removed-and-deprecated-features"></a>Odstranjene in opuščene funkcije

Članek [Odstranjene ali opuščene funkcije v aplikaciji Project Operations](removed-depreciated-features-project.md) opisuje funkcije, ki so bile za aplikacijo Dynamics 365 Project Operations odstranjene ali opuščene.

- Odstranjena funkcija v izdelku ni več na voljo.
- Opuščena funkcija se ne razvija več in bo lahko odstranjena s prihodnjo posodobitvijo.

Obvestilo o opustitvi bo prikazano v članku [Odstranjene ali zastarele funkcije v aplikaciji Project Operations](removed-depreciated-features-project.md), 12 mesecev preden bo katera koli funkcija odstranjena iz izdelka.

Za predirajoče spremembe, ki vplivajo le na čas zbiranja, vendar so binarno združljive s peskovnikom in produkcijskimi okolji, bo čas opustitve krajši od 12 mesecev. Običajno so te spremembe funkcionalne posodobitve, ki jih je treba izvesti v sestavljalniku.
