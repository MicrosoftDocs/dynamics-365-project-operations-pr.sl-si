---
title: Vrstice podizvajalske pogodbe, vezane na čas
description: Ta tema pojasnjuje, kako zapisati vrstice podizvajalske pogodbe, vezane na čas, in zabeležiti odkup časa od dobaviteljev.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547264"
---
# <a name="subcontract-lines-for-time"></a>Vrstice podizvajalske pogodbe, vezane na čas

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podizvajalska pogodba v storitvi Dynamics 365 Project Operations lahko vsebuje vrstico podizvajalske pogodbe, vezane na čas. Vrstice podizvajalske pogodbe, vezane na čas, vodji projekta omogočajo, da kupi čas dobaviteljevih virov za osebje projektnih nalog in zahteve za vir.

Dokončajte spodnje korake, da v storitvi Project Operations ustvarite vrstico podizvajalske pogodbe, vezane na čas.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe** in odprite podizvajalsko pogodbo.
2. V zavihku **Vrstice podizvajalske pogodbe** izberite **+ Novo**, da ustvarite novo vrstico podizvajalske pogodbe.
3. Na strani **Hitro ustvarjanje**, v polju **Razred transakcije**, izberite **Čas**.
4. Vnesite preostale podatke o polju in kliknite **Shrani**.

  Spodnja tabela vsebuje informacije o poljih na straneh **Vrstica podizvajalske pogodbe** in **Hitro ustvarjanje**.

| **Polje** | **Opis** | **Funkcionalni vpliv** |
| --- | --- | --- |
| Imenu | Ime podrobnosti podizvajalske pogodbe za pomoč pri identifikaciji. | To bo prikazano kot prvi stolpec v vseh iskanjih na podlagi podrobnosti podizvajalske pogodbe. |
| Opis | Kratek opis storitev, ki jih naročate v vrstici podizvajalske pogodbe. |Brez |
| Vrsta vrstice |   Privzeta vrednost tega polja je **Temelji na količini**.| Brez |
| Način obračunavanja | To je nabor možnosti, ki predstavlja dva glavna pogodbena modela, ki ju aplikacija Project Operations podpira: **Fiksna cena** in **Čas in material**. | Na podlagi izbranega načina obračunavanja je na voljo razpored za izdajanje računov, ki temelji na mejnikih, za podrobnosti podizvajalske pogodbe z načinom obračunavanja fiksne cene. |
| Razred transakcije | Privzeta vrednost je **Čas**. | To označuje, da se podrobnosti podizvajalske pogodbe uporabljajo za beleženje nakupa časa podizvajalca. |
| Vloga | Izberite vlogo vira podizvajalske pogodbe, katerega čas se kupuje. | Vloga, ki jo izvaja vir podizvajalske pogodbe, določa ceno nakupa. |
| Zahtevani datum začetka | Vnesite datum, kdaj morajo viri podizvajalcev začeti delati. | To se uporablja za izbiro cenika projekta iz cenikov projektov, priloženih podizvajalski pogodbi. Cena vloge v podrobnostih podizvajalske pogodbe izhaja iz tega cenika. |
| Zahtevani konec | Vnesite datum, ko se dodelitev vira podizvajalca konča. | To bo uporabljeno za prikaz opozoril, ko vodja projekta črpa zmogljivosti za potrebe virov, ki se pojavijo po tem datumu. |
| Naročena količina | Vnesite število ur vloge, ki se kupuje od dobavitelja. | To bo uporabljeno za prikaz opozoril, ko vodja projekta črpa čez te zmogljivosti za potrebe virov. |
| Skupina enot | Privzeta vrednost je **Skupina časovnih enot**, česar ni mogoče spremeniti. | Brez|
| Enota | Privzeta za to polje je osnovna enota ur iz možnosti **Skupina časovnih enot**. To vrednost lahko spremenite, če želite kupiti katero koli od možnosti **Skupina časovnih enot**, na primer dan ali teden. | Kombinacija **Vloga** in **Enota** bo uporabljena kot privzeta ali izračunana za ceno enote za podrobnosti podizvajalske pogodbe. |
| Cena enote | Privzeta cena enote uporablja kombinacijo možnosti **Vloga** in **Enota** iz cenika projekta, veljavnega za datum **Zahtevani začetek** v podrobnostih podizvajalske pogodbe. | Kadar je cena v veljavnem ceniku projekta določena v drugačni enoti kot enota v vrstici podizvajalske pogodbe, sistem za izračun cene na enoto uporabi pretvorbo enote. |
| Delna vsota |    To je polje samo za branje, ki se izračuna kot količina x cena na enoto, če vnesete vrednosti količine in cene na enoto. Če je prazno bodisi polje količina, cena enote ali pa sta prazna oba, lahko vrednost vnesete v polje. | Brez|
| Prometni davek |   Vnesite znesek prometnega davka. |Brez |
| Skupni znesek | Skupni znesek vrstice podizvajalske pogodbe z vključenimi davki. Vrednost tega polja je izračunana na naslednji način: delni znesek + prometni davek.|Brez |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]