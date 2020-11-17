---
title: Ustvarjanje razporedov računov v podrobnostih pogodbe na podlagi projekta
description: Ta tema vsebuje informacije o ustvarjanju razporedov računov in mejnikov za podrobnosti pogodbe.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2183b915dd2f67e03964246cb0689003e48363f7
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084990"
---
# <a name="creating-invoice-schedules-on-a-project-based-contract-line"></a>Ustvarjanje razporedov računov v podrobnostih pogodbe na podlagi projekta

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Ustvarite lahko razpored računov v podrobnostih pogodbe na podlagi projekta. Izdajanje računov je dovoljeno šele po pridobitvi pogodbe in ustvarjanju projektne pogodbe. Razpored računov omogoča samodejno ustvarjanje osnutkov računov podrobnosti pogodbe na podlagi projekta. Če pa račune ustvarjate samo ročno, lahko preskočite ustvarjanje razporedov računov v podrobnostih pogodbe.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Ustvarjanje razporeda računov za čas in material za podrobnosti pogodbe

Kadar je način obračunavanja v podrobnostih pogodbe na podlagi projekta mogoče prilagoditi glede na čas in material, lahko ustvarite razpored računov na podlagi datuma. Za samodejno ustvarjanje razporeda računov na podlagi datuma, izvedite naslednje korake.

1. V razdelku **Nastavitve** > **Pogostost izdajanja računov** nastavite pogostost izdajanja računov.
2. Odprite zapis o projektni pogodbi in v zavihku **Povzetek** izberite datum v polju **Zahtevani datum dostave**.
3. Odprite podrobnosti pogodbe za **Čas in material** , za katere morate ustvariti razpored računov na podlagi datuma. 
4. Na zavihku **Razpored računov** izberite datum začetka obračunavanja in pogostost izdajanja računov.
5. V podmreži izberite možnost **Ustvari razpored računov**. Razpored računov je ustvarjen s polji za **Datum izdaje računa** , **Datum zaključka transakcije** in **Stanje izdaje** , ki so nastavljeni na naslednji način:

    - **Datum izdaje računa** ta datum je določen glede na pogostost izdajanja računov.
    - **Datum zaključka transakcije** : dan pred datumom izdaje računa.
    - **Stanje izdaje** : samodejno nastavljeno na možnost **Ni izdano**. Ko se postopek samodejnega ustvarjanja računov zažene za posamezen datum izdaje računa, se vrednost polja posodobi na možnost **Uspešna izdaja** ali **Neuspešna izdaja**.


## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Ustvarjanje razporeda računov s fiksno ceno za podrobnosti pogodbe

Če imajo podrobnosti pogodbe fiksen način obračunavanja, lahko ustvarite razpored računov na podlagi mejnika. Dokončajte naslednje korake za generiranje razporeda računov na podlagi mejnikov za fiksen nabor enakomerno porazdeljenih mejnikov v koledarskem obdobju.

1. V razdelku **Nastavitve** > **Pogostost izdajanja računov** nastavite pogostost izdajanja računov.
2. Odprite zapis o projektni pogodbi in v zavihku **Povzetek** izberite datum v polju **Zahtevani datum dostave**.
3. Odprite podrobnosti pogodbe **Fiksna cena** , za katero želite ustvariti razpored mejnikov. Na zavihku **Mejniki obračunavanja** izberite datum začetka obračunavanja in pogostost izdajanja računov. 
4. V podmreži izberite možnost **Ustvari periodične mejnike**. Ustvari se razpored računov s polji **Ime mejnika** , **Datum mejnika** in **Znesek mejnika** , ki so nastavljeni, kot je prikazano spodaj:

    - **Ime mejnika** : ta datum je določen glede na pogostost izdajanja računov.
    - **Datum mejnika** : ta datum je določen glede na pogostost izdajanja računov.
    - **Znesek mejnika** : ta znesek se izračuna tako, da se znesek pogodbe v podrobnostih pogodbe deli s številom mejnikov, kot jih določa pogostost, začetek obračunavanja in zahtevani datumi prejetja.

    Če je v polju **Predvideni znesek davka** v podrobnostih pogodbe vpisana kakšna vrednost, se tudi to polje enakomerno porazdeli na vsak mejnik pri ustvarjanju periodičnih mejnikov.

Mejniki obračunavanja morajo biti enaki pogodbeni vrednosti podrobnosti pogodbe. Če niso, se vam bo prikazala napaka na strani **Podrobnosti pogodbe**. Napako lahko odpravite tako, da z ustvarjanjem, urejanjem ali brisanjem mejnikov preverite, ali mejniki obračunavanja seštevajo pogodbeno vrednost vrstice. Po opravljenih spremembah osvežite stran, da odstranite napako.

### <a name="manually-create-milestones"></a>Ročno ustvarjanje mejnikov

Mejnike s fiksno ceno lahko generirate tudi ročno, če se niso periodično deljeni. Dokončajte naslednje korake, da ročno ustvarite mejnik.

1. Odprite podrobnosti pogodbe s fiksno ceno, za katero ustvarjate mejnik, in v zavihku **Razpored računov** na podmreži izberite **+ Ustvari nov mejnik podrobnosti pogodbe**. 
2. Na strani **Ustvarjanje mejnika** vnesite zahtevane podatke na podlagi naslednje tabele.

| Polje | LOkacija | Ustreznost, namen in smernice | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Ime mejnika | Hitro ustvarjanje | Besedilno polje za ime mejnika. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Projektno opravilo | Hitro ustvarjanje | Če je mejnik vezan na projektno opravilo, lahko s to referenco dodate prilagojeno logiko za nastavitev stanja mejnika glede na stanje opravila. | Aplikacija nima nobenega nadaljnjega vpliva zaradi sklicevanja na opravilo. |
| Datum mejnika | Hitro ustvarjanje | Nastavite datum, ko želite, da se s postopkom samodejnega ustvarjanja računov preveri stanje mejnika za primernost izdaje računa. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Stanje računa | Hitro ustvarjanje | Ko je ustvarjen mejnik, je to stanje vedno nastavljeno na **Ni pripravljeno za izdajo računa** ali **Ni se še začelo**. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Znesek vrstice | Hitro ustvarjanje | Znesek ali vrednost mejnika, za katerega bo stranki izdan račun. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |
| Davek | Hitro ustvarjanje | Znesek davka, ki se uporablja za mejnik. | Prenese se na mejnik podrobnosti pogodbe projekta in na račun. |

3. Izberite možnost **Shrani in zapri**.
| Znesek vrstice | Hitro ustvarjanje | Znesek ali vrednost mejnika, ki bo zaračunan stranki | Ta se razširi na mejnik podrobnosti projektne pogodbe in na račun | | Davek | Hitro ustvarjanje | Znesek davka, ki se bo uporabil za mejnik | Ta se razširi na mejnik projektne pogodbe in na račun |