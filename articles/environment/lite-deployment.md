---
title: Namestite Project Operations Lite
description: Ta članek vsebuje informacije o tem, kako lahko namestite poenostavljeno uvedbo aplikacije Project Operations – od posla do izstavitve predračuna.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810999"
---
# <a name="deploy-project-operations-lite"></a>Namestite Project Operations Lite

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_



Storitev Project Operations podpira več modelov uvedbe. Če želite določiti najboljši model uvedbe, glejte [Vrste uvajanja](determine-deployment-type.md).


> [!IMPORTANT]
> Ta uvedba, poenostavljena uvedba – od posla do izstavitve predračuna, vodi v **uvedbo zgolj možnosti Dataverse za storitev Project Operations**.

- [Namestitev aplikacije Project Operations v novo okolje Dataverse](#new)
- [Namestitev v obstoječe okolje Dataverse](#existing)
- [Namestitev v obstoječe Dataverse okolje, ki ima komponente za dvojno pisanje](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Namestite Project Operations Lite v novo Dataverse okolje

1. Kot [globalni skrbnik ali skrbnik za Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations ustvarite novo okolje Dataverse v [skrbniškem središču PowerPlatform](https://admin.powerplatform.com). Prepričajte se, da sta omogočeni možnosti **Ustvarjanje zbirke podatkov za to okolje** in **Aplikacije Dynamics 365**. Za več informacij glejte [Ustvarjanje in upravljanje okolij v skrbniškem središču Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Izberite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Namestite Project Operations Lite v obstoječe Dataverse okolje 
1. Kot [globalni skrbnik ali skrbnik Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations poiščite okolje v [skrbniškem centru PowerPlatform](https://admin.powerplatform.com), kamor želite namestiti Project Operations.
1. Namestite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365. Če želite več informacij, glejte [Upravljanje aplikacij Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Namestite Project Operations Lite v obstoječe Dataverse okolje, kjer so že prisotne rešitve za dvojno pisanje

Če želite še naprej izvajati Project Operations v načinu Lite Deployment, sledite tem korakom:

1. Kot [globalni skrbnik ali skrbnik Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations poiščite okolje v [skrbniškem centru PowerPlatform](https://admin.powerplatform.com), kamor želite namestiti Project Operations.
1. Namestite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365. Če želite več informacij, glejte [Upravljanje aplikacij Dynamics 365](/power-platform/admin/manage-apps).
1. Ker ima vaše okolje nameščene komponente dvojnega pisanja, ki pomagajo pri integraciji v aplikacije za finance in operacije, bo namestitev Project Operations namestila tudi zmožnosti in razširitve, potrebne za integracijo podatkov, povezanih s projektom, v aplikacije za finance in operacije. Ker želite zagnati Project Operations v uvajanju Lite, je treba te integracijske komponente odstraniti, saj bodo ustvarile omejitve in stroške za scenarije uvajanja Lite. Ročno odstranite rešitvi **Dynamics 365 Project Operations Dual Write** in **Dynamics 365 Project Operations Dual Write Entity Maps** da odstranite te komponente.
1. Pojdite na **Projektne operacije -> Nastavitve -> Parametri**. Odprite stran s podrobnostmi **Project Parameter** in nastavite polje **Vedenje nadgradnje rešitve** na **Lite Samo**. To zagotavlja, da morebitne poznejše nadgradnje Project Operations ne bodo vrnile integracijskih komponent v Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
