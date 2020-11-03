---
title: Nastavitev mer stroškov in prodajnih zneskov za stroške
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za transakcije in kategorije stroškov.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084675"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Nastavitev mer stroškov in prodajnih zneskov za stroške

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko nastavite lastne in prodajne cene za kategorije transakcij. Ker so lastne in prodajne cene zasnovane za stroške, je treba vsako kategorijo transakcije, ki jih vključuje, nastaviti tudi kot kategorijo stroška. Ta nastavitev zagotavlja natančnost v nadaljnji funkcionalnosti. Lastne in prodajne cene za kategorije transakcij je mogoče navesti samo v eni valuti, ki mora biti valuta v glavi cenika.

Če želite nastaviti mere stroškov in prodajne zneske za kategorije transakcij, upoštevajte naslednje korake. 

1. Ustvarite cenik na podlagi glave cenika. 
2. Na razdelku **Cene kategorij** v meniju podmreže izberite **+ Nova cena kategorije**. 
3. Na strani **Hitro ustvarjanje** vnesite kategorijo transakcije in enoto, za katero ustvarjate novo ceno.

V spodnji tabeli so navedena polja, ki so na zavihku **Splošno** in na strani **Hitro ustvarjanje** vrstice s cenami kategorij, ki jo morate upoštevati pri ustvarjanju cen kategorij v prodajnem ceniku ali ceniku z lastnimi cenami.

| Polje | LOkacija | Ustreznost, namen in smernice | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Kategorija transakcije | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Izberite kategorijo transakcije, za katero ustvarjate lastno ali prodajno ceno. | Kategorija transakcije v dohodni vrstici ocene ali dejanske vrednosti za stroške se bo ujemala s to vrstico, da nastavi privzeto mero stroškov ali privzeti prodajni znesek kategorije transakcije. |
| Urnik enote | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Urnik enote sledi privzetim nastavitvam urnika enote kategorije transakcije. | S tega polja ni nadaljnjega vpliva. |
| Enota | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Izberite enoto, za katero se določajo cene. | Enota v dohodni vrstici ocene ali dejanske vrednosti se bo ujemala s to enoto v vrstici, da se privzeto določi cena pri oceni stroškov in dejanski vrednosti stroškov. |
| Način oblikovanja cen | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Možne vrednosti polja **Način oblikovanja cen** so **Cena na enoto** , **Nabavna cena** in **Pribitek na ceno**. | Če med nastavitvijo cene izberete vrednost **Cena na enoto** , zaklenete polje **Odstotek** v vrstici s cenami kategorij. Če izberete vrednost **Nabavna cena** , zaklenete polji **Cena** in **Odstotek** na prodajnem ceniku. Če izberete vrednost **Pribitek na ceno** zaklenete polje **Cena** na prodajnem ceniku. V dohodni vrstici za dejansko vrednost za stroške načina oblikovanja cen **Nabavna cena** ali **Pribitek na ceno** povzročita, da se ustrezni vrstici za neobračunano prodajo dodeli cena, ki je enaka ceni dejanskih stroškov ali izračunana kot pribitek na ceno. |
| Cena | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Nastavite stopnjo na enoto za kategorijo transakcije in kombinacijo enot. Na primer, stopnja kilometrine je 10 USD na miljo in 8 USD na kilometer. | Stopnja kilometrine je stopnja, ki privzeto določa ceno ali stroške na enoto dohodne vrstice ocene ali vrstice za dejansko vrednost za razred transakcije »Strošek«.|
| Odstotek | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Nastavite pribitek na ceno za kategorijo transakcije in kombinacijo enot. Na primer, prodajni znesek letalskih vozovnic mora biti višji za 10 odstotkov nad stroški nastalih stroškov za letalske vozovnice. | Ta odstotek pribitka na ceno v prodajnem ceniku velja samo, kadar je način oblikovanja cen nastavljen na **Pribitek na ceno**. |
| Valuta | Zavihek **Splošno** in strani **Hitro ustvarjanje** | Privzeto ta vrednost prihaja iz valute v glavi cenika. Pri določanju cen za kategorijo transakcije valute ni mogoče preglasiti. | Ta valuta privzeto določa ceno na enoto dohodne vrstice za dejansko vrednost za razred transakcije za stroške in prodajne cene. |

## <a name="pricing-methods-for-expenses"></a>Način oblikovanja cen za stroške

Ko nastavite cene kategorij, ki so pomembne samo v okviru oblikovanja stroškov, lahko uporabite enega od naslednjih treh načinov oblikovanja cen:

- **Cena na enoto**
- **Nabavna cena**
- **Pribitek na ceno**

### <a name="price-per-unit"></a>Cena na enoto
Ko je izbran ta način oblikovanja cen v vrstici s cenami kategorij, ki je povezana s prodajnim cenikom, se kombinacijo kategorij in enot cena privzeto nastavi v oceni in dejanski vrednosti. Ocena se nanaša na vrstice projektne ocene za stroške, podrobnosti vrstice ponudbe in podrobnosti vrstice pogodbe za stroške.

### <a name="at-cost"></a>Nabavna cena
Ko je izbran ta način oblikovanja cen v vrstici s cenami kategorij, ki je povezana s prodajnim cenikom, se kombinacijo kategorij in enot cena privzeto nastavi v dejanski vrednosti. Na primer, dejanska vrednost neobračunane prodaje za razred transakcije za stroške. Cena enote se določi za dejansko vrednost neobračunane prodaje iz cene enote na dejanskih stroških za ta strošek. Nastavljanje privzete cene na podlagi stroškov se ne izvaja pri ocenah projektov za stroške ali vrsticah ponudbe in podrobnostih pogodbe za stroške.

### <a name="markup-over-cost"></a>Pribitek na ceno
Ko je izbran ta način oblikovanja cen v vrstici s cenami kategorij, ki je povezana s prodajnim cenikom, se kombinacijo kategorij in enot cena privzeto nastavi v dejanski vrednosti. Na primer, dejanska vrednost neobračunane prodaje za razred transakcije za stroške. Po uveljavitvi določenega odstotka pribitka se ta cena enote za dejansko vrednost neobračunane prodaje določi na izračunano vrednost iz cene enote na dejanskih stroških za ta strošek. Nastavljanje privzete cene na podlagi stroškov se ne izvaja pri ocenah projektov za stroške ali vrsticah ponudbe in podrobnostih pogodbe za stroške.
