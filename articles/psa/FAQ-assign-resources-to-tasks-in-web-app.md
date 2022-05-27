---
title: Kako dodelim vir, ki ga je mogoče rezervirati, opravilu v spletni aplikaciji?
description: Pregled načinov dodeljevanja virov, ki jih je mogoče rezervirati.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0aaf7f69fa8ae081a74fbc4f18014686f625661c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578866"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Kako dodelim vir, ki ga je mogoče rezervirati, opravilu v spletni aplikaciji (aplikacija Project Service različice 2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Obstajata dva načina dodeljevanja virov opravilu v aplikaciji Project Service. Vir lahko rezervirate kot član ekipe in ga nato dodelite opravilu. Lahko pa ustvarite generičnega člana ekipe z dodeljevanjem vlog opravilom, ustvarite ekipo in nato s poimenovanim virom izpolnite zahteve za varnostno kopiranje.

Če želite vir, ki ga je mogoče rezervirati, dodeliti opravilu, mora imeti član ekipe vira, ki ga je mogoče rezervirati, na voljo dovolj rezervacij. Stanje rezervacije mora biti »Potrdi vrsto veljavne rezervacije« in »Stanje potrjeno«. Če ni dovolj rezervacij za vir, aplikacija Project Service odstrani dodelitev in prikaže naslednje sporočilo o napaki:

*Ni mogoče dodeliti vira opravilu – naslednji viri za ta projekt nimajo rezerviranega zadostnega števila ur*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervacija vira, pri čemer vir rezervirate kot član ekipe, in dodelitev vira opravilu

S tem načinom dodate vir projektni ekipi in nato opravila dodelite viru v načrtu projekta. To naredite tako:
1.  V mreži člana ekipe dodajte novega člana ekipe tako, da izberete **Novo**.
2.  V oknu »Hitro ustvarjanje člana ekipe« izberite ime vira, ki ga je mogoče rezervirati, in nastavite vlogo.
3.  Izberite datum **Od** in **Do**.

    > [!div class="mx-imgBorder"] 
    > ![Posnetek zaslona dodajanja člana ekipe.](media/FAQ-Resources-to-Tasks2-1.png "Posnetek zaslona dodajanja člana ekipe")
 
4.  Izberite enega od naslednjih načinov dodeljevanja za rezervacijo vira:
    - **Polna zmogljivost** rezervira polno zmogljivost vira za navedeni datumski obseg »Od« in »Do«.
    - **Odstotek zmogljivosti** rezervira vir za odstotek zmogljivosti vira za navedeni datumski obseg »Od« in »Do«.
    - **Enakomerna porazdelitev po urah** rezervira vir za določeno število ur, pri tem pa čas porazdeli enakomerno na dan v določenem časovnem obdobju »Od« in »Do«.
    - **Obremenitev na začetku po urah** rezervira vir za določeno število ur, pri tem pa ure na dan porazdeli na začetek dneva v določenem časovnem obdobju »Od« in »Do«.

    Ne izberite načina **Brez**, saj doda vir ekipi, vendar ne ustvari rezervacij, ki bi prevzele zmogljivost vira.
5.  Izberite **Shrani**.

    Upoštevajte, da morajo ure rezervacije zadostovati za pokritje ur dela in datumskih obsegov opravil, katerim dodelite ta vir. Če ure niso usklajene, vira ne morete dodeliti opravilu.

6.  Na strukturirani členitvi dela (SČD) za opravilo kliknite spustni seznam s celicami vira. Nato: 

    1. Izberite **Dodaj**.
    2. Izberite spustni seznam pod možnostjo **Viri** in izberite člana ekipe, ki ste ga dodali zgoraj.
    3. izberite **V redu**. Član ekipe je zdaj dodeljen opravilu.

    > [!div class="mx-imgBorder"] 
    > ![Posnetek zaslona dodajanja virov s SČD.](media/FAQ-Resources-to-Tasks2-2.png "Posnetek zaslona dodajanja virov s SČD")
 
V mreži člana ekipe boste pod možnostjo »Dodeljene ure« videli združeno število ur, dodeljenih viru. To število je manjše ali enako številu rezerviranih ur za vir. 

> [!div class="mx-imgBorder"] 
> ![Posnetek zaslona dodeljenih ur za vir.](media/FAQ-Resources-to-Tasks2-3.png "Posnetek zaslona dodeljenih ur za vir")
 
Če se opravilo, ki ga skušate dodeliti viru, začne po končnem datumu rezervacij virov, vir ne bo prikazan na spustnem seznamu.

Upoštevajte, da lahko vir dodelite več uram, kot je rezerviranih ur vira, če ima vir še kaj preostale nedodeljene zmogljivosti. V tem primeru bo vir le delno dodeljen do števila rezervacij. Te preostale nedodeljene ure za opravila lahko vidite tako, da stolpec »Osebju nedodeljene ure« dodate v strukturirano členitev dela.

Če so viri dodeljeni svojim rezerviranim uram (rezervirane ure virov so enake njihovim dodeljenim uram), boste videli naslednje sporočilo o napaki, če jim boste skušali dodeliti dodatna opravila:

*Ni mogoče dodeliti vira opravilu – naslednji viri za ta projekt nimajo rezerviranega zadostnega števila ur.*

Poleg tega je privzeti vodja projekta kot član ekipe, ki je dodan ekipi, ko ustvarite projekt, dodan brez rezervacij in ga ni mogoče dodeliti nobenemu opravilu. Ne bo prikazan na spustnem seznamu virov za opravila.

Če želite dodeliti ta vir, ga morate odstraniti iz ekipe in ga nato ponovno dodati na kateri koli način dodeljevanja, ki ni »Brez«. Ko ustvarite projekt, se vir ekipi doda z namenom, da ima projekt vsaj enega privzetega odobritelja.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Ustvarjanje generičnega člana ekipe z dodeljevanjem vlog opravilom

Ta način zagotavlja, da imajo viri dovolj rezervacij za opravila. Najprej ustvarite ogrado ali splošni vir, ki opisuje značilnosti poimenovanega vira, ki ga želite dodeliti opravilom, tako, da opravilom najprej dodelite vloge, nato pa ustvarite ekipo. To naredite tako:

1. V strukturirani členitvi dela izberite opravilo.
2. V celici vira izberite ikono spustnega seznama **Dodeljena vloga**.
3. Izberite spustni seznam **Vloga** in izberite vlogo za splošni vir.
4. Izberite **V redu**.

    > [!div class="mx-imgBorder"] 
    > ![Posnetek zaslona uporabe SČD za dodajanje vira.](media/FAQ-Resources-to-Tasks2-4.png "Posnetek zaslona uporabe SČD za dodajanje vira")
 
Ko končate z dodeljevanjem vlog opravilom v SČD, izberite **Ustvari projektno ekipo**. Storitev Project Service ustvari najmanjše število generičnih članov ekipe na podlagi njihovih vlog, organizacijskih enot vira in koledarja projekta z združevanjem dodelitev opravil.

> [!div class="mx-imgBorder"] 
> ![Posnetek zaslona ustvarjanja projektne ekipe.](media/FAQ-Resources-to-Tasks2-5.png "Posnetek zaslona ustvarjanja projektne ekipe")
 
V mreži člana ekipe boste videli vire vrste »Splošni vir« z vlogo in imenom položaja. Če sta potrebna dva vira za vlogo za dokončanje dela, funkcija »Ustvari ekipo« ustvari dva člana ekipe in uporabi ime položaja, da ju loči.

> [!div class="mx-imgBorder"] 
> ![Posnetek zaslona dodajanja dveh splošnih virov.](media/FAQ-Resources-to-Tasks2-6.png "Posnetek zaslona dodajanja dveh splošnih virov")
 
Zahtevo za rezervni vir za generičnega člana ekipe lahko odprete tako, da izberete povezavo pod možnostjo »Zahteva za vir«.

> [!div class="mx-imgBorder"] 
> ![Posnetek zaslona odpiranja zahteve za rezervni vir.](media/FAQ-Resources-to-Tasks2-7.png "Posnetek zaslona odpiranja zahteve za rezervni vir")

Za splošni vir izberite možnost **Rezerviraj**, nato pa prek plošče razporeda poiščite in rezervirajte pravi vir. Prav tako lahko pošljete zahtevo za izpolnitev s strani upravitelja virov tako, da izberete **Pošlji zahtevo**.

Ko je splošni vir izpolnjen s poimenovanim virom, se splošni vir odstrani iz ekipe, dodelitve opravil za splošni vir pa so dodeljene poimenovanemu viru, ki je izpolnil zahtevo za splošni vir.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
