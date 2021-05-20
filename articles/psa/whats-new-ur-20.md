---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 20, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za izdajo posodobitve 20 za Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949114"
---
# <a name="project-service-automation-update-release-20-v3"></a>Izdaja posodobitve 20 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 20. Številka graditve te različice je V3.10.31.37 in je na splošno na voljo prek samostojne posodobitve junija 2020.

## <a name="update-release-20"></a>Izdaja posodobitve 20

### <a name="bug-fixes"></a>Popravki napak

**Vodenje projektov**

Odpravljene so naslednje težave:

- Če uvažate člane projektne ekipe z načinom dodeljevanja, ki zahteva ure, se prikaže nejasno sporočilo o napaki, ko je določeno število ur enako nič.
- Ko uporabnik doseže največje dovoljeno število znakov v polju **Opis** projektne naloge, se pojavi neustrezna napaka.
- Če so nastavitve jezika uporabnika nastavljene na japonščino, vas stran za prenos dodatka **Microsoft Dynamics 365 Project Service Automation** preusmeri na stran za prenos v angleščini.
- Ko se pojavi napaka strežnika, se oznaka sinhronizacije na zavihku **Načrtovanje** obrazca **Projekti** včasih ohrani.
- Ko je opravilo spremenjeno, so odvečne posodobitve opravil poslane strežniku.

**Sales**

Odpravljene so naslednje težave:

- Če na obrazcu **Pogodba** dvokliknete možnost **Ustvari račun**, se za en zapis dejanske vrednosti ustvarita dva računa.
- V brskalniku Internet Explorer 11 uporabniki ne morejo ustvariti vnosov stroškov.
- Razveljavitev stroškov in razveljavitev neplačanih dejanskih opravljenih prodajnih del niso povezani.
- Z gumbom **Osvežitev opravljenih del** na obrazcu **Projekt** se ne osvežijo **Dejanske ure za opravilo**.
- Z vtičnikom **PreValidateProjectTeamMemberCreate** lahko ustvarite podvojene splošne vire, ki jih je mogoče rezervirati, ko je atribut **msdyn_isgenericresourceprojectscoped** nastavljeno na **False**.
- Z možnostjo **Znova izračunaj** počistite stroške, ki se zaračunajo za podrobnosti vrstice ponudb in podrobnosti vrstice pogodbe na podlagi izdelkov.
- V določenih primerih vtičnik **PostEstimateLineUpdate** prikazuje napako izjeme sklica z vrednostjo »null«.
- Trajanje časovne faze v razdelku **Tabela analize dobičkonosnosti** se ne ujema s trajanjem stroškov v podrobnostih vrstice ponudbe s fiksno ceno.
- Vrednosti enot in skupin enot niso pravilno privzete za kategorije stroškov v obrazcih **Podrobnosti vrstice pogodbe** in **Podrobnosti vrstice ponudbe**.
- Seznami **Lastna cena organizacijske enote** dovoljujejo prekrivanje datumske veljavnosti.
- Uporabniki ne smejo spreminjati možnosti **OrgUnit**, ko vrsta naročila ne temelji na delu, ker bo prišlo do napake izjeme sklica z vrednostjo »null«.
- Pri poskusu krmarjenja iz obrazca **Podrobnosti vrstice ponudbe** nazaj na zavihek **Ponudba** se obrazec osveži in prikaže se zavihek **Povzetek**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]