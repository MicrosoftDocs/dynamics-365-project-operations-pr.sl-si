---
title: Novosti za oktober 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta Dynamics 365 Project Operations oktobra 2022 za scenarije, ki temeljijo na virih/nezaloženih.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806751"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za oktober 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.57.0.176. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.30

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

| Območje funkcij | Ime funkcije | Več informacij |
| --- | --- | --- |
| Načrtovanje in sledenje projektov | **Zunanje razporejanje projektnih operacij**<br>Zunanji način razporejanja omogoča strankam izvorno ustvarjanje, posodabljanje in brisanje entitet, ki so povezane s strukturami razčlenitve dela (WBS) z uporabo izvornih Dataverse API-jev, brez trenutnih omejitev, ki jih uveljavlja Project for Web. | [Zunanje razporejanje](/dynamics365/project-operations/project-management/external-scheduling) |
| Uvajanje in konfiguracija | <p>**Omogočite strankam, da izberejo vrsto uvedbe**<br>Posodobitve, ki jih poganja izdelek (PDU-ji) za Project Operations, se uporabljajo za samodejno namestitev rešitve Project Operations Dual-write, ko so v okolju nameščene rešitve jedra in orkestracije Dual-write.</p><p>Ta funkcija uvaja nov parameter **Vedenje nadgradnje rešitve** v parametrih projekta. Ko je ta parameter nastavljen na **Lite only**, PUD-ji ne bodo več samodejno namestili rešitve za dvojno zapisovanje projektnih operacij, tudi če so v okolju nameščene jedrne in orkestracijske rešitve z dvojnim pisanjem. To vedenje bo koristilo strankam, ki nameravajo uporabiti rešitve dvojnega pisanja za integracijo prodajnih naročil v aplikacije za finance in operacije, vendar želijo uporabljati Project Operations v načinu Lite (to je brez integracije v aplikacije za finance in operacije).</p> | |
| Zaračunavanje in oblikovanje cen | <p>**Pretvorba valute za transakcijo neobračunane prodaje v integriranih okoljih**<br>Za stranke, ki uporabljajo Project Operations, integrirane z aplikacijami za finance in operacije (to je v vrsti uvedbe virov/brez zaloge), se menjalni tečaji običajno obvladajo v aplikacijah za finance in operacije. Če pa je treba kategorijo stroškov določiti z uporabo metode izračuna cene "po nabavni vrednosti" ali "pribitka nad nabavno vrednostjo", ko se stranka zaračuna, menjalni tečaj, ki se uporablja za izračun prodajnega zneska, uporablja menjalne tečaje v Dataverse, ne menjalni tečaji iz aplikacij za finance in poslovanje.</p><p>Ta funkcija uvaja nov parameter **Vedenje pretvorbe valut** v parametrih projekta. Ko je ta parameter nastavljen na **Razširjeno z nadomestno možnostjo**, se nezaračunani zneski prodaje pri stroškovnih transakcijah izračunajo z uporabo menjalnih tečajev iz aplikacij za finance in poslovanje.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2316317 | Sistem omogoča ustvarjanje faktur, ki nimajo zaračunanih transakcij. |
| Zaračunavanje in oblikovanje cen | 2737300 | Preverite razpoložljivost polja za  **stranko** pred dostopom do obrazca. |
| Zaračunavanje in oblikovanje cen | 2744948 | Dodajte ničelno preverjanje za način obračunavanja. |
| Zaračunavanje in oblikovanje cen | 2763515 | Obravnava napake ničelne reference, ko manjka prodajna pogodba računa. |
| Zaračunavanje in oblikovanje cen | 2844301 | Ustvarjanje paketnega računa ne uspe zaradi napake. |
| Zaračunavanje in oblikovanje cen | 2845869 | Nepravilno shranjevanje organizacijske storitve. |
| Zaračunavanje in oblikovanje cen | 2853729 | Podrobnosti o vlogi in ceni se posodobijo, ko se spremeni vrsta obračunavanja. |
| Zaračunavanje in oblikovanje cen | 2940350 | Ko so cene dejanske, naj se samodejno vnesejo samo aktivni ceniki. |
| Uvajanje in konfiguracija | 3001206 | Entiteta msdyn\_ replaylogheader preprečuje nadgradnje strankinih organizacij. |
| Upravljanje priložnosti | 2755582 | Obravnava izjem ničelne reference v pomočniku za pravila razdeljenega obračunavanja. |
| Upravljanje priložnosti | 2761477 | Ko je uporabljeno deljeno obračunavanje, izbris mejnika (glave) pusti mejnike osirotele. |
| Upravljanje priložnosti | 2767595 | Ko se zapis o uporabi materiala odpre v glavnem obrazcu, se vir za rezervacijo za zapis spremeni v trenutno prijavljenega uporabnika. |
| Načrtovanje in sledenje projektov | 2790384 | Časovna omejitev Pending OperationSet je prekratka. |
| Načrtovanje in sledenje projektov | 2957840 | Opravil ni mogoče shraniti in stolpcev ni mogoče dodati na stran **Opravila** v Integrated Project Operations. |
| Upravljanje virov | 2751560 | Nedosledne prednostne organizacijske enote v zahtevah po virih. |
| Podizvajalske pogodbe | 2853245 | Ujemanje za dejanske vrednosti vrstice računa dobavitelja ne posodobi statusa preverjanja, če je vrstica pogodbe že povezana z vrstico računa dobavitelja. |
| Podizvajalske pogodbe | 2907231 | Faza obdelave računov dobavitelja ne more napredovati. |
| Čas in strošek | 2867363 | Zapisi ne izpadejo iz pogleda Odsotnosti/počitnice za odobritev, ko so v čakalni vrsti za odobritev. |
| Čas in strošek | 2894405 | TESA: Neuporabljen imenik POC povzroča težave s skladnostjo. |

### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
