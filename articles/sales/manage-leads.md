---
title: Upravljanje možnih strank
description: Ta tema vsebuje informacije o upravljanju možnih strank, ki temeljijo na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898641"
---
# <a name="manage-leads"></a>Upravljanje možnih strank

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Možne stranke, ki temeljijo na projektu, je mogoče upravljati in potrditi v storitvi Project Operations. Postopek upravljanja možnih strank vključuje ustvarjanje možnih strank, ki temeljijo na projektu, in potrditvi teh možnih strank. 

## <a name="project-sales-leads"></a>Možne stranke, ki temeljijo na projektu

V razdelku **Prodaja** v levem podoknu za krmarjenje odprite stran s seznamom **Možne stranke**, da si ogledate seznam z vsemi zapisi vseh možnih strank v sistemu. Prikazani seznam možnih strank temelji na delu in drugih vrstah možnih strank, ki jih lahko ustvarite, če imate tudi aplikacijo Dynamics 365 Sales ali Dynamics 365 Field Service.

Ustvarite lahko filtrirani pogled, da si ogledate samo možne stranke, ki temeljijo na projektu, tako da ustvarite filter pri vrednosti **Vrsta**. Na primer, izberete lahko, da se prikazujejo samo možne stranke, ki temeljijo na delu.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Ustvarjanje nove možne stranke za posel, ki temelji na projektu

Ko je možna stranka, ki temelji na projektu, potrjena, se ustvarita priložnost in kupec. Priložnost, ki temelji na projektu, je izhodišče za prodajne dejavnosti v fazi priložnosti. Priložnosti, ki temeljijo na projektu, imajo edinstvene zmogljivosti, ki so potrebne za prodajo dela na projektu. Te zmogljivosti vključujejo:

- Obračunavanje časa in materiala ter fiksnih cen
- Več cenikov z datumom začetka veljavnosti za človeške vire, stroške in material, ki so bili potrebni pri projektih

Če želite potrjeni možni stranki omogočiti samodejno ustvarjanje priložnosti, nastavite atribut **Vrsta** na **Temelji na delu**, ko ustvarite možno stranko. Če izberete drugo vrsto, možna stranka ne bo ustvarila priložnosti, ki temelji na projektu, ko je potrjena. Če priložnost, ki temelji na projektu, ni ustvarjena, zmogljivosti, specifične za projekt, ne bodo na voljo v nadaljnjih prodajnih postopkih.

Naslednja tabela vključuje pomembne informacije glede polj za možno stranko in posledice teh polj v nadaljnjih postopkih.
 
| **Polje** | **Mesto** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Tema | Zavihek Splošno | To besedilno polje mora vsebovati kratek opis posla. | Tema možne stranke bo privzeto nastavljena kot tema priložnosti ter ime ponudbe in projektna pogodba. |
| Vnesi | Zavihek Splošno | To polje z naborom možnosti ima naslednje možnosti:</br>- temelji na delu (na voljo samo, če je nameščena storitev Project Operations)</br>- temelji na elementu (na voljo samo, če sta nameščeni storitvi Project Operations in Sales)</br>- temelji na vzdrževanju storitev (na voljo, ko je nameščena storitev Field Service) | Ko je vrednost tega polja nastavljena na **Temelji na delu** pri možni stranki, je možna stranka potrjena za ustvarjanje priložnosti, ki temelji na projektu. Priložnost, ki temelji na projektu, je potrebna za omogočanje vseh razširitev in funkcij, specifičnih za projekt, v nadaljnjem prodajnem postopku za ta posel. |
| Ime | Zavihek Splošno | Ime stika možnega kupca | Ko je možna stranka potrjena, se ustvarijo kupec, stik in priložnost. Tu nastavljena vrednost je ime stika. |
| Priimek | Zavihek Splošno | Priimek stika možnega kupca | Ko je možna stranka potrjena, se ustvarijo kupec, stik in priložnost. Tu nastavljena vrednost je priimek stika. |
| Podjetje | Zavihek Splošno | Ime podjetja možnega kupca | Ko je možna stranka potrjena, se ustvarijo kupec, stik in priložnost. Tu nastavljena vrednost je ime ustvarjenega kupca. |
| Valuta | Zavihek »Podrobnosti« | Valuta možnega kupca | Ko je možna stranka potrjena, se ustvarijo kupec, stik in priložnost. Tu nastavljena vrednost je valuta ustvarjenega kupca. |

## <a name="qualify-a-new-project-based-lead"></a>Potrjevanje nove možne stranke, ki temelji na projektu

Možne stranke, ki imajo vrednost **Vrsta** nastavljeno na **Temelji na delu**, se imenujejo možne stranke, ki temeljijo na projektu. Ko je potrjena možna stranka, ki temelji na projektu, se ustvari naslednje:

- Kupec, ki uporablja polje **Podjetje** pri možni stranki.
- Zapis stika, povezan s kupcem na podlagi vrednosti v poljih **Ime** in **Priimek** pri možni stranki.
- Priložnost, ki temelji na projektu, ima polje **Vrsta** nastavljeno na **Temelji na delu**.

Za podrobnejše informacije o potrjevanju možnih strank glejte[Potrjevanje ali pretvorba možnih strank](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Potrjevanje možnih strank in podatkov o pravnih osebah 

Ko zaženete Project Operations z modelom uvedbe, Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, bodo vse stranke in priložnosti zahtevale nastavitev polja **Lastniško podjetje**. Lastniško podjetje je pravna oseba v vaši organizaciji, ki je lastnica izvedbe projekta. Vsaka stranka ali kupec z vrsto odnosa »Stranka« mora imeti vrednost polja **Lastniško podjetje** nastavljeno na pravno osebo, ki sklepa pogodbe in se pogaja s to stranko. Stranka je lahko samo v eni pravni osebi.

Ko je možna stranka potrjena, bodo ustvarjeni zapisi o strankah in priložnostih imeli polje **Lastniško podjetje** nastavljeno na podjetje zapisa trenutnega uporabnika za vir, ki ga je mogoče rezervirati.

Če je zapis trenutnega uporabnika za vir, ki ga je mogoče rezervirati, prazen, se vrednost polja **Lastniško podjetje** pri uporabniškem zapisu privzeto uporablja za zapise strank in priložnosti.

## <a name="business-process-flow-for-project-based-deals"></a>Potek poslovnega procesa za posle, ki temeljijo na projektu

Za posle, ki temeljijo na projektu, v storitvi Project Operations so podprti naslednji poteki poslovnih procesov:

- Poslovni proces od možne stranke do priložnosti
- Prodajni proces priložnosti

Poslovni proces od možne stranke do priložnosti podpira naslednje stopnje:

| Ime stopnje | Preslikana entiteta | Funkcionalnost |
| --- | --- | --- |
| Kvalificiraj | Možna stranka | Potrdite možno stranko za ustvarjanje kupca, stika in priložnosti. |
| Razvoj | Priložnost | Razvijte priložnost za dodajanje več informacij o vključenem delu, ključnih zainteresiranih skupinah in konkurenci. |
| Predlaganje | Priložnost | Razvijte predlog in pridobite odobritev od skupine za notranji pregled. |
| Zaprto | Priložnost | Pridobite priložnost za sklenitev posla. |
