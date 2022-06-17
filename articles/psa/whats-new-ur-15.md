---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 15, V3
description: Ta članek vsebuje informacije o tem, kaj je novega v posodobitvi Project Service Automation, izdaja 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915664"
---
# <a name="project-service-automation-update-release-15-v3"></a>Izdaja posodobitve 15 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA). Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, posodobitev izdaje 15. Ta različica ima številko graditve V3.10.5.28 in je splošno na voljo s samostojno posodobitvijo v januarju 2020.

## <a name="update-release-15"></a>Izdaja posodobitve 15 

### <a name="enhancements"></a>Izboljšave

- Vodenje projektov

### <a name="bug-fixes"></a>Popravki napak

- Čas in strošek

  - Popravljeno: dodajanje obravnave napak pri nalaganju v pogledu usklajevanja.
  - Popravljeno: središče za projektne vire: preimenovanje za **Znesek**, da se zmanjša dvoumnost.
  - Popravljeno: prilagoditev pogleda **Kopiranje stolpcev časovnih vnosov**, da vključuje vrsto.
  - Popravljeno: ob urejanju trajanja časovnega vnosa v pogledu mreže z decimalnimi številkami nastane neznana napaka za nekatere številke.

- Vodenje projektov

  - Popravljeno: spustni meni za **Uporaba v pogledu sledenja** se zdaj razširi na podlagi širine možnosti.
  - Popravljeno: pri upravljanju projektov v časovnem pasu +13 lahko izračuni opravil prikazujejo netočne rezultate.
  - Popravljeno: **Končni čas člana ekipe** je bil popravljen ob uporabi 24-urnega koledarja.
  - Popravljeno: ponovna aktivacija **BPF** v glavnem obrazcu **msdyn_project**.
  - Popravljeno: izračun dodelitev več ne prezre enega dne.
  - Popravljeno: v obrazec projekta je bila dodana nova pasica z obvestili, ko se časovni pas razlikuje med uporabnikom in projektom.

- Sales

  - Popravljeno: iskanje kategorije ocene stroška se lahko uporabi za filtriranje dvojnikov.
  - Popravljeno: koda v **PluginDomain.ExecuteInTryCatchBlock(..)** ne skriva več izvora izjeme.
  - Popravljeno: ko je projektov več kot 1000 se ne prikaže več sporočilo o napaki v možnosti **Iskanje projektov** v obrazcu **Vrstica ponudbe**.
  - Popravljeno: mreža **Ocene** za ocene dela in ocene stroškov zdaj prikazuje pravilen simbol valute.
  - Popravljeno: ko organizacija posodobi PSA z izdaje posodobitve 14 na izdajo posodobitve 15, zavihek **Razpored** ni več prikazan prazen na obrazcu **Projekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
