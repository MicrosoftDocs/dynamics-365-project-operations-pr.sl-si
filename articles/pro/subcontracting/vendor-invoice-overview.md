---
title: Izdajanje računov dobaviteljem – koncept in ustvarjanje
description: Ta članek opisuje koncept računov, uporabnih scenarijev dobavitelja in pojasnjuje, kako ustvarite račune dobavitelja v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261964"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Izdajanje računov dobaviteljem – koncept in ustvarjanje

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Izdajanje računov dobaviteljem v aplikaciji Microsoft Dynamics 365 Project Operations se lahko uporablja za zapisovanje stroškov dobav storitev in/ali materialov za projekt, ki jih izvede dobavitelj.

Kadar so storitve in/ali materiali oddani v podizvajanje dobavitelju, podizvajalska pogodba predstavlja pogodbeni dogovor s tem dobaviteljem. Ko dobavitelj opravlja storitve ali ko so materiali prejeti in uporabljeni za opravila projekta, se stroški zapišejo za projekt. Dobavitelj občasno pošilja račune, ki so preverjeni in usklajeni s stroški, zabeleženimi za projekt. Po končanem postopku preverjanja je račun dobavitelja potrjen in sproščen v plačilo.

## <a name="scenarios-for-use"></a>Uporabni scenariji

Račune dobaviteljev v aplikaciji Project Operations lahko uporabite za podporo dveh različnih scenarijev.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Stranke uporabljajo vse izkušnje podizvajalske pogodbe

Izkušnje računov dobavitelja ponujajo način za preverjanje časovnih vnosov, porabe materiala in vnosov stroškov, ki se nanašajo na podizvajalske komponente, in njihovo ujemanje z vrsticami računa dobavitelja. Ta proces je mogoče uporabiti za preverjanje točnosti vrstic računa dobavitelja. Ko je postopek preverjanja končan in je račun dobavitelja potrjen, aplikacija razveljavi dejanske vrednosti, ki so bile zapisane v odobrenih dnevnikih časa, stroškov in porabe materiala, nato pa ustvari nove dejanske stroške z vrsticami računa dobavitelja.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Stranke ne uporabljajo vseh izkušenj podizvajalske pogodbe, ampak želijo imeti enoten pogled na stroške projektov v aplikaciji Project Operations

Če sledite procesu podizvajalske pogodbe v sistemu drugega ponudnika, lahko beležite stroške iz tega sistema v aplikaciji Project Operations tako, da ustvarite račune dobavitelja, ki se ne sklicujejo na podizvajalske pogodbe. Na ta način imajo lahko vaše vodje projekta en poenoten pogled na vse stroške na določenem projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Ustvarjanje računov dobaviteljev v aplikaciji Project Operations

Račune dobavitelja lahko ustvarite na dva načina:

- Na strani s seznamom računov dobavitelja ali na strani s podrobnostmi za račun posameznega dobavitelja
- Na strani s seznamom podizvajalskih pogodb ali strani s podrobnostmi za posamezno podizvajalsko pogodbo

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Ustvarjanje s strani s seznamom računov dobavitelja ali strani s podrobnostmi

1. Odprite razdelek **Nakup** \> **Računi dobavitelja**.
2. Na strani s seznamom računov dobavitelja ali strani s podrobnostmi za posamezen račun dobavitelja izberite možnost **Novo**, da ustvarite nov račun dobavitelja.

Računi dobavitelja, ki so ustvarjeni na ta način, se lahko sklicujejo tudi na podizvajalsko pogodbo.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Ustvarjanje s strani s seznamom podizvajalcev ali strani s podrobnostmi

1. Odprite razdelek **Nakup** \> **Podizvajalske pogodbe**.
2. Izberite eno ali več podizvajalskih pogodb.
3. Na strani s seznamom podizvajalskih pogodb ali strani s podrobnostmi za posamezno podizvajalsko pogodbo izberite možnost **Ustvarjanje računa dobavitelja**, da ustvarite nov račun dobavitelja.

Nov račun dobavitelja s stanjem **Osnutek** se ustvari za vsako podizvajalsko pogodbo, ki ste jo izbrali.

Računi dobavitelja, ki jih ustvarite na ta način, se vedno sklicujejo na podizvajalsko pogodbo v glavi računa dobavitelja. Vsaka vrstica v podizvajalski pogodbi, ki ima način obračunavanja »Čas in material«, bo povzročila ustvarjanje vrstice na računu dobavitelja. Vsaka vrstica v podizvajalski pogodbi, ki ima način zaračunavanja »Nespremenljiva cena«, bo povzročila ustvarjanje vrstice na računu dobavitelja za vsak mejnik podrobnosti podizvajalske pogodbe, ki ima stanje **Pripravljeno za izdajanje računov**.

Naslednja polja in povezani zapisi bodo kopirani iz podizvajalske pogodbe v glavo računa dobavitelja:

- Dobavitelj.
- Povezani ceniki bodo kopirani na račun prodajalca kot ceniki.
- Valuta
- Pogodbena enota.
- Plačilni pogoji.

Za podrobnosti podizvajalske pogodbe »Čas in material« bodo naslednja polja in povezani zapisi kopirani iz podrobnosti podizvajalske pogodbe v vrstico računa dobavitelja:

- Sklici podizvajalskih pogodb in podrobnosti podizvajalske pogodbe
- Razred transakcije
- Vloga
- Kategorija transakcije
- Polja izdelka
- Projekt
- opravilo,
- Vir, ki ga je mogoče rezervirati

Za podrobnosti podizvajalske pogodbe »Nespremenljiva cena« bodo naslednja polja kopirana iz podrobnosti podizvajalske pogodbe in mejnika podrobnosti podizvajalske pogodbe v vrstico računa dobavitelja:

- Sklici podizvajalskih pogodb in podrobnosti podizvajalske pogodbe.
- Razred transakcije. Privzeto bo nastavljena vrednost **Mejnik**.
- Ime mejnika in znesek bosta kopirana iz povezanega mejnika podrobnosti podizvajalske pogodbe.
- Uporabnik bo lahko v vrstici računa dobavitelja izbral projekt in opravilo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
