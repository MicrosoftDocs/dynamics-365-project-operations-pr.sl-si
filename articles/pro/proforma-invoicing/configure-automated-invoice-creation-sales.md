---
title: Konfiguracija samodejnega ustvarjanja predračunov
description: Ta tema vsebuje informacije o konfiguraciji samodejnega ustvarjanja predračunov.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e146dd510b3795d52d164fc6acf8e5400ba11310
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084665"
---
# <a name="configure-automated-proforma-invoice-creation"></a>Konfiguracija samodejnega ustvarjanja predračunov

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Samodejno ustvarjanje računov lahko konfigurirate v aplikaciji Dynamics 365 Project Operations. Sistem ustvari osnutek predračuna na podlagi razporeda izdajanja računov za vsako posamezno projektno pogodbo in podrobnost pogodbe. Razporedi izdajanja računov so konfigurirani na ravni podrobnosti pogodbe. Vsaka podrobnost pogodbe ima lahko različen razpored izdajanja računov ali pa je ta isti razpored izdajanja računov vključen v vsako podrobnost pogodbe.

Ko ustvarite račun, sistem ustvari vsaj en račun na projektno pogodbo. V nekaterih primerih je lahko ustvarjenih več računov.

Če ima na primer pogodba več strank, bo ustvarjeno toliko računov, kot je strank, ki imajo v tej projektni pogodbi določene plačljive transakcije, za katere je treba izdati račun.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Vključevanje transakcij v račun 

Včasih je za vsako podrobnost pogodbe, ki temelji na projektu, določen ločen razpored izdajanja računov. Storitve izvajanja pogodbe Adatum imajo na primer naslednje podrobnosti pogodbe:

- Prototip dela, ki je element s fiksno cena z dvema ročno ustvarjenima mejnikoma.
- Izvedbena dela, ki vključujejo čas in bodo obračunana vsak drugi ponedeljek.
- Nastali stroški, ki jih je treba obračunati vsak prvi ponedeljek v mesecu.

Razporedi izdajanja računov, opredeljeni za vsako od teh dveh postavk vrstice, izgledajo kot je prikazano na naslednji tabeli:

| Podrobnosti pogodbe | Datum izdaje računa | Datum prekinitve transakcije | Datum mejnika | Znesek mejnika |
| --- | --- | --- | --- | --- |
| Prototip dela | 5. oktober, ponedeljek | - | 5. oktober, ponedeljek | 5000 USD |
| - | 3. november, torek | - | 3. november, torek | 12,000 USD |
| Izvedbeno delo | 5. oktober, ponedeljek | 4. oktober, nedelja | - | - |
| - | 19. oktober, ponedeljek | 18. oktober, nedelja | - | - |
| - | 2. november, ponedeljek | 1. november, nedelja | - | - |
| - | 16. november, ponedeljek | 15. november, nedelja | - | - |
| Nastali stroški | 5. oktober, ponedeljek | 4. oktober, nedelja | - | - |
| - | 2. november, ponedeljek | 1. november, nedelja | - | - |

V primeru se samodejno izdajanje računov izvaja na dan:

- **4. oktober ali kateri koli datum pred tem** : za to pogodbo ni ustvarjen noben račun, saj tabela za **Razpored izdajanja računov** za nobeno od teh podrobnosti pogodbe nima predvidenega časa »4. oktober, nedelja« kot datuma izdaje računa.
- **5. oktober, ponedeljek** : izdan je en račun za:

    - prototip dela, ki vključuje mejnik, če ima oznako **Pripravljeno na izdajo računa**.
    - Izvedbeno delo, ki vključuje vse časovne transakcije, ustvarjene pred datumom prekinitve transakcije – 4. oktobra, v nedeljo – ki ima oznako **Pripravljeno na izdajo računa**.
    - Nastali strošek, ki vključuje vse stroške, ustvarjene pred datumom prekinitve transakcije – 4. oktobra, v nedeljo – ki ima oznako **Pripravljeno na izdajo računa**.
  
- **6. oktober ali kateri koli datum pred 19. oktobrom** : za to pogodbo ni ustvarjen noben račun, saj tabela za **Razpored izdajanja računov** za nobeno od teh podrobnosti pogodbe nima predvidenega časa »6. oktober ali kateri koli datum pred 19. oktobrom« kot datuma izdaje računa.
- **19. oktober, ponedeljek** : en račun je izdan za izvedbeno delo, ki vključuje vse časovne transakcije, ustvarjene pred datumom prekinitve transakcije – 18. oktobra, v nedeljo – ki ima oznako **Pripravljeno na izdajo računa**.
- **2. november, ponedeljek** : izdan je en račun za:

    - Izvedbeno delo, ki vključuje vse časovne transakcije, ustvarjene pred datumom prekinitve transakcije – 1. novembra, v nedeljo – ki ima oznako **Pripravljeno na izdajo računa**.
    - Nastali strošek, ki vključuje vse stroške, ustvarjene pred datumom prekinitve transakcije – 1. novembra, v nedeljo – ki ima oznako **Pripravljeno na izdajo računa**.

- **3. november, torek** : Za prototipno delo je ustvarjen en račun, ki vključuje mejnik za 12.000 USD, če ima oznako **Pripravljeno na izdajo računa**.

## <a name="configure-automatic-invoicing"></a>Konfiguracija samodejnega izdajanja računov

Če želite konfigurirati samodejno izdajanje računov, naredite naslednje.

1. V aplikaciji **Project Operations** odprite razdelek **Nastavitve** > **Nastavitev ponavljajočega se računa**.
2. Ustvarite paketno opravilo in ga poimenujte **Ustvarjanje računov v aplikaciji Project Operations**. Ime paketnega opravila mora vključevati izraz »ustvarjanje računov«.
3. V polju **Vrsta posla** izberite možnost **Brez**. Polji **Pogostost: dnevno** in **Je aktivno** sta privzeto nastavljeni na možnost **Da**.
4. Izberite **Zaženi potek dela**. V pogovornem oknu **Poišči zapis** vidite tri poteke dela:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Izberite **ProcessRunCaller** in nato **Dodaj**.
6. V naslednjem pogovornem oknu izberite **V redu**. Poteku dela **Spanje** sledi potek dela **Proces**. 

> [!NOTE]
> V 5. koraku lahko izberete tudi **ProcessRunner**. Ko nato izberete **V redu** , poteku dela **Proces** sledi potek dela **Spanje**.

Poteka dela **ProcessRunCaller** in **ProcessRunner** ustvarita račune. **ProcessRunCaller** prikliče **ProcessRunner**. **ProcessRunner** je potek dela, ki dejansko ustvari račune. Potek dela zajame vse podrobnosti pogodbe, za katere je treba ustvariti račune, in ustvari račune za te vrstice. Opravilo preveri datume izdaje računa za vrstice pogodbe, da ugotovi, za katere vrstice pogodbe je treba ustvariti račune. Če imajo vrstice pogodbe, ki pripadajo eni pogodbi, enak datum izdaje računa, se transakcije združijo v en račun, ki ima dve vrstici računa. Če ni transakcij, za katere je treba ustvariti račun, opravilo preskoči ustvarjanje računa.

Ko se potek dela **processrunner** preneha izvajati, prikliče potek dela **ProcessRunCaller** , navede končni čas in se zapre. Storitev **ProcessRunCaller** nato zažene časovnik, ki začne odštevati 24 ur pred navedenim končnim časom. Ko se časovnik preneha izvajati, se **ProcessRunCaller** zapre.

Paketna obdelava za ustvarjanje računov je ponavljajoče se opravilo. Če je paketna obdelava zagnana večkrat, je ustvarjenih več primerkov opravila, kar povzroči napake. Zato paketno obdelavo zaženite samo enkrat, znova jo zaženite le, če se preneha izvajati.

> [!NOTE]
> Paketno izdajanje računov v aplikaciji Project Operations se izvaja samo za podrobnosti pogodbe, ki so konfigurirane z razporedi izdajanja računov. V podrobnostih pogodbe z načinom obračunavanja s fiksno ceno morajo biti nastavljeni mejniki. V podrobnostih pogodbe z načinom obračunavanja za časovne in materialne transakcije je treba nastaviti datumski urnik računov.
