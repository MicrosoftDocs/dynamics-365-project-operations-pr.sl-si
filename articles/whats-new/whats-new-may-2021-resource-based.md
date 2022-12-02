---
title: 'Novosti pri izdaji: Maj 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta članek vsebuje podatke o posodobitvah kakovosti, ki so bile na voljo v izdaji Project Operations maja 2021 za scenarije, ki temeljijo na virih/nezalogi.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030009"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: Maj 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

- Project Operations v okolju Dataverse v storitvi Dynamics 365 različice 4.10.0.186
- Upravljanje projektov in računovodstvo v okoljih aplikacij za finance in postopke različice 10.0.18

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- [Načini razporejanja](../project-management/scheduling-modes.md): vodje projektov lahko določijo, ali naj se projekt upravlja z nespremenljivim trajanjem, nespremenljivim delom ali načinom razporejanja nespremenljivih enot.
- [Nastavitev prevožene razdalje z ravnmi za stopnjo prevožene razdalje](../expense/set-up-mileage.md): posodobite ravni za stopnjo prevožene razdalje za poročila o stroških zaposlenih.

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Na naslednjem seznamu so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz maja 2021.

| Preslikava entitete | Posodobljena različica | Pripombe |
| --- | --- | --- |
| Vir financiranja projekta (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sinhronizacija pogojev plačila stranke za projektno pogodbo. |
| Predlog za račune projekta V2 (računi) | 1.0.0.3 | Sinhronizacija pogojev plačila predračuna. |
| Entiteta za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Posodobitve kakovosti |
| Projekti V2 (msdyn\_projects) | 1.0.0.2 | Posodobitve kakovosti |

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in aplikacij za finance in postopke, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2227635 | Vrednosti v poljih **Skupina enot** in **Enota** so privzeto pridobljene od izdelka v mreži **Ocene materiala**. |
| Zaračunavanje in oblikovanje cen | 2234127 | Polje **ID naloge** se zdaj pravilno integrira v dejanske podatke o projektu v okolju Dataverse, ko je račun prodajalca knjižen. |
| Zaračunavanje in oblikovanje cen | 2235564 | Shranjevanje vrstice dnevnika zagotavlja, da se valuta, prikazana v vnosu vrstice dnevnika, po shranjevanju ujema s privzeto valuto in vrstico. |
| Zaračunavanje in oblikovanje cen | 2246671 | Če transakcijo med izstavljanjem računov označite za transakcijo, ki se ne zaračuna, se prvotni zapis neobračunane prodaje razveljavi in ustvari se nov zapis neobračunane prodaje, ki se ne zaračuna. |
| Zaračunavanje in oblikovanje cen | 2264042 | Veljavnega popravka računa ne smete blokirati, če v okolju obstajajo podatki o popravku računa, ki niso veljavni. |
| Zaračunavanje in oblikovanje cen | 2146367 | Preslikava dvojnega zapisovanja za glavo računa projekta je razširjena tako, da vključuje plačilne pogoje. |
|   Upravljanje priložnosti | 2086888 | Ne dodajajte vlog in kategorij, ki so deaktivirane pred kopiranjem ponudbe, plačljivim vlogam in kategorijam na novo kopirane ponudbe. |
|   Upravljanje priložnosti | 2234376 | Polja samo za branje so v mreži **Ocene materiala** sive barve. |
|   Upravljanje priložnosti | 2238337 | Ponudbo na podlagi stika lahko shranite, tudi če ni povezana s cenikom projekta. |
|   Upravljanje priložnosti | 2239810 | Zapiranje ponudbe s stanjem »izgubljena« zapre tudi povezani projekt in prekliče vse rezervacije. |
| Načrtovanje in sledenje projektov | 2099559 | Dodano je dodatno preverjanje stanja sistema, preden se odpre mreža **Opravila projekta**. |
| Načrtovanje in sledenje projektov | 2178987 | Odpravljena je začasna napaka, ki se pojavi pri izbiri možnosti **Naslednja stopnja** na strani **Projekti**. |
| Upravljanje virov | 2224817 | Funkcija podaljšanja rezervacij je privzeto pravilen status rezervacije. |
| Časovni vnos | 2202476 | Stran **Vnos časa** zdaj uporablja nadzor omrežja z odzivi in odpravlja težave, kot je neporavnana mreža. |
| Časovni vnos | 2223377 | Vnos časa je skrit v razdelku **Sorodno** na strani **Vir, ki ga je mogoče rezervirati**, da ne pride do zamenjave z uporabnostjo. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektov in računovodstvo v okoljih aplikacij Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations za scenarije, ki temeljijo na virih: zaradi napake pri integriranju ponudbe ni mogoče pretvoriti v pridobljeno. |
| Upravljanje projektov in računovodstvo | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: prikaže se sporočilo o napaki, ko poskusite povezati podrobnost pogodbe z ID-jem projekta zaradi preverjanja prekrivanja podrobnosti pogodbe in vrst transakcij. |
| Upravljanje projektov in računovodstvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** nastavi naslov računa za vir financiranja pri drugi stranki. |
| Potovanje in strošek | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Pride lahko do napake pri objavi, povezani z nastavitvijo prevožene razdalje. |
| Potovanje in strošek | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funkcija **Razdeli na osebno** ne deluje za stroškovne transakcije v tujih valutah. |
| Potovanje in strošek | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Vrednosti spustnega seznama za kategorije stroškov prikazujejo napačne kategorije za pooblaščence, ne glede na to, ali so nastavljeni kot vir. |
| Potovanje in strošek | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Poročila o stroških med podjetji ni mogoče shraniti zaradi napake pri **preverjanju virov/kategorij**. |
| Potovanje in strošek | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Napačni izračun stopnje prevožene razdalje pri objavljanju poročil o stroških ima ločene vrstice. |
| Potovanje in strošek | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Poročila o stroških med podjetji ni mogoče objaviti, če je vključen prometni davek, vrsta protikonta za plačilno metodo pa je možnost **Delavec**. |
| Potovanje in strošek | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Razveljavitev podatkovne entitete **TrvRequisitionLine** in edinstven indeks sta povezana. |
| Potovanje in strošek | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Poročilo o stroških podpira ustvarjanje in posodabljanje vrstice izvornega dokumenta. |
| Potovanje in strošek | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Napačen dnevnik pomožne poslovne knjige je prikazan v medpodjetniškem scenariju, če je prometni davek knjižen ciljni pravni osebi. |
| Potovanje in strošek | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: ocena stroška ni izbrisana iz storitve Finance, ko je izbrisana iz storitve Dataverse. |
| Potovanje in strošek | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Če kategorija stroška ni projektna kategorija, se finančne razsežnosti, izbrane na strani **Stroški**, ne kopirajo v poročilo o stroških. |
