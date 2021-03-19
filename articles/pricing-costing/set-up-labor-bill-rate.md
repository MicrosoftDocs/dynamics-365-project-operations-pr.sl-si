---
title: Nastavitev deležev obračunavanja dela
description: Ta tema vsebuje informacije o tem, kako nastaviti deleže obračunavanja dela v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4d09f4bf6788f93c028f084965faa6aac41a22d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274838"
---
# <a name="set-up-labor-bill-rates"></a>Nastavitev obračunske stopnje za delo

**Velja za**: za scenarije v aplikaciji Project Operations, ki temeljijo na virih/nezalogi

Vsak cenik ima nabor cen vlog ali stopenj dela, ki veljajo za kontekst in datum veljavnosti cenika, ki sta vključena v glavo cenika. Obračunske stopnje za čas v aplikaciji Dynamics 365 Project Operations lahko nastavite v samo eni valuti, ki je valuta v glavi cenika.

1. Če želite nastaviti deleže obračunavanja dela za prodajni cenik, ustvarite cenik na podlagi glave cenika. 
2. V podmreži na zavihku **Cena vloge** izberite **+ Nova cena vloge**. 
3. V podoknu **Hitro ustvarjanje** vnesite kombinacijo vloge in organizacijske enote, za katero želite nastaviti delež obračunavanja.

   Spodnja tabela vsebuje polja, ki so na zavihku **Splošno** in v podoknu **Hitro ustvarjanje** vrstice za ceno vloge, ki jo morate upoštevati pri ustvarjanju cen vloge v prodajnem ceniku:

    | Polje | LOkacija | Opis | Nadaljnji vpliv |
    | --- | --- | --- | --- |
    | Vloga | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Izberite vlogo, za katero nastavljate delež obračunavanja. | Vloga v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeti delež obračunavanja vloge. |
    | Podjetje, ki zagotavlja vire | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Izberite podjetje ali pravno osebo, iz katere prihaja vloga. Na primer razvijalec iz podjetja Fabrikam Indija ali razvijalec iz podjetja Fabrikam ZDA. | Podjetje, ki zagotavlja vire, v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeti delež obračunavanja vloge. |
    | Enota vira | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Izberite organizacijsko enoto ali oddelek podjetja, iz katere prihaja vloga. Na primer razvijalec iz oddelka robotike podjetja Fabrikam Indija ali razvijalec iz oddelka za programsko opremo podjetja Fabrikam ZDA. | Enota vira v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeti delež obračunavanja vloge. |
    | Cena | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Določite delež obračunavanja za kombinacijo vloge, podjetja, ki zagotavlja vire, in enoto vira. Na primer, delež obračunavanja za razvijalca iz podjetja Fabrikam Indija je 100 USD ali delež obračunavanja za razvijalca iz podjetja Fabrikam ZDA je 150 USD. | Ta cena je privzeti delež obračunavanja na ceno enote dohodne vrstice ocene ali vrstice za dejansko vrednost za razred transakcije »Čas«. |
    | Valuta | Zavihek **Splošno** in podokno **Hitro ustvarjanje**| Privzeto ta vrednost valute prihaja iz valute v glavi cenika. V prodajnem ceniku valute ni mogoče preglasiti. | Ta valuta je privzeta valuta cene na enoto dohodne vrstice dejanske vrednosti prodaje za razred transakcije »Čas«. |
    | Urnik enote | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Privzeti razred za urnik enote je »Čas« in ga ni mogoče spremeniti v entiteti za ceno vloge, ker se uporablja za izražanje zneskov v časovnih enotah. | To polje nima nadaljnjega vpliva. |
    | Enota | Zavihek **Splošno** in podokno **Hitro ustvarjanje** | Vrednost enote prihaja iz polja **Časovna enota** v glavi prodajnega cenika. Vendar vrednosti ni mogoče preglasiti. Na primer, delež obračunavanja za razvijalca iz podjetja Fabrikam Indija je 1.000 USD na enoto **indijski dan**. Delež obračunavanja za razvijalca iz podjetja Fabrikam ZDA je 1.500 USD na enoto **ameriški dan**. | Sistem uporablja sistem enot in pretvorbo v osnovne enote za izračun cene na enoto, ko je cena na enoto privzeto nastavljena v vrstici ocene ali vrstici za dejansko vrednost. Na primer, za razvijalca iz Indije je ocena za 10 **indijskih dni** in enota »indijski dan« je opredeljena kot 10 ur. Pri določanju cene za vrstico ocene aplikacija izračuna ceno enote na oceni kot 1.000 USD/10 ur = 100 USD na uro. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prenos cen ali nastavitev deležev obračunavanja za vire iz drugih organizacijskih enot ali oddelkov 

Podjetja, ki poslujejo na podlagi projektov, za delo na projektih pogosto uporabljajo zaposlene iz različnih pravnih oseb in različnih oddelkov znotraj pravne osebe. Projekti se lahko izvajajo iz določene pravne osebe ali oddelke, med tem ko lahko zaposleni ali svetovalci, ki delajo na projektih, prihajajo iz iste pravne osebe in oddelka ali iz druge. Projekt bi lahko sestavljala tudi kombinacija ljudi iz različnih pravnih oseb in oddelkov. V aplikaciji Project Operations je pravna oseba, ki je lastnica izvedbe projekta, **Lastniško podjetje** in oddelek, ki je lastnik izvedbe, **Pogodbena enota**. Vse druge pravne osebe, ki zagotavljajo sredstva, so **Podjetja, ki zagotavljajo vire** in oddelki, ki zagotavljajo vire, so **Enote vira**. Zaradi razlik v stroških dela med različnimi geografskimi območji in trgi dela po vsem svetu so tudi deleži obračunavanja za delo določena različno glede na geografska območja.

Na primer, urna postavka razvijalca iz oddelka robotike podjetja Fabrikam India, ki dela pri ameriškem projektu, se zaračuna v višini 100 USD na uro. Urna postavka razvijalca iz oddelka robotike podjetja Fabrikam ZDA, ki dela pri ameriškem projektu, se zaračuna v višini 150 USD na uro. 

### <a name="example-set-up-a-bill-rate"></a>Primer: nastavitev deleža obračunavanja 

1. Ustvarite prodajni cenik, ki se imenuje *Delež obračunavanja za podjetje Fabrikam ZDA*, in nastavite datumsko veljavnost.
2. V prodajni cenik vnesite naslednje podatke o stopnjah:

    | Vloga | Podjetje, ki zagotavlja vire | Enota vira | Delež obračunavanja |
    | --- | --- | --- | --- |
    | Razvijalec | Fabrikam Indija | Fabrikam Indija – robotika | 100 USD |
    | Razvijalec | Fabrikam Filipini | Fabrikam Filipini – robotika | 90 USD |
    | Razvijalec | Fabrikam ZDA | Fabrikam ZDA – robotika | 150 USD |

3. Prodajni cenik **Delež obračunavanja za podjetje Fabrikam ZDA** priložite ceniku za projekte projektne pogodbe ali določeni stranki.


[!INCLUDE[footer-include](../includes/footer-banner.md)]