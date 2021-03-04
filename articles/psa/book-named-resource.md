---
title: Rezervacija poimenovanih virov iz zahtevanih pogojev za vire
description: Ta tema vsebuje informacije o rezervaciji imenovanih virov za zahtevo za splošni vir.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145128"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezervacija poimenovanih virov iz zahtevanih pogojev za vire

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Poimenovani vir lahko rezervirate za zamenjavo splošnega vira, ki ima zahtevani pogoj za vir.

1. V aplikaciji Project Service Automation (PSA) na strani **Projekti** kliknite zavihek **Ekipa**.
2. Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato kliknite **Rezerviraj**. Ali pa odprite zahtevani pogoj za vir in kliknite **Rezerviraj**.


![Rezervacija splošnega člana ekipe](media/RM-how-to-14.png)


3. Na strani **Pomočnik za razporejanje** izberite poimenovani vir, ki ga želite rezervirati za projektno ekipo in nato kliknite **Rezerviraj.**

![Rezervacija splošnega člana ekipe s pomočnikom za razporejanje](media/RM-how-to-15.png)

Ko je rezervacija dokončana in izpolnjena s poimenovanim virom, se splošni vir zamenja s poimenovanim virom.

![Nadomestitev splošnega člana ekipe s poimenovanim članom ekipe](media/RM-how-to-16.png)

S poimenovanim virom se posodobijo tudi dodelitve v razporedu.

![Dodelitev poimenovanega člana ekipe projektnim opravilom](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Izpolnjevanje splošnega vira z več poimenovanimi viri
Izpolnjevanje zahtevanega pogoja za splošni vir z več poimenovanimi viri je podobno dodeljevanju enega samega poimenovanega vira. Če imate na primer opravilo, ki ima trajanje pet dni in 120 ur obsega dela. Tega opravila ni mogoče dokončati z enim virom, ki dela osem ur dnevno v petdnevnem tednu. 

![Opravilo, za katero je zahtevanih 120 ur obsega dela v petih dneh](media/RM-how-to-21.png)

Zahteva velja za 120 ur inženirske robotike v petih dneh, kar je 24 ur na dan.

![Zahteva na dan](media/RM-how-to-22.png)

To je primer, ko je za izpolnjevanje zahteve za splošni vir potrebnih več poimenovanih virov. Za izpolnitev zahteve morate rezervirati več virov.

![Rezervacija več virov za izpolnjevanje zahteve](media/RM-how-to-23.png)

Glavna razlika v tem primeru je, da splošni vir ostane v ekipi, ki je dodeljena opravilu, rezervirani člani ekipe poimenovanega vira pa niso dodeljeni kot del položaja. Vodja projekta lahko delo ustrezno dodeli poimenovanim virom. S pogledom **Uskladitev** si lahko vodja projekta pomaga pri razdelitvi rezervacij več virov na dodelitve opravil. To se ne izvede samodejno, ker je v vseh bolj zapletenih primerih od zgornjega, npr. ko imate paket opravil, ki sestavljajo zahtevo, treba domnevati način, na katerega želi vodja projekta dodeliti opravila. Ker sistem ne more razumeti tega namena, je mogoče, da bodo predpostavke drugačne od predvidenih in lahko pride do napačnih ali nepredvidljivih rezultatov. Predvidljiv rezultat je, da splošni vir ostane dodeljen, dokler vodja projekta namenoma ne ustvari dodelitev prek pogleda **Uskladitev**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]