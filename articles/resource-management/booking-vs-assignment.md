---
title: Rezervacije v primerjavi z dodelitvami
description: Ta tema ponuja informacije o razlikah med rezervacijami virov in dodeljevanjem virov.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008471"
---
# <a name="bookings-vs-assignments"></a>Rezervacije v primerjavi z dodelitvami

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Rezervacije so potrjene ali začasne dodelitve virov določenemu projektu. Potrjene rezervacije porabijo zmogljivost vira. Rezervacije predstavljajo organizacijske pojme za ekipe, da lahko te razumejo, kako bodo viri vključeni po različnih projektih. Dynamics 365 Project Operations obravnava rezervacije kot koncept na ravni projekta. 

Za razliko od rezervacij, so dodelitve zaveza virov k projektnih opravilom v razporedu projekta. Viri so lahko imenovani ali splošni.  Ko zahteva za vir izhaja iz dodelitev projektnih opravil, Project Operations uporabi krivulje obsega dela delitve virov za oblikovanje krivulje podrobnosti zahtevanega pogoja za vir. Vendar se sklic na dodelitve virov ne ohrani. Posodobitve rezervacij, ki izhajajo iz zahtevanega pogoja za vir, ne posodobijo dodelitev virov.

Običajno bo vsota rezervacij za vir enaka vsoti dodelitev vira po eni ali več opravilih. Vendar pa aplikacija Project Operations ne vsiljuje tega pravila. V pogledu **Usklajevanje** se vodji projekta prikažejo mesta, kjer se rezervacije in dodelitve vira ne skladajo.




[!INCLUDE[footer-include](../includes/footer-banner.md)]