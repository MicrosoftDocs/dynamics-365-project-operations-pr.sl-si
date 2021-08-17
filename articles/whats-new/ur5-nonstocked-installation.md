---
title: Posodobitev storitve Project Operations v okolju Finance
description: Ta tema vsebuje informacije o tem, kako posodobite Project Operations v okolju Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3665bccfa25c759c0f2351c691d24901867c178f7c339f4a524856842666aec5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986781"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Posodobitev storitve Project Operations v okolju Finance

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Ta tema vsebuje informacije o tem, kako posodobite Dynamics 365 Project Operations v okolju Dynamics 365 Finance. Trije postopki so obvezni za posodobitev storitve Project Operations na posodobitev 5 (UR5):

- [Uvoz paketa v projekt predogledne različice](#import)
- [Uveljavitev posodobitve](#apply)
- [Posodobitev okolja Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Uvoz paketa v projekt LCS

1. Prijavite se v storitve [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kot lastnik projekta ali kot upravitelj okolja.
2. Na seznamu projektov izberite svoj projekt LCS.
3. Na strani **Projekt** v skupini **Okolja** odprite okolje, ki ga želite posodobiti.
4. Prepričajte se, da se okolje izvaja. Če ni zagnano, zaženite okolje.
5. V razdelku **Nova izdaja** pod možnostjo **Razpoložljive posodobitve** izberite **Ogled posodobitev** za 10.0.15.

![Ogled gumba za posodobitev.](media/view-update.png)

6. Na strani **Binarne posodobitve** izberite **Shrani paket**.
7. Na strani **Preglej in shrani posodobitve** izberite **Shrani paket**.
8. V podoknu **Shrani paket v knjižnico sredstev**, ki se odpre, vnesite ime paketa in nato izberite **Shrani paket**.
9. Ko LCS konča shranjevanje paketa, je gumb **Končano** omogočen. Izberite **Dokončano**. Storitev LCS bo preverila paket. Preverjanje lahko traja nekaj minut ali do ene ure.


## <a name="apply-the-package-update"></a><a name="apply"></a>Uporabite posodobitev paketa

1. V LCS na strani **Podrobnosti o okolju** izberite **Ohranjaj** > **Uporabi posodobitve**.
2. Na seznamu izberite paket, ki ste ga prej shranili, in nato izberite **Uporabi**.
3. Izberite **Da**, da potrdite, da želite uvesti paket.

![Potrdite pogovorno okno za uvajanje paketa.](media/confirm-package-deployment.png)

4. Izberite **Da**, da potrdite, da želite posodobiti aplikacijo.

![Potrdite pogovorno okno za posodobitev aplikacije.](media/confirm-application-update.png)

Uvajanje in posodobitev aplikacije se začne. 

Na strani **Podrobnosti o okolju** v zgornjem desnem kotu se stanje okolja posodobi na **Vzdrževanje**. V približno dveh urah se posodobitev konča. Informacije o izdaji aplikacije se posodobijo na **Microsoft Dynamics 365 for Finance and Operations 10.0.15** in stanje okolja se posodobi na **Uvedeno**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Posodobitev okolja Dataverse

1. Vpišite se v [skrbniško središče za Power Platform](https://admin.powerplatform.com/).
2. Na seznamu poiščite in odprite okolje, ki ste ga uporabili za namestitev storitve Project Operations.
3. Na strani **Okolja** izberite **Vir** > **Aplikacije Dynamics 365**.
4. Na seznamu poiščite **Microsoft Dynamics 365 Project Operations** in v stolpcu **Stanje** izberite **Na voljo je posodobitev**.
5. Izberite potrditveno polje **Strinjam se s pogoji storitve** in nato izberite **Posodobi**. Nameščena bo najnovejša različica rešitve.

Po končani namestitvi boste imeli nameščeno različico 4.5.0.134.

## <a name="configure-new-features"></a>Konfiguracija novih funkcij

### <a name="enable-dual-write-mapping"></a>Omogočanje preslikave dvojnega zapisovanja

Ko končate posodobitev v okoljih Finance in Dataverse, lahko omogočite zahtevane preslikave dvojnega zapisovanja. Dokončajte naslednje postopke, da omogočite preslikave dvojnega zapisovanja.

- [Posodobitev varnostnih nastavitev v okolju Customer Engagement](#security)
- [Osvežitev entitet podatkov](#refresh)
- [Posodobitev in zagon preslikav dvojnega zapisovanja](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Posodobitev varnostnih nastavitev v okolju Dataverse

Naslednje posodobitve varnostnih pravic za entitete so zahtevane kot del posodobitve na UR5.

1. V svojem okolju Dataverse pojdite na **Nastavitve** in v skupini **Sistem** izberite **Varnost**.

![Nastavitve okolja Dataverse.](media/Picture21.png)

2. Izberite **Varnostne vloge**.
3. Na seznamu vlog izberite **uporabnik aplikacije dvojnega zapisovanja** in izberite zavihek **Entitete po meri**. 
4. Prepričajte se, da ima vloga dovoljenji **Branje** in **Prilaganje k** za:

      - **Vrsta menjalnega tečaja valute**
      - **Kontni načrt** 
      - **Poslovni koledar** 
      - **Knjiga**

5. Ko je varnostna vloga posodobljena, pojdite na **Nastavitve** > **Varnost** > **Ekipe**. Prepričajte se, da je bila vloga **uporabnik aplikacije dvojnega zapisovanja** uporabljena za ekipo. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Osvežitev entitet podatkov iz posodobitve

1. V svojem okolju Finance odprite delovni prostor **Upravljanje podatkov** in nato odprite stran **Parametri ogrodja**.
2. Na zavihku **Nastavitve entitete** izberite **Osvežitev seznama entitet**.
3. Izberite **Zapri**, da potrdite osvežitev entitet.

 > [!NOTE]
 > Ta postopek do konca traja približno 20 minut. Ko je osvežitev končana, boste obveščeni.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Posodobitev preslikav dvojnega zapisovanja

1. V delovnem prostoru **Upravljanje podatkov** izberite **Dvojno zapisovanje**.
2. Izberite **Uporabi rešitvi**, izberite obe rešitvi na seznamu in nato izberite **Uporabi**.
3. Na strani **Dvojno zapisovanje** izberite naslednje preslikave tabel in nato izberite **Ustavi**.

    - **Dejanske vrednosti integracije storitve Project Operations (msdyn_actuals)**
    - **Kategorije stroškov projekta za integracijo storitve Project Operations (msdyn_expensecategories)**
    - **Entiteta za izvoz stroškov projekta dejanskih vrednosti integracije storitve Project Operations (msdyn_expenses)**

4. Na strani **Različica preslikave tabele** uporabite novo različico preslikave za vsako od treh entitet.
5. Na strani **Dvojno zapisovanje** izberite izvajanje za ponovni zagon preslikav.
6. Na seznamu preslikav izberite preslikavo **Knjiga (msdyn_ledgers)** z vsemi zahtevami in izberite potrditveno polje **Začetna sinhronizacija**. 
7. V polju **Glavni za začetno sinhronizacijo** izberite **Aplikacije Finance and Operations** in nato izberite **Zagon**.
 
 ![Sinhronizacija preslikave knjige.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]