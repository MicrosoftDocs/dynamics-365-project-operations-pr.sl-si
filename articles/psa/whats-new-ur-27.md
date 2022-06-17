---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 27, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v posodobitvi Project Service Automation, izdaja 27, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912950"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, posodobitev izdaja 27. Ta različica ima številko graditve V3.10.45.98 in je splošno na voljo s samostojno posodobitvijo v januarju 2021.

## <a name="update-release-27"></a>Izdaja posodobitve 27

### <a name="bug-fixes"></a>Popravki napak

**Splošno**

Odpravljene so naslednje težave:

- Dnevniki, ki jih ustvarijo vtičniki v aplikaciji Project Service Automation, niso nastavljeni na samodejno brisanje.
- Samodejna nadgradnja ne uspe, ker rešitev Project Service Automation vsebuje podedovan nični element »NavBarArea« in element naslova.

**Čas in strošek**

Odpravljene so naslednje težave:

- Mreža **Časovni vnos** prikazuje napačne podatke za vedenje datuma **Neodvisno od časovnega pasu**.
- Mreža **Časovni vnos** ustvarja napačen čas za vedenje datuma **Neodvisno od časovnega pasu**.
- Iskanje opravil ni omejeno na izbrani projekt na strani **Urejanje časovnega vnosa**.
- Odobritev časa za neprojektne časovne vnose je blokirana, ker sistem išče odobritelja projekta.
- Funkcija »Pravi vnos za dejanske vrednosti« prikazuje napačno sporočilo o napaki.
- Če opravilo za dejanski strošek vsebuje vrednost »null« in po osvežitvi skupnih vrednosti za projekt, se pojavi naslednja napaka: »Navedeni ključ ni prisoten v slovarju«.
- V določenih primerih filtri **Združi po** na zavihku **Ocena projekta** ne prikazujejo ocen stroškov.
- Interval **Poletni čas** za časovne vnose ni pravilen.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Izboljšave predpomnjenja, ki izboljšajo učinkovitost, povezano z nalaganjem strani **Projekt**.
- Zastarelo pravilo poslovanja, ki preprečuje dokončanje projektnih opravil.
- Obrisi dodatka za Microsoft Project ne upoštevajo koledarja dodatka, kar ustvari napačne zahteve za vir.
- Ustvarjanje projektov iz predlog povzroči nepravilno nastavljanje datumov dodelitve in preprečuje možnost za ustvarjanje zahtev za vir.
- Uporabnik z uporabo tipkovnice ne more dostopati do možnosti **Kategorija**, **Opis** in **Stanje**.
- Dejanske vrednosti prodaje za projekt ne vključujejo prodajnih vrednosti dajatev in materiala.
- Združevanje dejanskih prodaj in dejanskih stroškov ni izvedeno pravilno, saj so uporabljeni različni menjalni tečaji.
- Opis v **Privzeta predloga za delovne ure** je zavajajoč.
- Umikanje opravila ne odstrani možnosti **Kategorija** v uporabniškem vmesniku, dokler ta ni osvežen.
- Manjka preverjanje veljavnosti, s katerim se zagotovi, da pomikanje projekta preko končnega datuma ni dovoljeno.

**Sales**

Odpravljene so naslednje težave:

- V vrstici projektne ponudbe je ustvarjena izjema s sklicem »null«, ker je možnost **Uvoz iz ocene projekta** vidna, ko projekt ni izbran.
- Napaka »Sklic na predmet ni nastavljen na primerek predmeta« se pojavi pri zapiranju ponudbe kot **Pridobljena**.
- Stanje prilagoditve ni nastavljeno med dejansko razveljavitvijo pri odstranjevanju povezave projekta s podrobnostmi pogodbe.
- Ko sta aplikaciji Dynamics 365 Field Service in Project Service Automation nameščeni, na strani **Račun** možnosti **Zakleni cene** in **Uporabi trenutne cene** nista prikazani hkrati.
- Za japonščino obstaja neskladen prevod z drugimi stranmi, ki temeljijo na koledarju.
- Dejanji **Aktiviranje** in **Deaktiviranje** sta bili odstranjeni iz entitet **Povezava cenika** v aplikaciji Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
