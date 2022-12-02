---
title: Preverjanje računov dobavitelja z odobrenimi dejanskimi vrednostmi
description: Ta članek pojasnjuje, kako aplikacija Microsoft Dynamics 365 Project Operations omogoča vodjem projektov, da preverijo račune dobaviteljev z dejanskimi vrednostmi, ki so bile potrjene, ko so izvajalci opravljali delo, in zabeleženim časom ter stroški in materiali, ki so jih porabili člani projektne ekipe.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522960"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Preverjanje računov dobavitelja z odobrenimi dejanskimi vrednostmi

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Microsoft Dynamics 365 Project Operations omogoča vodjem projektov, da preverijo vrstice računa dobavitelja na naslednje načine:

- Uporaba polja **Stanje preverjanja** v vrsticah računa dobavitelja.
- Če se vrstice računa dobavitelja sklicujejo na podrobnosti podizvajalske pogodbe, povežite dejanske stroške iz dejavnosti podizvajalca s temi vrsticami računa dobavitelja. Povezava se ustvari tako, da se dejanski stroški primerjajo z vrsticami računa dobavitelja.

    > [!NOTE]
    > Čeprav je stanju preverjanja mogoče slediti za vrstice računa dobavitelja, ki se ne sklicujejo na podizvajalsko pogodbo, dejanskih stroškov ni mogoče povezati s temi vrsticami računa dobavitelja.

## <a name="verification-status"></a>Stanje preverjanja

Polje **Stanje preverjanja** v vrstici računa dobavitelja označuje ta status preverjanja. Podprta so naslednja stanja:

1. Ni začeto
2. Poteka
3. Zaključevanje

Vrstico računa dobavitelja, ki ima stanje preverjanja **Ni začeto**, je mogoče urejati.

Vrstico računa dobavitelja, ki ima stanje preverjanja **V teku**, ni več mogoče urejati. Za vrstico računa dobavitelja, ki se sklicuje na podizvajalsko pogodbo, je status preverjanja samodejno nastavljen na **V teku**, takoj ko se prvi dejanski strošek ujema z vrstico računa dobavitelja.

Vrstico računa dobavitelja, ki ima stanje preverjanja **Dokončano**, ni več mogoče urejati. Ko imajo vse vrstice na računu dobavitelja to stanje preverjanja, računa dobavitelja ni mogoče potrditi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Ujemanje dejanskih vrednosti stroškov z vrsticami računa dobavitelja

Ujemanje dejanskih stroškov pomaga pri postopku preverjanja v vrstici računa dobavitelja. Če želite ujemati dejanske vrednosti stroškov z vrstico računa dobavitelja, sledite naslednjim korakom.

1. Odprite vrstico računa dobavitelja in izberite zavihek **Neujemanje dejanskih stroškov**. Mreža prikazuje seznam dejanskih stroškov, ki se sklicujejo na iste podrobnosti podizvajalske pogodbe kot vrstica računa dobavitelja.
2. Izberite enega ali več dejanskih stroškov in nato v orodni vrstici nad mrežo izberite možnost **Ujemanje**. Sistem potrdi, da je izbrane dejanske stroške mogoče ujemati. Ko je preverjanje veljavnosti opravljeno, se dejanski stroški povežejo z vrstico računa dobavitelja.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Merila preverjanja veljavnosti, ki se uporabljajo za povezavo dejanskih stroškov z vrsticami računa dobavitelja

Med postopkom ujemanja je mogoče vzpostaviti povezavo med dejanskim stroškom in vrstico računa dobavitelja le, če sta izpolnjena oba naslednja pogoja:

- Polje **Stanje prilagoditve** mora biti za vsak izbrani dejanski strošek prazno. Dejanskih stroškov torej ne smejo nadomestiti drugi dejanskimi stroški med postopkom priklica, preklica odobritve ali dnevnika popravkov.
- Vrednosti naslednjih polj se ujemajo med vrstico računa dobavitelja in izbranim dejanskim stroškom. Če katero koli polje v vrstici računa dobavitelja ni nastavljeno, se ne upošteva za ujemanje.

    - Projektna pogodba
    - Vrstica projektne pogodbe
    - Razred transakcije
    - Projekt
    - opravilo,
    - Kategorija vira
    - Kategorija transakcije
    - izdelek,
    - Podrobnosti podizvajalske pogodbe
    - Vir, ki ga je mogoče rezervirati

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Preklic ujemanja dejanskih vrednosti stroškov z vrstico računa dobavitelja

Neujemanje dejanskih stroškov lahko pomaga tudi pri postopku preverjanja na računu dobavitelja, tako da omogoči odstranitev predhodno vzpostavljenih povezav. Dejanski stroški se lahko ne ujemajo samo z vrsticami računa dobavitelja, ki imajo status preverjanja **V teku**. Če želite preklicati ujemanje dejanskih vrednosti stroškov z vrstico računa dobavitelja, sledite naslednjim korakom.

1. Odprite vrstico računa dobavitelja in izberite zavihek **Ujemanje dejanskih stroškov**. Mreža prikazuje seznam dejanskih stroškov, ki se sklicujejo na vrstico računa dobavitelja.
2. Izberite enega ali več dejanskih stroškov in nato v orodni vrstici nad mrežo izberite možnost **Preklic ujemanja**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
