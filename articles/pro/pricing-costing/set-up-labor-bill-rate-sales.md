---
title: Nastavitev obračunske stopnje za delo – poenostavljeno
description: Ta tema vsebuje informacije o nastavljanju deležev obračunavanja dela v aplikaciji Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b8c4a19260156480e40f2cc26afa83df3ec9fe9de53edc0ad0ca8c7b78bf352
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007616"
---
# <a name="set-up-labor-bill-rates---lite"></a>Nastavitev obračunske stopnje za delo – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Vsak cenik ima nabor cen vlog ali stopenj dela, ki veljajo za kontekst in datum veljavnosti cenika, ki sta vključena v glavo cenika. Obračunske stopnje za čas v aplikaciji Dynamics 365 Project Operations lahko nastavite v samo eni valuti, ki je valuta v glavi cenika.

1. Če želite nastaviti deleže obračunavanja dela za prodajni cenik, ustvarite cenik na podlagi glave cenika. 
2. V podmreži na zavihku **Cena vloge** izberite **+ Nova cena vloge**. 
3. V podoknu **Hitro ustvarjanje** vnesite kombinacijo vloge in organizacijske enote, za katero želite nastaviti delež obračunavanja.

  Spodnja tabela vsebuje polja, ki so na zavihku **Splošno** in v podoknu **Hitro ustvarjanje** vrstice za ceno vloge, ki jo morate upoštevati pri ustvarjanju cen vloge v prodajnem ceniku:

  | Polje | LOkacija | Opis | Nadaljnji vpliv |
  | --- | --- | --- | --- |
  | Vloga | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Izberite vlogo, za katero nastavljate delež obračunavanja. | Vloga v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeti delež obračunavanja vloge. |
  | Enota vira | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Izberite organizacijsko enoto ali oddelek podjetja, iz katere prihaja vloga. Na primer razvijalec iz oddelka robotike podjetja Fabrikam Indija ali razvijalec iz oddelka za programsko opremo podjetja Fabrikam ZDA. | Enota vira v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeti delež obračunavanja vloge. |
  | Cena | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Določite delež obračunavanja za kombinacijo vloge, podjetja, ki zagotavlja vire, in enoto vira. Na primer, delež obračunavanja za razvijalca iz podjetja Fabrikam Indija je 100 USD ali delež obračunavanja za razvijalca iz podjetja Fabrikam ZDA je 150 USD. | Ta cena je privzeti delež obračunavanja na ceno enote dohodne vrstice ocene ali vrstice za dejansko vrednost za razred transakcije »Čas«. |
  | Valuta | Zavihek **Splošno** in podokno **Hitro ustvarjanje**| Privzeto ta vrednost valute prihaja iz valute v glavi cenika. V prodajnem ceniku valute ni mogoče preglasiti. | Ta valuta je privzeta valuta cene na enoto dohodne vrstice dejanske vrednosti prodaje za razred transakcije »Čas«. |
  | Urnik enote | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Privzeti razred za urnik enote je »Čas« in ga ni mogoče spremeniti v entiteti za ceno vloge, ker se uporablja za izražanje zneskov v časovnih enotah. | To polje nima nadaljnjega vpliva. |
  | Enota | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Vrednost enote prihaja iz polja **Časovna enota** v glavi prodajnega cenika. Vendar vrednosti ni mogoče preglasiti. Na primer, delež obračunavanja za razvijalca iz podjetja Fabrikam Indija je 1.000 USD na enoto **indijski dan**. Delež obračunavanja za razvijalca iz podjetja Fabrikam ZDA je 1.500 USD na enoto **ameriški dan**. | Sistem uporablja sistem enot in pretvorbo v osnovne enote za izračun cene na enoto, ko je cena na enoto privzeto nastavljena v vrstici ocene ali vrstici za dejansko vrednost. Na primer, za razvijalca iz Indije je ocena za 10 **indijskih dni** in enota »indijski dan« je opredeljena kot 10 ur. Pri določanju cene za vrstico ocene aplikacija izračuna ceno enote na oceni kot 1.000 USD/10 ur = 100 USD na uro. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prenos cen ali nastavitev deležev obračunavanja za vire iz drugih organizacijskih enot ali oddelkov 

Podjetja, ki poslujejo na podlagi projektov, za delo na projektih uporabijo zaposlene iz različnih oddelkov podjetja. Projekti se lahko izvajajo iz enega oddelka, medtem ko zaposleni ali svetovalci prihajajo iz istega ali različnega oddelka podjetja. Projekt bi lahko sestavljala tudi kombinacija ljudi iz različnih oddelkov. V aplikaciji Project Operations se podjetje, ki je lastnik izvedbe projekta, imenuje **Pogodbena enota**. Vsi drugi oddelki, ki zagotavljajo vire, se imenujejo **Enote vira**. Zaradi razlik v stroških dela med različnimi geografskimi območji in trgi dela po vsem svetu so tudi deleži obračunavanja za delo določena različno glede na geografska območja.

Na primer, urna postavka razvijalca iz podjetja Fabrikam India, ki dela pri ameriškem projektu, se zaračuna v višini 100 USD na uro. Urna postavka razvijalca iz podjetja Fabrikam ZDA, ki dela pri ameriškem projektu, se zaračuna v višini 150 USD na uro.

### <a name="example-set-up-a-bill-rate"></a>Primer: nastavitev deleža obračunavanja

1. Ustvarite prodajni cenik, ki se imenuje *Delež obračunavanja za podjetje Fabrikam ZDA*, in nastavite datumsko veljavnost.
2. V prodajni cenik vnesite naslednje podatke o stopnjah:

    | Vloga | Organizacijska enota | Delež obračunavanja |
    | --- | --- | --- |
    | Razvijalec | Fabrikam Indija | 100 USD |
    | Razvijalec | Fabrikam Filipini | 90 USD |
    | Razvijalec | Fabrikam ZDA | 150 USD |

3. Prodajni cenik **Delež obračunavanja za podjetje Fabrikam ZDA** priložite ceniku za projekte projektne pogodbe ali določeni stranki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]