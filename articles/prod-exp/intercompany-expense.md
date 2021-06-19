---
title: Medpodjetni stroški
description: V tej temi so na voljo informacije o tem, kako uporabite stroške med podjetji za dodelitev stroškov delavca pravni osebi, za katero je bilo delo opravljeno.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005091"
---
# <a name="intercompany-expenses"></a>Medpodjetni stroški

Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji. Stroške med podjetji lahko uporabite za dodelitev stroškov delavca pravni osebi, za katero je bilo delo opravljeno. Pravna oseba, ki zaposli delavca, se imenuje posojilna pravna oseba. Pravna oseba, na katero se pišejo stroški delavca, se imenuje izposojevalna pravna oseba. 

Preden lahko delavec ustvari in predloži stroške med podjetji, morate omogočiti vrstice stroškov med podjetji. V posojilni pravni osebi na strani **Parametri upravljanja stroškov** izberite **Omogoči vrstice stroškov med podjetji**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Davčna napoved za medpodjetne stroške

[!include [banner](../includes/banner.md)]

Preden lahko v poročilu o stroških uporabite davčne skupine, ki so povezane s posojilno (izvorno) pravno osebo namesto z izposojevalno (ciljno) pravno osebo, morate omogočiti funkcijo v nastavitvi prometnega davka v glavni knjigi. Ko je parameter **Pravna oseba za davčno napoved med podjetji** nastavljen na **Vir**, **Uporabi davčna pravila za prometni davek** pa na **Ne**, se uporabi davčna kombinacija za posojilno pravno osebo. Ko je isti parameter nastavljen na **Cilj**, bo uporabljena kombinacija davka za izposojevalno pravno osebo. Za pravne osebe v ZDA velja naslednje: če je parameter nastavljen na **Vir**, mora biti polje **Terjatve od prometnega davka** konfigurirano tudi na novi strani **Skupine za vnašanje v glavno knjigo**. Računovodski mehanizem bo podatke iz tega polja uporabil za vnos računovodskih evidenc v zvezi z davki.   
To vedenje je skladno za vrstice stroškov, objavljene s projektom ali brez.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]