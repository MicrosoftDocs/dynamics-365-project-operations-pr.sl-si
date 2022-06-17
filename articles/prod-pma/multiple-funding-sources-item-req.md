---
title: Zahteve za elemente za projektne pogodbe z več viri financiranja
description: Ta članek vsebuje informacije o tem, kako konfigurirati in uporabljati zahteve elementov z več viri financiranja.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931212"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Zahteve za elemente za projektne pogodbe z več viri financiranja

_**Velja za:** Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Nekateri pogodbeni sporazumi za končne rezultate, ki temeljijo na projektih, lahko zahtevajo več virov financiranja. Ta članek pojasnjuje, kako izbrati in konfigurirati želene vire financiranja, ko je za projekt ali projektno pogodbo potrebnih več virov.

## <a name="terminology"></a>Terminologija

- **Vir financiranja** – Subjekt, ki financira delo projektne pogodbe. Ta subjekt je lahko notranja organizacija ali zunanji račun za račun (stranka ali donacija).
- **Stranka projekta** – Subjekt, ki mu je projektno delo dostavljeno.
- **Račun za račun** – Zunanji subjekt, ki plača projektno delo.

## <a name="example"></a>Primer

Contoso je pridobil pogodbo o obnovi opreme z dvema svojima strankama: Adatum US in Adatum Corporate. Pogodba vključuje storitve strojne opreme in namestitve, ki bodo dostavljene Adatum US (stranka projekta). Strojno opremo bo financiral Adatum Corporate (račun račun 1), inštalacijska dela pa Adatum US (račun račun 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nastavite privzeta pravila računa za račune za zahteve artiklov

### <a name="prerequisites"></a>Zahteve

- Microsoft Dynamics 365 Finance in poslovanje **različica 10.0.27 ali novejša** je potreben za uporabo zahtev elementov, ki imajo več računov računov.
- Vaš sistemski skrbnik mora omogočiti **Dovoli zahteve elementov z več viri financiranja za scenarije, ki temeljijo na zalogi projektnih operacij/proizvodnji** značilnost v **Upravljanje funkcij** delovni prostor.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nastavite privzeta pravila računa za račun

Če želite nastaviti privzeta pravila za račun za račun, sledite tem korakom.

1. Odprite **Vodenje projektov in računovodstvo** \> **Nastavitev** \> **Vodenje projekta in računovodski parametri**.
1. Na **General** zavihek, v **Prodajna naročila in zahteve za artikle** oddelek, nastavite **Dovolite projekte z več viri financiranja** možnost za **da**.
1. V **Privzeta stranka** polje, določite, od kod privzeto prihaja stranka za dostavo projekta na zahtevo po artiklu:

    - **Iz vira financiranja** – Privzeta stranka za izvedbo projekta prihaja iz vira financiranja. Če je s projektno pogodbo povezanih več virov financiranja, bo uporabljen prvi vir financiranja na seznamu.
    - **Iz projekta** – Privzeta stranka za dostavo projekta prihaja od stranke, ki je izbrana v **Račun evidence projekta** polje.

1. Izbirno: nastavite ali spremenite privzeti račun računa v zapisih projekta:

    1. Pojdi do **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in odprite podrobnosti o zapisu projekta.
    2. Na **General** zavihek, nastavite ali posodobite **Privzeti račun za račun** polje. Račun, ki ga podate, bo uporabljen kot privzeti račun za račune za nove zahteve artiklov, ki so ustvarjene za projekt. Če pustite polje prazno, bo privzeto uporabljen račun računa prvega vira financiranja pogodbe o projektu. Vendar pa bodo uporabniki lahko spremenili račun, ko bodo shranili zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Izberite račun za račun, ki ga želite uporabiti, ko ustvarite zahtevo po artiklu

Če želite izbrati račun za račun, ki ga želite uporabiti, ko ustvarite zahtevo po artiklu, sledite tem korakom.

1. Pojdi do **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in izberite zapis projekta.
1. Na **Načrtujte** zavihek, izberite **Zahteve za artikle**.
1. Ustvarite nov zapis potreb po artiklu.

    - Privzeto je **Račun za račun** polje v zapisu je nastavljeno na račun računa, ki je nastavljen za projekt. Lahko spremenite vrednost **Račun za račun** polje in nato shranite zapis. Ko je zapis shranjen, ga ne morete več posodobiti **Račun za račun** vrednost. Če morate posodobiti **Račun za račun** vrednost za zahtevo elementa, izbrišite obstoječo zahtevo po artiklu in nato ustvarite novo, ki ima želeno vrednost.
    - Privzeto je **Stranka** polje za zahtevo po artiklu je nastavljeno na podlagi **Privzeta stranka** vrednost, ki je nastavljena na **Vodenje projektov in računovodski parametri** stran.

    Ko je zapis zahteve po artiklu shranjen, ga sistem poveže z **Prodajno naročilo, zahtevano za artikle** zapis v glavi. Če nobena odprta glava prodajnega naloga nima izbranega računa računa, ga bo sistem ustvaril in z njim povezal vrstico potreb po artiklu.

> [!NOTE]
> Zahteve po artiklih se vedno v celoti zaračunajo na račun računa, ki je nastavljen v zapisu. Sistem trenutno ne podpira pravil za dodelitev sredstev, ki imajo zahteve po postavkah, in ne bo razdelil objave na podlagi nastavitve pravil za dodelitev sredstev.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Ustvarite zahtevo po artiklu iz zapisa napovedi artikla

Če želite ustvariti zahtevo po artiklu iz zapisa napovedi elementa, sledite tem korakom.

1. Pojdi do **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in izberite zapis projekta.
1. Na **Načrtujte** zavihek, izberite **Napovedi artiklov**.
1. Ustvarite nov zapis napovedi artiklov.
1. Neobvezno: na **Projekt** zavihek, v **Vir financiranja** polje, izberite želeni račun računa.
1. Izberite **Ustvarite zahtevo za predmet** in potrdite prejeto sporočilo.

    > [!NOTE]
    > Sistem kopira **Vir financiranja** vrednost iz zapisa napovedi artikla v novo ustvarjeni zapis potreb po artiklu.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Privzeti račun računa, ko sistem samodejno ustvari zahtevo po artiklu iz vrstice naročilnice

Če **Ustvarite zahtevo za predmet** možnost je nastavljena na **da** na **Vodenje projektov in računovodski parametri** strani, sistem samodejno ustvari zahtevo po artiklu, ko je shranjena nova vrstica naročilnice projekta. Privzeto je **Račun za račun** in **Zahteva za predmet** polja so nastavljena na vrednost **Privzeti račun za račun** polje v zapisu projekta. Sistem trenutno ne podpira posodabljanja ali spreminjanja računa računa za zapise te vrste.
