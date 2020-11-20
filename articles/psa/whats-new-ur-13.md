---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 13, V3
description: V tej temi so na voljo informacije o novostih v izdaji posodobitve za Project Service Automation 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121643"
---
# <a name="project-service-automation-update-release-13-v3"></a>Izdaja posodobitve 13 za Project Service Automation, V3
Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA). Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 13. Ta različica ima številko graditve V3.10.3.18 in je na voljo po naslednjem razporedu:

- **Splošna razpoložljivost (samostojna posodobitev):** november 2019
- **Samodejna posodobitev:** december 2019


## <a name="update-release-13"></a>Izdaja posodobitve 13 

### <a name="bug-fixes"></a>Popravki napak

- Čas in strošek

     - Popravljeno: funkcionalnost iskanja na strani **Odobritev stroškov** ne deluje pri iskanju po namenu stroška.

- Upravljanje virov

     - Popravljeno: številke pri usklajevanju so bile posodobljene, da so poravnane desno.
     - Popravljeno: imena virov ni mogoče dodeliti opravilom prek zavihka **Razpored**.

- Vodenje projektov

     - Popravljeno: ničelna referenčna izjema pri dodeljevanju člana ekipe, ko v **TransactionType** manjkajo informacije za nastavitev za **Enota** in **DefaultGroup**.

- Sales

     - Popravljeno: podvojeni zapisi vrste transakcije vrnejo napako, ko so ustvarjeni zapisi cene vloge.
     - Popravljeno: dodatni gumbi za možnosti **Nova priložnost**, **Ponudba**, **Vrstica naročila** in **Dodajanje izdelka** so vidni v ukazih za »Priložnosti«, »Ponudbe«, »Izdelki iz naročila« in podmrežo »Vrstice«, ki temelji na projektu.


