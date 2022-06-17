---
title: Pregled uporabe virov
description: Ta članek vsebuje informacije o uporabi virov v Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 5fbba4c9feaf3b26fba3423e160b09c58e049c70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918516"
---
# <a name="resource-utilization-overview"></a>Pregled uporabe virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Viri lahko imajo ciljno zaračunano uporabo. Ta ciljna uporaba je opredeljena kot atribut privzete vloge vira ali nastavljena v zapisu posameznega vira, ki ga je mogoče rezervirati. Izračuni uporabe temeljijo na dejanskih urah, ki so jih viri poročali na podlagi odobrenih časovnih vnosov.

Za izračun uporabe se uporabljajo naslednje enačbe:

  - Zaračunana uporaba = dejanske zaračunane ure ÷ zmogljivost vira
  - Nezaračunana uporaba = dejanski čas z ID-jem vrste obračunavanja = se ne zaračuna, brezplačno ali ni na voljo ÷ zmogljivost vira
  - Za interno uporabo = dejanski čas brez prodajne pogodbe ÷ zmogljivost vira
  - Zmogljivost vira = delovni čas vira – odsotnost – prosti dnevi

Pogled **Uporaba vira** lahko najdete v podoknu **Viri**.

Vsaka celica v mreži predstavlja delež zaračunane uporabe vira v določenem obdobju, na primer dnevu, tednu ali mesecu. Za obarvanje celic se uporabljajo naslednje enačbe:

  - **Zelena**: zaračunana uporaba > = ciljna uporaba za vir
  - **Rumena**: ciljna uporaba – 20 <= zaračunana uporaba < ciljna uporaba
  - **Rdeča**: zaračunana uporaba < ciljna uporaba – 20

Ker pogled **Uporaba vira** temelji na plošči razporeda, lahko rezultate filtrirate z možnostmi filtriranja na plošči razporeda.

Zaradi mreže morate nastaviti ciljno uporabo za vlogo ali posamezni vir. To nastavite v možnosti **Viri** > **Vloge virov**.

Poleg tega morate vsakemu viru, ki ga je mogoče rezervirati, dodati tudi privzeto vlogo. Odprite možnost **Viri** > **Viri**. Na zavihku **Project Service** preverite, ali je vloga vira določena in ali je polje **Je privzeto** nastavljeno na **Da**. Kjer je vrednost **Je privzeto** = **Ne**, lahko dodate dodatne vloge. Vloga, pri kateri je vrednost **Je privzeto** = **Da**, se uporablja za oceno uporabe vira v primerjavi s ciljem za to vlogo.

Na zavihku **Project Service** lahko nastavite tudi posamično ciljno uporabo za vir. Izračun uporabe nato uporabi to ciljno uporabo za oceno cilja vira namesto cilja privzete vloge vira.

Uporaba se za posamezen vir prikaže samo, če je vir odobril čas, ki se zaračuna, v obdobju, ki je prikazan v mreži.


[!INCLUDE[footer-include](../includes/footer-banner.md)]