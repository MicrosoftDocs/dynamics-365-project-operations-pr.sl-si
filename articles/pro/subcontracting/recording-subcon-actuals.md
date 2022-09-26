---
title: Beleženje časa, stroškov in uporabe materiala za podizvajalske komponente
description: V tem članku je pojasnjeno, kako Microsoft spremlja porabo časa, stroškov in materiala, zabeleženega pri projektih iz podizvajalskih komponent Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522534"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Beleženje časa, stroškov in porabe materiala na projektih za komponente podizvajalcev

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V tem članku je pojasnjeno, kako Microsoft spremlja porabo časa, stroškov in materiala, zabeleženega pri projektih iz podizvajalskih komponent Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Stroški časa podizvajalcev na projektih
V projektnih operacijah lahko pogodbeni delavci beležijo čas na projektih na podoben način kot zaposleni. Pri vnosu časa na projektih in/ali projektnih nalogah lahko pogodbeni delavec izbere določeno podizvajalsko pogodbo in podizvajalsko postavko.

Ko je čas, ki ga predložijo pogodbeni delavci, odobren, se stroški projekta zabeležijo z uporabo stopnje stroškov na enoto, ki je nastavljena za ta vir pogodbenega delavca v **Cene vlog** del nabavnega cenika o podizvajalski pogodbi.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Obračunavanje stroškov podizvajalcev na projektih
Pri vnosu nastalih stroškov na projektih lahko na vnosu stroškov izberete podizvajalsko pogodbo in podizvajalsko vrstico. 

Ko je ta vnos stroškov predložen in odobren, se stroški stroškov zabeležijo v projektu na podlagi stroškov na enoto, ki je nastavljen za to kategorijo transakcije v **Cene kategorij** del nabavnega cenika o podizvajalski pogodbi.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Stroški podizvajalskih materialov na projektih
Pri vnosu porabe materiala na projektih lahko v dnevniku porabe materiala izberete podizvajalsko pogodbo in postavko podizvajalca. Ko je dnevnik porabe materiala predložen in odobren, se stroški materiala zabeležijo v projektu na podlagi stroškov na enoto, ki so za ta izdelek nastavljeni v **Artikli cenika** del cenika podizvajalcev.

Porabo materiala je mogoče zabeležiti tudi za vpisne izdelke v projektih. Ta vrsta porabe materiala je lahko povezana tudi s podizvajalsko pogodbo in podizvajalsko linijo. Ko beležite porabo materiala za vpisne izdelke, morate vnesti stroške na enoto vpisnega izdelka. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
