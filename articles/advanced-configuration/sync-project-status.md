---
title: Sinhronizirajte status projekta, da preprečite vnose v zaprte projekte
description: Ta članek pojasnjuje, kako sinhronizirati stanje projekta, da preprečite vstop v neaktivne ali zaprte projekte.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348125"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinhronizirajte status projekta, da preprečite vnose v zaprte projekte

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

## <a name="scenario"></a>Scenarij

Družba Contoso je začela izvajati storitev Microsoft Dynamics 365 Project Operations za scenarije z viri/brez zalog. Kot del običajnih poslovnih dejavnosti se lahko projekti zaključijo ali zadržijo. Projekt lahko deaktivirate, da preprečite nastanek stroškov ali računov.

## <a name="solution"></a>Rešitev

### <a name="prerequisites"></a>Zahteve

-   Nameščena mora biti aplikacija Microsoft Dynamics 365 Finance različice 10.0.29 ali novejša.
-   Preslikava dvojnega zapisovanja 1.0.0.3 za Projekti V2 (msdyn\_projects) je treba namestiti ali ročno konfigurirati, kot je opisano spodaj.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Ustvarjanje posodobljene različico preslikave dvojnega zapisovanja za integracijo aplikacije Project Operations Projekti V2

Če želite posodobiti preslikavo dvojnega zapisovanja za aplikacijo Project Operations Projekti V2:

1. V delovnem prostoru **Upravljanje podatkov** izberite možnost **Dvojno zapisovanje**.
2. Izberite ploščico **Dvojno zapisovanje**.
3. V stolpcu **Preslikava tabele** poiščite in izberite možnost **Projekt V2 (msdyn\_projects)** in nato izberite možnost »Ustavi«.
4. Izberite ime preslikave, da jo odprete, in nato izberite možnost **[brez]**.
5. V pogovornem oknu »Izbira stolpca« izberite možnost **statecode\[Stanje projekta\]** in nato izberite možnost »V redu«. V vrednost filtra lahko vnesete **stanje**, da zožite seznam.
6.  V stolpcu **vrsta preslikave** izberite možnost **Dodajanje ali urejanje preoblikovanja**, če želite urejati preoblikovanje.
7.  V razdelku **Vrsta preoblikovanja** izberite možnost **ValueMap**.
8.  Izberite možnost **Dodajanje preslikave vrednosti** in nato dodajte naslednje **ključe** in **vrednosti**:

   Tipka       | Vrednost 
   ----------|-------
   InProcess | 0     
   končano | 1     

![Posnetek zaslona preslikave z dvojnim zapisovanjem](media/projectstage-dw-mapping.png)

9. Izberite **Shrani**.
10. Na vrhu strani **Dvojno zapisovanje > Projekti V2 (msdyn_projects)** izberite možnost **Shrani kot**.
11. V podoknu **Dodaj tabelo** v polju **Izdajatelj** izberite možnost **Privzeti izdajatelj CDS**.
12. Nastavite polje **Različica** na 1.0.0.3.
13. Vnesite **Opis** in nato izberite možnost **Shrani**.
14. Na vrhu strani **Dvojno zapisovanje > Projekti V2 (msdyn_projects)** izberite možnost **Zaženi**, da zaženete preslikavo, in nato izberite možnost **Da**, če je pred zagonom zahtevana potrditev. 

### <a name="close-a-newly-completed-project"></a>Zaprite pravkar zaključen projekt

Dynamics 365 Finance uporablja polje **stopnja projekta** za razlikovanje med projekti **v teku** in **dokončano**. **Dokončani** projekti ne morejo povzročiti stroškov ali biti zaračunani strankam.

1. Odprite projekt za deaktivacijo.
2. V zgornjem traku izberite polje **Deaktiviraj**.

> [!NOTE]
> Projekt lahko deaktivirate ali zaprete, saj se bosta oba v kontekstu aplikacije Finance obnašala enako.

3. V aplikaciji Finance odprite stran **Seznam vseh projektov**.
4. Potrdite, da deaktiviran projekt ni prikazan na seznamu.
5. V filtru **prikaz projektov** nad seznamom spremenite vrednost z **Aktivno** na **Vse**.
6. Zdaj boste videli deaktiviran projekt.

Če poskušate zabeležiti čas ali stroške za ta projekt v aplikaciji Finance, projekta ne bi smeli videti za izbiro. Če ročno vnesete številko projekta za strošek, boste videli sporočilo, kot je »Zaključena stopnja projekta ne dovoljuje snemanja v projektu«. Izdajanje računov in druge funkcije obračunavanja bi morale biti onemogočene, saj bodo v okviru zaprtega projekta.

