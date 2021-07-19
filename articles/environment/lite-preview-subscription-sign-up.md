---
title: Prijava za naročnino na predogledno različico – poenostavljena različica
description: Ta tema vsebuje informacije o tem, kako se lahko naročite in uvedete poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334802"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Prijava za naročnino na predogledno različico – poenostavljena različica 

Ta tema vsebuje informacije o tem, kako se naročiti na preskusno različico in uvesti poenostavljeno uvajanje storitve Dynamics 365 Project Operations – od posla do izstavitve predračuna.

> [!NOTE]
> Ta postopek se bo spremenil v prihodnjih izdajah storitve Project Operations.

## <a name="prerequisites"></a>Zahteve
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure. Med prvim koriščenjem ponudbe lahko ustvarite najemnika.

> [!IMPORTANT]
> To nalogo mora opraviti samo ena oseba in sicer skrbnik najemnika v organizaciji. Če niste naročnik te izdaje, počakajte, da se organizacija prijavi in prejmete svoje uporabniške poverilnice.
> 
> Preskusne različice v najemniku so namenjene enkratni uporabi. Preskusno različico lahko namestite samo enkrat. Priporočamo, da za preskusno različico ustvarite novega najemnika.

### <a name="dynamics-365-project-operations-trial"></a>Preskus storitve Dynamics 365 Project Operations 

Preden začnete, se prepričajte, da ste prijavljeni v brskalnik z uporabnikovim službenim računom v najemniku, kjer želite imeti predogled aplikacije Project Operations.

1. Izberite možnost [Preskusna različico aplikacije Project Operations](https://aka.ms/try-po) in izkoristite prvo kodo v okviru ponudbe **Dynamics 365 Project Operations**.
2. Potrdite svoje naročilo.

  Prikazalo se vam bo potrditveno sporočilo, da je bila ponudba uspešno obdelana.

## <a name="assign-licenses"></a>Dodeljevanje licenc

> [!IMPORTANT]
> Potrebovali boste skrbniški dostop do portala Microsoft 365 vaše organizacije, če želite dokončati naslednje korake.


1. Odprite [skrbniško središče za Microsoft 365](https://portal.office.com/), da dodelite licence svojim uporabnikom.
2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.
3. Preverite, ali je licenca **Dynamics 365 Project Operations** izbrana. 
4. Izberite **Shrani spremembe**.

## <a name="create-a-new-dataverse-environment"></a>Ustvarite novo okolje Dataverse

1. Zagotovite si novo okolje za uvajanje Dataverse v aplikaciji Project Operations tako, da upoštevate navodila v temi [Model uvajanja Dataverse](lite-deployment.md). Ko izberete vrsto okolja, obvezno izberite **Poskusna različica (na podlagi naročnine)**.

  ![Novo okolje](./media/19CreateEnvironment.png)

2. Izberite nastavitev **Omogoči aplikacije Dynamics 365** in pustite polje **Samodejno uvedi te aplikacije** prazno.  
3. Izberite **Shrani**, da ustvarite okolje.

  ![Dodaj zbirko podatkov](./media/20CreateEnvironment1.png)

4. Ko je okolje ustvarjeno, namestite rešitev **Microsoft Dynamics 365 Project Operations**. 

![Namestitev rešitve](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Namestitev predstavitvenih podatkov za nastavitev in konfiguracijo CDS

Namestite konfiguracijo CDS in nastavite predstavitvene podatke ob upoštevanju navodil v temi [Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
