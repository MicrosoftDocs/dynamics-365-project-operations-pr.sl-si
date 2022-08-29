---
title: Izdajanje računov dobaviteljem – koncept in ustvarjanje
description: Ta članek opisuje koncept dobaviteljskih računov, scenarije za uporabo in kako ustvariti dobaviteljske račune v Microsoftu Dynamics 365 Project Operations.
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

Fakturiranje dobavitelja v Microsoftu Dynamics 365 Project Operations se lahko uporablja za beleženje stroškov dobav storitev in/ali materialov na projektu s strani prodajalcev.

Kadar so storitve in/ali materiali oddani v podizvajanje prodajalcu, podizvajalska pogodba predstavlja pogodbeni dogovor s tem prodajalcem. Ko prodajalec opravi storitve ali ko materiale prejme in uporabi pri projektnih nalogah, se stroški evidentirajo na projektu. Občasno prodajalec pošilja račune, ki so preverjeni in usklajeni s stroški, ki so zabeleženi na projektu. Po končanem postopku preverjanja je račun dobavitelja potrjen in sproščen v plačilo.

## <a name="scenarios-for-use"></a>Scenariji za uporabo

Račune dobaviteljev v Project Operations je mogoče uporabiti za podporo dveh različnih scenarijev.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Stranke uporabljajo vse izkušnje podizvajalcev

Izkušnje z računi dobavitelja ponujajo način za preverjanje in ujemanje časovnih vnosov, porabe materiala in vnosov stroškov, ki se nanašajo na podizvajalske komponente z vrsticami računa dobavitelja. Ta postopek je mogoče uporabiti za preverjanje točnosti vrstic računa dobavitelja. Ko je postopek preverjanja končan in je račun dobavitelja potrjen, bo aplikacija razveljavila dejanske vrednosti, ki so bile zabeležene v odobrenih dnevnikih časa, stroškov in porabe materiala, ter ustvarila nove dejanske stroške z uporabo vrstic računa dobavitelja.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Stranke ne uporabljajo vseh podizvajalskih izkušenj, vendar želijo imeti enoten pogled na stroške projektov v projektnih operacijah

Če sledite postopku podizvajanja v sistemu tretje osebe, lahko beležite stroške iz tega sistema tretje osebe v Project Operations tako, da ustvarite račune dobavitelja, ki se ne sklicujejo na podizvajalske pogodbe. Na ta način imajo lahko vaši vodje projektov enoten, poenoten pogled na vse stroške na določenem projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Izdelava računov dobaviteljev v projektnih operacijah

Račune dobavitelja lahko ustvarite na dva načina:

- Na strani s seznamom računov dobavitelja ali na strani s podrobnostmi za račun posameznega dobavitelja
- Na strani s seznamom podizvajalcev ali strani s podrobnostmi za posamezno podizvajalsko pogodbo

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Ustvarjanje s strani s seznamom računov dobavitelja ali strani s podrobnostmi

1. Pojdi do **Nakupovanje** \> **Računi prodajalcev**.
2. Na strani s seznamom računov dobavitelja ali strani s podrobnostmi za posamezen račun dobavitelja izberite **Novo** za ustvarjanje novega računa dobavitelja.

Računi dobavitelja, ki so ustvarjeni na ta način, se lahko sklicujejo tudi na podizvajalsko pogodbo.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Ustvarjanje s strani s seznamom podizvajalcev ali strani s podrobnostmi

1. Pojdi do **Nakupovanje** \> **Podizvajalske pogodbe**.
2. Izberite eno ali več podizvajalskih pogodb.
3. Na strani s seznamom podizvajalcev ali strani s podrobnostmi za posamezno podizvajalce izberite **Ustvarite račun dobavitelja** za ustvarjanje novega računa dobavitelja.

Nov račun dobavitelja v **Osnutek** status se ustvari za vsako podizvajalsko pogodbo, ki ste jo izbrali.

Računi dobavitelja, ki jih ustvarite na ta način, se vedno sklicujejo na podizvajalsko pogodbo v glavi računa dobavitelja. Vsaka vrstica v podizvajalski pogodbi, ki ima metodo zaračunavanja časa in materiala, bo povzročila ustvarjanje vrstice na računu dobavitelja. Vsaka vrstica v podizvajalski pogodbi, ki ima metodo zaračunavanja po fiksni ceni, bo povzročila ustvarjanje vrstice na računu dobavitelja za vsak mejnik podizvajalske vrstice, ki ima status **Pripravljen za fakturiranje**.

Naslednja polja in povezani zapisi bodo kopirani iz podizvajalske pogodbe v glavo računa dobavitelja:

- Prodajalec.
- Povezani ceniki bodo kopirani na račun prodajalca kot ceniki.
- Valuta
- Pogodbena enota.
- Plačilni pogoji.

Za podizvajalske vrstice Čas in material bodo naslednja polja in povezani zapisi kopirani iz podizvajalske vrstice v vrstico računa dobavitelja:

- Reference podizvajalcev in podizvajalcev
- Razred transakcije
- Vloga
- Kategorija transakcije
- Polja izdelkov
- Projekt
- opravilo,
- Vir, ki ga je mogoče rezervirati

Za podizvajalske vrstice s fiksno ceno bodo naslednja polja kopirana iz podizvajalske vrstice in mejnika podizvajalske vrstice v vrstico računa dobavitelja:

- Reference podizvajalcev in podizvajalcev.
- Transakcijski razred. Privzeto bo vrednost **Mejnik**.
- Ime mejnika in znesek bosta kopirana iz povezanega mejnika vrstice podizvajalca.
- Uporabnik bo lahko izbral projekt in nalogo na vrstici računa dobavitelja.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
