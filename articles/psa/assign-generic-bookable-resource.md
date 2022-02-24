---
title: Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in projektni ekipi
description: Ta tema vsebuje informacije o rezervaciji splošnih virov za opravila in projektne ekipe.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145423"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje pogojev za vir 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Poleg rezervacije in dodeljevanja imenovanih ali pravih virov za projekt lahko projektnim opravilom dodelite splošne vire. Ti viri lahko označujejo mesto za imenovane vire, dokler niste pripravljeni, da projektu dodelite imenovane vire. 

1. V aplikaciji Project Service Automation (PSA) odprite stran **Projekt** in na zavihku **Načrtovanje** urnik vnesite ime položaja splošnega vira v celico razporeda **Vir**. Lahko pa v celici kliknete ikono **Vir**, da se odpre izbirnik za vire in nato vnesete ime splošnega vira,ki ga želite ustvariti.

![Ustvarjanje in dodeljevanje splošnega člana ekipe](media/RM-how-to-9.png)

Odpre se plošča **Hitro ustvarjanje: član projektne ekipe**. 

2. Vnesite vlogo in organizacijsko enoto splošnega člana ekipe virov in kliknite **Shrani**.

![Hitro ustvarjanje splošnega člana ekipe](media/RM-how-to-10.png)

3. Ko ustvarite novega splošnega člana ekipe virov, se dodeli opravilu. Ta splošni vir lahko nato dodelite tudi drugim opravilom v razporedu opravil.

![Dodeljevanje obstoječega splošnega člana ekipe opravilom](media/RM-how-to-11.png)

4. Ko dodelite splošen vir, lahko ustvarite zahtevo za vir in jo izpolnite tako, da neposredno rezervirate ali pošljete zahtevo za vir upravitelju virov.

![Ustvarjanje zahteve za splošnega člana ekipe](media/RM-how-to-12.png)

Poleg uporabe zgoraj omenjenega izbirnika virov lahko na mreži člana ekipe tudi neposredno dodajate splošne vire. Sredstva se dodajo z zahtevo za vir, ki temelji na začetnem/končnem datumih in metodi dodelitve, določeni v **hitrem ustvarjanju: panel člana** projektne skupine.

Razliko lahko vidite, če neposredno dodate splošnega člana ekipe in nato splošnemu viru dodate več opravil, kot ima na voljo delovnih ur. Kliknite **Ustvari zahtevo**, da se znova ustvari zahteva za uskladitev zahtevanih ur v povezavi z dodeljenimi opravili.

Na mreži ekipe lahko kliknete tudi **Zahtevani pogoj za vir**, da se odpre zahteva, nato dodate znanja, prednostne vire itd.

![Zahtevani pogoj za vir](media/RM-how-to-13.png)

