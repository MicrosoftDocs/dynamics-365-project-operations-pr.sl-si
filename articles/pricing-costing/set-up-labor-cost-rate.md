---
title: Nastavitev mer stroškov dela
description: Ta članek vsebuje informacije o nastavljanju stroškov dela v aplikaciji Project Operations
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5216c0af29eb33ce664857b1f42b4a3130f02c50
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924266"
---
# <a name="set-up-labor-cost-rates"></a>Nastavitev mer stroškov dela

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Vsak cenik ima nabor stopenj dela (cene vlog), ki se uskladijo z vsebino in datumom veljavnosti cenika.

1. Ustvarite cenik in v podmreži na zavihku **Cena vloge** izberite **Nova vloga**.
2. Na strani **Hitro ustvarjanje** izberite vlogo in organizacijsko enoto.
3. Vnesite vse druge zahtevane podatke o polju.

Naslednja tabela vključuje nekatera polja, ki so pomembna pri oblikovanju stopenj dela v ceniku z lastnimi cenami.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Vloga | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Izberite vlogo, za katero velja mera stroškov. | Vloga v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeto ceno vloge. |
| Podjetje, ki zagotavlja vire | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Izberite pravno osebo, ki ji je dodeljena vloga. Na primer razvijalec iz podjetja Fabrikam Indija ali razvijalec iz podjetja Fabrikam ZDA. | Podjetje, ki zagotavlja vire, v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeto mero stroškov vloge. |
| Enota vira | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Izberite organizacijsko enoto ali oddelek podjetja, iz katerega bo uporabljena ta vloga. Na primer razvijalec iz oddelka robotike podjetja Fabrikam Indija ali razvijalec iz oddelka za programsko opremo podjetja Fabrikam ZDA. | Enota vira v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to vrstico, da nastavi privzeto ceno vloge. |
| Cena | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Določite mero stroškov za kombinacijo vloge, podjetja, ki zagotavlja vire, in enoto vira. Na primer, stroški za razvijalca iz podjetja Fabrikam Indija so 1.000 INR ali stroški za razvijalca iz podjetja Fabrikam ZDA so 150 USD. | Cena je mera stroškov, ki privzeto določa stroške na enoto dohodne vrstice ocene ali vrstice za dejansko vrednost za razred transakcije **Čas**. |
| Valuta | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Privzeto vrednost valute prihaja iz valute v glavi cenika z lastnimi cenami, vendar jo je mogoče preglasiti. Na primer, stroški za razvijalca iz podjetja Fabrikam India so 1.000 INR. Stroški za razvijalca iz podjetja Fabrikam ZDA so 150 USD. | Ta valuta privzeto določa stroške na enoto dohodne dejanske vrstice cene za razred transakcije **Čas**. V projektni oceni se vrednost valute pretvori v valuto projekta in je prikazana v časovno razporejenem pogledu ocene. |
| Urnik enote | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Privzeti razred za urnik enote je »Čas« in ga ni mogoče spremeniti v entiteti za ceno vloge, ker se uporablja za izražanje zneskov v časovnih enotah. | To nima nadaljnjega vpliva. |
| Enota | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Privzeto vrednost prihaja iz polja **Časovna enota** v glavi cenika z lastnimi cenami. Vrednost je mogoče preglasiti. Na primer, stroški za razvijalca iz podjetja Fabrikam India so 1.000 INR na enoto **indijski dan**. Stroški za razvijalca iz podjetja Fabrikam ZDA so 150 USD na enoto **ameriški dan**. | Sistem uporablja sistem enot in pretvorbo v osnovne enote za izračun stroškov na enoto za izračun privzete cene na enoto v dohodni vrstici ocene ali vrstici za dejansko vrednost. Na primer, za razvijalca iz Indije je ocena za 10 **indijskih dni** in enota **indijski dan** je opredeljena kot 10 ur. Pri opredelitvi stroškov za vrstico ocene aplikacija izračuna strošek na enoto v vrstici ocene kot: 1.000 INR/10 h = 100 INR na uro, ki se pretvori v USD in prikaže kot strošek na enoto na strani **Ocene projekta**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Prenos cen in stroškov za vire zunaj oddelka ali pravne osebe

V podjetjih, ki poslujejo na podlagi projektov, običajno za delo na projektih uporabijo zaposlene iz različnih pravnih oseb ali oddelkov. Projekt lahko izvede ena pravna oseba, zaposleni ali svetovalci, ki delajo na projektu, pa lahko prihajajo iz iste pravne osebe ali iz druge ali pa iz kombinacije obeh. V aplikaciji Dynamics 365 Project Operations je pravna oseba, ki je lastnica izvajanja projekta, **Lastniško podjetje**, oddelek, ki je lastnik izvajanja, pa je **Pogodbena enota**. Druge pravne osebe, ki zagotavljajo sredstva, so **Podjetja, ki zagotavljajo vire** in oddelki, ki zagotavljajo vire, so **Enote vira**. V večini držav morajo podjetja zagotoviti, da pravna oseba ali oddelek, ki zagotavlja vire, lastniškemu podjetju in pogodbeni enoti zaračuna uporabo virov.

Podjetje Fabrikam mora na primer zagotoviti, da se je podjetje Fabrikam Indija – robotika dogovorilo o merah stroškov s podjetjem Fabrikam ZDA – robotika ali Fabrikam Združeno kraljestvo –robotics.

Stroški za razvijalca iz podjetja Fabrikam Indija – robotika so 100 USD, ko dela za Fabrikam ZDA – robotika, in 150 USD, ko dela za Fabrikam Združeno kraljestvo – robotika.

### <a name="set-up-costs-for-outside-resources"></a>Nastavitev stroškov za zunanje vire

1. Ustvarite cenik z lastnimi cenami, ki se imenuje *Mere stroškov za Fabrikam ZDA – robotika* in nastavite datumski obseg veljavnosti.
2. V ceniku z lastnimi cenami ustvarite mere s podatki spodnje tabele. 

| Vloga | Podjetje, ki zagotavlja vire | Enota vira | Mera stroškov |
| --- | --- | --- | --- |
| Razvijalec | Fabrikam Indija | Fabrikam Indija – Robotika | 100 USD |
| Razvijalec | Fabrikam Filipini | Fabrikam Filipini – Robotika | 90 USD |
| Razvijalec | Fabrikam ZDA | Fabrikam ZDA – Robotika | 150 USD |

3. Ta cenik z lastnimi cenami priložite organizacijski enoti podjetja Fabrikam ZDA – robotika.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Nastavitev cene prenosa za vir v ustrezni valuti 

V aplikaciji Project Operations lahko cene za vir določite v kateri koli valuti. Za valuto je privzeto nastavljeno tisto, kar je v glavi cenika, vendar je to mogoče spremeniti.

Če uporabimo primer za nastavitev cene prenosa lahko podatke spremenimo v:

Podjetje Fabrikam mora zagotoviti, da se je podjetje Fabrikam Indija – robotika dogovorilo o merah stroškov s podjetjem Fabrikam ZDA – robotika ali Fabrikam Združeno kraljestvo –robotika.

Stroški za razvijalca iz podjetja Fabrikam Indija – robotika so 5.000 INR, ko dela za Fabrikam ZDA – robotika, in 5.500 INR, ko dela za Fabrikam Združeno kraljestvo – robotika.

V ceniku z lastnimi cenami podjetja Fabrikam ZDA – robotika so mere stroškov izražene kot:

| Vloga | Podjetje, ki zagotavlja vire | Cena |
| --- | --- | --- |
| Razvijalec | Fabrikam Indija | 5.000 INR |
| Razvijalec | Fabrikam ZDA | 115 USD |

V ceniku z lastnimi cenami podjetja Fabrikam Združeno kraljestvo – robotika so mere stroškov izražene spodaj:

| Vloga | Podjetje, ki zagotavlja vire | Cena |
| --- | --- | --- |
| Razvijalec | Fabrikam Indija | 5.500 INR |
| Razvijalec | Fabrikam Združeno kraljestvo | 115 GBP |

Cenik z lastnimi cenami lahko navaja stopnje dela v več valutah. Pri izdelavi ocene stroškov za projekt aplikacija Project Operations pretvori te mere stroškov v valuto projekta in jo prikaže uporabniku. Ko je časovni vnos odobren in se ustvari dejanski strošek, se dejanski stroški izračunajo v valuti te ujemajoče se vrstice s cenami vloge na ceniku z lastnimi cenami. Dejanske stroške za čas je za posamezen projekt mogoče zabeležiti v več valutah. Vendar pa bo aplikacija Project Operations pri zbiranju ali seštevanju dejanskih stroškov dela na ravni projekta pretvorila vse zneske stroškov dela v valuto projekta, ki si jo lahko uporabnik ogleda.


[!INCLUDE[footer-include](../includes/footer-banner.md)]