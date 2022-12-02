---
title: Novosti ali spremembe v storitvi Project Operations, september 2021, za scenarije, ki temeljijo na zalogi/proizvodnji
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v septembrski izdaji (2021) aplikacije Project Operations za primere uporabe z naročili na zalogi/v proizvodnji.
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
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novosti ali spremembe v storitvi Project Operations, september 2021, za scenarije, ki temeljijo na zalogi/proizvodnji

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.21
 
## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
|---|---|---|
| Upravljanje projektov in računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Če ima vloga vodje nabave dostop do ene pravne entitete, pridobi tudi dostop do vseh projektov v vseh pravnih entitetah. |
| Upravljanje projektov in računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Težava pri zaokroževanju davka na dodano vrednost (DDV) se pojavi, ko se dobropis poravna glede na prvotni račun projekta. |
| Upravljanje projektov in računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Za preverjanje veljavnosti proračuna uporabite nadomestni proračun projekta. |
| Upravljanje projektov in računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Cenovna skupina **Prodajna cena za uro** ni izračunana na strukturirani razčlenitvi dela za ponudbe projektov. |
| Upravljanje projektov in računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Odstranjevanje ocene ne uspe, ko je omogočena funkcija **Omogoči valuto projektne pogodbe za izračun ocene**. |
| Upravljanje projektov in računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija prometnega davka po količini se doda znesku prodajne cene, ko se davek na uporabo uporabi v skupini prometnega davka v dnevniku stroškov projekta. |
| Upravljanje projektov in računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Pogojni davek ni izračunan pravilno za zadnje plačilo, ko je zadržanje dobavitelja in predplačilo uporabljeno za račune po naročilnici. |
| Upravljanje projektov in računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Sledenje prilagoditvi ne deluje za dnevnike začetnega salda. |
| Upravljanje projektov in računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Dodeljevanje revizije proračuna projekta po obdobjih** je razdeljeno na vsa proračunska obdobja. Ko je dodelitev predložena, se zapis ne počisti. |
| Upravljanje projektov in računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Knjiženja dela v teku (WIP) v glavno knjigo imajo nepravilni znesek. |
| Upravljanje projektov in računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobritev dnevnika projektnih ur ne deluje. |
| Upravljanje projektov in računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cena prilagoditve projekta ni posodobljena s posrednimi stroški, ko omejitev financiranja ni označena. |
| Upravljanje projektov in računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Zahteve po izdelku ni mogoče ustvariti, ko je glava tabele Prodaja fakturirana in je podporna naročilnica za obstoječe vrstice dokončana. |
| Upravljanje projektov in računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Znesek zadrževanja za pravilo obračunavanja, ki ima mejnik za drug projekt, ni knjižen v ustreznem ID-ju projekta, ki je bil izbran za mejnik. Namesto tega je knjižen s prvim projektom. |
| Upravljanje projektov in računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Ko na predlogu računa izberete možnost **Komplet finančnih razsežnosti**, se pojavi naslednja napaka: »Ni mogoče uvesti predmeta vrste 'Dynamics.AX.Application.FormIntControl' za vnos 'Dynamics.AX.Application.FormStringControl'.« |
| Upravljanje projektov in računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Poročilo **Račun projekta** preskakuje vrstice. |
| Upravljanje projektov in računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Pri izračunu nadzora stroškov za investicijski projekt pride do napake. |
| Upravljanje projektov in računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Način **ProjTable::InitFromCustTable – canDeletePostalAddress** povzroča težave z učinkovitostjo delovanja. |
| Upravljanje projektov in računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Sporočilo o napaki mora biti jasnejše kot »Nepričakovana napaka«. |
| Upravljanje projektov in računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Paket knjiženj računov za projekt obdeluje in knjiži predlog računa, tudi če vrstice računa niso bile ustvarjene. |
| Upravljanje projektov in računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Težava z zaokroževanjem se pojavi, ko je ključ konfiguracije licence javnega sektorja izklopljen. Napačen strošek ali prodajna cena se ustvari v urah časovnega lista za pogodbe, ki imajo več virov financiranja. |
| Upravljanje projektov in računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cena projekta na fakturirani naročilnici za projekt je nepravilno izračunana, ko je model prodajne cene **Razmerje prispevka**. |
| Upravljanje projektov in računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem pri izračunu veljavne stopnje dela za zaposlenega ne upošteva vmesnih dejavnih dni. |
| Upravljanje projektov in računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Na medpodjetnem časovnem listu pride napake pri knjiženju zaradi naslednje napake pri preverjanju veljavnosti: »Noben trgovski partner ni konfiguriran za pravno entiteto«. |
| Upravljanje projektov in računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz naročilnice, ki ima kategorijo stroškov, ni pridobljen na knjiženem seznamu transakcij projekta. |
| Upravljanje projektov in računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Prišlo je do nepravilne pretvorbe v dnevnikih postavk, ki so knjiženi v projektu. |
| Upravljanje projektov in računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Naročilnico lahko potrdite tudi, če je bila omejitev financiranja presežena. |
| Upravljanje projektov in računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Razdelek **Popravek/preklic računa** na računu s prostim besedilom izgine, ko je izbran ID projekta. |
| Upravljanje projektov in računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Ko je predlog računa za projekt knjižen iz prodajnega naročila projekta, ki vključuje založen izdelek, pride do težav z učinkovitostjo delovanja. |
| Upravljanje projektov in računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Računov projekta ni mogoče knjižiti, ker se pojavi naslednja napaka: »Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine je bila nepravilno klicana.« |
| Upravljanje projektov in računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Posodobite na ustvarjanje paketnih opravil ocene projekta za podporo izvajanja več podopravil. |
| Upravljanje projektov in računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Stanja časovnega lista ni mogoče posodobiti na **Osnutek**, ko se potek dela zaustavi v stanju **Preklicano**. |
| Upravljanje projektov in računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Zadržani zneski niso izračunani v predlogu računa za dobropis, če obstaja več vrstic. |
| Upravljanje projektov in računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Ko poskušate spremeniti znesek na ustvarjenem računu iz naročilnice, se pojavi naslednja napaka: »Transakcije na kuponu niso uravnotežene glede na XX/XX/XXXX. (računovodska valuta: 0,00 – valuta za poročanje: 0,01).« |
| Upravljanje projektov in računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Pri knjiženju predloga računa za projekt v paketnem načinu pride do težave z učinkovitostjo delovanja zaradi združevanja z vrednostjo **GeneralJournalAccountEntry**. |
| Upravljanje projektov in računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Pri knjiženju časovnega lista pride do težav z učinkovitostjo delovanja. |
| Upravljanje projektov in računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarhija ocen stroškov strukturirane razčlenitve dela ni pravilno poravnana po razširitvi vseh opravil ali po ročni razširitvi enega samega opravila. |
| Upravljanje projektov in računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excelove predloge projektne ponudbe ni mogoče dodati v meni **Odpri v Excelu**. |
| Upravljanje projektov in računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Številka upravičenca do oprostitve plačila davkov za pravno entiteto ni vključena na tiskanem računu za projekt. |
| Upravljanje projektov in računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Napaka »V enoti zaloge se ne posodabljajo nobeni finančni podatki«, ko je projekt prilagojen v povezavi z vrsticami dobroimetja. |
| Upravljanje projektov in računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Ko uporabite KB 461935, ne morete knjižiti ocen, če preklopite na neprekinjena številska zaporedja. |
| Upravljanje projektov in računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** povzroči, da se mobilna Project timesheet za Android preneha odzivati. |
| Upravljanje projektov in računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrnjena vrednost PVT iz knjiženja računa se razlikuje od prvotno knjižene vrednosti PVT iz časovnega vnosa. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | V uporabljenih primerih zadržanja transakcije kuponov niso pravilne pri knjiženju prihodkov, zaračunanih za projekt. |
| Upravljanje projektov in računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Ko je omogočena funkcija **Izboljšanje učinkovitosti delovanja razporejanja virov projekta**, so decimalne vrednosti nepravilno zaokrožene za razpoložljivost in zmogljivost vira. |
| Upravljanje projektov in računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Ko je omogočena funkcija **Ustvarjanje ocen projekta z več paketnimi opravili**, ustvarjanje ocen v paketu, ki ima več podopravil, deluje samo za trenutno obdobje. |
| Pot in stroški | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Pravilnik zahtev za pot se prezre in se odobri potek dela brez napak. |
| Pot in stroški | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobilna aplikacija za upravljanje stroškov ne shrani naslednjih informacij v vrstico stroškov:</p><ul><li>ID projekta</li><li>ali je strošek obračunljiv</li><li>številka dejavnosti opravila</li></ul> |
| Pot in stroški | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Polje **Priložena potrdila** je nastavljeno na **Da**, tudi če vrstici stroška ni priloženo potrdilo. |
| Pot in stroški | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Prikaže se napaka, ko spremenite kategorijo stroška na **Osebno**. |
| Pot in stroški | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Ne morete priložiti potrdila ali urejati nadrejenega stroška, potem ko je transakcija kreditne kartice razdeljena na osebni strošek. |
| Pot in stroški | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Pravilnik o stroških za transakcije med podjetji z ID-jem projekta ne deluje pravilno. |
| Pot in stroški | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informacije o datumu knjiženja manjkajo za knjižena poročila o stroških. |
| Pot in stroški | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Obstajajo težave z načinom plačila v mobilni aplikaciji za upravljanje stroškov. |
| Pot in stroški | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Zahtevo za pot, ustvarjeno za enega delavca, je mogoče uporabiti za poročilo o stroških drugega delavca pred datumom pooblastitve. |
| Pot in stroški | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Ko ustvarite strošek, se spreminjanje vrednosti finančnih razsežnosti ne posodablja pravilno na ravni računovodskega porazdeljevanja v delovnem prostoru **Upravljanje stroškov**. |
| Pot in stroški | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stanje odobritve glavne vrstice stroška se ne sinhronizira s stanjem odobritve poteka dela razčlenjene vrstice. |
| Pot in stroški | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Napaka se pojavi, če knjižite poročilo o stroških in je izterjava davka omogočena. |
| Pot in stroški | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Pooblaščenec ne more izbrisati dokumentov o stroških za odpuščenega zaposlenega. |
| Pot in stroški | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje vrstice stroškov traja dlje časa, kot je bilo pričakovano, in vpliva na učinkovitost delovanja. |
| Pot in stroški | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** povzroči osiroteli zapis **TaxUncommitted**, ker je izbrisana samo možnost **SourceDocumentLine**. |
| Pot in stroški | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **Posodobitev izdaje DB72_Expense.updateTrvExpTransProjTransId()** ne omogoča elementu **trvExpTrans.ReferenceDataAreaId**, da bi ustvaril novo zaporedje števil. |

## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije za finance in postopke glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prav tako se lahko prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si s pomočjo orodja za iskanje težav ogledate načrtovane regulativne posodobitve. Iskanje težav omogoča iskanje po državi ali regiji, vrsti funkcije in izdaji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
