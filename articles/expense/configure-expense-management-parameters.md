---
title: Konfiguriranje parametrov upravljanja stroškov
description: V tej temi so opisani parametri, ki nadzorujejo splošno vedenje pri upravljanju stroškov.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1cabb0be624f7f6c12761e4fb6d5a095396a5940a37616bb3a304798e1f97808
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007796"
---
# <a name="configure-expense-management-parameters"></a>Konfiguriranje parametrov upravljanja stroškov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

V tej temi so opisani parametri, ki nadzorujejo splošno vedenje pri upravljanju stroškov.

## <a name="general"></a>Splošno

| Polje                                                    | Opis |
|----------------------------------------------------------|-------------|
| Standardna stopnja kilometrine                                 | Vnesite stopnjo nadomestila za stroške prevoženih kilometrov. Stopnja se pomnoži s kilometrino, vneseno za stroške, da se izračuna znesek, ki je povrnjen za potne stroške. |
| Potrjevanje namena stroškov                                 | To možnost vklopite, če želite uporabnike pri ustvarjanju poročil o stroških omejiti na obstoječi nabor vrednosti, ki je konfiguriran v polju **Poročilo o namenu stroškov**. |
| Plačnik osebnih stroškov                                | Izberite, kdo je odgovoren za plačilo zneskov transakcij s kreditno kartico, ki so kategorizirani kot osebni. |
| Prikaz celotnega poročila o stroških pri ogledu podrobnosti               | Izberite to možnost, če želite prikazati vse stroške v poročilu o stroških, ko si ogledate podrobnosti izvirnega dokumenta za določen kupon, ki je bil ustvarjen ob objavi poročila o stroških. |
| Predhodna pooblastitev poti je obvezna                 | Izberite to možnost, če želite, da se zahtevek za pot predloži in odobri, preden lahko zaposleni predloži poročilo o stroških. |
| Dovoljenje za urejanje porazdelitev pred objavo            | Izberite, ali se lahko porazdelitve v poročilu o stroških ureja, preden je objavljeno. |
| Ocena pravilnikov za upravljanje stroškov                     | Izberite, kdaj se ocenjujejo stroški, da ugotovite, ali je bil kršen pravilnik o stroških. Stroške je mogoče ovrednotiti glede kršitev, ko je vnos stroškov vnesen in shranjen ali ko je strošek poslan v odobritev. Pravila pravilnika o zahtevanih računih bodo ovrednotena, ko se shrani vrstica stroškov. |
| Dovoljenje za vrstice stroškov med podjetji                         | Izberite, ali je mogoče v poročilo o stroških vpisati stroške za druge pravne osebe. |
| Dovoljenje za urejanje menjalnega tečaja za stroške kreditne kartice | Izberite to možnost, če želite uporabniku omogočiti urejanje menjalnega tečaja za uvožene stroške kreditne kartice. |
| Polja večstopenjske hierarhije za prikaz                  | Izberite, katera polja odobritelja so prikazana, če je vrsta dodelitve poteka dela nastavljena na hierarhijo in je izbor **Hierarhija** nastavljen za uporabo hierarhije odobritve, večstopenjske odobritve stroškov. Ko se za potek dela uporablja večstopenjska hierarhija odobritve, bodo izbrana polja prikazana v poročilu o stroških in jih je mogoče urejati. |
| Vnos številke kreditne kartice zaposlenega                        | Izberite, ali lahko v polje **ID kartice** na strani **Kreditne kartice** za zaposlenega vnesete 15- ali 16-mestno številko. |
| Potrditev namena zahteve za pot                      | To možnost vklopite, če želite uporabnike pri ustvarjanju zahtev za pot omejiti na obstoječi nabor vrednosti, ki je konfiguriran v polju **Poročilo o namenu stroškov**. |

## <a name="financial"></a>Finance

| Polje                                                                                    | Opis |
|------------------------------------------------------------------------------------------|-------------|
| Ime dnevnika za glavno knjigo                                                                | Izberite ime dnevnika za glavno knjigo, v katerem so objavljena odobrena poročila o stroških. |
| Omogočanje izterjave davkov za stroške                                                        | Izberite to možnost, da omogočite izterjavo davka za stroške za upravičene stroške. Te možnosti ni mogoče izbrati, če sta omogočena ameriški prometni davek in davek na uporabo. |
| Takojšnja objava denarnih predujmov                                                           | Izberite to možnost, če želite po zaključku postopka plačila in nakazila objaviti odobreni denarni predujem. Če ta možnost ni izbrana, postopek plačila in nakazila ustvari neobjavljeno splošno temeljnico. |
| Popravljanje datuma knjiženja med objavo                                                   | Izberite to možnost, če želite posodobiti datum knjiženja, ko so objavljeni stroški, če je trenutno obdobje zadržano ali zaprto. Datum knjiženja bo nastavljen na naslednje odprto obdobje. |
| Dovoljenje za združevanje transakcij na podlagi protikonta za stroške, določenega v načinu plačila       | Izberite to možnost, če želite povzeti transakcije stroškov za poročilo o stroških, in sicer na podlagi protikonta za stroške, določenega v načinu plačila za stroške. |
| Davek je vključen                                                                             | Izberite to možnost, če želite privzeto vključiti prometni davek v znesek stroškov. |
| Sprostitev obremenitev glede zaprtja zahtev za pot                                      | Izberite to možnost, če želite sprostiti obremenjena sredstva, ko je zaprta odobrena zahteva za pot. |
| Dovoljenje za oddajo zahteve za pot ob prekoračitvi proračuna za register proračuna in proračun projekta | Izberite to možnost, če želite zaposlenim v odobritev poslati zahtevo za pot, čeprav presegajo dovoljeni proračun, ki je določen v registru proračuna, ali dovoljeni proračun za projekt. |
| Dovoljenje za oddajo poročila o stroških ob prekoračitvi proračuna za register proračuna in proračun projekta     | Izberite to možnost, če želite zaposlenim v odobritev poslati poročila o stroških, čeprav presegajo dovoljeni proračun, ki je določen v registru proračuna, ali dovoljeni proračun za projekt. |
| Dovoljenje za odobritev poročila o stroških ob prekoračitvi proračuna samo za register proračuna                 | Izberite to možnost, če želite, da odobritelji odobrijo poročila o stroških, ki presegajo dovoljeni proračun, določen v registru proračuna. |

## <a name="per-diem"></a>Dnevnica

| Polje                                 | Opis |
|---------------------------------------|-------------|
| Najmanjše število ur za dnevnice            | Vnesite privzeto najmanjše število ur, ki jih mora zaposleni opraviti na dan, da je upravičen do dnevnice za stroške, povezane s potovanjem. Ta vrednost se uporablja kot privzeta vrednost samo za polje **Najmanjše število ur** za stopnje vrednosti dnevnic. |
| Odstotek za obroke                          | Vnesite privzeti odstotek dnevnice za obroke, ki se uporablja prvi in zadnji dan stroškov, povezanih s potovanjem, ko je polje **Izračun znižanja za obrok glede na** nastavljeno na bodisi **Vrsta obroka na dan** ali **Število obrokov na dan**. Delovni dan za prvi in zadnji dan je lahko krajši od običajnega delovnika. Zato se lahko znesek dnevnice za te dni razlikuje od običajnega zneska. Če je odstotek nastavljen na **0** (nič), bodo odbitki za prvi in zadnji dan 0,00. |
| Odstotek za hotele                         | Vnesite privzeti odstotek dnevnice za hotele, ki se uporablja prvi in zadnji dan stroškov, povezanih s potovanjem. Delovni dan za prvi in zadnji dan je lahko krajši od običajnega delovnika. Zato se lahko znesek dnevnice za te dni razlikuje od običajnega zneska. Če je odstotek nastavljen na **0** (nič), bodo odbitki za prvi in zadnji dan 0,00. |
| Drugi odstotki                         | Vnesite privzeti odstotek dnevnice za druge stroške, ki se uporablja prvi in zadnji dan stroškov, povezanih s potovanjem. Delovni dan za prvi in zadnji dan je lahko krajši od običajnega delovnika. Zato se lahko znesek dnevnice za te dni razlikuje od običajnega zneska. Če je odstotek nastavljen na **0** (nič), bodo odbitki za prvi in zadnji dan 0,00. |
| Znižanje odstotka za zajtrk | Vnesite znesek, za katerega se dnevnica zniža za zajtrk. Če na primer zaposleni prejme brezplačen zajtrk, boste morda želeli znesek dnevnice znižati za 10 odstotkov. |
| Znižanje odstotka za kosilo     | Vnesite znesek, za katerega se dnevnica zniža za kosilo. Če na primer zaposleni prejme brezplačno kosilo, boste morda želeli znesek dnevnice znižati za 15 odstotkov. |
| Znižanje odstotka za večerjo    | Vnesite znesek, za katerega se dnevnica zniža za večerjo. Če na primer zaposleni prejme brezplačno večerjo, boste morda želeli znesek dnevnice znižati za 25 odstotkov. |
| Izračun znižanja za obrok glede na           | Določite, kako naj sistem izračuna znižanje dnevnice za obrok tako, da izberete, ali znižanje temelji na vrsti obroka na potovanje oz. na dan ali na podlagi dovoljenega števila obrokov na dan. |
| Zaokroževanje dnevnic                     | Izberite vrsto zaokroževanja, ki se uporablja za stroške dnevnic. Če izberete običajno zaokroževanje, se vsi stroški dnevnic, ki imajo znesek 0,50, zaokrožijo na 1,00, vsi stroški dnevnic, ki imajo znesek, ki je manjši od 0,50, pa zaokrožijo na 0,00. |
| Izračun osnove za dnevnice glede na          | Izberite, ali znesek dnevnice temelji na koledarskem dnevu ali 24-urnem obdobju. |

## <a name="fax-cover-pages"></a>Naslovne strani faksa

| Polje                          | Opis |
|--------------------------------|-------------|
| Navodila                   | Vnesite navodila, ki jih morajo upoštevati zaposleni, ko ustvarjajo naslovno stran za faks, ki se uporablja za pošiljanje računov, povezanih s poročilom o stroških. Če želite vnesti besedilo, ki bo prikazano v skladu z uporabniškim jezikom, izberite **Prevodi**. |
| ID uporabnika (podatki črtnih kod) | Izberite to možnost, da shranite edinstveni identifikator zaposlenega v črtno kodo, ki se uporablja na naslovni strani faksa. |
| Črtna koda                       | Izberite črtno kodo, ki se uporablja na naslovni strani faksa. Črtni kodi 39 in 128 sta podprti za upravljanje stroškov. |

## <a name="anti-corruption"></a>Protikorupcijske možnosti

| Polje                                 | Opis |
|---------------------------------------|-------------|
| Prikaz potrdila za preprečevanje korupcije   | Izberite to možnost, da prikažete besedilo za preprečevanje korupcije, ko se ustvari poročilo o stroških. Nato lahko omogočite posebne kategorije stroškov, ki bodo zahtevale, da se v poročilu o stroških izbere potrdilo za preprečevanje korupcije. Na primer, kategorija daril, ki je povezana s stroški državnega uslužbenca, lahko zahteva, da zaposleni potrdi, da stroški ustrezajo pravilnikom podjetja, ki so povezani z državnimi uslužbenci. |
| Sporočilo za preprečevanje korupcije za pošiljatelja | Vnesite besedilo, ki naj bo prikazano zaposlenemu, ki ustvarja poročilo o stroških. Če želite vnesti besedilo, ki bo prikazano v skladu z uporabniškim jezikom, izberite **Prevodi**. |
| Sporočilo za preprečevanje korupcije za odobritelja  | Vnesite besedilo, ki naj bo prikazano odobritelju, ko je ustvarjeno poročilo o stroških. Če želite vnesti besedilo, ki bo prikazano v skladu z uporabniškim jezikom, izberite **Prevodi**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]