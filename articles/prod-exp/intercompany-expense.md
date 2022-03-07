---
title: Medpodjetni stroški
description: V tej temi so na voljo informacije o tem, kako uporabite stroške med podjetji za dodelitev stroškov delavca pravni osebi, za katero je bilo delo opravljeno.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001226"
---
# <a name="intercompany-expenses"></a>Medpodjetni stroški

Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji. Stroške med podjetji lahko uporabite za dodelitev stroškov delavca pravni osebi, za katero je bilo delo opravljeno. Pravna oseba, ki zaposli delavca, se imenuje posojilna pravna oseba. Pravna oseba, na katero se pišejo stroški delavca, se imenuje izposojevalna pravna oseba. 

Preden lahko delavec ustvari in predloži stroške med podjetji, morate omogočiti vrstice stroškov med podjetji. V posojilni pravni osebi na strani **Parametri upravljanja stroškov** izberite **Omogoči vrstice stroškov med podjetji**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Davčna napoved za medpodjetne stroške

[!include [banner](../includes/banner.md)]

Preden lahko v poročilu o stroških uporabite davčne skupine, ki so povezane s posojilno (izvorno) pravno osebo namesto z izposojevalno (ciljno) pravno osebo, morate omogočiti funkcijo v nastavitvi prometnega davka v glavni knjigi. Ko je parameter **Pravna oseba za davčno napoved med podjetji** nastavljen na **Vir**, **Uporabi davčna pravila za prometni davek** pa na **Ne**, se uporabi davčna kombinacija za posojilno pravno osebo. Ko je isti parameter nastavljen na **Cilj**, bo uporabljena kombinacija davka za izposojevalno pravno osebo. Za pravne osebe v ZDA velja naslednje: če je parameter nastavljen na **Vir**, mora biti polje **Terjatve od prometnega davka** konfigurirano tudi na novi strani **Skupine za vnašanje v glavno knjigo**. Računovodski mehanizem bo podatke iz tega polja uporabil za vnos računovodskih evidenc v zvezi z davki.   
To vedenje je skladno za vrstice stroškov, objavljene s projektom ali brez.  

## <a name="new-expense-expression-builder"></a>Nov graditelj izrazov stroškov

Novi graditelj izrazov stroškov obravnava težave z medpodjetniškimi scenariji stroškov, ki uporabljajo projekte. Ta funkcija zagotavlja, da je pravilnik glede stroškov med podjetji pravilno preverjen glede na projekt, ki je izbran v vrstici stroškov, in da je poročilo o stroških mogoče uspešno oddati.

Če želite ustvariti funkcijo graditelja izrazov stroškov, jo morate vklopiti. Poleg tega je treba določiti pravilnik glede stroškov, ki ima ID projekta.

Če ste v vrstici stroškov že konfigurirali pravilnike, ki preverjajo ID projekta, je treba te pravilnike umakniti. Nato lahko vklopite funkcijo in znova konfigurirate pravilnike.

Če želite vklopiti te funkcije, upoštevajte naslednja navodila.

1. Odprite zavihek **Delovni prostori** \> **Upravljanje funkcije**.
2. Na seznamu izberite možnost **Novi graditelj izrazov stroškov za obravnavanje težav z medpodjetniškimi scenariji stroškov, ki uporabljajo projekte**. Nato izberite **Omogoči zdaj**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
