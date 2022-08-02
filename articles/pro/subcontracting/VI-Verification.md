---
title: Preverjanje računov dobavitelja z odobrenimi dejanskimi vrednostmi
description: Ta članek pojasnjuje, kako Microsoft Dynamics 365 Project Operations naj vodje projektov preverijo račune dobaviteljev z dejanskimi podatki, ki so bili potrjeni kot izvajalci opravljenih del in evidentiranim časom ter stroški in materiali, ki so jih porabili člani projektne skupine.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204195"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Preverjanje računov dobavitelja z odobrenimi dejanskimi vrednostmi

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Microsoft Dynamics 365 Project Operations naj vodje projektov preverijo vrstice računa dobavitelja na naslednje načine:

- Uporabi **Stanje preverjanja** polje v vrsticah računa dobavitelja.
- Če se vrstice računa dobavitelja sklicujejo na vrstico podizvajalca, povežite dejanske stroške iz dejavnosti podizvajalca s temi vrsticami računa dobavitelja. Povezava se ustvari tako, da se dejanski stroški primerjajo z vrsticami računa dobavitelja.

    > [!NOTE]
    > Čeprav je statusu preverjanja mogoče slediti za vrstice računa dobavitelja, ki se ne sklicujejo na podizvajalsko pogodbo, dejanskih stroškov ni mogoče povezati s temi vrsticami računa dobavitelja.

## <a name="verification-status"></a>Stanje preverjanja

The **Stanje preverjanja** polje v vrstici računa dobavitelja označuje ta status preverjanja. Podprti so naslednji statusi:

1. Ni začeto
2. Poteka
3. Zaključevanje

Vrstice računa dobavitelja, ki imajo status preverjanja **Ni se začelo** lahko urejate.

Vrstice računa dobavitelja, ki imajo status preverjanja **V postopku** ni več mogoče urejati. Za vrstico računa dobavitelja, ki se sklicuje na podizvajalsko pogodbo, je status preverjanja samodejno nastavljen na **V postopku** takoj ko se prvi dejanski strošek ujema z vrstico računa dobavitelja.

Vrstice računa dobavitelja, ki imajo status preverjanja **Popolna** ni več mogoče urejati. Ko imajo vse vrstice na računu dobavitelja ta status preverjanja, je mogoče račun dobavitelja potrditi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Povežite dejanske stroške z vrsticami računa dobavitelja

Ujemanje dejanskih stroškov pomaga pri postopku preverjanja v vrstici računa dobavitelja. Če želite uskladiti dejanske stroške z vrstico računa dobavitelja, sledite tem korakom.

1. Odprite vrstico računa dobavitelja in izberite **Neprimerljivi dejanski stroški** zavihek. Mreža prikazuje seznam dejanskih stroškov, ki se nanašajo na isto podizvajalsko vrstico kot vrstica računa dobavitelja.
2. Izberite enega ali več dejanskih stroškov in nato izberite **Ujemanje** v orodni vrstici nad mrežo. Sistem potrdi, da je izbrane dejanske stroške mogoče ujemati. Ko je preverjanje opravljeno, se dejanski stroški povežejo z vrstico računa dobavitelja.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Merila veljavnosti, ki se uporabljajo za povezavo dejanskih stroškov z vrsticami računa dobavitelja

Med postopkom ujemanja je mogoče vzpostaviti povezavo med dejanskim stroškom in vrstico računa dobavitelja le, če sta izpolnjena oba naslednja pogoja:

- The **Stanje prilagoditve** polje za vsak izbrani dejanski strošek mora biti prazno. Z drugimi besedami, dejanski stroški ne smejo biti nadomeščeni z drugimi dejanskimi stroški med postopkom odpoklica, preklica odobritve ali dnevnika popravkov.
- Vrednosti naslednjih polj se ujemajo med vrstico računa dobavitelja in izbranim dejanskim stroškom. Če katero koli polje v vrstici računa dobavitelja ni nastavljeno, se ne upošteva za ujemanje.

    - Projektna pogodba
    - Vrstica projektne pogodbe
    - Razred transakcije
    - Projekt
    - opravilo,
    - Kategorija vira
    - Kategorija transakcije
    - izdelek,
    - Podizvajalska linija
    - Vir, ki ga je mogoče rezervirati

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Odstranite ujemanje dejanskih stroškov iz vrstice računa dobavitelja

Neujemanje dejanskih stroškov lahko pomaga tudi pri postopku preverjanja na računu prodajalca, tako da omogoči odstranitev predhodno vzpostavljenih povezav. Dejanski stroški se lahko ne ujemajo samo z vrsticami računa dobavitelja, ki imajo status preverjanja **V postopku**. Če želite odstraniti ujemanje dejanskih stroškov iz vrstice računa dobavitelja, sledite tem korakom.

1. Odprite vrstico računa dobavitelja in izberite **Ujemanje dejanskih stroškov** zavihek. Mreža prikazuje seznam dejanskih stroškov, ki se sklicujejo na vrstico računa dobavitelja.
2. Izberite enega ali več dejanskih stroškov in nato izberite **Razveljavi ujemanje** v orodni vrstici nad mrežo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
