---
title: Konfiguracija samodejnega ustvarjanja računov
description: Ta tema vsebuje informacije o tem, kako konfigurirati sistem za samodejno ustvarjanje računov.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287933"
---
# <a name="configure-automatic-invoice-creation"></a>Konfiguracija samodejnega ustvarjanja računov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Izvedite naslednje korake, da v aplikaciji Dynamics 365 Project Operations konfigurirate samodejno izdajanje računov.

1. Odprite zavihek **Nastavitve** > **Paketna opravila**.
2. Ustvarite paketno opravilo in ga poimenujte **Ustvarjanje računov v storitvi Project Operations**. Ime paketnega opravila mora vključevati izraz »ustvarjanje računov«.
3. V polju **Vrsta posla** izberite možnost **Brez**. Možnosti **Pogostost: dnevno** in **Je aktivno** sta nastavljeni na **Da**.
4. Izberite **Zaženi potek dela**. V pogovornem oknu **Poišči zapis** vidite tri poteke dela:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Izberite **ProcessRunCaller** in nato **Dodaj**.
6. V naslednjem pogovornem oknu izberite **V redu**. Poteku dela **Spanje** sledi potek dela **Proces**.

  > [!NOTE]
  > V 5. koraku lahko izberete tudi **ProcessRunner**. Ko nato izberete **V redu**, poteku dela **Proces** sledi potek dela **Spanje**.

Poteka dela **ProcessRunCaller** in **ProcessRunner** ustvarita račune. **ProcessRunCaller** prikliče **ProcessRunner**. **ProcessRunner** je potek dela, ki dejansko ustvari račune. Gre skozi vse vrstice pogodbe, za katere je treba ustvariti račune, in ustvari račune za te vrstice. Opravilo preveri datume izdaje računa za vrstice pogodbe, da ugotovi, za katere vrstice pogodbe je treba ustvariti račune. Če imajo vrstice pogodbe, ki pripadajo eni pogodbi, enak datum izdaje računa, se transakcije združijo v en račun, ki ima dve vrstici računa. Če ni transakcij, za katere bi se lahko ustvarili računi, opravilo preskoči ustvarjanje računa.

Ko se potek dela **processrunner** preneha izvajati, prikliče potek dela **ProcessRunCaller**, navede končni čas in se zapre. **ProcessRunCaller** nato zažene časovnik, ki se izvaja 24 ur od navedenega končnega časa. Ko se časovnik preneha izvajati, se **ProcessRunCaller** zapre.

Paketna obdelava za ustvarjanje računov je ponavljajoče se opravilo. Če se paketna obdelava zažene večkrat, se ustvari več primerkov opravila in pride do napak. Zato paketno obdelavo zaženite samo enkrat in jo znova zaženite le, če se preneha izvajati.

> [!NOTE]
> Paketno izdajanje računov se izvaja samo za podrobnosti pogodbe, ki so konfigurirane z razporedi izdajanja računov. V podrobnostih pogodbe z načinom obračunavanja s fiksno ceno morajo biti nastavljeni mejniki. V podrobnostih pogodbe z načinom obračunavanja za časovne in materialne transakcije je treba nastaviti datumski urnik računov. Enako velja v podrobnosti pogodbe za projekt.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]