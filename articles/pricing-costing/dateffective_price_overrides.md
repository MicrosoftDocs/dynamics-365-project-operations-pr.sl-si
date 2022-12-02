---
title: Preglasitve cen, ki začnejo veljati na določen datum
description: V tem članku je pojasnjeno, kako nastaviti preglasitve cen za določene cene v ceniku.
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
# <a name="date-effective-price-overrides"></a>Preglasitve cen, ki začnejo veljati na določen datum 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Funkcija *Preglasitve cen, ki začnejo veljati na določen datum*, omogoča način za preglasitev ali spremembo določenih cen v ceniku. Primer: imate standardni cenik, ki velja od 1. januarja 2022 do 31. decembra 2022. Ta cenik vsebuje cene za številne vloge. Cena, ki je določena za vlogo **Omrežni tehnik**, je 100 ameriških dolarjev (USD) na uro. Ko omrežni tehnik beleži čas med 1. januarjem 2022 in 31. decembrom 2022, je čas ocenjen na 100 USD. 1. oktobra 2022 morate prilagoditi ceno *samo* za vlogo **Omrežni tehnik**, od 100 USD na uro do 110 USD na uro. Funkcija **Preglasitve cen, ki začnejo veljati na določen datum**, omogoča, da to spremembo nastavite kot preglasitev vrstice za ceno določene vloge. Zato vam ni treba kopirati celotnega cenika in spremeniti cene le te ene vrstice.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Preglasitve cen za določanje cen dela, ki začnejo veljati na določen datum

Postopek nastavitve preglasitev cen za določanje cen dela na projektu, ki začnejo veljati na določen datum, je sestavljen iz dveh osnovnih korakov.

1. Omogočite funkcijo **Preglasitve cen, ki začnejo veljati na določen datum**.
1. Nastavite preglasitev cene, ki začne veljati na določen datum.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Omogočanje funkcije »Preglasitve cen, ki začnejo veljati na določen datum«

> [!NOTE]
> Ko je funkcija **Preglasitve cen, ki začnejo veljati na določen datum**, omogočena, je ni mogoče onemogočiti.

Za omogočanje funkcije **Preglasitve cen, ki začnejo veljati na določen datum**, sledite tem korakom.

1. Odprite možnost **Nastavitve** \> **Parametri**.
1. Odprite zapis **Parametri**.
1. V podoknu za dejanja v zavihku **Nadzor funkcij** izberite **Omogoči preglasitve cen, ki začnejo veljati na določen datum**.
1. V potrditvenem pogovornem oknu izberite **V redu**.
1. Čez nekaj trenutkov osvežite brskalnik. Zdaj bi morale biti na voljo zmožnosti preglasitve cen, ki začnejo veljati na določen datum. Če so te zmožnosti omogočene, se možnost **Omogoči preglasitve cen, ki začnejo veljati na določen datum** ne prikaže več v podoknu za dejanja.

### <a name="set-up-a-date-effective-price-override"></a>Nastavitev preglasitve cene, ki začne veljati na določen datum

Preglasitve cen, ki začnejo veljati na določen datum, lahko nastavite v cenikih **Cena**, **Prodaja** ali **Nakup**.

> [!NOTE]
>Vedenje funkcije **Preglasitve cen, ki začnejo veljati na določen datum**, ima trenutno naslednje omejitve:
>
> - Samo cene vlog in pribitki na cene vlog podpirajo funkcijo **Preglasitve cen, ki začnejo veljati na določen datum**, v aplikaciji Project Operations.
> - Ko kopirate cenik z uporabo dejanja **Kopiraj** na strani **Podrobnosti o ceniku** in ko ustvarite cenik projekta iz standardnega cenika ali cenika po meri med ustvarjanjem pogodbe, se preglasitve cen, ki začnejo veljati na določen datum, **ne** kopirajo iz izvornega cenika.

Če želite nastaviti preglasitev cene, ki začne veljati na določen datum, za ceno vloge ali pribitek na ceno vloge, sledite tem korakom.

1. Odprite stran za cenik, za katerega želite nastaviti preglasitev cene, ki začne veljati na določen datum.
1. Izberite zavihek **Cene vlog**. Ta zavihek prikaže vse zapise **Cena vloge** v ceniku.
1. Izberite zapis **Cena vloge**, za katerega želite nastaviti novo preglasitev cene, ki začne veljati na določen datum, in se nato dvakrat dotaknite (ali dvokliknite) možnosti **Cena vloge**, da odprete stran **Podrobnosti o ceni vloge**.
1. Izberite zavihek **Preglasitve, ki začnejo veljati na določen datum**. Mreža na tem zavihku navaja vse preglasitve cen, ki začnejo veljati na določen datum, za izbran zapis **Cena vloge**.
1. V orodni vrstici nad mrežo izberite **Nova preglasitev cene vloge**. Odpre se drsnik **Nova preglasitev cene vloge**.
1. Določite datum začetka veljavnosti, enoto in novo ceno za preglasitev cene. Nato izberite možnost **Shrani** in zaprite obrazec.

> [!NOTE]
> - preglasitev cene, ki začne veljati na določen datum, za ceno vloge ali pribitek na ceno vloge velja za isto kombinacijo vrednosti cenovnih razsežnosti, ki obstaja v nadrejeni vrstici **Cena vloge** ali **Pribitek na ceno vloge**.
> - Datum, ki je izbran v polju **Datum začetka veljavnosti** mora biti znotraj datumov veljavnosti nadrejenega cenika. Preglasitev cene bo začela veljati na datum, ki je izbran v polju **Datum začetka veljavnosti**, in bo veljala do konca končnega datuma nadrejenega cenika. Če nastavite drugo preglasitev cene, ki začne veljati na določen datum, za isto ceno vloge, bo prva preglasitev cene začela veljati na datum, ki je izbran v polju **Datum začetka veljavnosti**, in bo veljalo do začetka druge preglasitve.

## <a name="examples"></a>Primeri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Primer 1: Določanje datuma veljavnosti za ceno vloge, ki ima preglasitve cene vloge

Naslednji primer prikazuje, kako se določi datum veljavnosti za določeno ceno vloge, za katero so nastavljene preglasitve cene vloge.

**Cenik A: od 1. januarja do 30. junija**

*Cena vloge*

| Cena vloge | Enota | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|---|
| Omrežni tehnik | Ura | 100 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 1. januarjem in 14. marcem. |

*Preglasitev cene vloge*

| Datum začetka veljavnosti | Enota | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|---|
| Marec 15 | Ura | 110 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 15. marcem in 30. marcem. |
| april 1 | Ura | 120 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 1. aprilom in 30. junijem. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Primer 2: Določanje datuma veljavnosti za pribitek na ceno vloge, ki ima preglasitve pribitka na ceno vloge

Naslednji primer prikazuje, kako se določi datum veljavnosti za določen pribitek na ceno vloge, za katerega so nastavljene preglasitve pribitka na ceno vloge.

**Cenik A: od 1. januarja do 30. junija**

*Cena vloge*

| Cena vloge | Delovni čas | Enota | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|---|---|
| Omrežni tehnik | Redno | Ura | 100 | Ta cena bo uporabljena za vse transakcije, pri katerih je datum transakcije med 1. januarjem in 14. marcem. |

*Pribitek na ceno vloge*

| Organizacijska enota | Delovni čas | Pribitek % |
|---|---|---|
| Contoso, ZDA | Nadure | 10 % |

*Preglasitev pribitka na ceno vloge*

| Datum začetka veljavnosti | Cena | Vpliv na cene za dohodne transakcije |
|---|---|---|
| Marec 15 | 20 % | Ta odstotek pribitka bo uporabljen za vse transakcije, pri katerih je datum transakcije med 15. marcem in 30. marcem. |
| april 1 | 25 % | Ta pribitek bo uporabljen za vse transakcije, pri katerih je datum transakcije med 1. aprilom in 30. junijem. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
