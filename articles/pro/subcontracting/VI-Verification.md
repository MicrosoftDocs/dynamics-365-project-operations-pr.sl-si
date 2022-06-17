---
title: Preverjanje računov dobavitelja z odobrenimi dejanskimi vrednostmi
description: Ta članek pojasnjuje, kako Microsoft Dynamics 365 Project Operations naj vodje projektov preverijo račune dobaviteljev z dejanskim stanjem, ki so bili odobreni, saj so izvajalci opravili delo in evidentiran čas ter stroške in materiale, ki so jih porabili člani projektne skupine.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914238"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Preverjanje računov dobavitelja z odobrenimi dejanskimi vrednostmi

[!include [banner](../../includes/dataverse-preview.md)]

_ **Velja za:** Lite uvedba – dogovor s predračunom

Microsoft Dynamics 365 Project Operations naj vodje projektov preverijo vrstice računov prodajalca na naslednje načine:

- Uporabi **Stanje preverjanja** polje v vrsticah računa prodajalca.
- Če se vrstice računa prodajalca sklicujejo na vrstico podizvajalcev, povežite dejanske stroške iz dejavnosti podizvajalca s temi vrsticami računa prodajalca. Povezava je ustvarjena tako, da se dejanski stroški ujemajo z vrsticami računa prodajalca.

    > [!NOTE]
    > Čeprav je stanje preverjanja mogoče slediti za vrstice računov prodajalca, ki se ne sklicujejo na podizvajalsko pogodbo, dejanskih stroškov ni mogoče povezati s temi vrsticami računov dobavitelja.

## <a name="verification-status"></a>Stanje preverjanja

The **Stanje preverjanja** polje v vrstici računa prodajalca označuje status preverjanja. Podprta so naslednja stanja:

1. Ni začeto
2. Poteka
3. Zaključevanje

Vrstice računov prodajalca, ki imajo status preverjanja **Ni se začelo** se lahko ureja.

Vrstice računov prodajalca, ki imajo status preverjanja **V postopku** ni več mogoče urejati. Za vrstico računa prodajalca, ki se sklicuje na podizvajalsko pogodbo, je status preverjanja samodejno nastavljen na **V postopku** takoj ko se prvi dejanski strošek ujema z vrstico računa prodajalca.

Vrstice računov prodajalca, ki imajo status preverjanja **Dokončano** ni več mogoče urejati. Ko imajo vse vrstice na računu prodajalca ta status preverjanja, je mogoče račun prodajalca potrditi.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Uskladite dejanske stroške z vrsticami računa prodajalca

Usklajevanje dejanskih stroškov pomaga pri postopku preverjanja v vrstici računa prodajalca. Če želite uskladiti dejanske stroške z vrstico računa prodajalca, sledite tem korakom.

1. Odprite vrstico za račun prodajalca in izberite **Neprimerljivi dejanski stroški** zavihek. Mreža prikazuje seznam dejanskih stroškov, ki se sklicujejo na isto vrstico podizvajalcev kot vrstica računa prodajalca.
2. Izberite eno ali več dejanskih stroškov in nato izberite **Tekma** na orodni vrstici nad mrežo. Sistem potrdi, da se izbrani dejanski stroški lahko ujemajo. Po opravljeni validaciji so dejanski stroški povezani z vrstico računa prodajalca.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Merila za potrditev, ki se uporabljajo za povezavo dejanskih stroškov z vrsticami računov prodajalca

Med postopkom ujemanja je mogoče vzpostaviti povezavo med dejansko ceno in vrstico računa prodajalca le, če sta izpolnjena oba naslednja pogoja:

- The **Stanje prilagoditve** polje za vsak izbrani dejanski strošek mora biti prazno. Z drugimi besedami, dejanski stroški ne smejo biti zamenjani z drugimi dejanskimi stroški med postopkom odpoklica, preklica odobritve ali dnevnika popravkov.
- Vrednosti naslednjih polj se ujemajo med vrstico računa prodajalca in izbranim dejanskim stroškom. Če katero koli polje ni nastavljeno v vrstici računa prodajalca, se ne upošteva za ujemanje.

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

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Neujemanje dejanskih stroškov iz vrstice računa prodajalca

Neujemanje dejanskih stroškov lahko pomaga tudi pri postopku preverjanja na računu prodajalca, tako da omogoči odstranitev predhodno vzpostavljenih povezav. Dejanski stroški so lahko neusklajeni samo iz vrstic računov prodajalca, ki imajo status preverjanja **V postopku**. Če želite razveljaviti dejanske stroške iz vrstice računa prodajalca, sledite tem korakom.

1. Odprite vrstico za račun prodajalca in izberite **Ustrezni dejanski stroški** zavihek. Mreža prikazuje seznam dejanskih stroškov, ki se sklicujejo na vrstico računa prodajalca.
2. Izberite eno ali več dejanskih stroškov in nato izberite **Neprimerljivo** na orodni vrstici nad mrežo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
