---
title: Odstranitev rešitve Dynamics 365 Project Operations
description: Ta tema vsebuje informacije o odstranjevanju aplikacije Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783663"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Odstranitev rešitve Dynamics 365 Project Operations 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Za odstranitev aplikacije Dynamics 365 Project Operations vam mora biti dodeljena vloga skrbnika.

1. Odprite možnost **Nastavitve** > **Rešitve**.

    ![Stran »Nastavitve«.](./media/uninstall-proj-ops-solutions.png)
  
2. Odstranite rešitve v enakem vrstnem redu, kot so navedene v naslednji tabeli. 

    | Korak | Ime   rešitve                                    | Opomba                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Če je ne najdete, preskočite to rešitev.                                                            |
    | 2 | ProjectOperations_Anchor                           | Če je ne najdete, preskočite to rešitev.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Če je ne najdete, preskočite to rešitev.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Če je ne najdete, preskočite to rešitev.                                                            |
    | 5 | ProjectService                                     | Ni dodatnih opomb.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Ni dodatnih opomb.                                                                         |
    | 7 | ProjectServiceCore                                 | Ni dodatnih opomb.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Če je ne najdete, preskočite to rešitev.                                                            |
    | 9 | FieldServiceCommon                                 | Zahtevano za dvojno zapisovanje z aplikacijo Dynamics 365 Finance ali Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Zahtevano za dvojno zapisovanje z aplikacijo Dynamics 365 Finance ali Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Zahtevano za Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Če je ne najdete, preskočite to rešitev.                                                            |
    | 19 | Dynamics365Notes                                   | Če je ne najdete, preskočite to rešitev.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Če je ne najdete, preskočite to rešitev.                                                            |
    | 21 | DualWriteCore                                      | Če je ne najdete, preskočite to rešitev.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Če je ne najdete, preskočite to rešitev.                                                            |
    | 23 | Dynamics365AssetManagement                         | Če je ne najdete, preskočite to rešitev.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Če je ne najdete, preskočite to rešitev.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Če je ne najdete, preskočite to rešitev.                                                            |
    | 26 | HCMCommon                                          | Če je ne najdete, preskočite to rešitev.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Če je ne najdete, preskočite to rešitev.                                                            |
    | 28 | Udeleženec                                              | Če je ne najdete, preskočite to rešitev.                                                            |
    | 29 | Dynamics365Company                                 | Če je ne najdete, preskočite to rešitev.                                                            |
    | 30 | CurrencyExchangeRates                              | Če je ne najdete, preskočite to rešitev.                                                            |
    | 31 | AssetCommon                                        | Če je ne najdete, preskočite to rešitev.                                                            |
