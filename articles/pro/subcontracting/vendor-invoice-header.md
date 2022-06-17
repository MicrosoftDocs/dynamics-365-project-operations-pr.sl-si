---
title: Podrobnosti glave za račune dobavitelja
description: Ta članek pojasnjuje funkcionalnost, ki je na voljo v glavi računa prodajalca v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929878"
---
# <a name="header-details-for-vendor-invoices"></a>Podrobnosti glave za račune dobavitelja

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek pojasnjuje funkcionalnost, ki je na voljo v glavi računa prodajalca v Microsoftu Dynamics 365 Project Operations.

Ko vodje projektov načrtujejo in izvajajo projekte, lahko zaposlujejo podizvajalce in kupujejo izdelke in storitve od prodajalcev. Med izvajanjem projekta nastanejo stroški iz storitev, materiala in kategorij stroškov, ki so nabavljeni na podlagi podizvajalcev s prodajalci. Prodajalci zaračunajo te stroške projektom tako, da ustvarijo račune prodajalcev.

Naslednja tabela vsebuje informacije o poljih v glavah računov dobavitelja v Operacijah projekta.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime računa prodajalca. | Na vseh spustnih seznamih računov dobavitelja je v prvem stolpcu navedeno ime računa prodajalca, ki vam pomaga pri prepoznavanju računa prodajalca. Privzeto, ko je račun prodajalca ustvarjen iz podizvajalske pogodbe, se **ime** polje računa prodajalca je nastavljeno na vrednost, ki je sestavljena iz imena podizvajalske pogodbe in trenutnega datuma. |
| Description | Kratek opis storitev in izdelkov, ki so zaračunani na računu prodajalca. | Ni priprav ali omejitev |
| Dobavitelj | Ime podjetja, ki izdaja račune za izdelke in storitve. To podjetje mora biti evidenca računa, ki ima vrsto razmerja **Prodajalec** oz **dobavitelj**. | <p>Glede na izbranega prodajalca se privzete vrednosti samodejno vnesejo v naslednja polja:</p><ul><li>Valuta</li><li>Ceniki</li><li>Plačilni pogoji</li><li>Naslov za plačilo</li></ul> |
| Podizvajalska pogodba | Sklic na podizvajalsko pogodbo za račun prodajalca. | <p>Na podlagi izbrane podizvajalske pogodbe se privzete vrednosti samodejno vnesejo v naslednja polja:</p><ul><li>Valuta</li><li>Ceniki</li><li>Plačilni pogoji</li><li>Naslov za plačilo</li></ul><p>Podizvajalska pogodba, ki je izbrana v glavi računa dobavitelja, je privzeto vnesena v vrstice računa dobavitelja in je tam ni mogoče spremeniti.</p> |
| Datum računa | Datum dejanskih stroškov, ki bodo ustvarjeni, ko bo potrjen račun prodajalca. | Datum računa se uporablja tudi za izbiro pravilnega nabavnega cenika bodisi iz cenikov, ki so priloženi povezanemu ponudniku, bodisi iz parametrov projekta. |
| Razlog stanja | Status računa prodajalca. | <p>Status določa, kje je račun prodajalca v poslovnem procesu in ali ga je mogoče urejati. Tukaj je nekaj razpoložljivih vrednosti:</p><ul><li>**Osnutek** – Račun prodajalca je mogoče urejati.</li><li>**Potrjeno** – Račun prodajalca je bil preverjen in potrjen. Računov prodajalca v tem statusu ni mogoče urejati ali izbrisati.</li><li>**V teku** – Račun prodajalca je v pregledu. Račune prodajalca v tem statusu je mogoče urejati, vendar jih ni mogoče izbrisati.</li><li>**Prekinjeno** – Račun prodajalca je bil preklican. Računov prodajalca v tem statusu ni mogoče urejati ali izbrisati.</li></ul> |
| Valuta | Valuta, v kateri prodajalec izdaja račune za izdelke in storitve na računu prodajalca. | Na računu prodajalca, ki se sklicuje na podizvajalsko pogodbo, je valuta podizvajalske pogodbe privzeto vnesena kot valuta računa prodajalca. Na računu prodajalca, ki se ne sklicuje na pogodbo o podizvajanju, se privzeta vrednost vnese iz zapisa računa prodajalca in jo je mogoče spremeniti. Ko je račun prodajalca shranjen, valute ni več mogoče urejati. |
| Pogodbena enota | Oddelek podjetja, ki je odgovoren za prejemanje storitev in/ali izdelkov od prodajalca. | Ni priprav ali omejitev |
| Plačilni pogoji | Pogoji plačila na računih prodajalca, ki so izdani. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Plačilni pogoji iz podizvajalske pogodbe se kopirajo na vse račune prodajalcev, ki so povezani s podizvajalsko pogodbo. Plačilne pogoje je mogoče posodobiti, če ima račun prodajalca status **Osnutek**. |
| Naslov za plačilo | Naslov dobavitelja, na katerega je treba poslati plačila. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Plačilni naslov iz podizvajalske pogodbe se kopira kot naslov za plačilo na vse račune prodajalca, ki so ustvarjeni za to podizvajalsko pogodbo. Naslov za plačilo je mogoče posodobiti, če ima račun prodajalca status **Osnutek**. |
| Delna vsota | Če na računu prodajalca ni vrstic, vnesite vmesni seštevek računa pred davki. Če ima račun prodajalca vrstice, je to polje samo za branje. V tem primeru je prikazani znesek vmesni znesek iz vseh vrstic na računu prodajalca. | Ni priprav ali omejitev |
| Skupni davek | Če na računu prodajalca ni vrstic, vnesite skupne davke na podizvajalsko pogodbo. Če ima račun prodajalca vrstice, je to polje samo za branje. V tem primeru je prikazan znesek vsota zneskov davka iz vseh vrstic na računu prodajalca. | Ni priprav ali omejitev |
| Skupni znesek | Ta polje z izračunom prikazuje skupni znesek računa prodajalca po vključitvi davkov. | Ni priprav ali omejitev |

> [!NOTE]
> Naslednjih polj na računu prodajalca ni mogoče spremeniti, ko je račun prodajalca shranjen: **Prodajalec**, **·**, **·**, **enota**, in **Plačilni pogoji**. Če so potrebne kakršne koli spremembe teh polj na računu prodajalca, morate izbrisati račun prodajalca in ustvariti nov račun prodajalca.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
