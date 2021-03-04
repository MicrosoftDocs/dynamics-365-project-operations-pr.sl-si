---
title: Prikaz zaračunane uporabe virov
description: V tej temi so na voljo informacije o prikazu uporabe virov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146413"
---
# <a name="view-chargeable-utilization-for-resources"></a>Prikaz zaračunane uporabe virov

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Pogled »Uporaba«** na strani **Project Service – uporaba virov** prikazuje zaračunano uporabo za vsak vir, ki ga je mogoče rezervirati. Ker pogled temelji na plošči razporeda, ima veliko podobnih funkcij.

> ![Posnetek zaslona pogleda Uporaba](media/FAQ-utilization-1.png)
 

Izračun zaračunane uporabe se izvaja kot sledi:

   Zaračunana uporaba = (dejanske zaračunane ure) / (zmogljivost vira)

Celice predstavljajo izračunano zaračunano uporabo za izbrano obdobje (dnevi, tedni ali meseci).

Barve v vsaki celici prikazujejo zaračunano uporabo za vir, primerjano s ciljno zaračunano uporabo. 

Ciljna uporaba se lahko določi glede na privzeto vlogo vira ali glede na posamezni vir. Izračun najprej poišče posamezni vir in njegov cilj, šele nato privzeto vlogo vira.

## <a name="set-target-on-a-resource"></a>Nastavljanje cilja v viru

1. Odprite možnost **Viri** \> **Viri**. 
2. Izberite vir, da odprete zapis. 
3. Na zavihku **Project Service** lahko nastavite ciljno uporabo za vir.

> ![Posnetek zaslona z zavihkom Project Service za nastavitev ciljne uporabe](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Nastavljanje ciljne uporabe v vlogi

1. Odprite **Viri** \> **Vloge virov**. 
2. Izberite vlogo in odprite zapis. 
3. Nastavite ciljno uporabo za to vlogo.

> ![Posnetek zaslona z možnostjo Vloge virov za nastavitev ciljne uporabe](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Izračun zaračunane uporabe za vir

Za izračun zaračunane uporabe vira morate izpolniti nekaj pogojev. 

### <a name="set-default-role-for-individual-resource"></a>Nastavljanje privzete vloge za posamezni vir

Ciljna uporaba se določi glede na posamezni vir ali vloge vira. Če za cilje uporabljate vloge vira, mora imeti vsak posamezni vir privzeto vlogo. 

1. To nastavite v možnosti **Viri** \> **Viri**. 
2. Izberite vir, odprite zapis in nato izberite zavihek **Project Service**. 
3. V mreži **Vloga vira** preverite, ali vir ima vlogo in ali je možnost **Je privzeta** nastavljena na **Da**.
 
### <a name="change-billing-type-for-resource-role"></a>Spreminjanje vrste obračunavanja za vlogo vira

Vloge virov morajo biti nastavljene tako, da je za vrsto obračunavanja izbrana možnost **Se zaračuna**. 

1. Odprite **Viri** \> **Vloge virov**. 
2. Odprite zapis, ki ga želite posodobiti, in nato privzeto vrsto obračunavanja nastavite na **Se zaračuna**.

### <a name="set-working-hours-for-resource-role"></a>Nastavitev delovnega časa za vlogo vira
 
Vir mora imeti delovnik, ki ustreza izračunani zmogljivosti. 

1. Odprite možnost **Viri** \> **Viri**. 
2. Izberite vir, da odprete zapis, in nato izberite **Prikaži delovne ure**. 
3. Seznam virov lahko množično posodobite tako, da v pogledu **Seznam virov** uporabite **predlogo za delovne ure**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Odpravljanje težav z dejanskimi zaračunanimi urami

Dejanske zaračunane ure so pridobljene iz entitete **Opravljeno delo**. Opravljeno delo z vrsto obračunavanja **Se zaračuna** je vključeno v izračun, zato potrebujete projekte, v katerih je opravljeno delo mogoče zaračunati.

Če ne vidite zaračunane uporabe, lahko preverite naslednje:

- Delovne ure vira so določene za zmogljivost.
- Vir ima individualno določen ciljno uporabo ali mu je dodeljena vloga. Vloga ima opredeljeno ciljno uporabo.
- Vrsta obračunavanja za opravljeno delo je **Se zaračuna** in velja za obdobje, za katerega pričakujete izračun uporabe. Če je opravljeno delo prikazano z drugimi vrstami obračunavanja, kot je »Se zaračuna«, preverite naslednje:

  - Vloga, ki se uporablja za opravljeno delo, ima privzeto vrsto obračunavanja drugačno od Se zaračuna.
  - Vloga v podrobnostih pogodbe za projekt je nastavljena na Se ne zaračuna.
  - Projekt nima povezanih podrobnosti pogodbe.



[!INCLUDE[footer-include](../includes/footer-banner.md)]