---
title: Potrdite račune prodajalca projekta
description: V tem članku je razloženo, kako potrditi račun prodajalca projekta v Microsoftu Dynamics 365 Project Operations in opisuje finančni učinek potrditve računa prodajalca projekta.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475490"
---
# <a name="confirm-project-vendor-invoices"></a>Potrdite račune prodajalca projekta

**Velja za**: za scenarije v aplikaciji Project Operations, ki temeljijo na virih/nezalogi

Ko **Potrebna je ročna potrditev PM** parameter omogočen, računi dobavitelja, ki so ustvarjeni v Microsoft Dataverse imajo **Osnutek** stanje. Tako oblikovane račune dobaviteljev je treba pregledati in ročno potrditi. Ko **Potrebna je ročna potrditev PM** parameter onemogočen, računi dobavitelja, ki so ustvarjeni v Dataverse se samodejno potrdijo. Nadaljnji ukrepi niso potrebni. 

Ko preverite vse vrstice na računu dobavitelja v Dynamics 365 Project Operations, izberite **Potrdi** za potrditev računa prodajalca.

Ko izberete **Potrdi** na računu prodajalca se zgodi naslednje:

1. Status računa dobavitelja se posodobi na **Potrjeno**.
1. Potrjeni račun dobavitelja in z njim povezani zapisi postanejo samo za branje in jih ni mogoče urejati ali brisati.
1. Če se kateri koli dejanski stroški sklicujejo na vrstico računa dobavitelja kot del postopka ujemanja, so vsi dejanski stroški, ki so povezani z referenčno vrstico računa dobavitelja, obrnjeni.
1. Novi dejanski stroški se ustvarijo z uporabo informacij v vrstici računa dobavitelja.
1. Ne morete več ustvariti dnevnikov popravkov, obdelati odpoklicev časovnih vnosov ali preklicati odobritve izvirnega časa, stroškov ali bistvenih dejanskih vrednosti, ki so bile razveljavljene.
1. V Dynamics 365 Finance je **Stroški projekta** vrednost se posodobi z uporabo dnevnika integracije projekta, račun integracije nabave pa je *obrnjeno* po objavi dnevnika integracije projekta.

> [!NOTE]
> Če ima katera koli vrstica na računu dobavitelja status preverjanja, ki ni **Popolna**, računa dobavitelja ni mogoče potrditi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
