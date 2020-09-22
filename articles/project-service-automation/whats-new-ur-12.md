---
title: Novosti v izdaji posodobitve za Project Service Automation 12, V3
description: V tej temi so na voljo informacije o novostih v izdaji posodobitve za Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755796"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, izdaja posodobitve 12
Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA). Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 12. Ta različica ima številko graditve V3.10.2.34 in je splošno na voljo s samostojno posodobitvijo v oktobru 2019.

## <a name="update-release-12"></a>Izdaja posodobitve 12

### <a name="bug-fixes"></a>Popravki napak

- Čas in strošek

    - Popravljeno: sporočila o napakah časovnih vnosov so bila posodobljena z bolj relevantnim kontekstom.
    - Popravljeno: mreža in razpored časovnih vnosov pravilno prikazujeta navpični drsni trak, ko je potrebno.
    - Popravljeno: poslani stroškovni in časovni vnosi so lahko odobreni.
    - Popravljeno: pogovorno okno za potrditev preklica odobritve je bilo popravljeno, da odraža stanje odobritve ob spremembi z **Odobreno** na **Poslano**.
    - Popravljeno: polja **Cena**, **Enota** in **Količina** so zdaj zaklenjena na zapisu »Strošek«, potem ko je odobren.

- Vodenje projektov

    - Popravljeno: dejanje **Novo** na glavnem obrazcu **Član ekipe** je bilo odstranjeno.
    - Popravljeno: dodelitve virov so bile posodobljene, da se upoštevajo napake zaradi netočnega zaokroževanja, zaradi česar se je končni datum opravila prestavil.
    - Popravljeno: v mreži opravil bodo strežniške napake prikazane uporabniku.
    - Popravljeno: v izbirniku oseb za opravilo je zdaj upodobljeno ime člana ekipe, namesto imena položaja.

- Upravljanje virov

    - Popravljeno: podrobnosti zahtevanega pogoja za vir za projekte, ustvarjene iz predloge, zdaj uporabljajo projektni koledar.
    - Popravljeno: znanja in sposobnosti so zdaj privzeta iz glavnih podatkov vloge v zahtevan pogoj za vir za to vlogo.

- Sales

    - Popravljeno: podvojeni ID-ji predmetov, najdeni na glavnem obrazcu **Pogodba**.
    - Popravljeno: logika je bila posodobljena, da je zavihek **Analiza ponudbe** viden, tako da prikazuje nastavitev metapodatkov zavihka.
    - Popravljeno: datum knjiženja na dejanskem zapisu zdaj prihaja iz datuma časovnega/stroškovnega vnosa in ne datuma odobritve.
