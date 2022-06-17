---
title: Oddaja del podizvajalcem, ki so člani projektne ekipe
description: V tem članku je razloženo, kako skleniti podizvajalsko pogodbo s člani projektne skupine v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 649687cb9ac66e684069434a353b63155103aefb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916906"
---
# <a name="subcontracting-project-team-members"></a>Oddaja del podizvajalcem, ki so člani projektne ekipe

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V Microsoftu Dynamics 365 Project Operations, se lahko odločite za podizvajanje članov projektne skupine brez osebja ali osebja.

- Članom projektne skupine brez osebja je dodeljen splošni vir.
- Zaposleni člani ekipe imajo dodeljen poimenovani vir.

Ko povežete člana projektne skupine s podizvajalsko vrstico, bodo vse dodelitve nalogam, ki jih ima član ekipe, preračunane na podlagi nabavnega cenika, priloženega podizvajalski pogodbi.  Na **Ocene** zavihek na **Podrobnosti o projektu** strani, izberite **Posodobite cene** gumb za ogled posodobljenih cen in/ali stroškov, ki izhajajo iz odločitve o podizvajalcu. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Oddaja podizvajalskega člana projektne skupine brez osebja
The **Podrobnosti o članu ekipe** stran vsebuje vrstica podizvajalcev in podizvajalcev, ki vodji projekta omogočata, da izrazi, kako želi črpati potrebno zmogljivost iz podizvajalske pogodbe. Če želite člana projektne skupine oddati podizvajalcem kot generični vir, sledite tem korakom:

1.  Izberite podizvajalsko pogodbo na **Podrobnosti o članu ekipe** stran.

2.  Izberete lahko samo podizvajalce z **Osnutek** oz **Potrjeno** stanje. **Zaprto** oz **Prekinjeno** podizvajalcev ni mogoče izbrati. 

3.  The **Podizvajalska linija** polje postane vidno, ko izberete podizvajalsko pogodbo.

4.  V **Podizvajalska linija** polje, lahko izberete samo podizvajalske vrstice, ki so za čas. Ne morete izbrati vrstic podizvajalcev za stroške ali material.

5.  Vloga za zapis člana projektne skupine se mora ujemati z vlogo v vrstici podizvajalcev. To zagotavlja, da je čas za vlogo, ki se ocenjuje v projektu, enaka vloga, kot je kupljena v vrstici podizvajalcev. 

Ko je generični član ekipe povezan s podizvajalcem in podizvajalsko linijo, **Vrsta delavca** polje v vrstici s splošnimi člani ekipe bo posodobljeno v **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** bo nastavljeno na **veljavno**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Oddajanje podizvajalskega člana projektne skupine z osebjem
Tako kot splošni člani skupine ali člani ekipe brez osebja je tudi zmogljivost osebja, ki je potrebna za projekt, povezana s podizvajalsko pogodbo. Če želite imenovanega člana projektne skupine oddati podizvajalcem, sledite tem korakom:

1.  Prepričajte se, da je imenovani vir nastavljen kot vrsta vira, ki ga je mogoče rezervirati, kot pogodbeni delavec. Prav tako se prepričajte, da **Prodajalec** polje na viru, ki ga je mogoče rezervirati, se ujema s prodajalcem v podizvajalski pogodbi, ki jo izberete. 

2.  Izberete lahko samo podizvajalce v **Osnutek** oz **Potrjeno** stanje. **Zaprto** oz **Prekinjeno** podizvajalcev ni mogoče izbrati. 

3.  The **Podizvajalska linija** polje postane vidno, ko izberete podizvajalsko pogodbo.

4.  V **Podizvajalska linija** polje, lahko izberete samo podizvajalske vrstice, ki so za čas. Ne morete izbrati vrstic podizvajalcev za stroške ali material.

5.  Vloga za zapis člana projektne skupine se mora ujemati z vlogo v vrstici podizvajalcev. To zagotavlja, da je čas za vlogo, ki se ocenjuje v projektu, enaka vloga, kot je kupljena v vrstici podizvajalcev. 

Imenovani člani projektne skupine, ki so nastavljeni kot pogodbeni delavec **Vir, ki ga je mogoče rezervirati** bo prikazan s statusom veljavnosti podizvajalca **Ni veljaven** če niso povezani s podizvajalsko pogodbo. Ko je imenovani član projektne skupine povezan s podizvajalcem in podizvajalsko linijo, **Vrsta delavca** polje v vrstici za člane ekipe se bo posodobilo na **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** bo nastavljeno na **veljavno**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
