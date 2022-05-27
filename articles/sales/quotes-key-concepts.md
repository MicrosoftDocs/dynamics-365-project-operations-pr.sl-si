---
title: Ponudbe – ključni pojmi
description: Ta tema vsebuje informacije o ponudbah in prodajnih ponudbah za projekt, ki so na voljo v storitvi Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fbaed6a0967ce4ef4eec572de9e2a7da95c3cbd9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579954"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepti, enolični za ponudbe, ki temeljijo na projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations obstajata dve vrsti ponudb: projektne in prodajne. Vrsti ponudb se razlikujeta na naslednje načine:

- **Mreže za vrstične postavke**: v prodajni ponudbi obstaja samo ena mreža za vrstične postavke. V projektni ponudbi sta dve mreži za vrstične postavke. Ena mreža je za projektne vrstice in druga je za vrstice izdelka.
- **Aktivacija in popravki**: prodajna ponudba podpira aktivacijo in popravke. Ti procesi niso podprti pri projektni ponudbi.
- **Priložena naročila**: prodajni ponudbi lahko priložite več naročil. Projektni ponudbi lahko priložite samo eno projektno pogodbo.
- **Dobitna ponudba**: ko dobite prodajno ponudbo, lahko povezana priložnost ostane odprta. Ko je projektna ponudba pridobljena, se povezana priložnost zapre.
- **Polja in koncepti**: prodajna ponudba ne vsebuje nekaterih polj in konceptov, ki so vključeni v projektno ponudbo. Polja vključujejo **pogodbeno enoto**, **upravitelja kupcev** in **ime stika za plačilo**.  
- **Vrsta**: prodajne in projektne ponudbe so določene tudi s poljem, ki temelji na naboru možnosti in se imenuje **Vrsta**. Za prodajno ponudbo ima to polje vrednost **Temelji na elementu**. Za projektno ponudbo pa ima polje vrednost **Temelji na delu**.

V tej temi se osredotočamo na podrobnosti projektnih ponudb.

Projektna ponudba v storitvi Project Operations ima lahko več vrstičnih postavk ali vrstic ponudbe. U bistvu ima projektna ponudba dve mreži za vrstične postavke. Ena mreža je za vrstice, ki temeljijo na projektih in omogočajo podrobne ocene. Druga mreža je za vrstice, ki temeljijo na izdelkih in uporabljajo enostavno ceno enote in pristop na podlagi količine.

- **Na podlagi projektov**: ponudbena vrednost je določena po tem, ko ocenite, koliko dela je potrebno. Delo lahko ocenite na visoki ravni, neposredno kot podrobnosti vrstice pod vsako ponudbeno vrstico ali na podlagi začetnih ocen z uporabo projekta in projektnega načrta. Vrstice ponudbe, ki temeljijo na projektih, so na voljo samo v ponudbah, ki temeljijo na projektih in so ustvarjene s storitvijo Project Operations. Ta vrsta vrstice ponudb je prilagojena oblika vrstic ponudb iz kataloga, na voljo v aplikaciji Microsoft Dynamics 365 Sales.

- **Na podlagi izdelkov**: ponudbena vrednost je določena na podlagi količine prodanih enot in prodajne cene enote. Izdelek v vrstici, ki temelji na izdelku, lahko izhaja iz kataloga izdelkov aplikacije Sales, lahko pa gre za izdelek, ki ga določite. Ta vrsta vrstice ponudbe je na voljo tudi v ponudbah, ki temeljijo na projektih in so ustvarjene s storitvijo Project Operations.

Znesek v ponudbi je skupna vrednost iz vrstic, ki temeljijo na izdelkih, in vrstic, ki temeljijo na projektih.

> [!NOTE]
> Ponudbe in vrstice ponudbe niso zahtevane v storitvi Project Operations. Postopek projekta lahko začnete s projektno pogodbo (prodanim projektom). Vendar vedno potrebujete priložnost, ne glede na to, ali začnete s ponudbo ali projektno pogodbo.

## <a name="project-based-quote-lines"></a>Podrobnosti ponudb, ki temeljijo na projektih

Vrstice ponudb v storitvi Project Operations, ki temeljijo na projektih, uporabljajo naslednje načine obračunavanja:

- Čas in material
- Fiksna cena

### <a name="time-and-material"></a>Čas in material

Način obračunavanja »Čas in material« temelji na porabi. Ko izberete ta način obračunavanja, je stranki zaračunano, ko nastanejo stroški pri projektu. Računi so ustvarjeni glede na periodično pogostost na osnovi datuma. Ponudbena vrednost komponente časa in materiala med prodajnim postopkom zagotavlja samo oceno končnih stroškov za kupca. Dobavitelj se ne zavezuje, da bo projekt dokončal na točno ponudbeni vrednosti. Komponente časa in materiala povečujejo tveganje za kupca. Stranke se bodo morda želele pogajati o dodatnih klavzulah nepreseganja, da zmanjšajo tveganje. Project Operations ne podpira nastavitve klavzul nepreseganja.

### <a name="fixed-price"></a>Fiksna cena

V načinu obračunavanja Fiksna cena se dobavitelj zaveže, da bo projekt dostavil stranki po fiksni ceni. Stranki je zaračunana ponudbena vrednost vrstice ponudbe za fiksno ceno, ne glede na stroške, ki nastanejo za dobavitelja, pri zagotavljanju te vrstice ponudbe. Vrednost vrstice ponudbe za fiksno ceno je zaračunana na enega od naslednjih načinov: 

- Kot enkratno izplačilo ob začetku ali koncu projekta ali pa ko je dosežen mejnik projekta. 
- S pogostostjo, ki temelji na datumu, enakih obrokov fiksne cene v vrstici ponudbe. Ti obroki so znani kot periodični mejniki.
- V obrokih z denarno vrednostjo, ki je poravnana z napredkom dela ali posebnimi mejniki, ki so doseženi v projektu. V tem primeru se lahko vrednost vsakega obroka razlikuje, vendar ne sme presegati vrednosti fiksne cene v vrstici ponudbe.

Project Operations podpira vse tri vrste razporedov izdajanja računov za vrstice ponudb fiksne cene.

## <a name="transaction-classification"></a>Klasifikacije transakcij

Organizacije, ki ponujajo strokovne storitve, svojim kupcem običajno dajejo ponudbe in jim zaračunajo glede na razvrstitev stroškov. Stroški so predstavljeni z naslednjimi klasifikacijami transakcij:

- **Čas**: ta klasifikacija predstavlja stroške dela ali časa človeških virov v projektu.
- **Strošek**: ta klasifikacija predstavlja vse druge vrste stroškov v projektu. Ker so stroški lahko razvrščeni na splošno, večina organizacij ustvari podkategorije, kot so potni stroški, stroški najema avtomobila, hotelski stroški ali stroški pisarniškega materiala.
- **Nadomestilo**: ta klasifikacija predstavlja razne dodatne stroške, kazni in druge elemente, ki se zaračunajo kupcu. 
- **Davek**: ta klasifikacija predstavlja davčne zneske, ki jih uporabniki dodajo med vnašanjem stroškov.
- **Materialna transakcija**: ta klasifikacija predstavlja dejanske vrednosti iz vrstice izdelkov na potrjenem računu projekta.
- **Mejnik**: to klasifikacijo uporablja logika obračunavanja fiksnih cen.

Z vsako vrstico ponudbe je mogoče povezati eno ali več teh klasifikacij transakcij. Ko je ponudba pridobljena, se preslikava med klasifikacijo transakcije in vrstico ponudbe prenese v podrobnosti pogodbe.
  
Ponudba lahko na primer vsebuje naslednji vrstici ponudbe: 

- Svetovalno delo, ki uporablja način obračunavanja na podlagi časa in materiala, v katerem je mogoče uveljavljati klasifikacije transakcij na podlagi časa in nadomestila. Npr. vse transakcije časa in nadomestila za primer projekta **Uvedba Dynamics AX** se stranki zaračunajo na podlagi uporabljenega časa in materialov. 
- Povezani potni stroški, ki uporabljajo način obračunavanja »Fiksna cena«. Vsi potni stroški za primer projekta **Uvedba Dynamics AX** so zaračunani po fiksni denarni vrednosti.

> [!NOTE]
> Kombinacija projekta in klasifikacij transakcij **Čas**, **Strošek** in **Nadomestilo**, ki so povezane z vrstico ponudbe ali podrobnostmi pogodbe, mora biti edinstvena. Če je ista kombinacija razreda projekta in transakcije povezana z več kot enimi podrobnostmi pogodbe ali vrsticami ponudbe, storitev Project Operations ne bo pravilno delovala.

## <a name="billing-types"></a>Vrste obračunavanja

Polje **Vrsta obračunavanja** določa pojem zaračunavanja. To je nabor možnosti, ki ima naslednje možne vrednosti:

- **Se zaračuna**: strošek, ki se obračuna s to vlogo/kategorijo, se šteje kot neposreden strošek, ki spodbuja izvedbo projekta, stranka pa bo plačala za to delo. Plačilo se lahko upravlja kot dogovor, zasnovan na času in materialu ali fiksni ceni. Zaposleni, ki porabi ta čas, pa bo dobil ustrezno plačilo za svojo zaračunano porabo.
- **Se ne zaračuna**: strošek, ki se obračuna s to vlogo/kategorijo, se šteje kot neposreden strošek, ki spodbuja izvedbo projekta, tudi če stranka tega dejstva ne upošteva in ne želi plačati za to delo. Zaposleni, ki porabi ta čas, ne bo plačan za zaračunano porabo za ta čas.
- **Brezplačno**: strošek, ki se obračuna s to vlogo/kategorijo, se šteje kot neposreden strošek, ki spodbuja izvedbo projekta, stranka pa to dejstvo priznava. Zaposleni, ki porabi ta čas, bo plačan za zaračunano porabo za ta čas. Vendar se ta strošek ne zaračuna kupcu.
- **Ni na voljo**: s to možnostjo se spremljajo stroški, nastali pri internih projektih, ki ne zahtevajo sledenja prihodkom.

## <a name="invoice-schedule"></a>Razpored izdajanja računov

Razpored izdajanja računov je niz datumov, ob katerih se izvaja izdajanje računov za projekt. Po želji lahko ustvarite razpored izdajanja računov v vrstici ponudbe. Vsaka vrstica ponudbe ima lahko svoj razpored izdajanja računov. Če želite ustvariti razpored izdajanja računov, morate navesti naslednje vrednosti atributov:

- Začetni datum obračunavanja 
- Datum dostave, ki predstavlja končni datum obračunavanja v projektu
- Pogostost izdajanja računov

Te tri vrednosti atributov se uporabljajo za ustvarjanje pogojnega nabora datumov za vzpostavitev izdajanja računov.

## <a name="invoice-frequency"></a>Pogostost izdajanja računov

Pogostost izdajanja računov je entiteta, ki shranjuje vrednosti atributov, ki pomagajo izraziti pogostost ustvarjanja računa. Naslednji atributi izražajo ali določajo entiteto pogostosti izdajanja računov:

- **Obdobje**: podprta so mesečna, dvotedenska in tedenska obdobja. 
- **Izvajanje na obdobje**: za tedenska in dvotedenska obdobja lahko določite samo eno izvajanje na obdobje. Za mesečna obdobja lahko določite eno ali do štiri izvajanja na obdobje. 
- **Dnevi izvajanja**: dnevi, ko je treba izvesti izdajanje računov. Ta atribut lahko konfigurirate na dva načina:
  - **Delavniki**: lahko na primer določite, da se izdajanje računov izvaja vsak ponedeljek ali vsak drug ponedeljek. Takšna vrsta konfiguracije je lahko bolj všeč strankam, ki morajo nastaviti izvajanje izdajanja računov ob delovnih dneh. 
  - **Koledarski dnevi**: lahko na primer določite, da se izdajanje računov izvaja sedmi in enaindvajseti dan vsakega meseca. Tovrstna konfiguracija bo morda všeč nekaterim organizacijam, ker zagotavlja, da se izdajanje računov izvaja vsak mesec po fiksnem razporedu.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Razpored izdajanja računov za vrstico ponudbo fiksne cene

Za vrstico ponudbe fiksne cene lahko uporabite mrežo **Razpored izdajanja računov**, da ustvarite mejnike obračunavanja, ki so enaki vrednosti v vrstici ponudbe.

- Da ustvarite mejnike obračunavanja, ki so enako razdeljeni, izberite pogostost izvajanja računov, vnesite začetni datum obračunavanja v vrstico ponudbe in izberite **Zahtevani datum zaključka** za ponudbo v razdelku glave ponudbe **Povzetek**. Nato izberite **Ustvari periodične mejnike**, da ustvarite enakomerno razdeljene mejnike na podlagi izbrane pogostosti izdajanja računov. 
- Če želite ustvariti mejnik obračunavanja za enkratno izplačilo, ustvarite mejnik in nato vnesite vrednost vrstice ponudbe kot znesek mejnika.
- Če želite ustvariti mejnike obračunavanja, ki temeljijo na določenih opravilih v načrtu projekta, ustvarite mejnik in ga preslikajte v element projektnega razporeda v uporabniškem vmesniku mejnika obračunavanja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
