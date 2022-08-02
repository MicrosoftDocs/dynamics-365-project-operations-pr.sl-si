---
title: Kaj je novega ali spremenjenega v Project Operations, oktober 2021 za scenarije, ki temeljijo na zalogi/produkciji
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations iz oktobra 2021 za scenarije, ki temeljijo na zalogi/produkciji.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029963"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Kaj je novega ali spremenjenega v Project Operations, oktober 2021 za scenarije, ki temeljijo na zalogi/produkciji

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance verzija 10.0.22
 
## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
|--------------|------------------|----------------|
| Upravljanje projektov in računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektno delo v teku (WIP) in zneski vnaprej vračunanih prihodkov niso pravilno razveljavljeni, ko je medpodjetniški račun stranke knjižen. |
| Upravljanje projektov in računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | The **Preprečite zaprtje projekta, če obstajajo odprte transakcije** funkcionalnost ne deluje. |
| Upravljanje projektov in računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija zaračunavanja na računu s prostim besedilom ne izpolni samodejno dimenzij iz projektov, ko je ta funkcija omogočena. |
| Upravljanje projektov in računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | V scenarijih, ki niso medpodjetniški, se zneski WIP in vnaprej vračunanih prihodkov ob knjižbi računa za projekt ne razveljavijo pravilno. |
| Upravljanje projektov in računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Vrednosti bremenitve in kredita se zamenjajo, ko je Microsoft Excel dodatek se uporablja z dnevnikom stroškov projekta in **Vrsta računa za izravnavo** polje je nastavljeno na **Projekt**. |
| Upravljanje projektov in računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Ko **UseTax** je označena. |
| Upravljanje projektov in računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem razdeli znesek med poročila o dobičku in izgubi projekta ter poročila WIP projekta. |
| Upravljanje projektov in računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventar pri roki je napačen po prilagoditvi zahteve za delno vrnjen predmet. |
| Upravljanje projektov in računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Imena virov se podvojijo v Project Operations, ko se urejajo v Microsoft Projectu. |
| Upravljanje projektov in računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Poročila o medpodjetniških stroških, ki imajo medpodjetniške obveznosti na čakanju na stroške fakture dobavitelja, se najprej knjižijo v **Stroški projekta WIP** vrsto objave. Vendar se med obdelavo stroški, povezani z oceno, knjižijo v **Stroški projekta** vrsto objave namesto pričakovane **Medpodjetniški stroški** vrsto objave. |
| Upravljanje projektov in računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadrževanja prodajalca v transakcijah stroškov projekta niso prikazani. |
| Upravljanje projektov in računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Časovnica mora zaokrožiti znesek transakcije v transakcijski valuti na določeno število decimalnih mest na vseh računovodskih razdelitvah in vnosih splošnih dodelitev v dnevniku. |
| Upravljanje projektov in računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine zahtev projektnih postavk se samodejno posodobijo, ko so načrtovana naročila potrjena. |
| Upravljanje projektov in računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Številke vavčerja, stanja prodajalca vrste transakcije in številke računa ni mogoče razveljaviti na računu za predplačilo naročilnice. |
| Upravljanje projektov in računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Medpodjetniška faktura dobavitelja je pokvarjena, ko je vklopljena integracija fakture dobavitelja. |
| Upravljanje projektov in računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Ko ustvarite dnevnik stroškov projekta, je znesek stroškov prikazan v **Kredit** polje. |
| Upravljanje projektov in računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Plačilni pogoji na projektnih računih ne delujejo po pričakovanjih. |
| Upravljanje projektov in računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Če je številčno zaporedje nastavljeno kot neprekinjeno, se lahko znova uporabijo potrdila o časovnem listu. |
| Upravljanje projektov in računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJA: The **Znesek ročnega zadrževanja** logika se ne ujema **Samodejni znesek zadrževanja** logika v predlogu računa za projektno pogodbo. |
| Upravljanje projektov in računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ko je zadrževanje prodajalca sproščeno, ima knjižba vavčerja nepravilne dodatne vrstice. |
| Upravljanje projektov in računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ko **Datum računa** polje na **Ustvari predlog računa** strani spremenjena, lahko pride do naslednje napake: "Referenca na objekt ni nastavljena na primerek predmeta." |
| Upravljanje projektov in računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Napaka se pojavi, ko poskušate odobriti časovnico iz **TSLine** potek dela, za soboto in nedeljo pa obstaja pravilnik o časovnem listu. |
| Upravljanje projektov in računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta postavke projekta začetnega stanja je izključena **Povzetki transakcij predloga računa** ko se izračuna vsota računa predloga računa. |
| Upravljanje projektov in računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Če je strošek porabe v proizvodnem nalogu projekta 0 (nič), pride do naslednje napake, ko poskušate oceniti: "Poskus delitve z ničlo." |
| Upravljanje projektov in računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilna aplikacija Project Timesheet za Android se neha odzivati. Zadeva je povezana z **TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektov in računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Dnevnik integracije projektnih operacij ne uspe, ko ga objavite, ker računu manjkajo dimenzije. Vendar pa račun, ki mu manjkajo dimenzije, ni račun, v katerega objavljate. |
| Upravljanje projektov in računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | The **DoDate** filter pri iskanju ni počiščen, ko je odstranjen iz **Izberite** pogovorno okno na **Stroški objave** strani. |
| Upravljanje projektov in računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Ponastavi vso distribucijo** ne uspe in prikaže napako za časovne liste, ustvarjene za projekt **Samo čas** vrsta. |
| Upravljanje projektov in računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | The **Projekt** zavihka ni mogoče urejati na čakajočem računu dobavitelja, ko je predmetu dodeljena kategorija nabave. |
| Upravljanje projektov in računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigacijsko podokno manjka, če niste prijavljeni v Project Operations Dataverse. |
| Upravljanje projektov in računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pri medpodjetniških transakcijah prilagajanja projektov obstajajo težave v ciljnem podjetju. |
| Upravljanje projektov in računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Prevzeti stroški za projekt izračunajo napačno količino in stroškovno ceno, če je naročilo obdelal **Postopek naročila ob koncu leta** v glavni knjigi. |
| Upravljanje projektov in računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ko je proizvodno naročilo projekta, ki ima naročila kakovosti, sporočeno kot dokončano, se pojavi naslednja napaka: »Ni virtualne transakcije, označene s transakcijo inventarja«. |
| Upravljanje projektov in računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Ko je račun za obveznosti v zvezi s projektom objavljen, se pojavi naslednja napaka: "Oštevilčeno besedilo Projekt - stroški - postavka ne obstaja." |
| Upravljanje projektov in računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Če ročno naberete prihodek, se posredni stroški podvojijo. |
| Upravljanje projektov in računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Nabiranje prihodkov in knjiženje WIP ne ustvarja transakcij. |
| Upravljanje projektov in računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija čakajoče cene ne uspe za standardno stroškovno postavko, ko obstaja prejeto naročilo za projekt. |
| Upravljanje projektov in računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Razveljavljena vrednost WIP iz knjižbe računa se razlikuje od prvotno objavljene vrednosti WIP iz časovnega vnosa. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Obstaja težava pri knjiženju za fakturirani prihodek projekta v primerih uporabljenega zadrževalnika, kjer transakcije na kuponu niso uravnotežene. |
| Upravljanje projektov in računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Ustvarjanje ocene po objavi predloga računa blokira uvoz vrstic popravkov v projektnih operacijah. |
| Upravljanje projektov in računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Spreminjanje popolnoma fakturiranega zapisa mejnika ne bi smelo biti mogoče. |
| Upravljanje projektov in računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Pri uporabi samodejnih zaračunavanj medpodjetniškega računa stranke za časovni list ni mogoče objaviti in prikaže se sporočilo o napaki. |
| Upravljanje projektov in računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Naslov podprojekta ni pravilno posodobljen. |
| Upravljanje projektov in računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Stroški za zahteve po artiklih se posodobijo z nabavno ceno za konsolidirana naročila. |
| Upravljanje projektov in računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Objavljena cena ni pravilna, potem ko sta nakupna cena posodobljena in parameter **Aktivirajte upravljanje sprememb** je omogočeno. |
| Pot in stroški | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Vse uporabniške stroške lahko vidite, ko poiščete kategorijo v mobilni aplikaciji Expense. |
| Pot in stroški | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepravilni zneski pri transakcijah prodajalca in transakcijah prometnega davka so knjiženi iz odhodka, ki je bil ustvarjen s transakcijo s kreditno kartico. |
| Pot in stroški | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Ko osvežite strani s poročilom o stroških, se prikaže nepomembno opozorilno sporočilo. |
| Pot in stroški | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Napačen vmesni odobritelj se uporabi, ko izbrišete vmesnega odobritelja in nato znova predložite skozi potek dela. |
| Pot in stroški | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojavi se napaka pri knjiženju, ki je povezana z nastavitvijo kilometrine. |
| Pot in stroški | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribucija ne posodobi pravne osebe, ko je nepovezana transakcija ponovno dodana v poročilo o stroških za medpodjetniške stroške. |

### <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije za finance in poslovanje glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prijavite se lahko tudi v Microsoft Dynamics Lifecycle Services (LCS) in uporabite orodje za iskanje težav, da si ogledate načrtovane regulativne posodobitve. Iskanje po težavah vam omogoča iskanje po državi ali regiji, vrsti funkcije in izdaji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
