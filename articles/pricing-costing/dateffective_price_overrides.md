---
title: Preglasitve cen z datumom veljavnosti
description: V tem članku je razloženo, kako nastaviti preglasitve cen za določene cene v ceniku.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446012"
---
# <a name="date-effective-price-overrides"></a>Preglasitve cen z datumom veljavnosti 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

*Preglasitve cen z datumom veljavnosti* omogočite način za preglasitev ali spremembo določenih cen v ceniku. Na primer, imate standardni cenik, ki velja od 1. januarja 2022 do 31. decembra 2022. Ta cenik vsebuje cene za številne vloge. Cena, ki je določena za **omrežni tehnik** vloga je 100 ameriških dolarjev (USD) na uro. Ko omrežni tehnik beleži čas med 1. januarjem 2022 in 31. decembrom 2022, je čas ocenjen na 100 USD. 1. oktobra 2022 morate prilagoditi ceno *samo* za **omrežni tehnik** vlogo, od 100 USD na uro do 110 USD na uro. The **Datum veljavnosti cene preglasi** vam omogoča, da to spremembo nastavite kot preglasitev vrstice za določeno ceno vloge. Zato vam ni treba kopirati celotnega cenika in spremeniti cene le te ene vrstice.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Cene z datumom veljavnosti preglasijo cene dela

Postopek nastavitve datumsko veljavnih preglasitev cen za delovni čas na projektu je sestavljen iz dveh osnovnih korakov.

1. Omogoči **Datum veljavnosti cene preglasi** funkcija.
1. Nastavite preglasitev cene glede na datum.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Omogočite funkcijo preglasitve datuma veljavnosti cene

> [!NOTE]
> Po **Datum veljavnosti cene preglasi** funkcija omogočena, je ni mogoče onemogočiti.

Da omogočite **Preglasitve cen z datumom veljavnosti** funkcijo, sledite tem korakom.

1. Pojdi do **nastavitve** \> **Parametri**.
1. Odprite **Parametri** zapis.
1. V podoknu z dejanji na **Nadzor funkcij** zavihek izberite **Omogoči preglasitve datuma veljavnosti cene**.
1. V potrditvenem pogovornem oknu izberite **V redu**.
1. Po nekaj trenutkih osvežite brskalnik. Zdaj bi morale biti na voljo zmožnosti preglasitve cen z veljavnostjo datuma. Vedeli boste, da so te zmožnosti omogočene, če **Omogoči preglasitve datuma veljavnosti cene** se ne prikaže več v podoknu z dejanji.

### <a name="set-up-a-date-effective-price-override"></a>Nastavite preglasitev cene glede na datum

Nastavite lahko preglasitve cen z datumom veljavnosti **Stroški**, **·**, oz **Nakup** ceniki.

> [!NOTE]
>Obnašanje **Datum veljavnosti cene preglasi** trenutno ima naslednje omejitve:
>
> - Samo cene vlog in pribitki na cene vlog podpirajo **Datum veljavnosti cene preglasi** funkcijo v projektnih operacijah.
> - Ko kopirate cenik z uporabo **Kopirati** ukrepanje na **Podrobnosti o ceniku** in ko med ustvarjanjem pogodbe ustvarite cenik projekta iz standardnega cenika ali cenika po meri, so preglasitve cen z datumom veljavnosti **ne** prepisano iz izvornega cenika.

Če želite nastaviti preglasitev cene z datumom veljavnosti za ceno vloge ali pribitek cene vloge, sledite tem korakom.

1. Odprite stran za cenik, za katerega želite nastaviti preglasitev cene z datumom veljavnosti.
1. Izberite **Cene vlog** zavihek. Ta zavihek navaja vse **Cena vloge** zapise v ceniku.
1. Izberite **Cena vloge** zapis, za katerega želite nastaviti novo preglasitveno ceno z veljavnostjo datuma, in nato dvakrat tapnite (ali dvokliknite) **Cena vloge** odpreti **Podrobnosti o ceni vloge** strani.
1. Izberite **Datum veljavnosti preglasitev** zavihek. Mreža na tem zavihku navaja vse preglasitve cen z datumom veljavnosti za izbrano **Cena vloge** zapis.
1. V orodni vrstici nad mrežo izberite **Nova preglasitev cene vloge**. The **Nova preglasitev cene vloge** drsnik se odpre.
1. Določite datum začetka veljavnosti, enoto in novo ceno za preglasitev cene. Nato izberite **Shrani**, in zaprite obrazec.

> [!NOTE]
> - Preglasitev cene z datumom veljavnosti za ceno vloge ali pribitek cene vloge velja za isto kombinacijo vrednosti dimenzij cen, ki obstaja v nadrejenem **Cena vloge** oz **Pribitek na ceno vloge** vrstica.
> - Datum, ki je izbran v **Učinkovito od** polje mora biti znotraj datumov veljavnosti matičnega cenika. Preglasitev cene bo začela veljati na datum, ki je izbran v **Učinkovito od** polje in bo veljalo do konca končnega datuma nadrejenega cenika. Če nastavite drugo preglasitev cene z datumom veljavnosti za isto ceno vloge, bo prva preglasitev cene začela veljati na datum, ki je izbran v **Učinkovito od** polje in bo veljalo do začetka druge preglasitve.

## <a name="examples"></a>Primeri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Primer 1: Določanje datuma veljavnosti za ceno vloge, ki ima preglasitve cene vloge

Naslednji primer prikazuje, kako se določi datum veljavnosti za določeno ceno vloge, za katero so nastavljene preglasitve cene vloge.

**Cenik A: od 1. januarja do 30. junija**

*Cena vloge*

| Cena vloge | Enota | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|---|
| Omrežni tehnik | Ura | 100 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 1. januarjem in 14. marcem. |

*Preglasitev cene vloge*

| Učinkovito od | Enota | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|---|
| Marec 15 | Ura | 110 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 15. in 30. marcem. |
| april 1 | Ura | 120 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 1. aprilom in 30. junijem. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Primer 2: Določanje datumske veljavnosti za pribitek cene vloge, ki ima preglasitve pribitka cene vloge

Naslednji primer prikazuje, kako se določi datum veljavnosti za določen pribitek cene vloge, za katerega so nastavljene preglasitve pribitka cene vloge.

**Cenik A: od 1. januarja do 30. junija**

*Cena vloge*

| Cena vloge | Delovni čas | Enota | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|---|---|
| Mrežni tehnik | Redno | Ura | 100 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 1. januarjem in 14. marcem. |

*Pribitek na ceno vloge*

| Organizacijska enota | Delovni čas | Pribitek % |
|---|---|---|
| Contoso, ZDA | Nadure | 10 % |

*Preglasitev pribitka na ceno vloge*

| Učinkovito od | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|
| Marec 15 | 20 % | Ta odstotek pribitka bo uporabljen za vse transakcije, pri katerih je datum transakcije med 15. in 30. marcem. |
| april 1 | 25 % | Ta pribitek bo uporabljen za vse transakcije, pri katerih je datum transakcije med 1. aprilom in 30. junijem. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
