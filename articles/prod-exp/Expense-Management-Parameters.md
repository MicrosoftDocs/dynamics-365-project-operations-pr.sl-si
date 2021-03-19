---
title: Parametri upravljanja stroškov
description: Naslednji parametri nadzorujejo delovanje pri upravljanju stroškov.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 498d597fe811192ce313a1b0384de81e7ef55c58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271943"
---
# <a name="expense-management-parameters"></a>Parametri upravljanja stroškov


Parametri nadzorujejo osnovno delovanje pri upravljanju stroškov.

### <a name="general"></a>Splošno

| **Polje**                                                | **Opis**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardna stopnja kilometrine**                             | Vnesite stopnjo nadomestila za stroške prevoženih kilometrov. Stopnja se bo pomnožila s kilometrino, vneseno za stroške, da se izračuna znesek, ki je povrnjen za potne stroške.                       |
|**Plačnik osebnih stroškov**                             | Izberite, kdo je odgovoren za plačilo zneskov transakcij s kreditno kartico, ki so kategorizirani kot osebni.                                                                                                     |
|**Prikaz celotnega poročila o stroških pri ogledu podrobnosti**               | Izberite to možnost, če želite prikazati vse stroške v poročilu o stroških, ko si ogledate podrobnosti izvirnega dokumenta za določen kupon, ki je bil ustvarjen ob objavi poročila o stroških.              |
|**Predhodna pooblastitev poti je obvezna**                 | Izberite to možnost, če želite, da se zahtevek za pot predloži in odobri, preden lahko zaposleni predloži poročilo o stroških.                                                                    |
|**Dovoljenje za urejanje porazdelitev pred objavo**            | Izberite, ali se lahko porazdelitve v poročilu o stroških ureja, preden je objavljeno.                                                                                                                 |
|**Ocena pravilnikov za upravljanje stroškov**                     | Izberite, kdaj se ocenjujejo stroški, da ugotovite, ali je bil kršen pravilnik o stroških. Stroške je mogoče preveriti glede kršitev, ko je vnos stroškov vnesen in shranjen ali ko je strošek poslan v odobritev. Pravila pravilnika o zahtevanih računih bodo preverjena, ko se shrani vrstica stroškov.                   |
|**Dovoljenje za vrstice stroškov med podjetji**                         | Izberite, ali je v poročilo o stroških dovoljen vnos stroškov za druge pravne osebe.                                                                                                          |
|**Dovoljenje za urejanje menjalnega tečaja za stroške kreditne kartice** | Izberite to možnost, če želite uporabniku omogočiti urejanje menjalnega tečaja za uvožene stroške kreditne kartice.                                                                        |
|**Polja večstopenjske hierarhije za prikaz**                  | Izberite, katera polja odobritelja naj bodo prikazana, kadar je vrsta dodelitve poteka dela za poročilo o stroških nastavljena na hierarhijo in je izbrana hierarhije nastavljena za uporabo hierarhije večstopenjske odobritve stroškov. Ko se za potek dela uporablja večstopenjska hierarhija odobritve, bodo izbrana polja prikazana v poročilu o stroških in jih bo mogoče urejati. |
|**Vnos številke kreditne kartice zaposlenega (posodobitev iz julija 2017)**     | Izberite, ali lahko v polje **ID kartice** na strani **Kreditne kartice** za zaposlenega vnesete 15- ali 16-mestno številko.                                                                          |

### <a name="financial"></a>Finance

| **Polje**                                                            | **Opis**     |
|----------------------------------------------------------------------|------------------------------------|
|**Ime dnevnika za glavno knjigo**                                         | Izberite ime dnevnika za glavno knjigo, v katerem so objavljena odobrena poročila o stroških.            |
|**Omogočanje izterjave davkov za stroške**                                  | Izberite to možnost, da omogočite izterjavo davka za stroške za upravičene stroške. Te možnosti ni mogoče izbrati, če sta omogočena ameriški prometni davek in davek na uporabo.      |
|**Takojšnja objava denarnih predujmov**                                     | Izberite to možnost, če želite po zaključku postopka plačila in nakazila objaviti odobreni denarni predujem. Če ta možnost ni izbrana, bo postopek plačila in nakazila ustvaril neobjavljeno splošno temeljnico. |
|**Popravljanje datuma knjiženja med objavo**                             | Izberite to možnost, če želite posodobiti datum knjiženja, ko so objavljeni stroški, če je trenutno obdobje zadržano ali zaprto. Datum knjiženja bo nastavljen na naslednje odprto obdobje.   |
|**Dovoljenje za združevanje transakcij na podlagi protikonta za stroške, določenega v načinu plačila**      | Izberite to možnost, če želite povzeti transakcije stroškov za poročilo o stroških, in sicer na podlagi protikonta za stroške, določenega v načinu plačila za stroške.   
|**Davek je vključen**                                                   | Izberite to možnost, če želite privzeto vključiti prometni davek v znesek stroškov.             |
|**Sprostitev obremenitev glede zaprtja zahtev za pot**            | Izberite to možnost, če želite sprostiti obremenjena sredstva, ko je zaprta odobrena zahteva za pot.                                                                                   |
|**Dovoljenje za oddajo zahteve za pot ob prekoračitvi proračuna za register proračuna in proračun projekta** | Izberite to možnost, če želite zaposlenim v odobritev poslati zahteve za pot, ki presegajo dovoljeni proračun, določen v registru proračuna, ali dovoljeni proračun za projekt.            |
|**Dovoljenje za oddajo poročila o stroških ob prekoračitvi proračuna za register proračuna in proračun projekta**    | Izberite to možnost, če želite zaposlenim v odobritev poslati poročila o stroških, ki presegajo dovoljeni proračun, določen v registru proračuna, ali dovoljeni proračun za projekt.                |
|**Dovoljenje za odobritev poročila o stroških ob prekoračitvi proračuna samo za register proračuna**                | Izberite to možnost, če želite, da odobritelji odobrijo poročila o stroških, ki presegajo dovoljeni proračun, določen v registru proračuna.                                                                       |

### <a name="per-diem"></a>Dnevnica

| **Polje**                             | **Opis**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Najmanjše število ur za dnevnice**           | Vnesite privzeto najmanjše število ur, ki jih mora zaposleni opraviti na dan, da je upravičen do dnevnice za stroške, povezane s potovanjem.  Ta vrednost se uporablja kot privzeta vrednost samo za polje Najmanjše število ur za stopnje vrednosti dnevnic.                                                                                      |
|**Odstotek za obroke**                          | Vnesite privzeti odstotek dnevnice za obroke, ki se uporablja prvi in zadnji dan stroškov, povezanih s potovanjem, ko je polje **Izračun znižanja za obrok glede na** nastavljeno na bodisi **Vrsta obroka na dan** ali **Število obrokov na dan**. Delovni dan za prvi in zadnji dan je lahko krajši od običajnega delovnika. Zato se lahko znesek dnevnice za te dni razlikuje od običajnega zneska. Če je odstotek nastavljen na 0, bodo odbitki za prvi in zadnji dan 0,00. |
|**Odstotek za hotele**                        | Vnesite privzeti odstotek dnevnice za hotele, ki se uporablja prvi in zadnji dan stroškov, povezanih s potovanjem. Delovni dan za prvi in zadnji dan je lahko krajši od običajnega delovnika. Zato se lahko znesek dnevnice za te dni razlikuje od običajnega zneska. Če je odstotek nastavljen na 0, bodo odbitki za prvi in zadnji dan 0,00.                                              |
|**Drugi odstotki**                        | Vnesite privzeti odstotek dnevnice za druge stroške, ki se uporablja prvi in zadnji dan stroškov, povezanih s potovanjem. Delovni dan za prvi in zadnji dan je lahko krajši od običajnega delovnika. Zato se lahko znesek dnevnice za te dni razlikuje od običajnega zneska. Če je odstotek nastavljen na 0, bodo odbitki za prvi in zadnji dan 0,00.                                                                                                     |
|**Znižanje odstotka za zajtrk** | Vnesite znesek, za katerega se dnevnica zniža za zajtrk. Če na primer zaposleni prejme brezplačen zajtrk, boste morda želeli znesek dnevnice znižati za 10 odstotkov.                               |
|**Znižanje odstotka za kosilo**    | Vnesite znesek, za katerega se dnevnica zniža za kosilo. Če na primer zaposleni prejme brezplačno kosilo, boste morda želeli znesek dnevnice znižati za 15 odstotkov.                                       |
|**Znižanje odstotka za večerjo**   | Vnesite znesek, za katerega se dnevnica zniža za večerjo. Če na primer zaposleni prejme brezplačno večerjo, boste morda želeli znesek dnevnice znižati za 25 odstotkov.                                     |
|**Izračun znižanja za obrok glede na**         | Izberite, kako naj sistem izračuna znižanje dnevnice za obrok tako, da izberete, ali znižanje temelji na vrsti obroka na potovanje oz. na dan ali na podlagi dovoljenega števila obrokov na dan.|
|**Zaokroževanje dnevnic**                  | Izberite vrsto zaokroževanja, ki se uporablja za stroške dnevnic. Če izberete običajno zaokroževanje, se vsi stroški dnevnic, ki imajo znesek 0,50, zaokrožijo na 1,00, vsi stroški dnevnic, ki imajo znesek, ki je manjši od 0,50, pa zaokrožijo na 0,00.                                                                                              |
|**Izračun osnove za dnevnice glede na**         | Izberite, ali znesek dnevnice temelji na koledarskem dnevu ali 24-urnem obdobju.       |

### <a name="fax-cover-pages"></a>Naslovne strani faksa

| **Polje**                      | **Opis**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Navodila**                   | Vnesite navodila, ki jih morajo upoštevati zaposleni, ko ustvarjajo naslovno stran za faks, ki se uporablja za pošiljanje računov, povezanih s poročilom o stroških. Če želite vnesti besedilo, ki bo prikazano v skladu z uporabniškim jezikom, kliknite gumb **Prevodi**. |
|**ID uporabnika (podatki črtnih kod)** | Izberite to možnost, da shranite edinstveni identifikator zaposlenega v črtno kodo, ki se uporablja na naslovni strani faksa.                 |
|**Črtna koda**                      | Izberite črtno kodo, ki se uporablja na naslovni strani faksa. Črtni kodi 39 in 128 sta podprti za upravljanje stroškov.               |

### <a name="anti-corruption"></a>Protikorupcijske možnosti

|                 <strong>Polje</strong>                 |                                                                                                                                                                                            <strong>Opis</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Prikaz potrdila za preprečevanje korupcije</strong>  | Izberite to možnost, da prikažete besedilo za preprečevanje korupcije, ko se ustvari novo poročilo o stroških. Nato lahko omogočite posebne kategorije stroškov, ki bodo zahtevale, da se v poročilu o stroških izbere potrdilo za preprečevanje korupcije. Na primer, kategorija daril, ki je povezana s stroški državnega uslužbenca, lahko zahteva, da zaposleni potrdi, da stroški ustrezajo pravilnikom podjetja, ki so povezani z državnimi uslužbenci. |
| <strong>Sporočilo za preprečevanje korupcije za pošiljatelja</strong> |                                                                                             Vnesite besedilo, ki se bo zaposlenemu prikazalo pri ustvarjanju novega poročila o stroških. Če želite vnesti besedilo, ki bo prikazano v skladu z uporabniškim jezikom, kliknite gumb <strong>Prevodi</strong>.                                                                                             |
| <strong>Sporočilo za preprečevanje korupcije za odobritelja</strong>  |                                                                                             Vnesite besedilo, ki se bo odobritelju prikazalo pri ustvarjanju novega poročila o stroških. Če želite vnesti besedilo, ki bo prikazano v skladu z uporabniškim jezikom, kliknite gumb <strong>Prevodi</strong>.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]