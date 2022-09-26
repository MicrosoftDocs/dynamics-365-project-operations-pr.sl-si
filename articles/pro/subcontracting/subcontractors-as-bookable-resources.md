---
title: Nastavitev podizvajalskih pogodb kot vire, ki jih je mogoče rezervirati
description: Ta članek pojasnjuje, kako nastaviti in vzdrževati vire podizvajalcev, ki so ustvarjeni iz uporabnikov in stikov v sistemu, tako da jih je mogoče povezati s podizvajalci v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522722"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Nastavitev podizvajalskih pogodb kot vire, ki jih je mogoče rezervirati

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Sledite tem korakom, da nastavite podizvajalske pogodbe kot vire za rezervacijo v storitvi Microsoft Dynamics 365 Project Operations.

1. Pojdite v razdelek **Projekt** \> **Viri** in izberite **Novo**.
2. V polju **Vrsta vira polja** v razdelku **Nov vir za rezervacijo** izberite eno od naslednjih možnosti:

    - **Uporabnik** - Izberite to vrsto vira, če mora podizvajalec dostopati do storitve Project Operations za vnos časa ali stroškov. Če izberete možnost **Uporabnik**, podizvajalec za dostop do sistema potrebuje veljavno licenco.
    - **Stik** ali **Kupec** - Izberite eno od teh vrst virov, če podizvajalec ne potrebuje dostopa do storitve Project Operations, vendar mora biti na voljo za dodelitve nalog ali rezervacije projektov. Nobena od teh vrst virov ne omogoča dostopa do sistema. Izberite možnost **Kupec**, da podjetje dobavitelja predstavite kot vir, ki ga je mogoče rezervirati. Izberite možnost **Stik**, če želite zastopati posamezne zaposlene dobavitelja.

3. Glede na vrsto vira, ki ste ga izbrali, boste morali izbrati ustreznega uporabnika, kupca ali stik.
4. V polju **Vrsta delavca**, izberite "Pogodbeni delavec", da podizvajalca nastavite kot vir, ki ga je mogoče rezervirati.

    > [!NOTE]
    > Če pustite polje **Vrsta delavca** prazno, bo vir, ki ga je mogoče rezervirati, obravnavan kot zaposleni delavec.

5. Če ste izbrali možnost **Pogodbeni delavec** kot vrsto delavca, izberite dobavitelja, pri katerem je vir zaposlen.
6. Izberite časovni pas vira in nato izberite možnost **Shrani**. Če želite viru, ki ga je mogoče rezervirati, dodeliti predlogo za delovne ure, lahko izberete možnost **Nastavite koledar** na strani s seznamom **Vir, ki ga je mogoče rezervirati**.

Da vir, ki ga je mogoče rezervirati, povežete s podizvajalsko pogodbo, morajo biti izpolnjeni naslednji pogoji:

- Vir, ki ga je mogoče rezervirati, mora biti pogodbeni delavec.
- Vir, ki ga je mogoče rezervirati z izbrano možnostjo **Stik**, mora biti povezan z računom dobavitelja kot stik. Vir, ki ga je mogoče rezervirati z izbrano možnostjo **Stik**, ne potrebuje biti povezan z računom dobavitelja kot stik.
- Vrednost polja **Prodajalec** za vir, ki ga je mogoče rezervirati, se mora ujemati z vrednostjo polja **Prodajalec** podizvajalske pogodbe.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Posodobitev vrste preslikave delavcev in dobaviteljev za vire, ki jih je mogoče rezervirati

Polje **Vrsta delavca** za vir, ki ga je mogoče rezervirati, določa, ali je vir, ki ga je mogoče rezervirati, pogodbeni delavec ali zaposleni. Polje **Prodajalec** določa račun dobavitelja, s katerim je povezan vir, ki ga je mogoče rezervirati. Če vir, ki ga je mogoče rezervirati, povežete z dobaviteljem kot stikom, označite, da je ta stik zaposleni v podjetju dobavitelja.

Če sta polji **Vrsta delavca** in **Prodajalec** vir, ki ga je mogoče rezervirati, spremembe vplivajo na vsa prihodnja preverjanja novih zapisov, ki jih ustvari vir, ki ga je mogoče rezervirati, kot na primer na časovne vnose. Vendar spremembe ne razveljavijo obstoječih zapisov.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
