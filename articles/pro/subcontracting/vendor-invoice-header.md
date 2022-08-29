---
title: Podrobnosti glave za račune dobavitelja
description: Ta članek pojasnjuje funkcionalnost, ki je na voljo v glavi računa dobavitelja v Microsoftu Dynamics 365 Project Operations.
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

Ta članek pojasnjuje funkcionalnost, ki je na voljo v glavi računa dobavitelja v Microsoftu Dynamics 365 Project Operations.

Ko vodje projektov načrtujejo in izvajajo projekte, lahko zaposlijo podizvajalce ter kupijo izdelke in storitve od prodajalcev. Med izvajanjem projekta nastanejo stroški storitev, materialov in kategorij stroškov, ki se nabavljajo na podlagi podizvajalskih pogodb s prodajalci. Prodajalci fakturirajo te stroške projektom tako, da ustvarijo račune prodajalcev.

Naslednja tabela vsebuje informacije o poljih v glavah računov dobavitelja v Project Operations.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime računa dobavitelja. | Na vseh spustnih seznamih računov dobavitelja je ime računa dobavitelja navedeno v prvem stolpcu, da vam pomaga prepoznati račun dobavitelja. Privzeto, ko je račun dobavitelja ustvarjen iz podizvajalske pogodbe, je **Ime** polje računa dobavitelja je nastavljeno na vrednost, ki je sestavljena iz imena podizvajalca in trenutnega datuma. |
| Description | Kratek opis storitev in izdelkov, ki se fakturirajo na računu dobavitelja. | Ni priprav ali omejitev |
| Dobavitelj | Ime podjetja, ki izdaja račun za izdelke in storitve. To podjetje mora biti evidenca računa, ki ima vrsto razmerja **Prodajalec** oz **Dobavitelj**. | <p>Glede na izbranega prodajalca se privzete vrednosti samodejno vnesejo v naslednja polja:</p><ul><li>Valuta</li><li>Ceniki</li><li>Plačilni pogoji</li><li>Plačilni naslov</li></ul> |
| Podizvajalska pogodba | Sklic na podizvajalsko pogodbo za račun dobavitelja. | <p>Glede na izbrano podizvajalsko pogodbo se privzete vrednosti samodejno vnesejo v naslednja polja:</p><ul><li>Valuta</li><li>Ceniki</li><li>Plačilni pogoji</li><li>Plačilni naslov</li></ul><p>Podizvajalska pogodba, ki je izbrana v glavi računa dobavitelja, je privzeto vnesena v vrstice računa dobavitelja in je tam ni mogoče spremeniti.</p> |
| Datum računa | Datum za dejanske stroške, ki bodo ustvarjeni, ko bo potrjen račun dobavitelja. | Datum računa se uporablja tudi za izbiro pravilnega nabavnega cenika bodisi iz cenikov, ki so priloženi povezanemu prodajalcu, bodisi iz parametrov projekta. |
| Razlog stanja | Status računa dobavitelja. | <p>Status določa, kje v poslovnem procesu je račun dobavitelja in ali ga je mogoče urejati. Tukaj je nekaj razpoložljivih vrednosti:</p><ul><li>**Osnutek** – Račun dobavitelja je mogoče urejati.</li><li>**Potrjeno** – Račun dobavitelja je bil preverjen in potrjen. Računov dobaviteljev v tem statusu ni mogoče urejati ali brisati.</li><li>**V teku** – Račun dobavitelja je v pregledu. Račune dobaviteljev v tem statusu lahko urejate, ne morete pa jih izbrisati.</li><li>**Prekinjeno** – Račun dobavitelja je bil preklican. Računov dobaviteljev v tem statusu ni mogoče urejati ali brisati.</li></ul> |
| Valuta | Valuta, v kateri prodajalec izda račun za izdelke in storitve na računu prodajalca. | Na računu dobavitelja, ki se sklicuje na podizvajalsko pogodbo, je valuta podizvajalske pogodbe privzeto vnesena kot valuta računa dobavitelja. Na računu dobavitelja, ki se ne sklicuje na podizvajalsko pogodbo, je privzeta vrednost vnesena iz zapisa računa dobavitelja in jo je mogoče spremeniti. Ko je račun dobavitelja shranjen, valute ni več mogoče urejati. |
| Pogodbena enota | Oddelek podjetja, ki je odgovoren za prejemanje storitev in/ali izdelkov od prodajalca. | Ni priprav ali omejitev |
| Plačilni pogoji | Plačilni pogoji na izdanih računih dobaviteljev. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Plačilni pogoji iz podizvajalske pogodbe se kopirajo na vse račune dobavitelja, ki so povezani s podizvajalsko pogodbo. Plačilne pogoje je mogoče posodobiti, če ima račun prodajalca status **Osnutek**. |
| Plačilni naslov | Naslov dobavitelja, na katerega je treba poslati plačila. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Plačilni naslov iz podizvajalske pogodbe se kopira kot plačilni naslov na vse račune dobavitelja, ustvarjene za to podizvajalsko pogodbo. Plačilni naslov je mogoče posodobiti, če ima račun prodajalca status **Osnutek**. |
| Delna vsota | Če račun dobavitelja nima vrstic, vnesite vmesno vsoto računa pred davki. Če ima račun dobavitelja vrstice, je to polje samo za branje. V tem primeru je prikazani znesek vmesni seštevek vseh vrstic na računu dobavitelja. | Ni priprav ali omejitev |
| Skupni davek | Če račun dobavitelja nima vrstic, vnesite skupne davke na podizvajalsko pogodbo. Če ima račun dobavitelja vrstice, je to polje samo za branje. V tem primeru je prikazani znesek vsota zneskov davka iz vseh vrstic na računu dobavitelja. | Ni priprav ali omejitev |
| Skupni znesek | Ta polje z izračunom prikazuje skupni znesek računa prodajalca po vključenih davkih. | Ni priprav ali omejitev |

> [!NOTE]
> Naslednjih polj na računu dobavitelja ni mogoče spremeniti, ko je račun dobavitelja shranjen: **Prodajalec**, **·**, **·**, **enota**, in **Plačilni pogoji**. Če so potrebne kakršne koli spremembe teh polj na računu dobavitelja, morate izbrisati račun dobavitelja in ustvariti nov račun dobavitelja.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
