---
title: Podrobnosti glave za podizvajalske pogodbe
description: V okviru te teme so pojasnjene funkcije, ki so na voljo v glavi podizvajalske pogodbe v aplikaciji Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323661"
---
# <a name="header-details-for-subcontracts"></a>Podrobnosti glave za podizvajalske pogodbe

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V okviru te teme so pojasnjene funkcije, ki so na voljo v glavi podizvajalske pogodbe v aplikaciji Dynamics 365 Project Operations.

Vodja projektov, ki načrtuje in izvaja projekte, lahko zaposli podizvajalce in od dobaviteljev kupi izdelke ali naroči storitve. Ko vodja projekta kupuje izdelke ali naroča storitve, lahko v aplikacij Project Operations ustvari podizvajalsko pogodbo.

Če želite ustvariti podizvajalsko pogodbo, upoštevajte naslednja navodila.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe**, na strani **Podizvajalska pogodba** pa možnost **Nova**.
2. Vnesite zahtevane informacije in izberite **Shrani**.

    Spodnja tabela vsebuje informacije o poljih na strani o glavi podizvajalske pogodbe.

    | **Polje** | **Opis** |
    | --- | --- | 
    | Imenu | Ime podizvajalske pogodbe. |
    | Opis | Kratek opis storitev in izdelkov, naročilo katerih je opredeljeno v podizvajalski pogodbi. |
    | Dobavitelj | Ime podjetja, pri katerem so naročeni izdelki in storitve. Vrsta odnosa za zapis računa je **Prodajalec** ali **Dobavitelj**. |
    | Datum podizvajalske pogodbe | Datum ustvarjenja podizvajalske pogodbe. |
    | Razlogu stanja | Stanje podizvajalske pogodbe. |
    | Valuta | Valuta, v kateri je izvedeno plačilo izdelkov in storitev. Vrednost v tem polju je privzeto določena na podlagi računa dobavitelja, vendar jo je mogoče spremeniti. Na projektnih cenikih, ki določajo cene za izdelke in storitve, opredeljene v podizvajalski pogodbi, mora biti uporabljena ta valuta. Ceniki v katerikoli drugi valuti se na podizvajalsko pogodbo ne morejo nanašati. Stroški izdelkov in storitev, ki nastanejo s to pogodbo, bodo k projektu zabeleženi v tej valuti. |
    | Pogodbena enota | Oddelek podjetja, ki z dobaviteljem sklepa prodajno ali podizvajalsko pogodbo. |
    | Plačilni pogoji | Plačilni pogoji na računih dobavitelja, ki so izdani v okviru podizvajalske pogodbe. Vrednost v tem polju je privzeto določena na podlagi zapisa računa dobavitelja. |
    | Naslov za plačilo | Naslov, na katerega je poslan znesek, ki ga določajo računi dobavitelja. Vrednost v tem polju je privzeto določena na podlagi zapisa računa dobavitelja. |
    | Ime plačnika | Ime osebe iz dobaviteljevega podjetja, ki bo poslala račun, ali naziv oddelka, iz katerega bo poslan. Vrednost v tem polju je privzeto določena na podlagi zapisa računa dobavitelja in bo uporabljena kot ime glavnega stika na računih dobavitelja, ki bodo izdani v okviru izpolnjevanja podizvajalske pogodbe. |
    | Naslov plačnika | Naslov, uporabljen na računih dobavitelja. Vrednost v tem polju je privzeto določena na podlagi zapisa računa dobavitelja. Ta naslov se uporablja tudi kot naslov na računih dobavitelja, ki so izdani v okviru podizvajalske pogodbe. |
    | Delna vsota | Če podizvajalska pogodba nima vrstic, v to polje vnesite vrednost, ki označuje delno vsoto pred obdavčitvijo. Če pa jih ima, je to polje namenjeno samo za branje. Prikazani znesek predstavlja delno vsoto vseh vrstic podizvajalske pogodbe. |
    | Skupni davek | Če podizvajalska pogodba nima vrstic, v to polje vnesite vrednost, ki označuje davke v okviru te pogodbe. Če pa jih ima, je to polje namenjeno samo za branje. Prikazani znesek predstavlja vsoto vseh davkov v okviru podizvajalske pogodbe. |
    | Skupni znesek |  Polje z izračunom prikazuje skupni znesek v okviru podizvajalske pogodbe po vključitvi davkov.  |
    | Datum potrditve | Datum potrditve podizvajalske pogodbe.  |
    | Zahteval(-a) | Vrednost v tem polju je privzeto določena na podlagi imena uporabnika, ki ustvari podizvajalsko pogodbo. Vrednost lahko spremeni ustvarjalec podizvajalske pogodbe ter navede osebo, v imenu katere jo ustvarja.  |
    | Upravitelj kupcev pri dobavitelju | Ime glavnega stika za račun dobavitelja. Vrednost v tem polju je privzeto določena na podlagi zapisa računa dobavitelja. Uporabnik lahko spremeni vrednost polja in kot upravljavca računa dobavitelja za podizvajalsko pogodbo določi drugi stik. Ta stik lahko pošilja e-poštna sporočila in se pogaja o cenah ter vse to tudi konfigurira. |


