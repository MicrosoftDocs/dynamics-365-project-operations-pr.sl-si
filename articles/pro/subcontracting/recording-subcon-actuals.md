---
title: Beleženje časa, stroškov in uporabe materiala za podizvajalske komponente
description: V tem članku je pojasnjeno, kako Microsoft Dynamics 365 Project Operations spremlja čas, stroške in porabo materiala, zabeleženo pri projektih iz podizvajalskih komponent.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Beleženje časa, stroškov in uporabe materiala pri projektih za podizvajalske komponente

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V tem članku je pojasnjeno, kako Microsoft Dynamics 365 Project Operations spremlja čas, stroške in porabo materiala, zabeleženo pri projektih iz podizvajalskih komponent.

## <a name="costing-for-subcontractor-time-on-projects"></a>Stroški za čas podizvajalcev pri projektih
V aplikaciji Project Operations lahko pogodbeni delavci beležijo čas pri projektih na podoben način kot zaposleni. Pri vnašanju časa pri projektih in/ali projektnih opravilih lahko pogodbeni delavec izbere določeno podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe.

Ko je čas, ki ga predložijo pogodbeni delavci, odobren, se stroški projekta zapišejo na meri cene na enoto, ki je nastavljena za ta vir pogodbenega delavca v razdelku **Cene vlog** cenika nabave na podizvajalski pogodbi.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Izračun stroškov podizvajalskih pogodb za projekte
Pri vnosu nastalih stroškov na projektih lahko na vnosu stroškov izberete podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe. 

Ko je vnos stroškov predložen in odobren, se stroški zapišejo za projekt za ceno na enoto, ki je nastavljena za to kategorijo transakcij v razdelku **Cene kategorij** cenika nabave na podizvajalski pogodbi.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Izračun stroškov za materiale podizvajalskih pogodb za projekte
Pri vnosu porabe materiala na projektih lahko na vnosu stroškov izberete podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe v dnevniku uporabe materiala. Ko je dnevnik uporabe materiala predložen in odobren, se stroški materiala zapišejo za projekt za ceno na enoto, ki je nastavljena za ta izdelek v razdelku **Elementi cenika** na ceniku podizvajalske pogodbe.

Uporabo materiala je mogoče zapisati tudi za izdelke projekta, ki niso v katalogu. Ta vrsta uporabe materiala je lahko povezana tudi s podizvajalsko pogodbo in podrobnostmi podizvajalske pogodbe. Ko zapisujete uporabo materiala za izdelke, ki niso v katalogu, morate vnesti ceno za enoto izdelka, ki ni v katalogu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
