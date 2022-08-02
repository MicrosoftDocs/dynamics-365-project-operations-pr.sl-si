---
title: Zahteve za elemente za projektne pogodbe z več viri financiranja
description: Ta članek nudi informacije o tem, kako konfigurirati in uporabiti zahteve za elemente z več viri financiranja.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028508"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Zahteve za elemente za projektne pogodbe z več viri financiranja

_**Velja za:** Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Nekatere pogodbene pogodbe za končne rezultate, ki temeljijo na projektih, lahko zahtevajo več virov financiranja. Ta članek pojasnjuje, kako izbrati in konfigurirati želene vire financiranja, ko je za projekt ali projektno pogodbo potrebnih več virov.

## <a name="terminology"></a>Terminologija

- **Vir financiranja** – Subjekt, ki financira projektno pogodbeno delo. Ta entiteta je lahko notranja organizacija ali račun zunanjega računa (stranka ali donacija).
- **Stranka projekta** – Subjekt, ki mu je projektno delo dostavljeno.
- **račun račun** – Zunanji subjekt, ki plača projektno delo.

## <a name="example"></a>Primer

Contoso je pridobil pogodbo za obnovo opreme z dvema svojima strankama: Adatum US in Adatum Corporate. Pogodba vključuje storitve strojne opreme in namestitve, ki bodo dostavljene podjetju Adatum US (stranka projekta). Strojno opremo bo financiral Adatum Corporate (konto fakture 1), inštalacijska dela pa bo financiral Adatum US (konto fakture 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nastavite privzeta pravila računa računa za zahteve artiklov

### <a name="prerequisites"></a>Zahteve

- Microsoft Dynamics 365 Finance **različica 10.0.27 ali novejša** mora uporabljati zahteve za elemente, ki imajo več računov računov.
- Vaš skrbnik sistema mora omogočiti **Dovolite zahteve po artiklih z več viri financiranja za scenarije, ki temeljijo na zalogah/produkciji projektnih operacij** funkcija v **Upravljanje funkcij** delovni prostor.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nastavite privzeta pravila računa računa

Če želite nastaviti privzeta pravila za račun za račune, sledite tem korakom.

1. Odprite **Vodenje projektov in računovodstvo** \> **Nastavitev** \> **Vodenje projekta in računovodski parametri**.
1. Na **Splošno** zavihek, v **Prodajna naročila in zahteve po artiklih** razdelek, nastavite **Dovolite projekte z več viri financiranja** možnost za **ja**.
1. V **Privzeta stranka** polje določite, od kod privzeto prihaja naročnik dostave projekta na zahtevo za postavko:

    - **Iz vira financiranja** – Privzeta stranka za izvedbo projekta prihaja iz vira financiranja. Če je s projektno pogodbo povezanih več virov financiranja, bo uporabljen prvi vir financiranja na seznamu.
    - **Iz projekta** – Privzeta stranka za dostavo projekta prihaja od stranke, ki je izbrana v **Projektni račun** polje.

1. Izbirno: nastavite ali spremenite privzeti račun za račun v zapisih projekta:

    1. Pojdi do **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in odprite podrobnosti zapisa projekta.
    2. Na **Splošno** zavihek, nastavite ali posodobite **Privzeti račun za račune** polje. Račun, ki ga podate, bo uporabljen kot privzeti račun za račune za nove zahteve po artiklih, ki so ustvarjene za projekt. Če pustite polje prazno, bo privzeto uporabljen konto računa prvega vira financiranja projektne pogodbe. Vendar pa bodo uporabniki lahko spremenili račun, ko bodo shranili zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Izberite račun računa, ki ga želite uporabiti, ko ustvarite zahtevo po artiklu

Če želite izbrati račun računa, ki ga želite uporabiti, ko ustvarite zahtevo po artiklu, sledite tem korakom.

1. Pojdi do **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in izberite zapis projekta.
1. Na **Načrtujte** zavihek izberite **Zahteve za artikle**.
1. Ustvarite nov zapis zahteve za postavko.

    - Privzeto je **račun račun** polje v zapisu je nastavljeno na račun računa, ki je nastavljen za projekt. Lahko spremenite vrednost **račun račun** polje in nato shranite zapis. Ko je zapis shranjen, ne morete več posodobiti **račun račun** vrednost. Če morate posodobiti **račun račun** vrednost za zahtevo postavke, izbrišite obstoječo zahtevo postavke in nato ustvarite novo, ki ima želeno vrednost.
    - Privzeto je **Stranka** polje za zahtevo artikla je nastavljeno na podlagi **Privzeta stranka** vrednost, ki je nastavljena na **Projektno vodenje in računovodski parametri** strani.

    Ko je zapis zahteve postavke shranjen, ga sistem poveže z **Zahteva po predmetu Prodajno naročilo** zapis glave. Če nobena odprta glava prodajnega naročila nima izbranega računa računa, ga bo sistem ustvaril in z njim povezal vrstico zahteve artikla.

> [!NOTE]
> Zahteve po artiklih se vedno v celoti fakturirajo na račun računa, ki je nastavljen v zapisu. Sistem trenutno ne podpira pravil za dodeljevanje sredstev, ki imajo zahteve za postavke, in ne bo razdelil objav na podlagi nastavitve pravil za dodeljevanje sredstev.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Ustvarite zahtevo za postavko iz zapisa napovedi postavke

Če želite ustvariti zahtevo postavke iz zapisa napovedi postavke, sledite tem korakom.

1. Pojdi do **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in izberite zapis projekta.
1. Na **Načrtujte** zavihek izberite **Napovedi artiklov**.
1. Ustvarite nov zapis napovedi artikla.
1. Izbirno: na **Projekt** zavihek, v **Vir financiranja** izberite želeni račun za račune.
1. Izberite **Ustvari zahtevo po predmetu** in potrdite prejeto sporočilo.

    > [!NOTE]
    > Sistem kopira **Vir financiranja** vrednost iz zapisa napovedi postavke v novo ustvarjen zapis zahteve za postavko.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Privzeti račun računa, ko sistem samodejno ustvari zahtevo po artiklu iz vrstice naročilnice

Če je **Ustvari zahtevo po predmetu** možnost je nastavljena na **ja** na **Vodenje projektov in računovodski parametri** strani, sistem samodejno ustvari zahtevo po artiklu, ko je shranjena nova vrstica naročilnice projekta. Privzeto je **račun račun** in **Zahteva po artiklu** polja so nastavljena na vrednost **Privzeti račun za račune** polje v zapisu projekta. Sistem trenutno ne podpira posodabljanja ali spreminjanja računa računa za zapise te vrste.
