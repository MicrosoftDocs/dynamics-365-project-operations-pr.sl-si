---
title: Dodeljevanje vira opravilu
description: Ta tema vsebuje informacije o dodeljevanju virov opravilom.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150013"
---
# <a name="assign-a-resource-to-a-task"></a>Dodeljevanje vira opravilu

[!include [banner](../includes/psa-now-project-operations.md)]

Obstajajo trije načini dodeljevanja virov opravilu v aplikaciji Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervirajte vir kot član ekipe in nato dodelite vir opravilu

Vir lahko dodate projektni ekipi in ga nato dodelite opravilom v načrtu projekta.

1. Na zavihku **Član ekipe** dodate novega člana ekipe tako, da izberete **Novo**. 

2. Odpre se plošča **Hitro ustvarjanje člana ekipe**, na kateri lahko izberete ime vira, ki ga je mogoče rezervirati, in nastavite vlogo. 

    Izberite enega od spodnjih načinov dodeljevanja za rezervacijo vira:

    - **Polna zmogljivost** rezervira polno zmogljivost vira za navedeni datumski obseg »Od« in »Do«.
    - **Odstotek zmogljivosti** rezervira vir za odstotek zmogljivosti vira za navedeni datumski obseg »Od« in »Do«.
    - **Enakomerna porazdelitev po urah** rezervira vir za določeno število ur, pri tem pa čas porazdeli enakomerno na dan v določenem datumskem obsegu.
    - **Obremenitev na začetku po urah** rezervira vir za določeno število ur, pri tem pa ure na dan porazdeli na začetek dneva v določenem časovnem obdobju »Od« in »Do«.
    - Način **Brez** doda vir ekipi, vendar ne ustvari rezervacij, ki bi prevzele zmogljivost vira.

3. V mreži za opravilo **Načrtovanje** v celici vira izberite ikono **Vir**, nato pa pod možnostjo **Člani ekipe** izberite člana ekipe, ki ste ga pravkar dodali. 

> [!NOTE]
> Na zavihkih **Član ekipe** in **Uskladitev** vir prikazuje rezervirane in dodeljene ure. Ure bi morale biti enake, vendar to ni pogoj, saj rezervacije in dodelitve niso tesno povezane. Na zavihku **Uskladitev** so navedene podrobnosti o tem, kdaj so vrednosti različne, na primer, če viru dodelite več ur, kot ste jih rezervirali. Po potrebi lahko popravite informacije tako, da razširite rezervacije vira ali spremenite dodelitev.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Ustvarite generičnega člana ekipe z dodeljevanjem opravila

Ko z dodeljevanjem opravila ustvarite generičnega člana ekipe, ustvarite označbo mesta ali splošni vir, ki opisuje značilnosti poimenovanega vira, s katerim želite delati v opravilih. Nato ustvarite zahtevo (ali pošljete prošnjo z uporabo zahteve), ki se uporablja za iskanje in rezervacijo poimenovanega vira.

1. V mreži za opravilo **Načrtovanje** v celici vira izberite ikono **Vir**.

2. Vnesite ime, ki bo služilo kot ime vira označbe mesta. Na primer »Upravitelj programa«.

3. Izberite **Ustvari** in v polju **Hitro ustvarjanje člana projektne ekipe** nastavite vlogo za splošni vir.

4. Z dodeljevanjem opravil temu viru označbe mesta nadaljujete tako, da izberete vir v kontrolniku **Izbirnik virov** za opravilo. Navedeni so pod možnostjo **Člani ekipe**.

5. Ko zaključite z dodeljevanjem splošnega vira, izberite splošni vir na zavihku **Ekipa** in nato izberite **Ustvari zahtevo**, da ustvarite zahtevo za splošni vir.

6. Za splošni vir izberite možnost **Rezerviraj**. Nato lahko prek plošče razporeda poiščete in rezervirate pravi vir. Prav tako lahko pošljete zahtevo za izpolnitev s strani upravitelja virov.

7. Ko je splošni vir izpolnjen s poimenovanim virom, se splošni vir odstrani iz ekipe, dodelitve opravil za splošni vir pa so dodeljene poimenovanemu viru, ki je izpolnil zahtevo za splošni vir.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodelite poimenovani vir s seznama vseh virov, ki jih je mogoče rezervirati

Uporabite lahko iskalno polje v kontrolniku **Izbirnik virov**, da poiščete vse vire, ki jih je mogoče rezervirati, in jih dodelite opravilu.

Viri, dodeljeni na ta način, se dodajo ekipi brez rezervacij. To je podobno dodajanju člana ekipe in izbiri možnosti »Brez« kot načina dodeljevanja. Vir je na zavihkih **Ekipa** in **Uskladitev** prikazan kot vir samo z dodelitvami in primanjkljajem za rezervacijo. Če želite uporabiti njihovo razpoložljivost, jih rezervirajte.

1. V mreži za opravilo **Načrtovanje** v celici vira izberite ikono **Vir**.

2. Začnite vnašati ime. Rezultati iskanja za ime so prikazani v kontrolniku **Izbirnik virov** v možnosti **Drugi viri**.

3. Izberite vir, ki ga želite dodeliti opravilu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]