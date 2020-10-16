---
title: Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo
description: Ta tema vsebuje informacije o uporabi predstavitvenih podatkov za nastavitev in konfiguracijo za storitev Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949077"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo za poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna

_**Poenostavljena uvedba – od posla do izstavitve predračuna_

1. Prenesite [paket glavnih podatkov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – integrirani CMT* in zaženite izvedljivo datoteko *DataMigrationUtility*.
3. Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. strani čarovnika CMT izberite **Office 365** kot možnost **Vrsta uvajanja**.
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

- Valuta
- Organizacijska enota
- Stik
- Skupina davka
- Skupina strank
- Enota
- Skupina enot
- Cenik
- Cenik parametrov projekta
- Pogostost izdajanja računov
- Podrobnost o pogostosti izdajanja računov
- Kategorija vira, ki ga je mogoče rezervirati
- Kategorija transakcije
- Kategorija stroška
- Cena vloge
- Cena kategorije transakcije
- Značilnost
- Vir, ki ga je mogoče rezervirati
- Povezava kategorije vira, ki ga je mogoče rezervirati
- Lastnost vira, ki ga je mogoče rezervirati

![Zaključek uvoza](./media/6CompleteImport.png)
