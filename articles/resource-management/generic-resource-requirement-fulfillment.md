---
title: Izpolnitev zahteve za splošni vir
description: Ta tema vsebuje informacije o rezervaciji imenovanih virov za zahtevo za splošni vir.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897606"
---
# <a name="generic-resource-requirement-fulfillment"></a>Izpolnitev zahteve za splošni vir

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Poimenovani vir lahko rezervirate za zamenjavo splošnega vira, ki ima zahtevani pogoj za vir.

1. Na strani **Projekti** izberite zavihek **Ekipa**.
2. Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato izberite **Rezerviraj**. Ali pa odprite zahtevani pogoj za vir in izberite **Rezerviraj**.
3. Na strani **Pomočnik za razporejanje** izberite poimenovani vir, ki ga želite rezervirati za projektno ekipo in nato izberite **Rezerviraj.**

Ko je rezervacija dokončana in izpolnjena s poimenovanim virom, se splošni vir zamenja s poimenovanim virom.

S poimenovanim virom se posodobijo tudi dodelitve v razporedu.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Izpolnjevanje splošnega vira z več poimenovanimi viri
Izpolnjevanje zahtevanega pogoja za splošni vir z več poimenovanimi viri je podobno dodeljevanju enega samega poimenovanega vira. Če imate na primer opravilo, ki ima trajanje pet dni in 120 ur obsega dela. Tega opravila ni mogoče dokončati z enim virom, ki dela osem ur dnevno v petdnevnem tednu. 

Zahteva velja za 120 ur inženirske robotike v petih dneh, kar je 24 ur na dan.

To je primer, ko je za izpolnjevanje zahteve za splošni vir potrebnih več poimenovanih virov. Za izpolnitev zahteve morate rezervirati več virov.

Glavna razlika v tem primeru je, da splošni vir ostane v ekipi, ki je dodeljena opravilu, rezervirani člani ekipe poimenovanega vira pa niso dodeljeni kot del položaja. Vodja projekta lahko delo ustrezno dodeli poimenovanim virom. S pogledom **Uskladitev** si lahko vodja projekta pomaga pri razdelitvi rezervacij več virov na dodelitve opravil. To se ne izvede samodejno, ker v vseh bolj zapletenih primerih od enostavnega zgornjega, npr. ko imate paket opravil, ki sestavljajo zahtevo, ali namen, kako želi vodja projekta dodeliti opravila, sistem predpostavlja. Ker sistem ne more razumeti namena, je verjetno, da bodo predpostavke drugačne od nameravanih in lahko pride do napačnega ali nepredvidljivega rezultata. Predvidljiv rezultat je, da splošni vir ostane dodeljen, dokler vodja projekta namenoma ne ustvari dodelitev prek pogleda **Uskladitev**.


