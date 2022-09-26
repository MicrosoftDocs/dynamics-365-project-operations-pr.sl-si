---
title: Oddaja del podizvajalcem, ki so člani projektne ekipe
description: Ta članek pojasnjuje, kako skleniti pogodbe s člani projektne skupine v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522816"
---
# <a name="subcontracting-project-team-members"></a>Oddaja del podizvajalcem, ki so člani projektne ekipe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V Microsoftu Dynamics 365 Project Operations, se lahko odločite za podizvajanje članov projektne skupine brez osebja ali zaposlenih.

- Članom projektne skupine brez osebja je dodeljen generični vir.
- Člani ekipe z osebjem imajo dodeljen imenovani vir.

Ko člana projektne skupine povežete s podizvajalsko linijo, bodo vse dodelitve nalog, ki jih ima član ekipe, preračunane na podlagi nabavnega cenika, priloženega podizvajalski pogodbi.  Na **Ocene** zavihek na **Podrobnosti projekta** strani izberite **Posodobite cene** gumb za ogled posodobljenih cen in/ali stroškov, ki izhajajo iz odločitve o podizvajalcu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Sklenitev pogodbe s podizvajalcem za člana projektne skupine brez osebja
The **Podrobnosti o članih ekipe** stran ima polja za podizvajalce in vrstice za podizvajalce, ki vodji projekta omogočajo, da izrazi, kako želi črpati zahtevano zmogljivost iz podizvajalske pogodbe. Če želite člana projektne skupine skleniti s podizvajalci kot splošnega vira, sledite tem korakom:

1.  Izberite podizvajalsko pogodbo na **Podrobnosti o članu ekipe** strani.

2.  Izberete lahko le podizvajalske pogodbe z **Osnutek** oz **Potrjeno** stanje. **Zaprto** oz **Prekinjeno** podizvajalcev ni mogoče izbrati. 

3.  The **Podizvajalska linija** polje postane vidno, ko izberete podizvajalsko pogodbo.

4.  V **Podizvajalska linija** polje, lahko izberete samo podizvajalske vrstice, ki so za čas. Podizvajalskih vrstic ne morete izbrati za stroške ali material.

5.  Vloga za evidenco člana projektne skupine se mora ujemati z vlogo v podizvajalski liniji. To zagotavlja, da je čas za vlogo, ki se ocenjuje na projektu, enak vlogi, ki je kupljena na podizvajalski liniji. 

Ko je generični član skupine povezan s podizvajalcem in podizvajalsko linijo, **Delavski tip** polje v vrstici s splošnimi člani ekipe bo posodobljeno na **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** bo nastavljeno na **Veljavno**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Sklenitev pogodbe s podizvajalcem zaposlenega člana projektne skupine
Tako kot generični člani ekipe ali člani ekipe brez osebja je tudi zmogljivost članov ekipe z osebjem, potrebna za projekt, lahko povezana s podizvajalsko pogodbo. Če želite s podizvajalcem skleniti imenovanega člana projektne skupine, sledite tem korakom:

1.  Prepričajte se, da je imenovani vir nastavljen kot vrsta pogodbenega delavca vira, ki ga je mogoče rezervirati. Prepričajte se tudi, da je **Prodajalec** polje v viru, ki ga je mogoče rezervirati, se ujema s prodajalcem v podizvajalski pogodbi, ki jo izberete. 

2.  Izberete lahko le podizvajalske pogodbe v **Osnutek** oz **Potrjeno** stanje. **Zaprto** oz **Prekinjeno** podizvajalcev ni mogoče izbrati. 

3.  The **Podizvajalska linija** polje postane vidno, ko izberete podizvajalsko pogodbo.

4.  V **Podizvajalska linija** polje, lahko izberete samo podizvajalske vrstice, ki so za čas. Podizvajalskih vrstic ne morete izbrati za stroške ali material.

5.  Vloga za evidenco člana projektne skupine se mora ujemati z vlogo v podizvajalski liniji. To zagotavlja, da je čas za vlogo, ki se ocenjuje na projektu, enak vlogi, ki je kupljena na podizvajalski liniji. 

Imenovani člani projektne skupine, ki so nastavljeni kot vrsta pogodbenega delavca **Vir, ki ga je mogoče rezervirati** bo prikazan s statusom veljavnosti podizvajalske pogodbe **Ni veljaven** če niso povezani s podizvajalsko pogodbo. Ko je imenovani član projektne skupine povezan s podizvajalcem in podizvajalsko linijo, **Delavski tip** polje v vrstici za člana ekipe bo posodobljeno na **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** bo nastavljeno na **Veljavno**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
