---
title: Sinhronizirajte status projekta, da preprečite vstop v zaprte projekte
description: Ta članek pojasnjuje, kako sinhronizirati status projekta, da preprečite vstop v neaktivne ali zaprte projekte.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinhronizirajte status projekta, da preprečite vstop v zaprte projekte

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

## <a name="scenario"></a>Scenarij

Contoso je v živo z Microsoftom Dynamics 365 Project Operations za scenarije virov/nezaloženih. Kot del običajnih poslovnih dejavnosti se lahko projekti zaključijo ali odložijo. Projekt lahko deaktivirate, da zagotovite, da ne nastanejo stroški ali računi.

## <a name="solution"></a>Rešitev

### <a name="prerequisites"></a>Zahteve

-   Microsoft Dynamics Nameščen mora biti 365 Finance 10.0.29 ali novejši.
-   Zemljevid dvojnega pisanja 1.0.0.3 za projekte V2 (msdyn\_ projekti) je treba namestiti ali ročno konfigurirati, kot je opisano spodaj.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Ustvarite posodobljeno različico preslikave dvojnega pisanja za integracijo Project Operations Projects V2

Če želite posodobiti preslikavo dvojnega pisanja Project Operations Projects V2:

1. Pojdi na **Upravljanje podatkov** delovni prostor in izberite **Dvojno pisanje**.
2. Izberite **Dvojno pisanje** ploščica.
3. Od T **Namizni zemljevid** stolpec, poiščite in izberite **Projekt V2 (msdyn\_ projekti)** in nato izberite Ustavi.
4. Izberite ime zemljevida, da odprete zemljevid, in nato izberite **[brez]**.
5. V pogovornem oknu Izberi stolpec izberite **državna koda\[ Status projekta\]** in nato izberite V redu. Lahko tipkaš **država** v vrednosti filtra, da zožite seznam.
6.  Izberite **Dodajte ali uredite transformacijo** v **vrsta zemljevida** stolpec za urejanje transformacije.
7.  Od **Vrsta preoblikovanja** izberite **ValueMap**.
8.  Izberite **Dodajte preslikavo vrednosti** in nato dodajte naslednje **Ključi** in **Vrednote**:

   Tipka       | Vrednost 
   ----------|-------
   V teku | 0     
   končano | 1     

![Posnetek zaslona, ki prikazuje preslikavo dvojnega pisanja](media/projectstage-dw-mapping.png)

9. Izberite **Shrani**.
10. Z vrha **Dvojno pisanje > Projekti V2 (msdyn_projects)** stran, izberite **Shrani kot**.
11. Od **Dodaj tabelo** v **Založnik** polje izberite **Privzeti založnik CDS**.
12. Nastavite **Različica** polje za 1.0.0.3.
13. Vrsta a **Opis** in nato izberite **Shrani**.
14. Z vrha **Dvojno pisanje > Projekti V2 (msdyn_projects)** stran, izberite **Teči** za zagon zemljevida in nato poiščite **ja** če se zahteva potrditev pred začetkom. 

### <a name="close-a-newly-completed-project"></a>Zaprite pravkar zaključen projekt

Dynamics 365 Finance uporablja **fazi projekta** polje za razlikovanje med projekti **v teku** oz **Dokončano**. **Dokončano** projekti ne morejo povzročiti stroškov ali biti zaračunani strankam.

1. Odprite projekt za deaktivacijo.
2. Na traku izberite **Deaktiviraj**.

> [!NOTE]
> Projekt lahko deaktivirate ali zaprete, saj se bosta oba v kontekstu Finance obnašala enako.

3. V Financah odprite **Seznam vseh projektov** strani.
4. Potrdite, da deaktivirani projekt ni prikazan na seznamu.
5. V **razstavni projekti** filter nad seznamom, spremenite vrednost iz **Aktiven** do **Vse**.
6. Zdaj boste videli deaktiviran projekt.

Če poskušate zabeležiti čas ali stroške za ta projekt v Financah, ne bi smeli videti projekta za izbiro. Če ročno vnesete številko projekta za strošek, boste videli sporočilo, kot je »Zaključena faza projekta ne dovoljuje snemanja v projektu«. Izdajanje računov in druge funkcije zaračunavanja bi morale biti onemogočene, saj bodo v okviru zaprtega projekta.

