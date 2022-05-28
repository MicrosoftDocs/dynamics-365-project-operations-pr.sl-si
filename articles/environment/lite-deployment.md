---
title: Uvedba aplikacije Project Operations – poenostavljena različica
description: Ta tema vsebuje informacije o tem, kako lahko namestite poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580752"
---
# <a name="deploy-project-operations---lite"></a>Uvedba aplikacije Project Operations – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_



Storitev Project Operations podpira več modelov uvedbe. Če želite določiti najboljši model uvedbe, glejte [Vrste uvajanja](determine-deployment-type.md).


> [!IMPORTANT]
> Ta uvedba, poenostavljena uvedba – od posla do izstavitve predračuna, vodi v **uvedbo zgolj možnosti Dataverse za storitev Project Operations**.

- [Namestite Project Operations v novo Dataverse okolje](#new)
- [Namestite v obstoječo Dataverse okolje](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Namestite Project Operations na novo Dataverse okolje

1. Kot [Globalno oz Power Platform skrbnik](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations ustvarite novo Dataverse okolje v [Skrbniško središče PowerPlatform](https://admin.powerplatform.com). Poskrbi da **Ustvarite bazo podatkov za to okolje** in **Aplikacije Dynamics 365** so omogočene. Za več informacij glejte [Ustvarjanje in upravljanje okolij v skrbniškem središču Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Izberite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Namestite Project Operations na obstoječo Dataverse okolje
1. Prepričajte se, da okolje ni bilo konfigurirano s [dvojno pisanje](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) saj bo namestitev nato namestila [Projektne operacije za scenarije, ki temeljijo na virih/brez zalog](project-operations-integrated-deployment-overview.md) zmogljivosti.
2. Kot [globalni skrbnik ali skrbnik Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations poiščite okolje v [skrbniškem centru PowerPlatform](https://admin.powerplatform.com), kamor želite namestiti Project Operations.
3. Namestite **Microsoft Dynamics 365 Project Operations** s seznama za uvajanje aplikacij Dynamics 365. Če želite več informacij, glejte [Upravljanje aplikacij Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
