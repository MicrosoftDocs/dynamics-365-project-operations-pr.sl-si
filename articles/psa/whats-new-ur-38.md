---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 38, V3
description: Ta članek navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 38, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915205"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 38, V3. Ta različica ima številko izdelave V3.10.59.117 in je splošno na voljo s samoposodobitvijo decembra 2021.

## <a name="update-release-38"></a>Izdaja posodobitve 38

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Čas in strošek**

- Do izjeme pride, ko dolžina dnevnikov nabora odobritev preseže 100.000 zapisov.
- Uporabniki ne morejo dostopati do mreže **Časovni vnos** iz glavne strani **Časovni vnos**.
- Pogovorno okno **Uvoz časovnega vnosa** ne prikaže nobenega besedila, če noben element ni primeren za uvoz.
- Uporabniki lahko ustvarijo nize odobritev, kjer je polje **Stanje cilja** nastavljeno na **Neznano**.

**Vodenje projektov**

- Krivulje niso pravilno prikazane v dodelitvah virov za UTC (+09:30) in UTC (+10:00), ko se začne poletni čas.
- Polje **Dodatni stolpec** za strukturirane členitve dela je v nekaterih lokalih skrito.
- Izbirnik datuma za kontrolnik za koledar v mreži **Opravilo projekta** ni pravilno lokaliziran za kitajščino.

**Prodaja**

- Vrednosti **Izvedba pogodbe** in **Dejanski stroški projekta** se ne ujemajo, ko viri, ki jih je mogoče rezervirati ter imajo različne pogodbene enote in valute, predložijo časovne vnose.
- Potek dela po meri za samodejno potrjevanje računov ne uspe, ko so računi uvoženi kot upravljana rešitev. Prikaže se naslednje sporočilo: »Sporočilo Microsoft.Xrm.Sdk.InvalidPluginExecutionException: Neveljavno stanje računa.«
- Ko je vrednost **Koren** izbrana kot možnost povzemanja in ima projekt ocene iz kombinacije razredov transakcij (na primer kombinacija ocen časa, stroškov in materiala), sistem povzema vse razrede transakcij kot eno vrstico nadomestil.
- V scenarijih, kjer je vrstica stroškov dodana, preden so podrobnosti pogodbe povezane s projektom, pravilna cena v polju **Posodobitev cene** ni vnesena kot privzeta vrednost.
- Negativni zneski prodaje niso dovoljeni za entiteti **Projekt** in **Opravilo**.
