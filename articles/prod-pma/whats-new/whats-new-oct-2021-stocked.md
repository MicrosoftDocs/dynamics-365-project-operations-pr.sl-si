---
title: Kaj je novega ali spremenjenega v Project Operations, oktober 2021 za scenarije, ki temeljijo na zalogi/produkciji
description: Ta tema ponuja informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations oktobra 2021 za scenarije, ki temeljijo na zalogi/produkciji.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818330"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Kaj je novega ali spremenjenega v Project Operations, oktober 2021 za scenarije, ki temeljijo na zalogi/produkciji

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta tema velja za naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.22
 
## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
|--------------|------------------|----------------|
| Upravljanje projektov in računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektno delo v obdelavi (WIP) in obračunani zneski prihodkov niso pravilno stornirani, ko je knjižen račun stranke med podjetji. |
| Upravljanje projektov in računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | The **Preprečite zaprtje projekta, če obstajajo odprte transakcije** funkcionalnost ne deluje. |
| Upravljanje projektov in računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija obračunavanja na računu z brezplačnim besedilom ne izpolni samodejno razsežnosti iz projektov, ko je ta funkcija omogočena. |
| Upravljanje projektov in računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | V scenarijih, ki niso medpodjetniški, zneski WIP in vnaprej vračunanih prihodkov niso pravilno stornirani, ko je račun projekta knjižen. |
| Upravljanje projektov in računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Vrednosti bremenitve in kredita se zamenjajo, ko se dodatek Microsoft Excel uporablja z dnevnikom stroškov projekta in **Vrsta Offset računa** polje je nastavljeno na **Projekt**. |
| Upravljanje projektov in računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Znesek, ki je knjižen v projektnih transakcijah, je precenjen v naročilnici projekta, ki vključuje založene artikle in ima neodbitne zneske davka, ko **UseTax** je označena. |
| Upravljanje projektov in računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem razdeli znesek med poročila o dobičku in izgubi projekta in poročila projekta WIP. |
| Upravljanje projektov in računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Priročni inventar ni pravilen po prilagoditvi zahteve za delno vrnjene artikle. |
| Upravljanje projektov in računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Imena virov se podvojijo v Project Operations, ko so urejena v Microsoft Projectu. |
| Upravljanje projektov in računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Poročila o medpodjetniških stroških, ki vsebujejo obveznosti med podjetji, čakajo na stroške računa prodajalca, se najprej knjižijo na **Stroški projekta WIP** vrsta objave. Vendar se med obdelavo stroški, povezani z oceno, knjižijo na **Stroški projekta** vrsta objave namesto pričakovane **Medpodjetniški stroški** vrsta objave. |
| Upravljanje projektov in računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadrževanja prodajalca v transakcijah stroškov projekta niso prikazani. |
| Upravljanje projektov in računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Časovni list mora zaokrožiti znesek transakcije v transakcijski valuti na določeno število decimalnih mest na vseh računovodskih razdelitvah in splošnih vnosih alokacije dnevnika. |
| Upravljanje projektov in računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine potreb projektnih artiklov se samodejno posodobijo, ko se načrtovana naročila potrdijo. |
| Upravljanje projektov in računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Številke kupona, vrste transakcije stanja pri prodajalcu in številke računa ni mogoče razveljaviti na računu za predplačilo naročila. |
| Upravljanje projektov in računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Račun dobavitelja med podjetjem je pokvarjen, ko je vklopljena integracija računov dobavitelja. |
| Upravljanje projektov in računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Ko ustvarite dnevnik stroškov projekta, je znesek stroškov prikazan v **Kredit** polje. |
| Upravljanje projektov in računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Pogoji plačila na projektnih računih ne delujejo po pričakovanjih. |
| Upravljanje projektov in računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Če je številčno zaporedje nastavljeno kot neprekinjeno, bono za časovni list je mogoče ponovno uporabiti. |
| Upravljanje projektov in računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJA: **Znesek ročnega zadrževanja** logika se ne ujema z **Samodejni znesek zadrževanja** logika v predlogu računa za projektno pogodbo. |
| Upravljanje projektov in računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ko se zadržanje prodajalca sprosti, ima knjiženje kupona napačne dodatne vrstice. |
| Upravljanje projektov in računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ko **Datum računa** polje na **Ustvarite predlog računa** stran spremeni, se lahko pojavi naslednja napaka: "Sklic na predmet ni nastavljen na primerek predmeta." |
| Upravljanje projektov in računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Napaka se pojavi, ko poskušate odobriti časovni list iz **TSLine** delovni potek, za soboto in nedeljo pa velja pravilnik o urniku. |
| Upravljanje projektov in računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta postavke projekta začetnega stanja je izključena **Povzetki transakcij predloga računov** ko se izračuna vsota računa predloga računa. |
| Upravljanje projektov in računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Če je strošek porabe pri proizvodnem naročilu projekta 0 (nič), se pri poskusu ocene pojavi naslednja napaka: "Poskus deliti z nič." |
| Upravljanje projektov in računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilna aplikacija Project Timesheet za Android se preneha odzivati. Zadeva je povezana z **TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektov in računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Integracijski dnevnik Project Operations ne uspe, ko ga objavite, ker v računu manjkajo dimenzije. Vendar račun, ki mu manjkajo dimenzije, ni račun, v katerega objavljate. |
| Upravljanje projektov in računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | The **ToDate** filter v iskanjih se ne počisti, ko je odstranjen iz **Izberite** pogovorno okno na **Stroški objave** stran. |
| Upravljanje projektov in računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Ponastavite vso distribucijo** ne uspe in prikaže napako za časovnice, ki so ustvarjene za projekt **Samo čas** tip. |
| Upravljanje projektov in računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | The **Projekt** kartice ni mogoče urejati na čakajočem računu prodajalca, ko je artiklu dodeljena kategorija nabave. |
| Upravljanje projektov in računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Podokno za krmarjenje manjka, če niste prijavljeni v Project Operations Dataverse. |
| Upravljanje projektov in računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pri transakcijah prilagajanja projektov med podjetji obstajajo težave v ciljnem podjetju. |
| Upravljanje projektov in računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Prevzeti stroški za projekt izračunajo napačno količino in stroškovno ceno, če je naročilo obdelal **Postopek naročila ob koncu leta** v glavni knjigi. |
| Upravljanje projektov in računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ko se naročilo izdelave projekta, ki vsebuje naročila kakovosti, poroča kot končano, se pojavi naslednja napaka: "Nobena navidezna transakcija je označena s transakcijo inventarja." |
| Upravljanje projektov in računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Ko je knjižen račun za plačljive račune v zvezi s projektom, se pojavi naslednja napaka: "Našteto besedilo Projekt - stroški - postavka ne obstaja." |
| Upravljanje projektov in računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Posredni stroški se podvojijo, če prihodke ustvarite ročno. |
| Upravljanje projektov in računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Pridobivanje prihodkov in knjiženje WIP ne povzroči transakcij. |
| Upravljanje projektov in računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija čakajoče cene ne uspe za postavko standardne stroške, ko obstaja prejeto naročilo projekta. |
| Upravljanje projektov in računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrnjena vrednost WIP iz knjiženja računa se razlikuje od prvotne knjižene vrednosti WIP iz časovnega vnosa. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Obstaja težava s knjiženjem za projektno fakturirani prihodek v primerih uporabljenih zadržanih, ko transakcije na kuponu niso uravnotežene. |
| Upravljanje projektov in računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Izdelava ocene po knjiženju predloga računa blokira uvoz popravkov v Operacije projekta. |
| Upravljanje projektov in računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Sprememba v celoti zaračunanega zapisa mejnika ne bi smela biti mogoča. |
| Upravljanje projektov in računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Ko se uporabljajo samodejne obremenitve, medpodjetniškega računa stranke za časovni list ni mogoče knjižiti in prikaže se sporočilo o napaki. |
| Upravljanje projektov in računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Naslov v podprojektu ni pravilno posodobljen. |
| Upravljanje projektov in računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Stroškovna cena pri zahtevah artiklov je posodobljena z nabavno ceno za konsolidirana naročila. |
| Upravljanje projektov in računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Objavljeni strošek ni pravilen po posodobitvi nabavne cene in parametra **Aktivirajte upravljanje sprememb** je omogočeno. |
| Pot in stroški | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Vse stroške uporabnika si lahko ogledate, ko iščete kategorijo v mobilni aplikaciji Expense. |
| Pot in stroški | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepravilni zneski pri transakcijah prodajalcev in prometnih davkah so knjiženi iz odhodka, ki je bil ustvarjen s transakcijo s kreditno kartico. |
| Pot in stroški | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Ko osvežite strani poročila o stroških, se prikaže nepomembno opozorilo. |
| Pot in stroški | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Napačen vmesni odobritelj se uporablja, ko izbrišete vmesnega odobritelja in ga nato znova pošljete prek poteka dela. |
| Pot in stroški | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojavi se napaka pri objavljanju, ki je povezana z nastavitvijo kilometrine. |
| Pot in stroški | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribucija ne posodobi pravne osebe, ko je neodvisna transakcija ponovno dodana v poročilo o stroških o stroških med podjetji. |

### <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije Finance in Operations glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prijavite se lahko tudi v Microsoft Dynamics storitve življenjskega cikla (LCS) in uporabite orodje za iskanje težav za ogled načrtovanih posodobitev predpisov. Iskanje težav vam omogoča iskanje po državi ali regiji, vrsti funkcije in izdaji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
