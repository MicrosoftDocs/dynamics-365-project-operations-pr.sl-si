---
title: Preslikava projektov in opravil v podrobnosti pogodbe, ki temeljijo na projektih – poenostavljeno
description: Ta članek vsebuje informacije o dodajanju in odstranjevanju projektov in opravil v pogodbeno vrstico.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c8075e3161acd904969f964e5ab32dfe04edc4b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932546"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Preslikava projektov in opravil v podrobnosti pogodbe, ki temeljijo na projektih 

_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/manjkajoči zalogi_

V podrobnostih pogodb, ki temeljijo na projektu, lahko določena opravila v projektu preslikate v podrobnosti pogodbe.

Ko preslikate določena opravila v podrobnosti pogodbe, bodo način obračunavanja, možnosti zaračunavanja, omejitve »Ni dovoljeno preseči« in stranke, opredeljene v podrobnosti pogodbe, veljali samo za ta določena opravila.

Če imate scenarij, pri katerem je ena faza projekta, na primer faza prototipa, fiksna cena, vse druge faze pa so čas in material, boste lahko fazo prototipa in vsa povezana podrejena opravila povezali s podrobnostmi pogodbe za to fazo z načinom obračunavanja s fiksno ceno.

Vse druge faze v projektu s strukturirano členitvijo dela (SČD) so lahko povezane s podrobnostmi pogodbe, ki temeljijo na času in materialu.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Povezava opravil s podrobnostmi pogodbe, ki temeljijo na projektu

Opravila lahko povežete s podrobnostmi pogodbe z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnosti pogodbe** ali z zavihka **Obračunavanje opravil** na strani **Projekt**.

### <a name="from-the-contract-line-page"></a>S strani »Podrobnosti pogodbe«

Upoštevajte spodnje korake za povezovanje projektnih opravil s podrobnostmi pogodbe z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnosti pogodbe**.

1. Na zavihku **Splošno** v podrobnosti pogodbe, ki temelji na projektu, preverite, ali je polje **Projekt** izpolnjeno.
2. V polju **Vključena opravila** izberite **Samo izbrana opravila**.
3. Shranite spremembe. Obrazec se bo osvežil in viden bo zavihek **Opravila, ki se zaračunajo**.
4. Izberite zavihek **Opravila, ki se zaračunajo** in v podmreži izberite **Dodaj opravilo podrobnosti pogodbe**.
5. Na strani **Opravila podrobnosti pogodbe** v spustnem meniju **Opravila** izberite opravilo. 
6. Vnesite podatke v polje **Vrsta obračunavanja** in nato izberite **Shrani in zapri**. Izbrano opravilo je povezano s podrobnostmi pogodbe.

> [!NOTE]
> To ni najbolj optimalna izkušnja za povezovanje projektnih opravil s podrobnostmi pogodbe. V tej izkušnji morate vsak projekt ročno povezati. Najprimernejši način je z zavihka **Obračunavanje opravil** na strani **Projekt**.

### <a name="from-the-project-page"></a>S strani »Projekt«

To je optimalni način za povezovanje opravil s podrobnostmi pogodbe. Izberete lahko več opravil in povežete njih in njihova podrejena opravila z izbranimi podrobnostmi pogodbe. Upoštevajte spodnje korake za povezovanje opravil s podrobnostmi pogodbe s strani **Projekt**.

1. Na zavihku **Splošno** v podrobnosti pogodbe, ki temelji na projektu, preverite, ali je polje **Projekt** izpolnjeno.
2. V polju **Vključena opravila** izberite **Samo izbrana opravila**.
3. Shranite podrobnosti pogodbe, ki temeljijo na projektu. Obrazec se bo osvežil in viden bo zavihek **Opravila, ki se zaračunajo**. To je samo za namene preverjanja pristnosti.
4. Na zavihku **Splošno** v podrobnosti pogodbe, ki temelji na projektu, v polju **Projekt** izberite povezavo projekta.
5. Na strani **Projekt** izberite zavihek **Nastavitev obračunavanja opravil**.
6. Obstajata dve mreži. Ena mreža je za podrobnosti pogodbe, ki veljajo za celoten projekt. Druga mreža velja za nastavitev obračunavanja za posamezna opravila. V drugi mreži izberite eno ali več opravil in nato izberite **Povezane podrobnosti pogodbe**.
7. Na strani pogovornega okna, ki se odpre, v spustnem meniju izberite podrobnosti pogodbe.
8. Če želite opravila označiti kot »se zaračuna« ali »se ne zaračuna«, uporabite spustni meni **Vrsta obračunavanja**.
9. Izberite potrditveno polje, če želite, da povezava vključuje tudi podrejena opravila izbranih opravil. Če potrdite polje, bodo podrejena opravila izbranih opravil povezana tudi s podrobnostmi pogodbe.
10. Izberite **V redu**, da zaprete pogovorno okno.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Prekinitev povezave med opravil in podrobnostmi pogodbe, ki temeljijo na projektu

### <a name="from-the-contract-line-page"></a>S strani »Podrobnosti pogodbe«

Upoštevajte spodnje korake za prekinitev povezave med projektnimi opravili in podrobnostmi pogodbe na zavihku **Opravila, ki se zaračunajo** na strani **Podrobnosti pogodbe**.

1. Na zavihku **Opravila, ki se zaračunajo** izberite **Izbriši opravilo nalogo podrobnosti pogodbe**.
2. Opozorilo pomeni, da lahko prekinitev te povezave povzroči razveljavitev dejanskega dela, ki je bil predhodno zabeležen v opravilu. V pogovornem oknu izberite **V redu** za prekinitev povezave med opravilom in podrobnostmi pogodbe, ki temelji na projektu. 

> [!NOTE]
> To ne izbriše opravila iz projekta. Namesto tega odstrani povezavo opravila iz podrobnosti pogodbe, ki temelji na projektu.

### <a name="from-the-project-page"></a>S strani »Projekt«

To je optimalna izkušnja za odstranjevanje povezave med projektnimi opravili in podrobnostmi pogodbe. Izberete lahko več opravil in odstranite povezavo med njimi in njihovimi podrejenimi opravili in izbranimi podrobnostmi pogodbe. Upoštevajte spodnje korake za odstranjevanje povezave med opravili in podrobnostmi pogodbe.

1. Z zavihka **Splošno** v podrobnosti pogodbe, ki temelji na projektu, v polju **Projekt** kliknite povezavo za projekt.
2. Na strani **Projekt** izberite zavihek **Nastavitev obračunavanja opravil**.
3. Na strani sta dve mreži. Ena mreža je za podrobnosti pogodb, ki veljajo za celoten projekt, druga pa za nastavitev obračunavanja za posamezna opravila. V drugi mreži izberite eno ali več opravil in nato izberite **Prekinitev povezave podrobnosti pogodbe**.
4. Na strani pogovornega okna, ki se odpre, v spustnem meniju izberite podrobnosti pogodbe.
5. Izberite potrditveno polje, če želite, da se povezava prekine tudi z podrejenimi opravili izbranih opravil. Če potrdite polje, bodo povezava prekinjena tudi med podrejenimi opravili izbranih opravil in podrobnostmi pogodbe.
6. Izberite **V redu**. Opozorilo pomeni, da lahko prekinitev te povezave povzroči razveljavitev dejanskega dela, ki je bil predhodno zabeležen v opravilu. V pogovornem oknu z opozorilom izberite **V redu** za prekinitev povezave med opravilom in podrobnostmi pogodbe, ki temelji na projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
