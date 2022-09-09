---
title: Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov – poenostavljena različica
description: Ta članek nudi informacije o uporabi predstavitvenih nastavitev in konfiguracijskih podatkov za Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410056"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov za Project Operations – poenostavljena različica 

_**Poenostavljena uvedba – od posla do izstavitve predračuna_



## <a name="prerequisites"></a>Zahteve

Preden začnete s konfiguracijo, morate imeti a Dataverse okolje, predvideno za Dynamics 365 Project Operations.


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
