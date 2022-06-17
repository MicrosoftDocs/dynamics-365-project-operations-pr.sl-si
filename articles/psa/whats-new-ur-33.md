---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 33, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v posodobitvi Project Service Automation, izdaja 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915436"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, posodobitev izdaja 33. Različica z delovno številko V3.10.54.98 je julija 2021 na voljo s samoposodobitvijo.

## <a name="update-release-33"></a>Izdaja posodobitve 33

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Zaklenjeni polji **msdyn_description** in **msdyn_externaldescription** je mogoče urediti po oddaji.
- Sporočilo o napaki se pojavi, če je ustvarjen strošek, ki ni povezan s projektom.
- Ko je časovni vnos ustvarjen, se vloga vira privzeto nastavi na nedejavno vlogo.
- Vrstice dnevnika, povezane s preklicanimi in izbrisanimi stroški, se ne odstranijo.
- V obrazcu **Obrazec za hitro ustvarjanje časovnega vnosa** posodobite **Seznam projektnih nalog** in tako datum, ki je prikazan privzeto, zamenjajte z datumom začetka opravila.
- Ko v zavihku **Povezano** za vir, ki ga je mogoče rezervirati, ustvarite časovni vnos, se slednji neustrezno ustvari za vpisane uporabnike namesto za nadrejeni vir, ki ga je mogoče rezervirati.
- V pogovorno okno **MDD za množične odobritve** so dodana nova polja.

**Načrtovanje projekta**

Odpravljene so naslednje težave:
- Ko so projektne predloge za delovne ure uporabljene v zapletenih koledarjih, se projekt ustvarja počasi.
- Ko je datum začetka poznejši od datuma zaključka, se na predlogi za kopiranje projekta zaradi razlik v časovnih komponentah vsakega polja prikaže napaka.

**Upravljanje virov**

Odpravljene so naslednje težave:
- V poizvedbi za uporabo virov je uporabljen napačen parameter, XML pa vodi do neustreznega filtriranja rezultatov v mreži **Uporaba virov**.
- Ob potrditvi možnosti **Podaljšanje rezervacij** se prikaže napačen končni datum rezervacije.

**Prodaja**

Odpravljene so naslednje težave:
- Sporočilo o napaki se pojavi, če je ustvarjena cena kategorije z manjkajočimi vrednostmi.
- Sporočilo o napaki se pojavi, če je mejnik podrobnosti pogodbe ustvarjen brez vrstice naročila.
