---
title: Novosti ali spremembe v storitvi Project Operations, oktober 2021, za scenarije, ki temeljijo na zalogi/proizvodnji
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v oktobrski izdaji (2021) aplikacije Project Operations za primere uporabe z naročili na zalogi/v proizvodnji.
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
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novosti ali spremembe v storitvi Project Operations, oktober 2021, za scenarije, ki temeljijo na zalogi/proizvodnji

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.22
 
## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
|--------------|------------------|----------------|
| Upravljanje projektov in računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektno delo v teku (WIP) in zneski vračunanih prihodkov niso pravilno razveljavljeni, ko je račun medpodjetne stranke knjižen. |
| Upravljanje projektov in računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcionalnost **Preprečevanje zaprtja projekta, če obstajajo odprte transakcije** ne deluje. |
| Upravljanje projektov in računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija obračunavanja na računu s prostim besedilom razsežnosti iz projektov ne izpolni samodejno, ko je ta funkcija omogočena. |
| Upravljanje projektov in računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Pri primerih uporabe, ki niso medpodjetna, WIP in zneski vračunanih prihodkov niso pravilno razveljavljeni, ko je račun projekta knjižen. |
| Upravljanje projektov in računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Vrednosti bremenitve in dobropisa se zamenjajo, ko se dodatek Microsoft Excel uporablja z dnevnikom stroškov projekta in je polje **Vrsta računa za odmik** nastavljeno na **Projekt**. |
| Upravljanje projektov in računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Znesek, ki je knjižen v transakcijah projekta, je previsok na naročilnici projekta, ki vključuje elemente zaloge in od katere ni odbit znesek davka, ko je označena možnost **UseTax**. |
| Upravljanje projektov in računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem razdeli znesek med poročila o dobičku in izgubi projekta ter poročila WIP projekta. |
| Upravljanje projektov in računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Zaloga je napačna po prilagoditvi zahteve za delno vrnjen element. |
| Upravljanje projektov in računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Imena virov se podvojijo v aplikaciji Project Operations, ko se urejajo v aplikaciji Microsoft Project. |
| Upravljanje projektov in računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Poročila o medpodjetnih stroških, ki imajo medpodjetne obveznosti v čakanju na stroške računa dobavitelja, se najprej knjižijo v vrsto knjiženja **Stroški projekta WIP**. Vendar se med obdelavo stroški, povezani z oceno, knjižijo v vrsto knjiženja **Stroški projekta** namesto pričakovane vrste knjiženja **Medpodjetni stroški**. |
| Upravljanje projektov in računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadrževanja dobavitelja v transakcijah stroškov projekta niso prikazani. |
| Upravljanje projektov in računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Časovni list mora zaokrožiti znesek transakcije v valuti transakcije na določeno število decimalnih mest na vseh računovodskih porazdelitvah in vnosih splošnih dodelitev v dnevniku. |
| Upravljanje projektov in računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine zahtev elementov projekta se samodejno posodobijo, ko so načrtovana naročila potrjena. |
| Upravljanje projektov in računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Številke kupona, saldo dobavitelja vrste transakcije in številke računa ni mogoče razveljaviti na predračunu naročilnice. |
| Upravljanje projektov in računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Medpodjetni računi dobavitelji so poškodovani, ko je vklopljena integracija računa dobavitelja. |
| Upravljanje projektov in računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Ko ustvarite dnevnik stroškov projekta, je znesek stroškov prikazan v polju **Dobropis**. |
| Upravljanje projektov in računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Plačilni pogoji na računih projekta ne delujejo po pričakovanjih. |
| Upravljanje projektov in računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Če je številčno zaporedje nastavljeno kot neprekinjeno, se kupni za časovni list lahko ponovno uporabijo. |
| Upravljanje projektov in računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJA: Logika **Znesek ročnega zadrževanja** se ne ujema z logiko **Samodejni znesek zadrževanja** v predlogu računa za projektno pogodbo. |
| Upravljanje projektov in računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ko je zadrževanje dobavitelja sproščeno, ima knjiženje kupona nepravilne dodatne vrstice. |
| Upravljanje projektov in računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Ko je polje **Datum računa** na strani **Ustvarjanje predloga računa** spremenjeno, lahko pride do naslednje napake: »Sklic predmeta ni nastavljen na primerek predmeta.« |
| Upravljanje projektov in računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Napaka se pojavi, ko poskušate odobriti časovni list iz poteka dela **TSLine**, za soboto in nedeljo pa obstaja pravilnik o časovnem listu. |
| Upravljanje projektov in računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta elementa projekta začetnega stanja je izključena iz **Povzetkov transakcij predloga računa**, ko se izračuna vsota računa za predlog računa. |
| Upravljanje projektov in računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Če je strošek porabe na proizvodnem naročilu projekta 0 (nič), pride do naslednje napake, ko poskušate oceniti: »Poskus delitve z ničlo.« |
| Upravljanje projektov in računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilna aplikacija Project Timesheet za Android se preneha odzivati. Težava je povezana z **TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektov in računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Dnevnik integracije aplikacije Project Operations ne uspe, ko ga knjižite, ker računu manjkajo razsežnosti. Vendar pa račun, ki mu manjkajo razsežnosti, ni račun, v katerega knjižite. |
| Upravljanje projektov in računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filter **ToDate** pri iskanju ni počiščen, ko je odstranjen iz pogovornega okna **Izberi** na strani **Stroški knjiženja**. |
| Upravljanje projektov in računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Ponastavitev vse porazdelitve** ne uspe in prikaže napako za časovne liste, ustvarjene za projekt vrste **Samo čas**. |
| Upravljanje projektov in računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Zavihka **Projekt** ni mogoče urejati na čakajočem računu dobavitelja, ko je kategorija nabave dodeljena elementu. |
| Upravljanje projektov in računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Podokno za krmarjenje manjka, če niste prijavljeni v aplikacijo Project Operations Dataverse. |
| Upravljanje projektov in računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pri medpodjetnih transakcijah prilagajanja projektov pride do težave v ciljnem podjetju. |
| Upravljanje projektov in računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Potrjene cene za projekt izračunajo napačno količino in lastno ceno, če je bila naročilnica obdelana z možnostjo **Postopek za naročilnice ob koncu leta** v glavni knjigi. |
| Upravljanje projektov in računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ko je naročilo v proizvodnji za projekt, ki ima naročila kakovosti, označeno kot dokončano, se pojavi naslednja napaka: »Nobena virtualna transakcija ni označena s transakcijo zaloge«. |
| Upravljanje projektov in računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Ko je račun za obveznosti, ki temelji na projektu, knjižen, se pojavi naslednja napaka: »Oštevilčeno besedilo Projekt – cena – element ne obstaja.« |
| Upravljanje projektov in računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Če ročno obračunate prihodke, se posredni stroški podvojijo. |
| Upravljanje projektov in računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Obračunavanje prihodkov in knjiženje WIP ne ustvarja transakcij. |
| Upravljanje projektov in računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija čakajoče cene ne uspe za postavko standardnega stroška, ko za projekt obstaja prejeta naročilnica. |
| Upravljanje projektov in računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrnjena vrednost PVT iz knjiženja računa se razlikuje od prvotno knjižene vrednosti PVT iz časovnega vnosa. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Pri knjiženju s prihodki, zaračunanimi za projekt, v uporabljenih primerih zadržanja, kjer stanja transakcij kuponov niso pravilna, prihaja do težave. |
| Upravljanje projektov in računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Ustvarjanje ocene po knjiženju predloga računa blokira uvoz vrstic popravkov v aplikaciji Project Operations. |
| Upravljanje projektov in računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Spreminjanje popolnoma zaračunanega zapisa mejnika ne bi smelo biti mogoče. |
| Upravljanje projektov in računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Pri uporabi samodejnih zaračunavanj medpodjetnega računa stranke za časovni list ni mogoče knjižiti in prikaže se sporočilo o napaki. |
| Upravljanje projektov in računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Naslov podprojekta ni pravilno posodobljen. |
| Upravljanje projektov in računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Lastne cene za zahteve elementa se posodobijo z nabavno ceno za konsolidirane naročilnice. |
| Upravljanje projektov in računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Knjižena cena ni pravilna, potem ko je nabavna cena posodobljena, parameter **Aktivacija upravljanja sprememb** pa je omogočen. |
| Pot in stroški | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Vse stroške uporabnika lahko vidite, ko poiščete kategorijo v mobilni aplikaciji za upravljanje stroškov. |
| Pot in stroški | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepravilni zneski za transakcije dobavitelja in prometnega davka, ki so knjiženi iz stroška, ki je bil ustvarjen iz transakcije kreditne kartice. |
| Pot in stroški | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Ko osvežite strani s poročilom o stroških, se prikaže nepomembno opozorilno sporočilo. |
| Pot in stroški | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Napačen vmesni odobritelj se uporabi, ko izbrišete vmesnega odobritelja in ga nato znova predložite skozi potek dela. |
| Pot in stroški | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pri knjiženju pride do napake, povezane z nastavitvijo prevožene razdalje. |
| Pot in stroški | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Porazdelitev ne posodobi pravne entitete, ko je nepovezana transakcija ponovno dodana v poročilo o stroških za medpodjetne stroške. |

### <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije za finance in postopke glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prav tako se lahko prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si s pomočjo orodja za iskanje težav ogledate načrtovane regulativne posodobitve. Iskanje težav omogoča iskanje po državi ali regiji, vrsti funkcije in izdaji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
