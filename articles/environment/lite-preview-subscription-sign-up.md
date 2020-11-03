---
title: Prijava za naročnino predogleda
description: Ta tema vsebuje informacije o tem, kako se lahko naročite in uvedete poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084619"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Prijavite se na naročnino predogleda za poenostavljeno uvedbo – od posla do izstavitve predračuna

Ta tema pojasnjuje, kako se lahko naročite na ponudbo partnerja za predogled in nastavite poenostavljeno uvedbo storitve Dynamics 365 Project Operations – od posla do izstavitve predračuna.

> [!NOTE]
> Ta postopek se bo spremenil v prihodnjih izdajah storitve Project Operations.

## <a name="prerequisites"></a>Zahteve

- Prejeli boste e-poštno sporočilo z vabilom k sodelovanju v predogledu. Predogled lahko zahtevate na [spletnem mestu storitve Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure.
- Preglejte vse pogoje in določila.

## <a name="subscribe"></a>Naročite se

Ko prejmete odobritev [zahteve za predogled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), boste od Microsofta po elektronski pošti prejeli dve ponudbi. Te ponudbe omogočajo uvedbo predogleda Project Operations:

- Dynamics 365 Project Operations (CRM) – preskus predogleda
- Office 365 Project Operations – poskusna različica

> [!IMPORTANT]
> To nalogo mora opraviti samo ena oseba in sicer skrbnik najemnika v organizaciji. Če niste naročnik te izdaje, počakajte, da se organizacija prijavi in prejmete svoje uporabniške poverilnice.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – preskus predogleda 

Preden začnete, se prepričajte, da ste prijavljeni v brskalnik z uporabnikovim službenim računom v najemniku, kjer želite imeti predogled aplikacije Project Operations.

1. Unovčite kodo prve ponudbe **Dynamics 365 Project Operations (CRM) – preskusna različica** , tako da jo prilepite v URL brskalnika.

![Prevzem ponudbe](./media/16RedeemFirstOfferNew.png)

2. Potrdite svoje naročilo.
![Potrdite naročilo](./media/17ConfirmOrderNew.png)

Videli boste, da je bila ponudba za potrditev uspešno izkoriščena.

![Potrditev](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – poskusna različica

Ponovite enake korake kot pri kodi prve ponudbe. Ne pozabite dodati kode druge ponudbe z istim uporabniškim računom, ki je bil uporabljen za kodo prve ponudbe.

## <a name="assign-licenses"></a>Dodeljevanje licenc

> [!IMPORTANT]
> Potrebovali boste skrbniški dostop do portala Microsoft 365 vaše organizacije, če želite dokončati naslednje korake.


1. Odprite [skrbniško središče za Microsoft 365](https://portal.office.com/), da dodelite licence svojim uporabnikom.

![Začetna stran skrbniškega središča](./media/14AdminPortal.png)

2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.

![Dodeljevanje licenc](./media/15AssignLicenses.png)

3. Preverite, ali sta izbrani licenci za **Dynamics 365 Project Operations (CRM) predogledna različica** in **Office 365 Project Operations – predogledna različica**. 
4. Izberite **Shrani spremembe**.

## <a name="create-a-new-cds-environment"></a>Ustvarjanje novega okolja CDS

1. Zagotovite si novo okolje za uvajanje CDS Project Operations tako, da upoštevate navodila v temi [Model za uvajanje CDS](lite-deployment.md). Ko izberete vrsto okolja, obvezno izberite **Poskusna različica (na podlagi naročnine)**.
![Novo okolje](./media/19CreateEnvironment.png)

2. Izberite nastavitev **Omogoči aplikacije Dynamics 365** in pustite polje **Samodejno uvedi te aplikacije** prazno.  
3. Izberite **Shrani** , da ustvarite okolje.

![Dodaj zbirko podatkov](./media/20CreateEnvironment1.png)

4. Ko je okolje ustvarjeno, namestite rešitev **Microsoft Dynamics 365 Project Operations**. 

![Namestitev rešitve](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Namestitev predstavitvenih podatkov za nastavitev in konfiguracijo CDS

Namestite konfiguracijo CDS in nastavite predstavitvene podatke ob upoštevanju navodil v temi [Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo](lite-apply-demo-setup-config-data.md).
