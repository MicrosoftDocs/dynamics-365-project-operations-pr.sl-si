---
title: Novosti v februarju 2022 – Project Operations za primere uporabe z viri/brez zalog
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v februarski izdaji (2022) aplikacije Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933006"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v februarju 2022 – Project Operations za primere uporabe z viri/brez zalog

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.28.0.120. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.24

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

- Od te izdaje naprej lahko enemu projektu dodate do 300 članov ekipe. Prej je bilo število članov ekipe omejeno na 150. Za več informacij glejte razdelek [Omejitve projektov](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Na naslednjem seznamu so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz februarja 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| --- | --- | --- |
| Entiteta za izvoz stroškov projekta pri integraciji aplikacije Project Operations (msdyn\_expenses) | 1.0.0.3 | Razširjeno za sinhronizacijo dejavnosti projekta v okolje Dataverse. |

Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in cene | 2415109 | Privzeta vrednost v polju **Plačilni pogoji poslovanja** mora biti zapis stranke projektne pogodbe in zapis predračuna. |
| Zaračunavanje in cene | 2497369 | Popravki materiala morajo slediti vrednosti datuma v parametrih **Popravek**. |
| Zaračunavanje in cene | 2498697 | Izboljšana varnostna konfiguracija za **Priklic vnosa časa**. |
| Zaračunavanje in cene | 2513824 | Za scenarije, ki temeljijo na virih, ID kategorije transakcije v aplikaciji Project Operations ne sme preseči 28 znakov. |
| Zaračunavanje in cene | 2517455 | Dejanje **Osveži transakcije v vrstici računa** ne sme biti sproženo večkrat hkrati za isti račun. |
| Zaračunavanje in cene | 2517465 | Dejanje **Deaktiviranje podrobnosti v vrstici računa** je blokirano, ker ni podprto. |
| Zaračunavanje in cene | 2556660 | Popravljena preverjanje učinkovitosti datuma, ki se izvaja na ceniku, priloženem zapisu parametrov projekta. |
| Upravljanje priložnosti | 2369202 | Popravljena poslovna logika, ki preverja, ali je mogoče cenike s prekrivajočimi datumi veljavnosti priložiti isti projektni pogodbi. |
| Upravljanje priložnosti | 2385965 | Popravljeno delovanje v zavihku **Stranke** na strani **Projektna pogodba**, ko izberete možnost **Shrani in zapri**. |
| Čas in strošek | 2538503 | Opravilo projekta mora biti na voljo v entiteti **Dejanske vrednosti projekta** po knjiženju poročila o stroških. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektov in računovodstvo v okoljih aplikacij Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Med uvozom dobropisov dobavitelja pride do napake. Sporočilo o napaki navaja: »Zadržani znesek ne sme biti višji od preostalega neto zneska.« |
| Upravljanje projektov in računovodstvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Če predlog računa vključuje kakršne koli transakcije brez dajatev, ki so dejanske neobračunane vrednosti prodaje, se račun ne more izdati. |
| Upravljanje projektov in računovodstvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Knjižena cena ni pravilna, potem ko je nabavna cena posodobljena, parameter **Aktivacija upravljanja sprememb** pa je omogočen.|
| Upravljanje projektov in računovodstvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Ocena knjiženja za projekt s fiksno ceno uporablja napačno valuto in znesek v kuponu ocene, tudi če je funkcija **Omogoči valuto projektne pogodbe za izračun ocene** omogočena. |
| Upravljanje projektov in računovodstvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** ne sme izvesti klica za omogočanje sledenja spremembam, ne da bi ujela izjeme za entitete, ki imajo ključe konfiguracije, ki niso omogočeni. |
| Upravljanje projektov in računovodstvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Paketno opravilo je popravljeno, ko je knjiženih več naprednih dnevnikov in pride do napake. |
| Pot in stroški | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Zaradi težave s poravnavo, ki je povezana z denarnimi predujmi v poročilih o stroških, znesek davka ni zajet kot del denarnega predujma. |
| Pot in stroški | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Podatki o prometnem davku niso vključeni v poročilo **Stroški – knjižene transakcije**. |
| Pot in stroški | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kršitev pravilnika o stroških **Zahtevani so računi** nepravilno prikazuje opozorilo v poročilih o stroških. |
| Pot in stroški | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projektna transakcija ne vključuje nepovratnega prometnega davka v skupnem znesku prodaje, če je transakcija posledica stroškov prevožene razdalje. |
| Pot in stroški | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ko ima razčlenjena vrstica davek, ne morete spremeniti datuma vrstice razčlenitve in pride do napake stanja izvornega dokumenta. |

## <a name="removed-and-deprecated-features"></a>Odstranjene in opuščene funkcije

Članek [Odstranjene ali opuščene funkcije v aplikaciji Project Operations](removed-depreciated-features-project.md) opisuje funkcije, ki so bile za aplikacijo Dynamics 365 Project Operations odstranjene ali opuščene.

- Odstranjena funkcija v izdelku ni več na voljo.
- Opuščena funkcija se ne razvija več in bo lahko odstranjena s prihodnjo posodobitvijo.

Obvestilo o opustitvi bo prikazano v članku [Odstranjene ali zastarele funkcije v aplikaciji Project Operations](removed-depreciated-features-project.md), 12 mesecev preden bo katera koli funkcija odstranjena iz izdelka.

Za predirajoče spremembe, ki vplivajo le na čas zbiranja, vendar so binarno združljive s peskovnikom in produkcijskimi okolji, bo čas opustitve krajši od 12 mesecev. Običajno so te spremembe funkcionalne posodobitve, ki jih je treba izvesti v sestavljalniku.
