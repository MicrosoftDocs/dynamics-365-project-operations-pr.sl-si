---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 32, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 32.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 3ad87eceb90a48997aadf00803b8d14c5108eb83
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580108"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 32. Ta različica ima številko gradnje V3.10.53.108 in je na splošno na voljo s samoposodobitvijo junija 2021.

## <a name="update-release-32"></a>Izdaja posodobitve 32

### <a name="bug-fixes"></a>Popravki napak

#### <a name="general"></a>Splošno

- Če večja nadgradnja ne uspe, je treba blokirati samo glavne vstopne točke aplikacije, da se zagotovi, da so entitete v skupni rabi še vedno dostopne.

#### <a name="time-and-expense"></a>Čas in strošek

Odpravljene so naslednje težave:

- **TimeEntriesImportFromResourceAssignment** ne vzdržuje začetnega in končnega časa rezine krivulje za dodelitev vira.
- Ko izberete možnost **Odpri vnos** v mreži **Vnos časa**, morda ne boste mogli izbirati drugih obrazcev.
- Medtem ko uvažate dodelitve v časovne vnose, lahko poizvedba odjemalske kode ustvari dolg URL, zaradi katerega poizvedba ne uspe.
- Ko je vrednost izbrisana iz celice v mreži **Vnos časa**, fokus ne ostane v mreži.
- Gumb **Zavrni** je odstranjen iz pogleda **Obdelava odobritev** za sodobne odobritve.
- Na stabilnost in zmogljivost množične odobritve vnosa časa vplivajo zastoji in neuspelo ravnanje s prilagajanji, povezanimi z entiteto **Vnos časa**.

#### <a name="project-planning"></a>Načrtovanje projekta

- Izjema z referenco z vrednostjo »null« se ustvari, ko posodobite projekt, ki ima v polju **Pogodbena enota** vrednost »null«.
- Funkcija **osvežitev skupnih vrednosti za projekt** napačno izračuna preostali strošek in preostale prodaje za projekt.
- Odvečni izračuni cen vplivajo na učinkovitost delovanja, ki je povezana s posodobitvami na krivuljah dodelitve virov.

#### <a name="resource-management"></a>Upravljanje virov

Ta težava je odpravljena:

- Ko je zmogljivost koledarja vira, ki ga je mogoče rezervirati, večja od 1, rešitev Project Service Automation napačno prepozna zmogljivost kot 0 (nič). Zato se v pogledu razporeda pojavi neskončna zanka.

#### <a name="sales"></a>Prodaja

Odpravljene so naslednje težave:

- Ko se ustvari vrstica dnevnika, ki ima vrsto transakcije po meri, pride do naslednje izjeme z referenco z vrednostjo »null«: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Vlog in kategorij, ki so deaktivirane pred kopiranjem ponudbe, ne smete dodajati plačljivim vlogam in kategorijam na novo kopirane ponudbe.
- Datum dokumenta in datum knjiženja računov nista usklajena z začetnim datumom, ki je naveden v podrobnosti vrstice računa, ustvarjene neposredno v osnutku računa.
- Izjeme z referenco z vrednostjo »null« se ustvarijo v scenarijih, ki so povezani z deaktivacijo vlog in kategorij pred kopiranjem ponudbe.
- Dejanje **Posodobi cene** na strani **Projekti** ne posodobi ocen stroškov in ocen materiala.
