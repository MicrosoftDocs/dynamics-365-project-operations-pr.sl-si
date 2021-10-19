---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 36, V3
description: Ta tema navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 36, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606821"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 36, V3. Ta različica ima številko graditve V3.10.57.152 in je splošno na voljo s samostojno posodobitvijo v oktobru 2021.

## <a name="update-release-36"></a>Izdaja posodobitve 36

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Splošno**
- Ime polja **Privzeta predloga za delovne ure** je nepravilno prevedeno na strani **Projektni parametri**.
- Asinhroni vtičniki ne obravnavajo pravilno izjem, povezanih z možnostjo **SharedVariableService**.

**Čas in strošek**
- Ko vrstice dnevnika manjkajo ali uporabnik nima pravilnih pravic za branje vrstic dnevnika, pride do napake zaradi nepravilnosti, ko so odobritve projekta preklicane.
- Uporabniki ne morejo preklicati odobritve, če ima vnos stroška ali časa več kot eno povezano odobritev projekta.
- Možnosti **Odsotnost** in **Dopust** sta nepravilno prevedeni za kitajski jezik v iskanju na strani za hitro ustvarjanje **Časovni vnos**.

**Upravljanje virov**
- Uporabnik ne more iskati virov v možnosti **Pomočnik za razporejanje**, ko je način pogleda nastavljen na **Dan**, **Teden** ali **Mesec**.
- Nepravilno je dovoljeno, da imajo splošni viri prazna imena položajev. 
- Zapiranje pogodbe kot izgubljene ne prekliče prihodnjih rezervacij.

**Prodaja**
- Ko ima okolje veliko količino izdelkov, se poslabša zmogljivost v mreži **Ocena materiala**.
- Pri ustvarjanju projekta iz predloge se za valuto projekta privzeto ne uporabi pogodbena enota zadevnega vodje projektov.
- Dejanski zneski se ne ujemajo vedno s tem, kar se odraža v zapadlem projektu, ali pa zneski v posebnih scenarijih odpoklica postanejo negativni.
- Pride do napake, ko povežete projekt, ustvarjen iz predloge projekta, s podrobnostmi pogodbe.
- Uporabniki lahko izbrišejo podrobnosti pogodbe z mejnikoma **Pripravljeno za izdajanje računov** in **Račun je ustvarjen**. To ne bi smelo biti dovoljeno.
- Ko se ocene uvažajo iz projekta, je možnost zaračunavanja podrobnosti vrstice ponudbe napačno nastavljena, če je za vrstico ponudbe omogočeno obračunavanje na podlagi opravil.
- Ko dodate mejnik pri obračunavanju s fiksno ceno, se mejnik ne odrazi v podmreži mejnika, dokler ni stran osvežena.
- Ustvarjena je izjema ničelnega sklica, ko ustvarite projektno pogodbo z imenom ponudbe, ki je ničelna.
- Opravila v ročnem načinu, pri katerih se valuta projekta razlikuje od valute vira, povzročijo napačne ocene cen.
- Uporabniki ne morejo preklicati transakcije, ki je bila uspešno popravljena s popravnim računom.
- Deaktivirane kategorije transakcij so prikazane v mreži **Ocene stroškov**.



