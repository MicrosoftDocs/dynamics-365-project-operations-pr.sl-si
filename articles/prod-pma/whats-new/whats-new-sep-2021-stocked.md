---
title: Kaj je novega ali spremenjenega v Project Operations, september 2021 za scenarije, ki temeljijo na zalogi/produkciji
description: Ta tema ponuja informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations septembra 2021 za scenarije, ki temeljijo na zalogi/produkciji.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815834"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Kaj je novega ali spremenjenega v Project Operations, september 2021 za scenarije, ki temeljijo na zalogi/produkciji

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta tema velja za naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.21
 
## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
|---|---|---|
| Upravljanje projektov in računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Če ima vloga vodje nabave dostop do ene pravne osebe, pridobi tudi dostop do vseh projektov v vseh pravnih osebah. |
| Upravljanje projektov in računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Težava pri zaokroževanju davka na dodano vrednost (DDV) se pojavi, ko se dobropis poravna na izvirnem računu projekta. |
| Upravljanje projektov in računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Za preverjanje proračuna uporabite nadomestni proračun projekta. |
| Upravljanje projektov in računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | The **Prodajna cena ura** cenovna skupina ni izračunana na strukturi razčlenitve dela za projektne ponudbe. |
| Upravljanje projektov in računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Izločanje ocene ne uspe, ko **Omogoči valuto projektne pogodbe za izračun ocene** funkcija je omogočena. |
| Upravljanje projektov in računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija prometnega davka po količini se doda znesku prodajne cene, ko je davek na uporabo uporabljen v skupini prometnega davka v dnevniku stroškov projekta. |
| Upravljanje projektov in računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Pogojni davek ni pravilno izračunan za zadnje plačilo, ko se za račune za naročilo uporabljata zadržanje prodajalca in predplačilo. |
| Upravljanje projektov in računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Sled prilagoditve ne deluje za dnevnike začetne bilance. |
| Upravljanje projektov in računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Razporeditev rebalansa proračuna projekta po obdobju** je razdeljen na vsa proračunska obdobja. Ko je dodelitev predložena, se zapis ne izbriše. |
| Upravljanje projektov in računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Knjižitve nedokončane proizvodnje (WIP) v glavni knjigi imajo napačen znesek. |
| Upravljanje projektov in računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobritev dnevnika projektnih ur ne deluje. |
| Upravljanje projektov in računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cena prilagoditve projekta ni posodobljena s posrednimi stroški, ko je omejitev financiranja neoznačena. |
| Upravljanje projektov in računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Zahteve po artiklu ni mogoče ustvariti, ko je glava tabele prodaje zaračunana in je podporno naročilnico za obstoječe vrstice dokončano. |
| Upravljanje projektov in računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Znesek hrambe za pravilo za obračun, ki ima mejnik za drug projekt, ni objavljen v ustreznem ID-ju projekta, ki je bil izbran za mejnik. Namesto tega je objavljen s prvim projektom. |
| Upravljanje projektov in računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Ko izberete **Nabor finančnih dimenzij** pri predlogu računa se pojavi naslednja napaka: "Ni mogoče prenesti predmeta tipa 'Dynamics.AX.Application.FormIntControl' v tip 'Dynamics.AX.Application.FormStringControl'." |
| Upravljanje projektov in računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | The **Projektni račun** poročilo preskoči vrstice. |
| Upravljanje projektov in računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Pri izračunu nadzora stroškov za investicijski projekt pride do napake. |
| Upravljanje projektov in računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | The **ProjTable::InitFromCustTable - canDeletePostalAddress** metoda povzroča težave z zmogljivostjo. |
| Upravljanje projektov in računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Sporočilo o napaki mora biti jasnejše od »Nepričakovana napaka«. |
| Upravljanje projektov in računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Projektni račun, ki knjiži paketno opravilo, obdeluje in knjiži predlog računa, tudi če vrstice računa niso bile ustvarjene. |
| Upravljanje projektov in računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Do težave z zaokroževanjem pride, ko je konfiguracijski ključ licence javnega sektorja izklopljen. Napačna cena ali prodajna cena je ustvarjena na urniku ur za pogodbe, ki imajo več ustanovitvenih virov. |
| Upravljanje projektov in računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cena projekta na fakturiranem naročilnici projekta je napačno izračunana, ko je model prodajne cene **Razmerje prispevka**. |
| Upravljanje projektov in računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem ne upošteva vmesnih aktivnih dni, ko izračuna efektivno stopnjo dela za zaposlenega. |
| Upravljanje projektov in računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Na medpodjetniškem časovnem listu pride do napake pri knjiženju zaradi naslednje napake pri validaciji: "Noben trgovski partner ni konfiguriran za pravno osebo." |
| Upravljanje projektov in računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz naročilnice, ki ima kategorijo odhodkov, ni pridobljen na objavljeni seznam transakcij projekta. |
| Upravljanje projektov in računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Obstaja napačna pretvorba v dnevnikih predmetov, ki so objavljeni v projektu. |
| Upravljanje projektov in računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Naročilo lahko potrdite, tudi če je bila omejitev financiranja presežena. |
| Upravljanje projektov in računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | The **Popravek/Preklic računa** razdelek na računu z brezplačnim besedilom izgine, ko izberete ID projekta. |
| Upravljanje projektov in računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Težave z zmogljivostjo se pojavijo, ko je predlog računa projekta objavljen iz projektnega prodajnega naloga, ki vključuje založeno postavko. |
| Upravljanje projektov in računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Računov za nakup projekta ni mogoče knjižiti, ker se pojavi naslednja napaka: "Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine je bila napačno poklicana." |
| Upravljanje projektov in računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Posodobitev ustvarjanja paketnih opravil ocene projekta za podporo izvajanju več podopravil. |
| Upravljanje projektov in računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Stanja urnika ni mogoče posodobiti na **Osnutek**, ko potek dela obstane v stanju **Prekinjeno**. |
| Upravljanje projektov in računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Zadržani zneski niso izračunani v predlogu računa za dobropis, če obstaja več vrstic. |
| Upravljanje projektov in računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Ko poskušate spremeniti znesek na ustvarjenem računu iz naročilnice, se pojavi naslednja napaka: »Transakcije na kuponu niso uravnotežene po XX/XX/XXXX. (računovodska valuta: 0,00 – valuta za poročanje: 0,01).« |
| Upravljanje projektov in računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Prišlo je do težave z zmogljivostjo, ko je predlog računa projekta objavljen v paketnem načinu zaradi združitve z **GeneralJournalAccountEntry**. |
| Upravljanje projektov in računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Pri objavi časovnega lista pride do težav z zmogljivostjo. |
| Upravljanje projektov in računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarhija ocen stroškov strukture razčlenitve dela ni pravilno poravnana, ko so vsa opravila razširjena ali ko je posamezno opravilo ročno razširjeno. |
| Upravljanje projektov in računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Predloge za predloge projekta Excel ni mogoče dodati v **Odprite v Excelu** meni. |
| Upravljanje projektov in računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Davčna oproščena številka za pravno osebo ni vključena na natisnjenem računu projekta. |
| Upravljanje projektov in računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | V napaki inventarne enote se finančni podatki ne posodobijo, ko je projekt prilagojen glede na kreditne linije. |
| Upravljanje projektov in računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Ko uporabite KB 461935, ne morete objaviti ocen, če preklopite na neprekinjena številska zaporedja. |
| Upravljanje projektov in računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** povzroči, da se mobilna aplikacija Project timesheet za Android preneha odzivati. |
| Upravljanje projektov in računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Obrnjena vrednost WIP iz knjiženja računa se razlikuje od prvotno knjižene vrednosti WIP iz časovnega vnosa. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | V primerih uporabljenih zadrževalnikov se transakcije na bonu ne uravnotežijo, ko se knjiži fakturirani prihodek za projekt. |
| Upravljanje projektov in računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Ko **Izboljšanje učinkovitosti načrtovanja projektnih virov** je funkcija omogočena, decimalne vrednosti so napačno zaokrožene glede na razpoložljivost in zmogljivost vira. |
| Upravljanje projektov in računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Ko **Ustvarite ocene projekta z uporabo več paketnih nalog** funkcija je omogočena, ustvarjanje ocen v paketu, ki ima več podopravil, deluje samo za trenutno obdobje. |
| Pot in stroški | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Politika potnih zahtev je prezrta in potek dela je odobren brez napak. |
| Pot in stroški | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikacija Mobile Expense ne shrani naslednjih informacij v vrstico stroškov:</p><ul><li>ID projekta</li><li>Ali je strošek plačljiv</li><li>Številka dejavnosti</li></ul> |
| Pot in stroški | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | The **Priloženi računi** polje je nastavljeno na **da** tudi če v vrstico stroškov ni priložen noben račun. |
| Pot in stroški | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Do napake pride, ko spremenite kategorijo stroškov v **Osebno**. |
| Pot in stroški | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Po tem, ko je transakcija s kreditno kartico razdeljena na osebne stroške, ne morete priložiti potrdila in urediti nadrejenih stroškov. |
| Pot in stroški | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Politika stroškov za transakcije med podjetji, ki imajo ID projekta, ne deluje pravilno. |
| Pot in stroški | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Za knjižena poročila o stroških manjkajo podatki o datumu knjiženja. |
| Pot in stroški | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | V mobilni aplikaciji Expense so težave z načinom plačila. |
| Pot in stroški | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Potni zahtevek, ki je ustvarjen za enega delavca, se lahko uporabi za poročilo o stroških drugega delavca pred datumom pooblastila. |
| Pot in stroški | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Ko ustvarite odhodek, spremembe vrednosti finančne razsežnosti niso pravilno posodobljene na ravni računovodske distribucije v **Upravljanje odhodkov** delovni prostor. |
| Pot in stroški | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Stanje odobritve glavne vrstice stroškov ni sinhronizirano s stanjem odobritve delovnega toka razčlenjene vrstice. |
| Pot in stroški | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Do napake pride, če objavite poročilo o stroških in je izterjava davka omogočena. |
| Pot in stroški | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Pooblaščenec ne more izbrisati dokumentov o stroških za odpuščenega zaposlenega. |
| Pot in stroški | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje odhodkovne vrstice traja dlje od pričakovanega in vpliva na uspešnost. |
| Pot in stroški | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** povzroči siroto **TaxUncommitted** zapis, ker samo **Izvorna vrstica dokumenta** je izbrisan. |
| Pot in stroški | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne spoštuje **trvExpTrans.ReferenceDataAreaId** da ustvarite novo številsko zaporedje. |

## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije Finance in Operations glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prijavite se lahko tudi v Microsoft Dynamics storitve življenjskega cikla (LCS) in uporabite orodje za iskanje težav za ogled načrtovanih posodobitev predpisov. Iskanje težav vam omogoča iskanje po državi ali regiji, vrsti funkcije in izdaji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
