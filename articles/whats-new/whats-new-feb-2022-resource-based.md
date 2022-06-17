---
title: Novosti v februarju 2022 – Project Operations za primere uporabe z viri/brez zalog
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations februarja 2022 za scenarije, ki temeljijo na virih/brez zalog.
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

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno delovanje v a Dataverse različica okolja 4.28.0.120
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.24

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

- Od te izdaje lahko enemu projektu dodate do 300 članov ekipe. Prej je bila omejitev števila članov ekipe 150. Za več informacij glejte [Omejitve projekta](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Posodobitve zemljevida z dvojnim zapisom Project Operations

Naslednji seznam prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations februarja 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| --- | --- | --- |
| Izvozni subjekt za stroške projekta integracije projektnih operacij (msdyn\_ stroški) | 1.0.0.3 | Razširjeno za sinhronizacijo projektne dejavnosti na Dataverse. |

Za trenutni seznam in različice preslikav z dvojnim pisanjem Project Operations glejte [Različice zemljevidov z dvojnim zapisom Project Operations](../environment/resource-dual-write-maps.md).

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili izključen zemljevid tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu zemljevida naletite na težavo, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelku vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in cene | 2415109 | Privzeta vrednost v **Operativni plačilni pogoji** polje mora biti zapis naročnika projektne pogodbe in zapis predračuna. |
| Zaračunavanje in cene | 2497369 | Popravek materiala mora slediti datumski vrednosti v **Popravek** parametrov. |
| Zaračunavanje in cene | 2498697 | Izboljšana varnostna konfiguracija za **Odpoklic časovnega vnosa**. |
| Zaračunavanje in cene | 2513824 | Za scenarije, ki temeljijo na virih, ID kategorije transakcije v Operacijah projekta ne sme presegati 28 znakov. |
| Zaračunavanje in cene | 2517455 | The **Osvežite transakcije v vrstici računov** dejanje ne sme biti sproženo večkrat hkrati za isti račun. |
| Zaračunavanje in cene | 2517465 | The **Deaktivirajte podrobnosti o vrstici računa** dejanje je blokirano, ker ni podprto. |
| Zaračunavanje in cene | 2556660 | Popravljeno preverjanje učinkovitosti datuma, ki se izvaja na ceniku, ki je priložen zapisu parametrov projekta. |
| Upravljanje priložnosti | 2369202 | Popravljena je poslovna logika, ki preverja, ali je mogoče cenike, ki imajo prekrivajoče se datume veljavnosti, priložiti isti projektni pogodbi. |
| Upravljanje priložnosti | 2385965 | Popravljeno vedenje na **Stranke** zavihek na **Projektna pogodba** stran, ko izberete **Shrani in zapri**. |
| Čas in strošek | 2538503 | Projektna naloga mora biti na voljo v **Dejansko stanje projekta** subjekt po objavi poročila o izdatkih. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vodenje projektov in računovodstvo na Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Med uvozom dobropisov prodajalca pride do napake. Sporočilo o napaki navaja: "Znesek zadrževanja ne sme biti večji od preostalega neto zneska." |
| Upravljanje projektov in računovodstvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Če predlog računa vključuje kakršne koli transakcije z ničelnimi provizijami, ki so dejanska nezaračunana prodaja, do izdajanja računov ni mogoče izvesti. |
| Upravljanje projektov in računovodstvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Objavljeni strošek ni pravilen po posodobitvi nabavne cene in **Aktivirajte upravljanje sprememb** je omogočeno.|
| Upravljanje projektov in računovodstvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Ocena knjiženja za projekt s fiksno ceno uporablja napačno valuto in znesek v predračunskem bonu, tudi če je **Omogoči valuto projektne pogodbe za izračun ocene** funkcija je omogočena. |
| Upravljanje projektov in računovodstvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Podaljšek** ne bi smeli poklicati, da bi omogočili sledenje spremembam, ne da bi zajeli izjeme za entitete, ki imajo konfiguracijske ključe, ki niso omogočeni. |
| Upravljanje projektov in računovodstvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Paketno opravilo je popravljeno, ko je objavljenih več naprednih dnevnikov in pride do napake. |
| Pot in stroški | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Zaradi težave s poravnavo, ki je povezana z gotovinskimi predujmi v poročilih o izdatkih, znesek davka ni zajet kot del gotovinskega predplačila. |
| Pot in stroški | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Podatki o prometnem davku niso vključeni v **Odhodki - knjižene transakcije** poročilo. |
| Pot in stroški | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | The **Obvezna potrdila** kršitev politike stroškov napačno prikazuje opozorilo na poročilih o stroških. |
| Pot in stroški | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projektna transakcija ne vključuje neizterljivega prometnega davka v skupni znesek prodaje, če je transakcija posledica stroškov prevoženih kilometrov. |
| Pot in stroški | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Ko ima razčlenjena vrstica davek, ne morete spremeniti datuma vrstice razčlenitve in pride do napake stanja izvornega dokumenta. |

## <a name="removed-and-deprecated-features"></a>Odstranjene in zastarele funkcije

The [Odstranjene ali zastarele funkcije v Project Operations](removed-depreciated-features-project.md) članek opisuje funkcije, ki so bile odstranjene ali zastarele Dynamics 365 Project Operations.

- Odstranjena funkcija v izdelku ni več na voljo.
- Zastarela funkcija ni v aktivnem razvoju in bo morda odstranjena v prihodnji posodobitvi.

Obvestilo o prenehanju veljavnosti bo prikazano v [Odstranjene ali zastarele funkcije v Project Operations](removed-depreciated-features-project.md) člen 12 mesecev preden se katera koli funkcija odstrani iz izdelka.

Za prekinitvene spremembe, ki vplivajo samo na čas kompilacije, vendar so binarno združljive s peskovnikom in produkcijskimi okolji, bo čas zastaranja krajši od 12 mesecev. Običajno so te spremembe funkcionalne posodobitve, ki jih je treba izvesti v prevajalnik.
