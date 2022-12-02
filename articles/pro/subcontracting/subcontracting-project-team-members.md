---
title: Oddaja del podizvajalcem, ki so člani projektne ekipe
description: Ta članek pojasnjuje, kako skleniti podizvajalsko pogodbo za člane projektne ekipe v aplikaciji Microsoft Dynamics 365 Project Operations.
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

V aplikaciji Microsoft Dynamics 365 Project Operations se lahko odločite za sklenitev podizvajalske pogodbe s člani projektne ekipe brez osebja ali z osebjem.

- Članom projektne ekipe brez osebja je dodeljen splošen vir.
- Člani ekipe z osebjem imajo dodeljen imenovani vir.

Ko člana projektne ekipe povežete s podrobnostmi podizvajalske pogodbe, bodo vse dodelitve opravil, ki jih ima član ekipe, preračunane na podlagi nabavnega cenika, priloženega podizvajalski pogodbi.  V zavihku **Ocene** na strani **Podrobnosti projekta** izberite gumb **Posodobitev cene**, da si ogledate posodobljene cene in/ali stroške, ki izhajajo iz odločitve o podizvajalski pogodbi. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Oddaja del podizvajalcu, ki je član projektne ekipe brez osebja
Stran **Podrobnosti o članih ekipe** ima polja za podizvajalske pogodbe in podrobnosti podizvajalske pogodbe, ki vodji projekta omogočajo, da izrazi, kako želi črpati zahtevano zmogljivost iz podizvajalske pogodbe. Če želite s podizvajalcem skleniti splošnega člana projektne ekipe, sledite tem korakom:

1.  Na strani **Podrobnosti o članu ekipe** izberite podizvajalsko pogodbo.

2.  Izberete lahko le podizvajalske pogodbe v stanju **Osnutek** ali **Potrjeno**. Podizvajalskih pogodb s stanjem **Zaprto** ali **Preklicano** ni mogoče izbrati. 

3.  Polje **Podrobnosti podizvajalske pogodbe** postane vidno, ko izberete podizvajalsko pogodbo.

4.  V polju **Podrobnosti podizvajalske pogodbe** lahko izberete samo podrobnosti podizvajalske pogodbe, ki so namenjene za čas. Podrobnosti podizvajalske pogodbe ne morete izbrati za stroške ali material.

5.  Vloga za zapis člana projektne ekipe se mora ujemati z vlogo v podrobnostih podizvajalske pogodbe. To zagotavlja, da je čas za vlogo, ki se ocenjuje na projektu, enak vlogi, ki je kupljena v podrobnostih podizvajalske pogodbe. 

Ko je splošni član ekipe povezan s podizvajalcem in podrobnostmi podizvajalske pogodbe, bo polje **Vrsta delavca** v vrsti splošnega člana ekipe posodobljeno na **Pogodbeni delavec**, vrednost **Veljavnost podizvajalske pogodbe** pa bo nastavljena na **Veljavno**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Oddaja del podizvajalcu, ki je član projektne ekipe z osebjem
Tako kot pri splošnih članih ekipe ali članih ekipe brez osebja je tudi pri članih ekipe z osebjem zmogljivost, potrebna za projekt, lahko povezana s podizvajalsko pogodbo. Če želite s podizvajalcem skleniti imenovanega člana projektne ekipe, sledite tem korakom:

1.  Prepričajte se, da je imenovani vir nastavljen kot vrsta pogodbenega delavca za vir, ki ga je mogoče rezervirati. Prepričajte se tudi, da se polje **Dobavitelj** v viru, ki ga je mogoče rezervirati, ujema z dobaviteljem v podizvajalski pogodbi, ki jo izberete. 

2.  Izberete lahko le podizvajalske pogodbe v stanju **Osnutek** ali **Potrjeno**. Podizvajalskih pogodb s stanjem **Zaprto** ali **Preklicano** ni mogoče izbrati. 

3.  Polje **Podrobnosti podizvajalske pogodbe** postane vidno, ko izberete podizvajalsko pogodbo.

4.  V polju **Podrobnosti podizvajalske pogodbe** lahko izberete samo podrobnosti podizvajalske pogodbe, ki so namenjene za čas. Podrobnosti podizvajalske pogodbe ne morete izbrati za stroške ali material.

5.  Vloga za zapis člana projektne ekipe se mora ujemati z vlogo v podrobnostih podizvajalske pogodbe. To zagotavlja, da je čas za vlogo, ki se ocenjuje na projektu, enak vlogi, ki je kupljena v podrobnostih podizvajalske pogodbe. 

Imenovani člani projektne ekipe, ki so nastavljeni kot vrsta pogodbenega delavca **Vir, ki ga je mogoče rezervirati**, bodo prikazani s stanjem veljavnosti podizvajalske pogodbe **Neveljavno**, če niso povezani s podizvajalsko pogodbo. Ko je imenovan član projektne ekipe povezan s podizvajalsko pogodbo in podrobnostmi podizvajalske pogodbe, bo polje **Vrsta delavca** v vrsti člana ekipe posodobljeno na **Pogodbeni delavec**, vrednost **Veljavnost podizvajalske pogodbe** pa bo nastavljena na **Veljavno**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
