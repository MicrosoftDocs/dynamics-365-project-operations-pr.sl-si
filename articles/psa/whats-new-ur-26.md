---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 26, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 26.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: fa526e97a366c01dae2547d79d0eda2fb204e07d0f6383b991165b9eecd836e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004286"
---
# <a name="project-service-automation-update-release-26-v3"></a>Izdaja posodobitve 26 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 26, V3. Ta različica ima številko izdelave V3.10.44.59 in je splošno na voljo s samoposodobitvijo decembra 2020.

## <a name="update-release-26"></a>Izdaja posodobitve 26

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Uporabniki lahko spremenijo opravilo v časovnem vnosu, ki je bil odobren/poslan.
- Pri shranjevanju časovnega vnosa se pojavi napaka »Object Reference Not Set«.
- Uvoz časovnega vnosa iz dodelitev virov ustvari časovne vnose z napačnimi vrednostmi DateTime.
- Ko sta nameščeni aplikaciji Project Service Automation in Field Service, se gumb **Novo** dvakrat prikaže v ukazni vrstici za časovne vnose v aplikaciji Field Service.
- Posodabljanje celic **Dovoli enoto** in **Skupina enot** zdaj ponovno deluje v mreži **Ocene stroškov**.
- Oblika **Posodobi urejanje časovnega vnosa** vključuje možnost **Časovnica**.
- Odobritev časa za neprojektne časovne vnose blokira sistem pri iskanju vloge odobritelja projekta.

**Upravljanje virov**

Odpravljene so naslednje težave:

- V vtičnik **PostProjectCreate** je dodano preverjanje za obstoj primarne zahteve, preden jo ustvarite.
- Obrazec za hitro ustvarjanje **Član projektne skupine** vrne izjemo s sklicem »null«, če so polja odstranjena iz obrazca.
- Ustvarjanje zahtev za 12 ur v celotnem letu ne bo uspelo.
- Izboljšano o napaki za izjemo s sklicem »null« pri ustvarjanju zahteve za vir.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Izboljšana potrditev veljavnosti za obravnavo izjeme s sklicem »null«, ustvarjene v vtičniku **PreProjectUpdate**.
- Projekti, ki jih je objavil namizni vtičnik Microsoft Project, izbrišejo nedodeljene naloge.
- Dodano je novo preverjanje veljavnosti, ko je sklic projektnega opravila neveljaven zaradi izjeme s sklicem »null« v vtičniku **PreValidateProjectTaskUpdate**.
- Mreža člana ekipe ne prikazuje posameznih nalog v zapisu člana ekipe.
- Dodano je novo preverjanje veljavnosti in sporočila o napakah zaradi izjeme s sklicem »null« v vtičniku **PreProjectTaskDelete**.

**Sales**

Odpravljene so naslednje težave:

- Pri izbiri podrobnosti ponudbe ali pogodbe, ki temelji na projektu, bi moral biti gumb **Predlog** viden samo pri izbiri podrobnosti, ki temeljijo na izdelku in so povezane z obstoječim izdelkom.
- Razdelite privilegij **Create_Product** iz privilegija **Create_ProjectContract**.
- Če izbrišete podrobnosti računa, bo prišlo do napake pri sklicu »null« za **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]