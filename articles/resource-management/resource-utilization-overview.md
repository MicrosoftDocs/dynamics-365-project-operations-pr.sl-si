---
title: Pregled uporabe virov
description: V tej temi so na voljo informacije o uporabi virov v storitvi Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 152f85669b56d128a7bb2317ee2cf0857c90ade1273d47ad1f0f387e00a6bbd8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002081"
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