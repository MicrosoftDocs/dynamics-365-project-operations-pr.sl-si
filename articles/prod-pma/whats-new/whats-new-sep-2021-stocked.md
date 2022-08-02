---
title: Kaj je novega ali spremenjenega v Project Operations, september 2021 za scenarije, ki temeljijo na zalogi/produkciji
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations septembra 2021 za scenarije, ki temeljijo na zalogi/produkciji.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029872"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Kaj je novega ali spremenjenega v Project Operations, september 2021 za scenarije, ki temeljijo na zalogi/produkciji

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno vodenje in računovodstvo v Dynamics 365 Finance okolju različica 10.0.21
 
## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
|---|---|---|
| Upravljanje projektov in računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Če ima vloga Vodja nabave dostop do ene pravne osebe, dobi tudi dostop do vseh projektov v vseh pravnih osebah. |
| Upravljanje projektov in računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Težava pri zaokroževanju davka na dodano vrednost (DDV) se pojavi, ko se dobropis poravna glede na prvotni projektni račun. |
| Upravljanje projektov in računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Za preverjanje proračuna uporabite nadomestni proračun projekta. |
| Upravljanje projektov in računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | The **Prodajna cena uro** cenovna skupina ni izračunana na strukturi razčlenitve dela za ponudbe projektov. |
| Upravljanje projektov in računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Izločitev ocene ne uspe, ko **Omogoči valuto projektne pogodbe za izračun ocene** funkcija je omogočena. |
| Upravljanje projektov in računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija prometnega davka po količini se doda znesku prodajne cene, ko se davek na uporabo uporabi v skupini prometnega davka v dnevniku stroškov projekta. |
| Upravljanje projektov in računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Pogojni davek ni pravilno izračunan za zadnje plačilo, ko se za račune naročilnic uporabita zadržanje prodajalca in predplačilo. |
| Upravljanje projektov in računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Sledenje prilagoditve ne deluje za dnevnike začetnih bilanc. |
| Upravljanje projektov in računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Razporeditev proračuna projekta po obdobjih** je razdeljen na vsa proračunska obdobja. Ko je dodelitev predložena, se zapis ne počisti. |
| Upravljanje projektov in računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Knjižbe v glavni knjigi v teku (WIP) imajo nepravilen znesek. |
| Upravljanje projektov in računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobritev dnevnika projektnih ur ne deluje. |
| Upravljanje projektov in računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cena prilagoditve projekta ni posodobljena s posrednimi stroški, ko omejitev financiranja ni označena. |
| Upravljanje projektov in računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Zahteve po artiklu ni mogoče ustvariti, ko je glava tabele Prodaja fakturirana in je podporno naročilo za obstoječe vrstice dokončano. |
| Upravljanje projektov in računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Znesek zadrževanja za pravilo zaračunavanja, ki ima mejnik za drug projekt, ni objavljen v ustreznem ID-ju projekta, ki je bil izbran za mejnik. Namesto tega je objavljen s prvim projektom. |
| Upravljanje projektov in računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Ko izberete **Nabor finančnih dimenzij** na predlogu računa se pojavi naslednja napaka: »Ni mogoče uvesti predmeta tipa 'Dynamics.AX .Application.FormIntControl', da vnesete 'Dynamics.AX .Application.FormStringControl'." |
| Upravljanje projektov in računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | The **Projektni račun** poročilo preskakuje vrstice. |
| Upravljanje projektov in računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Pri izračunu nadzora stroškov za investicijski projekt pride do napake. |
| Upravljanje projektov in računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | The **ProjTable:: InitFromCustTable – canDeletePostalAddress** metoda povzroča težave z zmogljivostjo. |
| Upravljanje projektov in računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Sporočilo o napaki mora biti jasnejše od »Nepričakovana napaka«. |
| Upravljanje projektov in računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Paketno opravilo knjiženja računa Project obdela in objavi predlog računa, tudi če vrstice računa niso bile ustvarjene. |
| Upravljanje projektov in računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Težava z zaokroževanjem se pojavi, ko je konfiguracijski ključ licence javnega sektorja izklopljen. Napačen strošek ali prodajna cena se ustvari v urah časovnega lista za pogodbe, ki imajo več ustanovnih virov. |
| Upravljanje projektov in računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cena projekta na fakturiranem naročilu za projekt je nepravilno izračunana, ko je model prodajne cene **Razmerje prispevka**. |
| Upravljanje projektov in računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem pri izračunu efektivne stopnje dela za zaposlenega ne upošteva vmesnih aktivnih dni. |
| Upravljanje projektov in računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Na medpodjetniškem časovnem listu pride do napake pri knjiženju zaradi naslednje napake pri preverjanju: »Noben trgovinski partner ni konfiguriran za pravno osebo«. |
| Upravljanje projektov in računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz naročilnice, ki ima kategorijo stroškov, ni pridobljen na objavljenem seznamu projektnih transakcij. |
| Upravljanje projektov in računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Prišlo je do nepravilne pretvorbe v dnevnikih postavk, ki so objavljene v projektu. |
| Upravljanje projektov in računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Naročilo lahko potrdite tudi, če je bila omejitev financiranja presežena. |
| Upravljanje projektov in računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | The **Popravek/Preklic računa** razdelek na računu s prostim besedilom izgine, ko je izbran ID projekta. |
| Upravljanje projektov in računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Ko je predlog računa za projekt objavljen iz projektnega prodajnega naročila, ki vključuje založen artikel, pride do težav z zmogljivostjo. |
| Upravljanje projektov in računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Računov za nakupe projekta ni mogoče objaviti, ker se pojavi naslednja napaka: »Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine je bila nepravilno poklicana.« |
| Upravljanje projektov in računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Posodobitev ustvarjanja paketnih opravil za oceno projekta za podporo izvajanja več podopravil. |
| Upravljanje projektov in računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Stanja časovnega lista ni mogoče posodobiti na **Osnutek**, če se potek dela zatakne pri stanju **Preklicano**. |
| Upravljanje projektov in računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Zadržani zneski niso izračunani v predlogu računa za dobropis, če obstaja več vrstic. |
| Upravljanje projektov in računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Ko poskušate spremeniti znesek na ustvarjenem računu iz naročila, se pojavi naslednja napaka: »Transakcije na bonu niso uravnotežene glede na XX/XX/XXXX. (računovodska valuta: 0,00 – valuta za poročanje: 0,01).« |
| Upravljanje projektov in računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Pri objavljanju predloga računa za projekt v paketnem načinu pride do težave z zmogljivostjo zaradi združevanja s **GeneralJournalAccountEntry**. |
| Upravljanje projektov in računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Pri objavi časovnice pride do težav z zmogljivostjo. |
| Upravljanje projektov in računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarhija ocen stroškov strukture razčlenitve dela ni pravilno poravnana po razširitvi vseh nalog ali po ročni razširitvi posamezne naloge. |
| Upravljanje projektov in računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excelove predloge projektne ponudbe ni mogoče dodati v **Odpri v Excelu** meni. |
| Upravljanje projektov in računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Številka oproščene davka za pravno osebo ni navedena na natisnjenem računu projekta. |
| Upravljanje projektov in računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Ko je projekt prilagojen glede na kreditne linije, se v napaki enote zaloge ne posodobi noben finančni podatek. |
| Upravljanje projektov in računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Ko uporabite KB 461935, ne morete objaviti ocen, če preklopite na neprekinjena številska zaporedja. |
| Upravljanje projektov in računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** povzroča mobilno aplikacijo Project timesheet za Android da se nehaš odzivati. |
| Upravljanje projektov in računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Razveljavljena vrednost WIP iz knjižbe računa se razlikuje od prvotno objavljene vrednosti WIP iz časovnega vnosa. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | V primerih uporabljenega zadrževalnika se transakcije na vavčerju ne izravnajo, ko se knjiži fakturirani prihodek za projekt. |
| Upravljanje projektov in računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Ko **Izboljšanje zmogljivosti razporejanja virov projekta** funkcija omogočena, so decimalne vrednosti nepravilno zaokrožene za razpoložljivost in zmogljivost vira. |
| Upravljanje projektov in računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Ko **Ustvarite ocene projekta z uporabo več paketnih opravil** funkcija omogočena, ustvarjanje ocen v paketu, ki ima več podopravil, deluje samo za trenutno obdobje. |
| Pot in stroški | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Politika zahtevkov za potovanje je prezrta in potek dela je odobren brez napak. |
| Pot in stroški | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikacija Mobile Expense ne shrani naslednjih informacij v vrstico stroškov:</p><ul><li>ID projekta</li><li>Ali je strošek zaračunljiv</li><li>Številka dejavnosti</li></ul> |
| Pot in stroški | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | The **Priloženi računi** polje je nastavljeno na **ja** tudi če vrstici stroškov ni priložen noben račun. |
| Pot in stroški | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Ko kategorijo stroškov spremenite v, pride do napake **Osebno**. |
| Pot in stroški | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Ne morete priložiti potrdila in urediti stroškov staršev, potem ko je transakcija s kreditno kartico razdeljena na osebne stroške. |
| Pot in stroški | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Politika stroškov za transakcije med podjetji, ki imajo ID projekta, ne deluje pravilno. |
| Pot in stroški | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informacije o objavljenem datumu manjkajo za objavljena poročila o stroških. |
| Pot in stroški | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | V mobilni aplikaciji Expense so težave s plačilnim sredstvom. |
| Pot in stroški | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Potni zahtevek, ki je ustvarjen za enega delavca, se lahko uporabi za poročilo o stroških drugega delavca pred datumom prenosa. |
| Pot in stroški | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Ko ustvarite odhodek, spremembe vrednosti finančne razsežnosti niso pravilno posodobljene na ravni distribucije računovodstva v **Upravljanje s stroški** delovni prostor. |
| Pot in stroški | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stanje odobritve vrstice glavnega odhodka ni sinhronizirano s statusom odobritve poteka dela razčlenjene vrstice. |
| Pot in stroški | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Napaka se pojavi, če objavite poročilo o stroških in je izterjava davka omogočena. |
| Pot in stroški | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Pooblaščenec ne more izbrisati dokumentov o stroških za odpuščenega zaposlenega. |
| Pot in stroški | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje stroškovne vrstice traja dlje, kot je bilo pričakovano, in vpliva na uspešnost. |
| Pot in stroški | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** povzroči osirotelost **TaxUncommitted** zapis, saj le **SourceDocumentLine** se izbriše. |
| Pot in stroški | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne v čast **trvExpTrans.ReferenceDataAreaId** da ustvarite novo zaporedje številk. |

## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije za finance in poslovanje glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prijavite se lahko tudi v Microsoft Dynamics Lifecycle Services (LCS) in uporabite orodje za iskanje težav, da si ogledate načrtovane regulativne posodobitve. Iskanje po težavah vam omogoča iskanje po državi ali regiji, vrsti funkcije in izdaji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
