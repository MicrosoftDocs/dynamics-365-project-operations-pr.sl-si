---
title: Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov – poenostavljena različica
description: Ta tema vsebuje informacije o uporabi predstavitvenih podatkov za nastavitev in konfiguracijo za storitev Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e25d358f1fd7705d580855d372d85690f6a5e265d3ba2b60fc26742bf3edc86f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993306"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov za Project Operations – poenostavljena različica 

_**Poenostavljena uvedba – od posla do izstavitve predračuna_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Zahteve

Preden začnete s konfiguracijo morate imeti omogočeno okolje Common Data Service (CDS) za Dynamics 365 Project Operations.


## <a name="instructions"></a>Navodila

1. Prenesite [paket glavnih podatkov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Pomaknite se v mapo *ProjOpsSampleSetupData - CE only CMT* in zaženite izvedljivo datoteko, *DataMigrationUtility*.
3. Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.

    ![Selitev konfiguracije.](./media/1ConfigurationMigration.png)

4. Na 2. strani čarovnika CMT izberite **Microsoft 365** kot možnost **Vrsta uvajanja**.
5. Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.
6. Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.

   ![Vpis v konfiguracijo.](./media/2ConfigurationSignin.png)

7. Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in nato izberite **Prijava**.
8. Na strani 4 izberite datoteko zip *SampleSetupAndConfigData* iz razpakirane mape *ProjOpsSampleSetupData - CE only CMT*.

   ![Datoteka ZIP.](./media/3ZipFile.png)

   ![Izbiranje datoteke.](./media/4SelectAFile.png)

9. Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.

   ![Uvoz podatkov.](./media/5ImportData.png)

10. Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja. Ko se konča, zapustite čarovnik CMT. 
11. Preverite, ali ima vaša organizacija podatke o naslednjih 18 entitetah:

    -   Valuta
    -   Račun
    -   Organizacijska enota
    -   Stik
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

    ![Uvoz je končan.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
