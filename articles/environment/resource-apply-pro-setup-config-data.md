---
title: Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations
description: Ta tema vsebuje informacije o nastavitvi in uporabi konfiguracijskih podatkov v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949080"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

## <a name="install-setup-and-configuration-data"></a>Namestitev podatkov za nastavitev in konfiguracijo

1. Prenesite, odblokirajte in razširite datoteko [Paket podatkov za namestitev in konfiguracijo](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Pomaknite se do mape z razširjenimi datotekami in zaženite izvedljivo datoteko *DataMigrationUtility*.
3. Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. strani čarovnika CMT izberite **Office 365** kot možnost **Vrsta uvajanja**.
5. Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.
6. Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.

![Prijava v konfiguracijo](./media/2ConfigurationSignin.png)

7. Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in kliknite **Prijava**.
8. Na 4. strani izberite datoteko ZIP *SampleSetupAndConfigData* iz razstavljene mape.

![Izbira datoteke ZIP](./media/3ZipFile.png)

![Izberite datoteko](./media/4SelectAFile.png)

9. Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.

![Uvozi podatke](./media/5ImportData.png)

10. Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja. Po dokončanem uvozu zapustite čarovnik CMT. 
11. Preverite, ali ima vaša organizacija podatke o naslednjih 19 entitetah:

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

## <a name="update-project-operations-configurations"></a>Posodobitev konfiguracij storitve Project Operations

1. Pomaknite se v okolje CE. Najdete ga tako, da odprete [skrbniško središče Power Platform](https://admin.powerplatform.microsoft.com/environments), izberete okolje in kliknete **Odpri okolje**. 

![Odpri okolje](./media/7OpenEnvironment.png)

2. Odprite **Projekti** > **Viri** in nato izberite **Novo**, da za svojega uporabnika ustvarite vir, ki ga je mogoče rezervirati.

![Viri, ki jih je mogoče rezervirati](./media/8BookableResources.png)

3. Na zavihku **Splošno** izberite skrbniškega uporabnika. Preverite, ali se časovni pas ujema s tistim, v katerem ste. 

![Novi vir, ki ga je mogoče rezervirati](./media/9NewBookableResource.png)

4. Na zavihku **Načrtovanje** v polju **Podjetje** izberite podjetje **USPM** in nato izberite **Shrani**. 

![Zavihek »Načrtovanje«](./media/10SchedulingTab.png)

5. Izberite zavihek **Delovni čas**.  

![Delovni čas](./media/11WorkHours.png)

6. Dvokliknite katero koli vrednost v koledarju in izberite **Uredi** > **Vsi dogodki v seriji**. 

![Delovni koledar](./media/12WorkCalendar.png)

7. Spremenite delovni čas v osemurni (8) delovnik, vikende označite kot dela proste dni in se prepričajte, da se časovni pas ujema z vašim. 
8. Izberite **Shrani in zapri**.

![Posodobitev koledarja](./media/13UpdateCalendar.png)

9. Odprite **Nastavitve** > **Predloge koledarja** in izberite **Novo**.
 
 ![Predloge koledarja](./media/14CalendarTemplates.png)
 
 10. Vnesite ime, izberite vir predloge, ki ste ga ustvarili, in nato **Shrani**. 
 
 ![Shranite predlogo koledarja](./media/15SaveCalendarTemplate.png)
 
 11. Odprite možnost **Parametri** in dvokliknite zapis. 
 
 ![Projektni parametri](./media/16ProjectParameters.png)
 
12. Posodobite naslednja polja:

 - **Privzeto podjetje**: USPM
 - **Privzeta organizacijska enota**: Contoso Robotics Global
 - **Pogostost izdajanja računov**: sedmi in zadnji dan
 - **Predloga delovnega časa**: preklopite na predlogo, ki ste jo ustvarili.

13. Izberite **Shrani**. 

![Posodobljeni projektni parametri](./media/17UpdatedProjectParameters.png)
