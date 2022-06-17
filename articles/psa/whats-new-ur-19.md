---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 19, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v posodobitvi Project Service Automation, izdaja 19, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: a17275220eec726107e8ce5f82bdf5cdd403033e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915526"
---
# <a name="project-service-automation-update-release-19-v3"></a>Izdaja posodobitve 19 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, posodobitev izdaje 19. Številka graditve te različice je V3.10.30.41 in je na splošno na voljo prek samostojne posodobitve maja 2020.

## <a name="update-release-19"></a>Izdaja posodobitve 19

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave: 

- Napake zaradi uvoza časovnih vnosov niso prikazane pravilno.
- Mreža časovnega vnosa ne podpira vedenja polja **Samo datum**.
- Viri projekta ne morejo ustvariti stroška s projektom.

**Vodenje projektov**

Odpravljene so naslednje težave: 

-  Podrejeno opravilo podrejenega opravila ustvari nepravilno oceno obsega dela med izračunom ocene končnih stroškov.

**Sales**

Odpravljene so naslednje težave: 

- Dejanje **Preračunaj** ne deluje s podrobnostmi vrstice pogodbe o stroških ali podrobnostmi vrstice ponudbe.
- V ocenah stroškov manjka možnost **Posodobi cene**.
-  Stranke na strani **Projektna pogodba** ne morejo izbrati razlogov stanja pogodb po meri.
- Stranke pri ustvarjanju cenika po meri iz ponudbe opažajo slabše delovanje.
- Stranke opažajo neskladnost s privzetimi vrednostmi **enot** na straneh **Podrobnosti vrstice ponudbe** in **Podrobnosti vrstice pogodbe**.
- Če so v vrstico pogodbe, ki se zaračunava, dodani elementi kategorije transakcije, ki se ne zaračunava, vrsta obračunavanja **Se ne zaračuna** kategorije transakcije ne bo upoštevana.
- Stranke novo dodanih vlog in kategorij ne morejo uporabiti za predhodno ustvarjene pogodbe.
- Stranke opažajo slabše delovanje funkcije »Nepotrebno pridobivanje« v datoteki PreValidateProjectTeamMemberUpdate.cs
- Vloge, ki so na seznamu **Kategorije virov** določene, da se ne zaračunavajo, morajo biti v vrstici pogodbe za projekt na zavihek **Vloge, ki se zaračunajo** dodane z opisom **Se ne zaračuna**.
- Stranke lahko pri ustvarjanju projekta opazijo slabše delovanje, ker **GetBookableResourceIdFromUser** pridobi vse stolpce virov, ki jih je mogoče rezervirati, ne le primarnega ID-ja.
- Entiteta **TransactionType** manjka v vtičniku posodobitve pred preverjanjem pristnosti, da uporabnikom prepreči vnos elementov **Enote** in **Skupine enot**, ki niso veljavne za vrste transakcij.
- Korak **Odstrani** ne deluje pri uvozu časovnega vnosa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
