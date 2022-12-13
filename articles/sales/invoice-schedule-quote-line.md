---
title: Razporedi računov v vrsticah projektnih ponudb
description: Ta članek vsebuje informacije o ustvarjanju razporedov računov in mejnikov za vrstice ponudb.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 98006cc2857f01298054c4f0e70781bf4b8b474b
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825774"
---
# <a name="invoice-schedules-on-project-quote-lines"></a>Razporedi računov v vrsticah projektnih ponudb

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Vrstica ponudbe projekta omogoča izražanje razporeda faktur. To v fazi ponudbe ni obvezno, saj aplikacija ne podpira izdaje računa za projekt, če je vezan na vrstico ponudbe. Izdajanje računov je dovoljeno šele po pridobitvi ponudbe. Edini nadaljnji učinek ustvarjanja razporeda računov med fazo ponudbe je, da se ta razpored računov prepiše v podrobnosti pogodbe, ki temelji na projektu. Če med fazo ponudbe ne ustvarite razporeda računov, boste to lahko storili v podrobnostih pogodbe, ki temeljijo na projektu.

Na splošno je namen razporedov računov omogočiti samodejno ustvarjanje osnutkov računov za podrobnosti pogodbe, ki temeljijo na projektu. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-quote-line"></a>Ustvarite razpored fakturiranja časa in materiala za vrstico ponudbe projekta

Kadar je način obračunavanja za ponudbeno vrstico , ki temelji na projektu, možnost Čas in material, se v sistemu ustvari časovni razpored računov na podlagi datuma. Za samodejno ustvarjanje razporeda računov na podlagi datuma, izvedite naslednje korake.

1. V razdelku **Nastavitve** > **Pogostost izdajanja računov** nastavite pogostost izdajanja računov.
2. Na strani **Ponudbe** odprite ponudbo za projekt in na zavihku **Povzetek** nastavite zahtevani datum prejetja.
3. Odprite vrstico ponudbe za čas in material, za katero morate ustvariti razpored računov na podlagi datuma. 
4. Na zavihku **Razpored računov** izberite vrednost za polji **Začetek obračunavanja** in **Pogostost izdajanja računov**. 
5. V podmreži izberite možnost **Ustvari razpored računov**.
6. Aplikacija ustvari razpored računov s polji za **Datum izdaje računa**, **Datum zaključka transakcije** in **Stanje izdaje**, ki so nastavljeni na naslednji način:

    - **Datum izdaje računa** je nastavljen na datum, ki je določen glede na pogostost izdajanja računov.
    - **Datum zaključka transakcije** je nastavljen na dan pred **datumom izdaje računa**.
    - **Stanje izdaje** je samodejno nastavljeno na možnost **Ni izdano**. Ko se postopek samodejnega ustvarjanja računov zažene za posamezen datum izdaje računa, se vrednost polja posodobi bodisi na možnost **Uspešna izdaja** ali pa **Neuspešna izdaja**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-quote-line"></a>Ustvarite razpored faktur s fiksno ceno za vrstico ponudbe projekta

Če ima vrstica ponudbe, ki temelji na projektu, **fiksen** način obračunavanja, se v sistemu ustvari razpored računov, ki temelji na mejniku. Dokončajte naslednje korake za samodejno generiranje razporeda za fiksen nabor mejnikov, ki so za koledarsko obdobje enakomerno porazdeljeni.

1. V razdelku **Nastavitve** > **Pogostost izdajanja računov** nastavite pogostost izdajanja računov.
2. Na strani **Ponudbe** odprite ponudbo za projekt in na zavihku **Povzetek** nastavite zahtevani datum prejetja.
3. Odprite vrstico ponudbe s fiksno ceno, za katero želite ustvariti razpored mejnikov. 
4. Na zavihku **Razpored računov** izberite vrednost za polji **Začetek obračunavanja** in **Pogostost izdajanja računov**. 
5. V podmreži izberite možnost **Ustvari periodične mejnike**.
6. V aplikaciji se ustvari razpored računov z imenom, datumom in zneskom mejnika.

    - Ime mejnika je nastavljeno na datum, ki je določen glede na pogostost izdajanja računov.
    - Datum mejnika je nastavljen na datum, ki je določen glede na pogostost izdajanja računov.
    - Znesek mejnika se izračuna tako, da se znesek ponudbe na vrstici ponudbe, ki temelji na projektu, deli s številom mejnikov, kot jih določa pogostost in začetek obračunavanja ter zahtevani datumi prejetja.
    - Če je v vrstici ponudbe ocenjen tudi znesek davka, se pri ustvarjanju periodičnih mejnikov ta vrednost enakomerno razdeli med posamezne mejnike.

### <a name="manually-create-milestones"></a>Ročno ustvarjanje mejnikov

Mejnike s fiksno ceno lahko generirate tudi ročno, če se niso periodično deljeni. Za ročno ustvarjanje mejnikov:

Odprite vrstico ponudbe s fiksno ceno, za katero želite ustvariti mejnik. Na zavihku **Razpored izdajanja računov** v podmreži izberite **+ Ustvarjanje novega mejnika vrstice ponudbe** in vnesite potrebne informacije na podlagi naslednje tabele.

| **Polje** | **Mesto** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Ime mejnika | Hitro ustvari | Ime mejnika | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Projektno opravilo | Hitro ustvari | Če je mejnik vezan na projektno opravilo, lahko s to referenco dodate prilagojeno logiko za nastavitev stanja mejnika glede na stanje opravila. | Aplikacija nima nobenega nadaljnjega vpliva zaradi sklicevanja na opravilo. |
| Datum mejnika | Hitro ustvari | Nastavite datum, ko želite, da se s postopkom samodejnega ustvarjanja računov preveri stanje mejnika za primernost izdaje računa. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Stanje računa | Hitro ustvari | Ko je ustvarjen mejnik, je to stanje vedno nastavljeno na **Ni pripravljeno za izdajo računa**. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Znesek vrstice | Hitro ustvari | Znesek ali vrednost mejnika, za katerega bo stranki izdan račun. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Davek | Hitro ustvari | Znesek davka, ki bo uporabljen za mejnik. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
