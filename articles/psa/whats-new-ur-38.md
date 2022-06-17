---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 38, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v Microsoft Dynamics 365 Project Service Automation Posodobitev izdaja 38, V3.
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

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za posodobitev Project Service Automation, izdaja 38, V3. Ta različica ima številko izdelave V3.10.59.117 in je splošno na voljo s samoposodobitvijo decembra 2021.

## <a name="update-release-38"></a>Izdaja posodobitve 38

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Čas in strošek**

- Izjema se pojavi, ko dolžina dnevnikov niza odobritev presega 100.000 zapisov.
- Uporabniki ne morejo dostopati do **Vnos časa** mreža iz The **Vnos časa** glavna stran.
- The **Uvoz časovnega vnosa** pogovorno okno ne prikaže nobenega besedila, če noben element ni primeren za uvoz.
- Uporabniki lahko ustvarijo nize odobritev, kjer **Ciljno stanje** polje je nastavljeno na **neznano**.

**Vodenje projektov**

- Obrisi niso pravilno prikazani v dodelitvah virov za UTC(+09:30) in UTC(+10:00), ko se začne poletni čas.
- The **Dodatni stolpec** polje za strukture razčlenitve dela je skrito v nekaterih jezikih.
- Izbirnik datuma za nadzor koledarja v **Projektna naloga** mreža ni pravilno lokalizirana za kitajščino.

**Prodaja**

- **Izvedba pogodbe** in **Dejanski stroški projekta** vrednosti se ne ujemajo, ko viri, ki jih je mogoče rezervirati, ki imajo različne pogodbene enote in valute, predložijo časovne vnose.
- Potek dela po meri za samodejno potrditev računov ne uspe, ko so računi uvoženi kot upravljana rešitev. Prikaže se naslednje sporočilo: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Neveljavno stanje računa."
- Kdaj **koren** je izbrana kot možnost povzetka, projekt pa ima ocene iz mešanice razredov transakcij (na primer kombinacija časovnih, stroškovnih in materialnih ocen), sistem povzema po razredih transakcij kot eno vrstico provizije.
- V primerih, ko je vrstica stroškov dodana, preden je pogodbena vrstica povezana s projektom, pravilna cena ni vnesena kot privzeta vrednost v **Posodobite ceno** polje.
- Negativni zneski prodaje niso dovoljeni **Projekt** in **Naloga** subjekti.
