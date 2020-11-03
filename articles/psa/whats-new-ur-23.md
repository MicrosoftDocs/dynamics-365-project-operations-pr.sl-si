---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 23, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 23.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084703"
---
# <a name="project-service-automation-update-release-23-v3"></a>Izdaja posodobitve 23 za Project Service Automation, V3

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 23. Ta različica ima številko graditve V 3.10.34.30 in je splošno na voljo s samostojno posodobitvijo od avgusta 2020.

## <a name="update-release-23"></a>Izdaja posodobitve 23

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:
- Obravnavanje mejnega primera v razdelku **Brisanje člana projektne ekipe** za zagotavljanje smiselne izjeme.
- Pri uvozu dodelitve se prikaže prazen zaslon za odstranjevanje.

**Upravljanje virov**

Odpravljene so naslednje težave:

- **Kartica virov v mreži za uporabo virov** prikazuje napačne podatke, če je časovno merilo več kot pet dni.
- Ko stranke ustvarijo vir, ki ga je mogoče rezervirati, vtičnik občasno ne uspe samodejno dodati vira v skupino Microsoft Office 365.
- Pogled **Uskladitev** napačno prikazuje ročne obrise v pogledu **Teden** ali **Mesec**.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Zaradi prekomernega števila entitet **RetrieveMultiple za uporabniške nastavitve** je delovanje odobritev projektov in drugih postopkov poslabšano.
- Iskanje virov v mreži **Načrtovanje opravil** je omejeno na prikaz največ pet članov projektne ekipe. 
- Iskanje virov v mreži **Načrtovanje opravil** ne filtrira nedejavnih virov.
- Ročni način ne deluje po pričakovanjih v strukturirani členitvi dela pri načrtovanju projekta.
- Mreža **Načrtovanje opravil** prikazuje **Nedejavne kategorije transakcij**.
- Mreža **Dodelitev virov** napačno zaokroži, če ima opravilo več dodelitev.
- Vrednosti zaokroževanja se razlikujejo med načrtovanimi in dejanskimi stroški za eno opravilo.

**Sales**

Odpravljene so naslednje težave:

- Z dvoklikom možnosti **Pridobi vse kategorije transakcij** se ustvari več vrstic.
