---
title: Konfiguracija avtomatiziranega ustvarjanja računov
description: Ta tema vsebuje informacije o tem, kako nastaviti sistem za samodejno ustvarjanje računov.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898146"
---
# <a name="configure-automated-invoice-creation"></a>Konfiguracija avtomatiziranega ustvarjanja računov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dokončajte naslednje korake, da konfigurirate samodejni zagon računa v storitvi Project Operations.

1. Odprite **Nastavitve** \> **Paketna opravila**.
2. Ustvarite paketno opravilo in ga poimenujte **Ustvarjanje računov v storitvi Project Operations**. Ime paketnega opravila mora vključevati izraz »Ustvarjanje računov«.
3. V polju **Vrsta posla** izberite **Brez**. Možnosti **Pogostost: dnevno** in **Je aktivno** sta nastavljeni na **Da**.
4. Izberite **Zaženi potek dela**. V pogovornem oknu **Poišči zapis** vidite tri poteke dela:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Izberite **ProcessRunCaller** in nato **Dodaj**.
6. V naslednjem pogovornem oknu izberite **V redu**. Poteku dela **Spanje** sledi potek dela **Proces**.

    V 5. koraku lahko izberete tudi **ProcessRunner**. Ko nato izberete **V redu**, poteku dela **Proces** sledi potek dela **Spanje**.

Poteka dela **ProcessRunCaller** in **ProcessRunner** ustvarita račune. **ProcessRunCaller** prikliče **ProcessRunner**. **ProcessRunner** je potek dela, ki dejansko ustvari račune. Gre skozi vse vrstice pogodbe, za katere je treba ustvariti račune, in ustvari račune za te vrstice. Opravilo preveri datume izdaje računa za vrstice pogodbe, da ugotovi, za katere vrstice pogodbe je treba ustvariti račune. Če imajo vrstice pogodbe, ki pripadajo eni pogodbi, enak datum izdaje računa, se transakcije združijo v en račun, ki ima dve vrstici računa. Če ni transakcij, za katere bi se lahko ustvarili računi, opravilo preskoči ustvarjanje računa.

Ko se potek dela **processrunner** preneha izvajati, prikliče potek dela **ProcessRunCaller**, navede končni čas in se zapre. **ProcessRunCaller** nato zažene časovnik, ki se izvaja 24 ur od navedenega končnega časa. Ko se časovnik preneha izvajati, se **ProcessRunCaller** zapre.

Paketna obdelava za ustvarjanje računov je ponavljajoče se opravilo. Če se paketna obdelava zažene večkrat, se ustvari več primerkov opravila in pride do napak. Zato paketno obdelavo zaženite samo enkrat in jo znova zaženite le, če se preneha izvajati.

> [!NOTE]
> Paketno izdajanje računov se izvaja samo za podrobnosti pogodbe, ki so konfigurirane z razporedi izdajanja računov. V podrobnostih pogodbe z načinom obračunavanja s fiksno ceno morajo biti nastavljeni mejniki. V podrobnostih pogodbe z načinom obračunavanja za časovne in materialne transakcije je treba nastaviti datumski urnik računov. Enako velja v podrobnosti pogodbe za projekt.     
