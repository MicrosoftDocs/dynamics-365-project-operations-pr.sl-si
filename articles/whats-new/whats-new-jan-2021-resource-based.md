---
title: Novosti v januarju 2021 – Project Operations za primere uporabe z viri/brez zalog
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v januarski izdaji (2021) aplikacije Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958953"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v januarju 2021 – Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

  - Project Operations v okolju Dataverse različice 4.6.0.154
  - Upravljanje projektov in računovodstvo v okolju Dynamics 365 Finance, različica 10.0.16

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| **Uvajanje in konfiguracija** | 2106818 | Popravljeno preimenovanje spletnega vira, ki je povzročalo težave v zvezi s prilagajanjem strani. |
| **Zaračunavanje in oblikovanje cen** | 2091908 | Popravljena vidljivost možnosti **Zakleni cene** in **Uporabi trenutne cene** na strani **Račun**, ko je storitev Project Operations nameščena skupaj s storitvijo Dynamics 365 Field Service. |
| **Zaračunavanje in oblikovanje cen** | 2103058 | Osvežena možnost **Skupaj za projekt** za obravnavo ničelnih vrednosti za dejanski strošek opravila. |
| **Zaračunavanje in oblikovanje cen** | 2116100 | Izboljšana sporočila o napakah, uporabljena s funkcionalnostjo **Pravi vnosi za dejanske vrednosti**. |
| **Zaračunavanje in oblikovanje cen** | 2116129 | Izboljšana vidljivost ocen stroškov na zavihku **Ocene** na strani **Projekti**. |
| **Zaračunavanje in oblikovanje cen** | 2119112 | Fiksno združevanje dejanske prodaje in dejanskih stroškov, ko se uporabijo različni menjalni tečaji. |
| **Zaračunavanje in oblikovanje cen** | 2134705 | Popravljena napaka »No mogoče prebrati lastnosti **getResourceString** nedoločenega«, ko je stran **Račun** odprta in je storitev Field Service nameščena. |
| **Upravljanje priložnosti** | 2022195 | Mreža obračunavanja na podlagi opravila na strani **Projekt** vključuje ikono, ki označuje, da je vrstica pogodbe ali ponudbe povezana z opravilom. |
| **Upravljanje priložnosti** | 2029135 | Popravljena napaka poslovnega procesa, do katere pride, ko uporabnik poskuša odpreti vrstico računa na potrjenem računu, ki ima fakturirani znesek predujma. |
| **Upravljanje priložnosti** | 2040713 | Popravljena napaka skripta, do katere pride, ko je račun ustvarjen iz pogodbe in je nameščena storitev Field Service. |
| **Načrtovanje in sledenje projektov** | 2090202 | Označena pravila poslovanja, ki se ne uporabljajo, kot **Zastarelo**. |
| **Čas in strošek** | 2091249 | Strožji nadzori, tako da uporabniki ne morejo spremeniti opravila na predloženem ali odobrenem časovnem vnosu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pregled upravljanja projektov in računovodstva v storitvi Dynamics 365 Finance

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| **Upravljanje projektov in računovodstvo** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Nepravilen pogodbeni znesek na strani **Za kupca** za projekt s fiksno ceno z več viri financiranja. |
| **Upravljanje projektov in računovodstvo** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Označba mesta **Invoiceproposal.PSAnfRefProjId** ne prikazuje ID-ja projekta za potek dela **Pregled predlogov za račune projekta**. |
| **Upravljanje projektov in računovodstvo** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Napačen datum gotovinskega popusta je uporabljen pri knjiženju predlogov za račune projekta. |
| **Upravljanje projektov in računovodstvo** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Odstranjevanje in branje dodelitev virov v storitvi Project Operations podvoji vnose projektnih napovedi v storitvi Finance. |
| **Upravljanje projektov in računovodstvo** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | V storitvi Project Operations ni mogoče ustvariti ocen projektov v storitvi Dataverse brez podrobnosti pogodbe za projekt. |
| **Upravljanje projektov in računovodstvo** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Finančna razsežnost transakcije stroškov projekta ni sinhronizirana s povezanim kuponom in računovodskim porazdeljevanjem poročila o stroških, ko se stroški knjižijo v saldo. |
| **Upravljanje projektov in računovodstvo** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filter **Stanje računa** za knjižene projektne transakcije za projekte s fiksno ceno ne deluje. |
| **Upravljanje projektov in računovodstvo** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Razveljavitev izločitev ocen ne deluje v razdelku **Redno**. |
| **Upravljanje projektov in računovodstvo** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Vrstice predloga računa so lahko izbrisane v storitvi Project Operations ob integraciji s storitvijo Dataverse. |
| **Upravljanje projektov in računovodstvo** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Ne omogočite funkcije za možnost uporabe več podrobnosti pogodb brez integracije storitve Dataverse. |
| **Upravljanje projektov in računovodstvo** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Ko je fakturiranje za kupca enako izkazu poslovnega izida, je fakturirani prihodek naveden kot nič na strani z ocenami. |
| **Upravljanje projektov in računovodstvo** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Popravki računov ne delujejo za integrirana okolja. |
| **Upravljanje projektov in računovodstvo** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Pri knjiženju zneska prodaje PVT pri medpodjetnem izdajanju računov za projekt je izbran napačen račun. |
| **Upravljanje projektov in računovodstvo** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | V storitvi Project Operations se odvisnosti od opravil ocenjevanja v storitvi Dataverse ne morejo posodobiti. |
| **Upravljanje projektov in računovodstvo** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Večkratno brisanje dnevnikov integracije Project Operations v storitvi Finance vodi v izgubo podatkov. |
| **Upravljanje projektov in računovodstvo** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Pride do naslednje napake pri knjiženju predloga za račun projekt »Transakcija se ne uskladi na valuto poročanja, ko je dodano odštetje računa predujma«. |
| **Upravljanje projektov in računovodstvo** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Napačen ID projekta je vključen na odbitkih, potem ko je privzeta pogodba projekta posodobljena v storitvi Project Operations. |
| **Upravljanje projektov in računovodstvo** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Ocene in prepoznavanja prihodka ni mogoče izvesti, ko je omogočena storitev Project Operations. |
| **Upravljanje projektov in računovodstvo** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | V storitvi Project Operations odstranitev projekta iz pogodbe ne ponastavi privzetega projekta v pogodbi. |
| **Upravljanje projektov in računovodstvo** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | V storitvi Project Operations na medpodjetnem računu so prikazane napačne vrstice stroškov na seznamu **Dodaj vrstico**. |
| **Potovanje in strošek** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Stroškovnih vrstic ni mogoče objaviti, ker v podrobnostih pogodbe manjka nastavitev ure. |
| **Potovanje in strošek** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Ko je potrjevanje projekta/kategorije obvezno, kategorije stroškov, povezane s projektom, niso vidne v poročilu o stroških. |
| **Potovanje in strošek** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldo denarnega predujma se ne posodobi, ko je poročilo o stroških knjiženo po vrstici. |
| **Potovanje in strošek** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Posel **Posodabljanje informacij za plačilo** ne uspe po storniranju poravnav, kjer je bil račun poravnan z dvema ali več plačilnimi transakcijami. |
| **Potovanje in strošek** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Pride do težave z izračunom zmanjšanega obroka za zadnji dan za dnevnico, eno od kategorij stroškov. |
| **Potovanje in strošek** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Poročilo **Vrsta stroškov na zaposlenega** ne prikazuje razčlenjenih stroškov, če je bila uporabnikova prva povezava v jeziku es-MX. |
| **Potovanje in strošek** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Plačilo dobavitelju za račun s poročilom o stroških uporablja napačen zbirni račun za knjiženje poravnave. |
| **Potovanje in strošek** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Ko je poročilo o stroških knjiženo z omogočenima možnostma **Omogoči razvrščanje transakcij na podlagi pobotanega računa** in **Popravek računovodskega datuma pri knjiženju**, računovodski datumi niso združeni v tabeli **Računovodsko porazdeljevanje**, ki vpliva na zapise o prometnem davku. |
| **Potovanje in strošek** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Preslikava podkategorije stroška je odstranjena, ko je potrditveno polje uporabe v strošku počiščeno in nato znova izbrano. |
| **Potovanje in strošek** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Poročila o medpodjetnih stroških ni mogoče ustvariti, če je ID projekta dodan na ravni glave. |
| **Potovanje in strošek** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Pride do težave s plačili stroškov, kadar je znesek stroška večji od zneska gotovinskega predplačila. |
| **Potovanje in strošek** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Polje **ID projekta** v medpodjetnem poročilu o stroških je prazno, če je uporabniška vloga dodeljena določeni organizaciji. |
| **Potovanje in strošek** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorija stroškov je zaklenjena pri dodajanju nove vrstice stroška. |
| **Potovanje in strošek** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Razčlenitev že razdeljenih vrstic poročila o stroških povzroči nepopolne knjižene obveznosti\kupona glavne knjige. Zaradi podvajanja elementa **TRVEXPTRANS.SOURCEDOCUMENTLINE** je prekinjen tudi raziskovalec vira računovodstva. |
| **Potovanje in strošek** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Kazalo, dodano v tabelo **TRVREQUISITIONLINE**, za katero ima stranka podvojitve, povzroči napako med nadgradnjo. |
| **Potovanje in strošek** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | V storitvi Project Operations ni mogoče ustvariti ali odobriti časa z medpodjetnimi opravili v storitvi Dataverse. |

## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije Finance and Operations glejte [Regulativne posodobitve](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Prav tako se lahko prijavite v storitev LCS in si ogledate načrtovane regulativne posodobitve z orodjem za iskanje težav. Iskanje težav omogoča iskanje po državi, vrsti funkcije in izdaji.


[!INCLUDE[footer-include](../includes/footer-banner.md)]