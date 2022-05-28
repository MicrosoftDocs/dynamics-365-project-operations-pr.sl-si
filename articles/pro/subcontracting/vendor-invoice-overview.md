---
title: Izdajanje računov prodajalcem – koncept in izdelava
description: Ta tema opisuje koncept računov dobavitelja, scenarije za uporabo in kako ustvariti račune dobaviteljev v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580568"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Izdajanje računov prodajalcem – koncept in izdelava

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Izdajanje računov prodajalcem v Microsoftu Dynamics 365 Project Operations se lahko uporablja za evidentiranje stroškov iz dobave storitev in/ali materiala na projektu s strani prodajalcev.

Ko so storitve in/ali materiali oddani v podizvajalce s prodajalcem, podizvajalska pogodba predstavlja pogodbeno pogodbo s tem prodajalcem. Ko prodajalec izvaja storitve ali je material prejet in uporabljen pri projektnih nalogah, se stroški evidentirajo v projektu. Prodajalec občasno pošilja račune, ki so preverjeni in usklajeni s stroški, ki so zabeleženi v projektu. Po končanem postopku preverjanja se račun prodajalca potrdi in sprosti v plačilo.

## <a name="scenarios-for-use"></a>Scenariji za uporabo

Računi prodajalcev v projektnih operacijah se lahko uporabljajo za podporo dveh različnih scenarijev.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Stranke uporabljajo vse izkušnje s podizvajalci

Izkušnje z računi prodajalca omogočajo preverjanje in ujemanje vnosov časa, porabe materiala in vnosov stroškov, ki se sklicujejo na komponente podizvajalcev z vrsticami računov dobavitelja. Ta postopek se lahko uporablja za preverjanje točnosti vrstic računa prodajalca. Ko je postopek preverjanja zaključen in je račun prodajalca potrjen, bo aplikacija razveljavila dejanske vrednosti, ki so bile zabeležene v potrjenih dnevnikih časa, stroškov in porabe materiala, ter ustvarila nove dejanske stroške z uporabo vrstic računa prodajalca.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Stranke ne uporabljajo vseh izkušenj s podizvajalci, ampak želijo imeti enoten pogled na stroške projektov v Project Operations

Če sledite postopku oddaje podizvajalcev v sistemu tretje osebe, lahko stroške iz tega sistema tretje osebe zabeležite v Project Operations, tako da ustvarite račune prodajalca, ki se ne sklicujejo na podizvajalske pogodbe. Na ta način imajo lahko vodje vaših projektov enoten, enoten pogled na vse stroške na določenem projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Izdelava računov dobaviteljev v projektnih operacijah

Račune prodajalca lahko ustvarite na dva načina:

- Na strani s seznamom računov dobavitelja ali strani s podrobnostmi za račun posameznega ponudnika
- S strani s seznamom podizvajalcev ali strani s podrobnostmi za posamezno podizvajalsko pogodbo

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Ustvarjanje na strani s seznamom računov dobavitelja ali strani s podrobnostmi

1. Pojdi do **Nakup** \> **Računi prodajalca**.
2. Na strani s seznamom računov dobavitelja ali strani s podrobnostmi za račun posameznega ponudnika izberite **Novo** ustvariti nov račun prodajalca.

Računi prodajalca, ki so ustvarjeni na ta način, se lahko sklicujejo tudi na podizvajalsko pogodbo.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Ustvarjanje na strani s seznamom podizvajalcev ali strani s podrobnostmi

1. Pojdi do **Nakup** \> **Podizvajalci**.
2. Izberite eno ali več podizvajalcev.
3. Na strani s seznamom podizvajalcev ali strani s podrobnostmi za posamezno podizvajanje izberite **Ustvarite račun prodajalca** ustvariti nov račun prodajalca.

Nov račun prodajalca **Osnutek** status se ustvari za vsako podizvajalsko pogodbo, ki ste jo izbrali.

Računi dobavitelja, ki jih ustvarite na ta način, se vedno sklicujejo na podizvajalsko pogodbo v glavi računa dobavitelja. Vsaka vrstica podizvajalske pogodbe, ki ima način obračunavanja časa in materiala, bo povzročila, da se na računu prodajalca ustvari vrstica. Vsaka vrstica v podizvajalski pogodbi, ki ima način obračunavanja s fiksno ceno, bo povzročila, da se na računu prodajalca ustvari vrstica za vsak mejnik vrstice podizvajalcev, ki ima status **Pripravljen za fakturiranje**.

Naslednja polja in povezani zapisi bodo kopirani iz podizvajalske pogodbe v glavo računa prodajalca:

- Prodajalec.
- Povezani ceniki bodo kopirani na račun prodajalca kot ceniki.
- Valuta
- Pogodbena enota.
- Plačilni pogoji.

Za vrstice podizvajalcev za čas in material bodo naslednja polja in povezani zapisi kopirani iz vrstice podizvajalcev v vrstico računa prodajalca:

- Sklici na vrstice podizvajalcev in podizvajalcev
- Razred transakcije
- Vloga
- Kategorija transakcije
- Polja izdelkov
- Projekt
- opravilo,
- Vir, ki ga je mogoče rezervirati

Za vrstice podizvajalcev s fiksno ceno bodo naslednja polja kopirana iz vrstice podizvajalcev in mejnika vrstice podizvajalcev v vrstico računa prodajalca:

- Sklici na vrstice podizvajalcev in podizvajalcev.
- Transakcijski razred. Privzeto bo vrednost **Mejnik**.
- Ime in znesek mejnika bosta kopirana iz povezanega mejnika podizvajalske vrstice.
- Uporabnik bo lahko izbral projekt in nalogo v vrstici računa prodajalca.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
