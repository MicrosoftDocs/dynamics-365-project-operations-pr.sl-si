---
title: Zahteve za elemente za projektne pogodbe z več viri financiranja
description: Ta članek vsebuje informacije o tem, kako konfigurirati in uporabiti zahteve za elemente z več viri financiranja.
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

Nekateri pogodbeni dogovori lahko za izdelke, ki temeljijo na projektih, zahtevajo več virov financiranja. Ta članek pojasnjuje, kako izbrati in konfigurirati želene vire financiranja, ko je za projekt ali projektno pogodbo potrebnih več virov.

## <a name="terminology"></a>Terminologija

- **Vir financiranja** – entiteta, ki financira projektno pogodbeno delo. Ta entiteta je lahko notranja organizacija ali zunanji račun za obračun (stranka ali donacija).
- **Stranka projekta** – entiteta, ki ji je projektno delo dostavljeno.
- **Račun za obračun** – zunanja entiteta, ki plača projektno delo.

## <a name="example"></a>Primer

Družba Contoso je dobila pogodbo za obnovo opreme z dvema svojima strankama: Adatum US in Adatum Corporate. Pogodba vključuje storitve strojne opreme in namestitve, ki bodo dostavljene podjetju Adatum US (stranka projekta). Strojno opremo bo financiralo podjetje Adatum Corporate (račun za obračun 1), namestitvena dela pa bo financiralo podjetje Adatum US (račun za obračun 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nastavitev pravil o privzetem nastavljanju računa za obračun za zahteve za elemente

### <a name="prerequisites"></a>Zahteve

- Microsoft Dynamics 365 Finance **različica 10.0.27 ali novejša** mora uporabljati zahteve za elemente, ki imajo več računov za obračun.
- Vaš skrbnik sistema mora omogočiti funkcijo **Dovoli zahteve za elemente z več viri financiranja za aplikacijo Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji** v delovnem prostoru **Upravljanje funkcij**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nastavitev pravil o privzetem nastavljanju računa za obračun

Če želite nastaviti pravila o privzetem nastavljanju računa za obračun, sledite tem korakom.

1. Odprite **Vodenje projektov in računovodstvo** \> **Nastavitev** \> **Vodenje projekta in računovodski parametri**.
1. V zavihku **Splošno** v razdelku **Prodajni nalogi in zahteve za elemente** nastavite možnost **Dovoli projekte z več viri financiranja** na **Da**.
1. V polju **Privzeta stranka** določite, od kod privzeto prihaja stranka, ki izvaja projekt, v zahtevo za element:

    - **Iz vira financiranja** – privzeta stranka, ki izvaja projekt, prihaja iz vira financiranja. Če je s projektno pogodbo povezanih več virov financiranja, bo uporabljen prvi vir financiranja na seznamu.
    - **Iz projekta** – privzeta stranka, ki izvaja projekt, prihaja od stranke, ki je izbrana v polju **Račun zapisa projekta**.

1. Izbirno: nastavite ali spremenite privzeti račun za obračun v zapisih projekta:

    1. Odprite **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in odprite podrobnosti zapisa projekta.
    2. V zavihku **Splošno** nastavite ali posodobite polje **Privzeti račun za obračun**. Račun, ki ga določite, bo uporabljen kot privzeti račun za obračun za nove zahteve za elemente, ki so ustvarjene za projekt. Če pustite polje prazno, bo privzeto uporabljen račun za obračun prvega vira financiranja projektne pogodbe. Uporabniki bodo vseeno lahko spremenili račun, ko bodo shranili zapis.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Izbira računa za obračun, ki ga želite uporabiti, ko ustvarite zahtevo za element

Za izbiro računa za obračun, ki ga želite uporabiti, ko ustvarite zahtevo za element, sledite tem korakom.

1. Odprite **Upravljanje projektov in vodenje računov** \> **Projekti** \> **Vsi projekti** in izberite zapis projekta.
1. V zavihku **Načrt** izberite **Zahteve za elemente**.
1. Ustvarite nov zapis o zahtevi za element.

    - Privzeto je polje **Račun za obračun** v zapisu nastavljeno na račun za obračun, ki je nastavljen za projekt. Lahko spremenite vrednost polja **Račun za obračun** in nato shranite zapis. Ko je zapis shranjen, ne morete več posodobiti vrednosti **Račun za obračun**. Če morate posodobiti vrednost **Račun za obračun** za zahtevo za element, izbrišite obstoječo zahtevo za element in nato ustvarite novo, ki ima želeno vrednost.
    - Privzeto je polje **Stranka** za zahtevo za element nastavljeno na podlagi vrednosti **Privzeta stranka**, ki je nastavljena na strani **Vodenje projekta in računovodski parametri**.

    Ko je zapis o zahtevi za element shranjen, ga sistem poveže zapisom glave **Prodajni nalog z zahtevo za element**. Če nobena odprta glava prodajnega naloga nima izbranega računa za obračun, ga bo sistem ustvaril in z njim povezal vrstico zahteve za element.

> [!NOTE]
> Zahteve za elemente se vedno v celoti zaračunajo na račun za obračun, ki je nastavljen v zapisu. Sistem trenutno ne podpira pravil za dodeljevanje sredstev, ki imajo zahteve za elemente, in ne bo razdelil objav na podlagi nastavitve pravil za dodeljevanje sredstev.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Ustvarjanje zahteve za element iz zapisa napovedi elementa

Za ustvarjanje zahteve za element iz zapisa napovedi elementa sledite tem korakom.

1. Odprite **Upravljanje projektov in vodenje računov** \> **Projekti** \> **Vsi projekti** in izberite zapis projekta.
1. V zavihku **Načrt** izberite **Napovedi elementa**.
1. Ustvarite nov zapis napovedi elementa.
1. Izbirno: v zavihku **Projekt** v polju **Vir financiranja** izberite želeni račun za obračun.
1. Izberite **Ustvari zahtevo za element** in potrdite prejeto sporočilo.

    > [!NOTE]
    > Sistem kopira vrednost **Vir financiranja** iz zapisa napovedi elementa v novo ustvarjen zapis o zahtevi za element.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Privzeti račun za obračun, ko sistem samodejno ustvari zahtevo za element iz vrstice naročilnice

Če je možnost **Ustvari zahtevo za element** nastavljena na **Da** na strani **Vodenje projekta in računovodski parametri**, sistem samodejno ustvari zahtevo za element, ko je shranjena nova vrstica naročilnice projekta. Privzeto sta polji **Račun za obračun** in **Zahteva za element** nastavljeni na vrednost polja **Privzeti račun za obračun** v zapisu projekta. Sistem trenutno ne podpira posodabljanja ali spreminjanja računa za obračun za zapise te vrste.
