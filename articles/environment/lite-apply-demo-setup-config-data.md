---
title: Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov – poenostavljena različica
description: Ta tema vsebuje informacije o uporabi predstavitvenih podatkov za nastavitev in konfiguracijo za storitev Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401283"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov za Project Operations – poenostavljena različica 

_**Poenostavljena uvedba – od posla do izstavitve predračuna_

## <a name="prerequisites"></a>Zahteve

Preden začnete konfiguracijo morate imeti omogočeno okolje Common Data Service (CDS) za Dynamics 365 Project Operations.


## <a name="instructions"></a>Navodila

1. Prenesite [paket glavnih podatkov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – integrirani CMT* in zaženite izvedljivo datoteko *DataMigrationUtility*.
3. Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. strani čarovnika CMT izberite **Microsoft 365** kot možnost **Vrsta uvajanja**.
5. Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.
6. Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.

![Prijava v konfiguracijo](./media/2ConfigurationSignin.png)

7. Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in nato izberite **Prijava**.
8. Na 4. strani izberite datoteko ZIP, *MasterAndSetupData* iz razstavljene mape, *ProjOpsDemoDataSetupAndMaster – integrirani CMT*.

![Datoteka ZIP](./media/3ZipFile.png)

![Izberite datoteko](./media/4SelectAFile.png)

9. Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.

![Uvozi podatke](./media/5ImportData.png)

10. Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja. Ko se konča, zapustite čarovnik CMT. 
11. Preverite, ali ima vaša organizacija podatke o naslednjih 20 entitetah:

-   Valuta
-   Račun
-   Organizacijska enota
-   Stik
-   Skupina davka
-   Skupina strank
-   Enota
-   Skupina enot
-   Cenik
-   Cenik parametrov projekta 
-   Pogostost izdajanja računov
-   Kategorija vira, ki ga je mogoče rezervirati
-   Kategorija transakcije
-   Kategorija stroška
-   Cena vloge
-   Cena kategorije transakcije
-   Značilnost
-   Vir, ki ga je mogoče rezervirati
-   Povezava kategorije vira, ki ga je mogoče rezervirati
-   Lastnost vira, ki ga je mogoče rezervirati

![Zaključek uvoza](./media/6CompleteImport.png)
