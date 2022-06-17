---
title: Beleženje časa, stroškov in uporabe materiala za podizvajalske komponente
description: V tem članku je razloženo, kako Microsoft spremlja porabo časa, stroškov in materiala, zabeležene pri projektih iz podizvajalcev Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927670"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Beleženje časa, stroškov in porabe materiala pri projektih za podizvajalske komponente

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V tem članku je razloženo, kako Microsoft spremlja porabo časa, stroškov in materiala, zabeležene pri projektih iz podizvajalcev Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Stroški časa podizvajalcev pri projektih
V projektnem poslovanju lahko pogodbeni delavci beležijo čas na projektih na podoben način kot zaposleni. Pri vnašanju časa za projekte in/ali projektne naloge lahko pogodbeni delavec izbere določeno podizvajalsko in podizvajalsko vrstico.

Ko je čas, ki ga predložijo pogodbeni delavci, odobren, se stroški projekta evidentirajo z uporabo stroškovne stopnje na enoto, ki je določena za ta vir pogodbenega delavca v **Cene vlog** razdelku nabavnega cenika na podizvajalski pogodbi.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Stroški za podizvajalske stroške pri projektih
Pri vnosu stroškov, ki nastanejo pri projektih, lahko na vnosu stroškov izberete vrstico podizvajalcev in podizvajalcev. 

Ko je ta vnos odhodkov predložen in odobren, se stroški odhodkov zapišejo v projekt na podlagi stroškov na enoto, ki so nastavljeni za to kategorijo transakcij v **Cene kategorij** razdelku nabavnega cenika na podizvajalski pogodbi.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Stroški za podizvajalske materiale za projekte
Pri vnašanju porabe materiala na projektih lahko v dnevniku porabe materiala izberete vrstico podizvajalcev in podizvajalcev. Ko je dnevnik porabe materiala predložen in odobren, se stroški materiala evidentirajo na projektu na podlagi stroškov na enoto, ki so za ta izdelek določeni v **Artikli na ceniku** razdelek cenika podizvajalcev.

Porabo materiala je mogoče zabeležiti tudi za izdelke za vpis v projekte. To vrsto uporabe materiala je mogoče povezati tudi s podizvajalcem in podizvajalsko linijo. Pri evidentiranju porabe materiala za vpisne izdelke morate vnesti strošek na enoto vpisanega izdelka. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
