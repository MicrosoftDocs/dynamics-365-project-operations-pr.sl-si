---
title: Uvedba aplikacije Project Operations – poenostavljena različica
description: Ta članek vsebuje informacije o tem, kako lahko namestite poenostavljeno uvedbo aplikacije Project Operations – od posla do izstavitve predračuna.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930338"
---
# <a name="deploy-project-operations---lite"></a>Uvedba aplikacije Project Operations – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_



Storitev Project Operations podpira več modelov uvedbe. Če želite določiti najboljši model uvedbe, glejte [Vrste uvajanja](determine-deployment-type.md).


> [!IMPORTANT]
> Ta uvedba, poenostavljena uvedba – od posla do izstavitve predračuna, vodi v **uvedbo zgolj možnosti Dataverse za storitev Project Operations**.

- [Namestitev aplikacije Project Operations v novo okolje Dataverse](#new)
- [Namestitev v obstoječe okolje Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Namestitev aplikacije Project Operations v novo okolje Dataverse

1. Kot [globalni skrbnik ali skrbnik za Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations ustvarite novo okolje Dataverse v [skrbniškem središču PowerPlatform](https://admin.powerplatform.com). Prepričajte se, da sta omogočeni možnosti **Ustvarjanje zbirke podatkov za to okolje** in **Aplikacije Dynamics 365**. Za več informacij glejte [Ustvarjanje in upravljanje okolij v skrbniškem središču Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Izberite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Namestitev aplikacije Project Operations v obstoječe okolje Dataverse
1. Prepričajte se, da okolje ni bilo konfigurirano z [dvojnim zapisovanjem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), saj bodo nato nameščene zmogljivosti [Project Operations , ki temeljijo na virih/nezalogi](project-operations-integrated-deployment-overview.md).
2. Kot [globalni skrbnik ali skrbnik Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations poiščite okolje v [skrbniškem centru PowerPlatform](https://admin.powerplatform.com), kamor želite namestiti Project Operations.
3. Namestite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365. Če želite več informacij, glejte [Upravljanje aplikacij Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
