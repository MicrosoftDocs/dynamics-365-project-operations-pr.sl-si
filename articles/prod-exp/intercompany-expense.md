---
title: Medpodjetni stroški
description: Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji. V tem primeru lahko s funkcijo medpodjetnih stroškov dodelite stroške delavca tisti pravni osebi, za katero je bilo delo opravljeno.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084907"
---
# <a name="intercompany-expenses"></a>Medpodjetni stroški

[!include [banner](../includes/banner.md)]

Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji. V tem primeru lahko s funkcijo medpodjetnih stroškov dodelite stroške delavca tisti pravni osebi, za katero je bilo delo opravljeno. Pravna oseba, ki zaposli delavca, se imenuje posojilna pravna oseba. Pravna oseba, na katero se pišejo stroški delavca, se imenuje izposojevalna pravna oseba. 

Preden lahko delavec ustvari in predloži stroške dela, ki ga opravlja za drugo pravno osebo, na strani **Parametri upravljanja stroškov** za posojilno pravno osebo izberite možnost **Dovoli vrstice medpodjetnih stroškov**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Davčna napoved za medpodjetne stroške

[!include [banner](../includes/banner.md)]

Če želite v poročilu o stroških uporabiti davčne skupine, ki so povezane s posojilno (izvorno) pravno osebo namesto z izposojilno (ciljno) pravno osebo, boste morali to nastaviti v možnosti za nastavitev prometnega davka v glavni knjigi. Ko je parameter glavne knjige **Pravna oseba za medpodjetno davčno napoved** nastavljen na **Vir** in **Uporabi pravila o obdavčitvi za prometni davek** nastavljen na **Ne** , bo uporabljena kombinacija davkov za posojilno pravno osebo. Ko je isti parameter nastavljen na **Cilj** , bo uporabljena kombinacija davka za izposojevalno pravno osebo. Za pravne osebe v ZDA velja naslednje: če je parameter nastavljen na **Vir** , mora biti polje **Terjatve od prometnega davka** konfigurirano tudi na novi strani **Skupine za vnašanje v glavno knjigo**. Računovodski mehanizem bo podatke iz tega polja uporabil za vnos računovodskih evidenc v zvezi z davki.   
To vedenje je skladno za vrstice stroškov, objavljene s projektom ali brez.  
