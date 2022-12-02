---
title: Podrobnosti glave za račune dobavitelja
description: Ta članek pojasnjuje funkcionalnost, ki je na voljo v glavi računa dobavitelja v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261703"
---
# <a name="header-details-for-vendor-invoices"></a>Podrobnosti glave za račune dobavitelja

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek pojasnjuje funkcionalnost, ki je na voljo v glavi računa dobavitelja v aplikaciji Microsoft Dynamics 365 Project Operations.

Vodja projektov, ki načrtuje in izvaja projekte, lahko zaposli podizvajalce in od dobaviteljev kupi izdelke ali naroči storitve. Med izvajanjem projekta nastanejo stroški storitev, materialov in kategorij stroškov, ki se dobavljajo na podlagi podizvajalskih pogodb z dobavitelji. Dobavitelji projektom izdajo račune za te stroške tako, da ustvarijo račune dobavitelja.

Naslednja tabela vsebuje informacije o poljih v glavi računa dobavitelja v aplikaciji Project Operations.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime računa dobavitelja. | Na vseh spustnih seznamih računa dobavitelja je ime računa dobavitelja navedeno v prvem stolpcu, da vam pomaga prepoznati račun dobavitelja. Ko je račun dobavitelja ustvarjen iz podizvajalske pogodbe, je polje **Ime** računa dobavitelja privzeto nastavljeno na vrednost, ki je sestavljena iz imena podizvajalca in trenutnega datuma. |
| Description | Kratek opis storitev in izdelkov, ki so obračunana na računu dobavitelja. | Ni priprav ali omejitev |
| Dobavitelj | Ime podjetja, ki izdaja račun za izdelke in storitve. To podjetje mora biti zapis računa, ki ima vrsto odnosa **Prodajalec** ali **Dobavitelj**. | <p>Na podlagi izbranega dobavitelja se privzete vrednosti samodejno vnesejo za naslednja polja:</p><ul><li>Valuta</li><li>Ceniki</li><li>Plačilni pogoji</li><li>Naslov za plačilo</li></ul> |
| Podizvajalska pogodba | Sklic na podizvajalsko pogodbo za račun dobavitelja. | <p>Na podlagi izbrane podizvajalske pogodbe se privzete vrednosti samodejno vnesejo za naslednja polja:</p><ul><li>Valuta</li><li>Ceniki</li><li>Plačilni pogoji</li><li>Naslov za plačilo</li></ul><p>Podizvajalska pogodba, ki je izbrana v glavi računa dobavitelja, je privzeto vnesena v vrstice računa dobavitelja in je tam ni mogoče spremeniti.</p> |
| Datum računa | Datum za dejanske stroške, ki bodo ustvarjeni, ko bo potrjen račun dobavitelja. | Datum računa se uporablja tudi za izbiro pravilnega nabavnega cenika bodisi iz cenikov, ki so priloženi sorodnemu dobavitelju, bodisi iz parametrov projekta. |
| Razlog stanja | Stanje računa dobavitelja. | <p>Stanje določa, kje je račun dobavitelja v poslovnem procesu in ali ga je mogoče urejati. Tukaj so naštete nekatere vrednosti, ki so na voljo:</p><ul><li>**Osnutek** – račun dobavitelja je mogoče urejati.</li><li>**Potrjeno** – račun dobavitelja je bil preverjen in potrjen. Računa dobavitelja v tem stanju ni mogoče urediti ali izbrisati.</li><li>**V teku** – račun dobavitelja je v pregledu. Računa dobavitelja v tem stanju ni mogoče urediti, lahko pa ga izbrišete.</li><li>**Preklicano** – račun dobavitelja je bil preklican. Računa dobavitelja v tem stanju ni mogoče urediti ali izbrisati.</li></ul> |
| Valuta | Valuta, v kateri dobavitelj izda račun za izdelke in storitve na računu dobavitelja. | Na računu dobavitelja, ki se sklicuje na podizvajalsko pogodbo, je valuta podizvajalske pogodbe privzeto vnesena kot valuta računa dobavitelja. Na računu dobavitelja, ki se ne sklicuje na podizvajalsko pogodbo, je privzeta vrednost vnesena iz zapisa računa dobavitelja in jo je mogoče spremeniti. Ko je račun dobavitelja shranjen, valute ni več mogoče urejati. |
| Pogodbena enota | Oddelek podjetja, ki je odgovoren za prejemanje storitev in/ali izdelkov od dobavitelja. | Ni priprav ali omejitev |
| Plačilni pogoji | Plačilni pogoji na izdanih računih dobaviteljev. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Plačilni pogoji iz podizvajalske pogodbe se kopirajo na vse račune dobaviteljev, ki so povezani s to podizvajalsko pogodbo. Plačilne pogoje je mogoče posodobiti, če ima račun dobavitelja stanje **Osnutek**. |
| Naslov za plačilo | Naslov dobavitelja, na katerega je treba poslati plačila. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Naslov za plačilo iz podizvajalske pogodbe se kopira kot naslov za plačilo za vse račune dobaviteljev, ki so ustvarjeni za to podizvajalsko pogodbo. Naslov za plačilo je mogoče posodobiti, če ima račun dobavitelja stanje **Osnutek**. |
| Delna vsota | Če račun dobavitelja nima vrstic, vnesite delno vsoto računa brez davkov. Če pa jih ima, je to polje namenjeno samo za branje. V tem primeru je prikazani znesek delna vsota vseh vrstic računa dobavitelja. | Ni priprav ali omejitev |
| Skupni davek | Če račun dobavitelja nima vrstic, vnesite skupno vsoto davkov na podizvajalski pogodbi. Če pa jih ima, je to polje namenjeno samo za branje. V tem primeru je prikazani znesek vsota zneskov davkov vseh vrstic računa dobavitelja. | Ni priprav ali omejitev |
| Skupni znesek | Polje z izračunom prikazuje skupni znesek v okviru računa dobavitelja po vključitvi davkov. | Ni priprav ali omejitev |

> [!NOTE]
> Naslednjih polj na računu dobavitelja ni mogoče spremeniti, ko je račun dobavitelja shranjen: **Dobavitelj**, **Podizvajalec**, **Valuta**, **Pogodbena enota** in **Plačilni pogoji**. Če so potrebne kakršne koli spremembe teh polj na računu dobavitelja, morate izbrisati račun dobavitelja in ustvariti novega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
