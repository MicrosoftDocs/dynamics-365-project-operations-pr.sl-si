---
title: Ustvarjanje razporedov izdajanja računov v podrobnostih pogodbe, ki temelji na projektu – poenostavljena različica
description: V tej temi so na voljo informacije o ustvarjanju razporedov računov in mejnikov.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: edacae144f5c4879d3cfdf9585281858d7312589
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581994"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Ustvarjanje razporedov izdajanja računov v podrobnostih pogodbe, ki temelji na projektu – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Razpored izdajanja računov lahko priložite v podrobnostih pogodbe, ki temelji na projektu. Zaračunavanje je dovoljeno samo potem, ko je pogodba pridobljena, da se ustvari projektna pogodba. Razporedi računov omogočajo, da so samodejno ustvarjeni osnutki računov podrobnosti pogodbe, ki temeljijo na projektu. Če načrtujete, da boste vedno ročno ustvarjali račune, lahko preskočite ustvarjanje razporedov računov v podrobnostih pogodbe, ki temelji na projektu, ali podrobnostih pogodbe.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Ustvarjanje razporeda izdajanja računov za čas in material za podrobnosti pogodbe, ki temelji na projektu.

Kadar je način obračunavanja v podrobnostih pogodbe na podlagi projekta mogoče prilagoditi glede na čas in material, lahko ustvarite razpored računov na podlagi datuma. Za samodejno ustvarjanje razporeda računov na podlagi datuma, izvedite naslednje korake.

1. Pojdite na **Nastavitve** > **Pogostost izdajanja računov**, da nastavite pogostost izdajanja računov.
2. Odprite projektno pogodbo in na zavihku **Povzetek** nastavite zahtevani datum dostave.
3. Odprite podrobnosti pogodbe za čas in material, za katero želite ustvariti razpored za izdajanje računov na podlagi datuma. 
4. Na zavihku **Razpored izdajanja računov** izberite začetni datum obračunavanja in pogostost izdajanja računov. 
5. V podmreži izberite možnost **Ustvari razpored računov**.

    Sistem ustvari razpored za izdajanje računov z naslednjimi informacijami polja:

    - **Datum izdaje računa** je nastavljen na datum na podlagi pogostosti izdajanja računov.
    - **Datum prekinitve transakcije** je nastavljen na dan pred možnostjo **Datum izdaje računa**.
    - **Stanje izdaje** je samodejno nastavljeno na možnost **Ni izdano**. Ko se postopek samodejnega ustvarjanja računov zažene za posamezen **Datum izdaje računa**, se vrednost polja posodobi na možnost **Uspešna izdaja** ali **Neuspešna izdaja**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Ustvarjanje razporeda izdajanja računov fiksne cene za podrobnosti pogodbe, ki temelji na projektu

Ko imajo podrobnosti pogodbe, ki temelji na projektu, način obračunavanja fiksne cene, lahko ustvarite razpored za izdajanje računov na podlagi mejnika. Dokončajte naslednje korake za samodejno ustvarjanje razporeda za izdajanje računov na podlagi mejnika za fiksni nabor mejnikov, ki se enakomerno razporedijo za koledarsko obdobje.

1. Pojdite na **Nastavitve** > **Pogostost izdajanja računov**, da nastavite pogostost izdajanja računov.
2. Odprite projektno pogodbo in na zavihku **Povzetek** nastavite zahtevani datum dostave.
3. Odprite podrobnosti pogodbe za fiksno ceno, za katero morate ustvariti razpored mejnikov. 
4. Na zavihku **Razpored izdajanja računov (mejniki obračunavanja)** izberite začetni datum obračunavanja in pogostost izdajanja računov. 
5. V podmreži izberite možnost **Ustvari periodične mejnike**.

    Sistem ustvari razpored za izdajanje računov z naslednjimi informacijami mejnika:

    - **Ime mejnika** je nastavljeno na datum, ki je določen na podlagi pogostosti izdajanja računov.
    - **Datum mejnika** je nastavljeno na datum, ki je določen na podlagi pogostosti izdajanja računov.
    - **Znesek mejnika** je izračunan z delitvijo pogodbenega zneska na podrobnostih pogodbe, ki temelji na projektu, s številom mejnikov, kot določa pogostost, začetek obračunavanja in zahtevani datumi dostave.
    - Če imajo podrobnosti pogodbe vrednost v polju **Predvideni znesek davka**, je to polje prav tako dodeljeno vsakemu mejniku enakomerno ob ustvarjanju rednih mejnikov.

Mejniki obračunavanja bi morali biti enaki pogodbeni vrednosti podrobnosti pogodbe, ki temelji na projektu. Če niso enaki, pride do napake. Napako lahko odpravite, tako da preverite celotno pogodbeno vrednost mejnikov obračunavanja podrobnosti, tako da ustvarite, uredite ali izbrišete mejnike. Ko so spremembe uveljavljene, osvežite stran.

### <a name="manually-create-milestones"></a>Ročno ustvarjanje mejnikov

Mejnike s fiksno ceno je mogoče ustvariti ročno, ko niso redno deljeni. Če želite ročno ustvariti mejnik, izvedite naslednje korake.

1. Odprite podrobnosti pogodbe za fiksno ceno, za katero želite ustvariti mejnik. 
2. Na zavihku **Razpored izdajanja računov** v podmreži izberite **+ Ustvarjanje novega mejnika podrobnosti pogodbe**.
3. V obrazcu **Ustvarjanje mejnika** vnesite zahtevane informacije na podlagi naslednje tabele. 

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Ime mejnika | Hitro ustvarjanje | Besedilno polje za ime mejnika. | To polje je vključeno v mejnik in račun podrobnosti pogodbe projekta. |
| Projektno opravilo | Hitro ustvarjanje | Če je mejnik vezan na projektno opravilo, uporabite ta sklic za dodajanje logike po meri in nastavite stanje mejnika na podlagi stanja opravila. | Ta sklic ne vpliva navzdol na opravilo. |
| Datum mejnika | Hitro ustvarjanje | Datum, ko naj avtomatizirani postopek ustvarjanja računov poišče stanje tega mejnika, da ga obravnava za izstavljanje računov. | To je vključeno v mejnik in račun podrobnosti pogodbe projekta. |
| Stanje računa | Hitro ustvarjanje | Ko je mejnik ustvarjen, je to stanje vedno nastavljeno na **Ni pripravljeno za izdajanje računov** ali **Ni začeto**. | To je vključeno v mejnik in račun podrobnosti pogodbe projekta. |
| Znesek vrstice | Hitro ustvarjanje | Znesek ali vrednost mejnika, ki bo zaračunan stranki. | To polje je vključeno v mejnik in račun podrobnosti pogodbe projekta. |
| Davek | Hitro ustvarjanje | Znesek davka, ki se uporablja za mejnik. | To je vključeno v mejnik in račun podrobnosti pogodbe projekta. |

4. Izberite možnost **Shrani in zapri**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]