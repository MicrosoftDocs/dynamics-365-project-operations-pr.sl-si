---
title: Uporaba predstavitvenih podatkov v okolju, gostovanem v oblaku Finance
description: Ta tema vsebuje razlago, kako uporabiti predstavitvene podatke iz storitve Project Operations v okolju Dynamics 365 Finance v oblaku.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c04aab6ffb332a3095ca2a7890deb73f15a8b5e3713021c60eec02eb13dbd0cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009686"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Uporaba predstavitvenih podatkov v okolju, gostovanem v oblaku Finance

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

> [!IMPORTANT]
> Ta tema se nanaša samo na Microsoft Dynamics 365 Finance različice 10.0.13 in jo je mogoče izvajati samo v okolju, ki je gostovano v oblaku. Dokončajte korake v tej temi, **PREDEN** izvedete posodobitev kakovosti v okolju.

1. V projektu LCS odprite stran **Podrobnosti o okolju**. Upoštevajte, da vključuje podrobnosti, ki so potrebne za povezavo z okoljem prek protokola RDP (Remote Desktop Protocol).

![Podrobnosti o okolju.](./media/1EnvironmentDetails.png)

Prvi nabor označenih poverilnic so poverilnice lokalnih računov, ki vsebujejo hiperpovezavo do povezave z oddaljenim namizjem. Poverilnice vključujejo uporabniško ime in geslo skrbnika okolja. Drugi nabor poverilnic se uporablja za prijavo v strežnik SQL Server v tem okolju.

2. Povežite se z oddaljenim okoljem prek hiperpovezave v možnosti **Lokalni računi** in uporabite **Poverilnice lokalnega računa** za preverjanje pristnosti.
3. Odprite **Internet Information Services** > **Skupine programov** > **AOSService** in zaustavite storitev. S tem boste zaustavili storitev, da boste lahko nadaljevali z menjavo zbirke podatkov SQL.

![Zaustavitev storitve AOS.](./media/2StopAOS.png)

4. Odprite možnost **Storitve** in zaustavite naslednja dva elementa:

- Microsoft Dynamics 365 Unified Operations: storitev za paketno upravljanje
- Microsoft Dynamics 365 Unified Operations: ogrodje za uvoz in izvoz podatkov

![Zaustavitev storitev.](./media/3StopServices.png)

5. Odprite Microsoft SQL Server Management Studio. Prijavite se s poverilnicami strežnika SQL in uporabite uporabniško ime in geslo za axdbadmin na strani **Podrobnosti o okoljih LCS**.

![Storitev SQL Server Management Studio.](./media/4SSMS.png)

6. V raziskovalcu predmetov odprite **Zbirke podatkov** in poiščite **AXDB**. Zbirko podatkov boste zamenjali z novo, ki se nahaja v [Središču za prenose](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopirajte datoteko ZIP v VM, v katerega ste prijavljeni na daljavo, in razširite vsebino datoteke ZIP.
8. V programu SQL Server Management Studio z desno tipko miške kliknite **AxDB** in nato izberite **Opravila** > **Obnovitev** > **Zbirka podatkov**.

![Obnovitev zbirke podatkov.](./media/5RestoreDatabase.png)

9. Izberite **Izvorna naprava** in se pomaknite do datoteke, ki ste jo razširili iz kopirane datoteke ZIP.

![Izvorne naprave.](./media/6SourceDevice.png)

10. Izberite **Možnosti** in nato **Prepiši obstoječo zbirko podatkov** in **Zapri obstoječe povezave do ciljne zbirke podatkov**. 
11. Izberite **V redu**.

![Obnovitev nastavitev.](./media/7RestoreSetting.png)

Prejeli boste potrditev, da je bila obnovitev AXDB uspešna. Ko prejmete to potrditev, lahko zaprete SQL Services Management Studio.

12. Vrnite se do **Internet Information Services** > **Skupine programov** > **AOSService** in zaženite storitev AOSService.
13. Odprite **Storitve** in zaženite obe storitvi, ki ste ju predhodno zaustavili.

14. Poiščite orodje AdminUserProvisioning na tej VM. Poglejte v K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Zaženite datoteko .ext, tako da vpišete svoj uporabniški naslov v polje **E-poštni naslov**. 
16. Izberite **Pošlji**.

![Omogočanje uporabe skrbnikom.](./media/8AdminUserProvisioning.png)

To traja nekaj minut. Prejeti bi morali potrditveno sporočilo, da je bil skrbnik uspešno posodobljen.

17. Na koncu zaženite ukazni poziv kot skrbnik in izvedite ukaz iisreset

![Ponastavitev storitev IIS.](./media/9IISReset.png)

18. Zaprite sejo oddaljenega namizja in uporabite stran **Podrobnosti o okolju** LCS, da se prijavite v okolje in potrdite, da deluje po pričakovanjih.

![Storitve Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]