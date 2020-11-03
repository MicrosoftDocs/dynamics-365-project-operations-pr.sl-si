---
title: Zahteve za pot
description: Ta tema vsebuje informacije o zahtevah za pot.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084625"
---
# <a name="travel-requisitions"></a>Zahteve za pot

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Zahteva za pot navaja stroške, ki bodo nastali zaradi potovanja. Zahteva za pot se predloži v pregled in se lahko uporabi za odobritev stroškov.

Morda boste morali predložiti zahtevo za pot, preden boste imeli kakršne koli stroške, ki se zaračunajo organizaciji. Ta zahteva velja ne glede na to, ali za stroške bremenite kreditno kartico podjetja, uporabite gotovino, ki ste jo prejeli kot denarni predujem, ali sami plačate stroške, ki jih bo organizacija povrnila.

Zahteve za pot in pravilniki se lahko uporabljajo za pomoč pri upravljanju izdatkov organizacije. Če na primer vaša organizacija dela na projektu s fiksno ceno, pri katerem je potrebno potovanje, se morajo potni stroški članov projektne ekipe ujemati s proračunom projekta. Z zahtevo po odobritvi potnih stroškov, preden nastanejo, lahko organizacija pomaga zagotoviti, da projekt ostane v okviru proračuna.

## <a name="configuration"></a>Konfiguracija 

Zahteve za pot lahko nastavite kot »obvezne«, tako da v parametrih upravljanja stroškov omogočite parameter »Predhodna odobritev potovanja je obvezna«. 

## <a name="create-and-submit-a-travel-requisition"></a>Ustvarjanje in pošiljanje zahtev za pot

1. Odprite možnost **Moji stroški: Zahteva za pot** in izberite **Nova zahteva za pot**.
2. Vnesite namen in cilj zahteve.
3. V polje **Opis potovanja** vnesite dodatne podatke. 
4. Za vsakega od pričakovanih stroškov, kot so let, prehrana ali najem avtomobila, ustvarite postavko vrstice stroška. Vključite predvideni datum, predvideni znesek in valuto za vsak strošek. 
5. Ko končate z dodajanjem pričakovanih stroškov, izberite **Shrani**.
6. Ko ste pripravljeni na pošiljanje zahteve za pot, izberite **Potek dela** > **Pošlji**.

Odobrene zahteve za pot si lahko ogledate v možnosti **Moji stroški: Zahteva za pot**. 

## <a name="view-available-travel-requisitions"></a>Oglejte si zahteve za pot, ki so na voljo

Vse svoje zahteve za pot si lahko ogledate v možnosti **Moji stroški: Zahteve za pot**.

## <a name="approve-travel-requisitions"></a>Odobritev zahtev za pot

Izberite zahtevo za pot, ki jo želite odobriti, in nato izberite **Potek dela** > **Odobri**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Pošiljanje poročila o stroških z odobreno zahtevo za pot

1. Ustvarite novo poročilo o stroških in v glavi poročila o stroških ter na seznamu odobrenih zahtev za pot izberite **Preslikava v zahtevo za pot**.
2. Polje **Znesek zahteve za pot** polje se samodejno posodobi v glavi poročila o stroških.
3. Dodajte vse stroške, nastale na potovanju. Če je omogočeno polje **Vnaprej odobreno** , se usklajeni znesek in odobreni znesek za določeno kategorijo stroškov posodobita.

> [!NOTE]
> Ko preslikate poročilo o stroških v odobreno zahtevo za pot, znesek transakcije ne sme biti večji od odobrenega zneska. 
