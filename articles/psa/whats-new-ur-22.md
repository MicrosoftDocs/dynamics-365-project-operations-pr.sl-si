---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 22, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 22.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126638"
---
# <a name="project-service-automation-update-release-22-v3"></a>Izdaja posodobitve 22 za Project Service Automation, V3

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 22. Številka graditve te različice je V3.10.33.48 in je na splošno na voljo prek samostojne posodobitve junija 2020.

## <a name="update-release-22"></a>Izdaja posodobitve 22

### <a name="bug-fixes"></a>Popravki napak



**Čas in strošek**

Odpravljene so naslednje težave:

- **Časovni vnosi** po uvozu niso samodejno dodani v urnik časovnih vnosov.
- Mrežni izbirnik datuma **Časovni vnos** ne prepozna uporabnikovih področnih nastavitev.

**Upravljanje virov**

Odpravljene so naslednje težave:

- V ročnem načinu se spremembe obrisov v razdelku **Dodelitev vira** ne prepoznajo, ko gre za ustvarjanje zahtev v razdelku **Zahteve za vir**.
- V razdelku **Zahteve za vir** statusi zahtev po meri niso podprti.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Z dvoklikom možnosti EstimateGridControl ne dobite pravilne razčlembe številk nizozemskega zapisa.
- Dodeljene ure se ne posodabljajo pravilno, ko se dodeljena opravila spreminja z dodatkom za namizni odjemalec Microsoft Project.
- V omrežjih za sledenje in ocene projektov je prikazana napačna koda prodajne valute, kadar je pogodbena valuta drugačna od valute stranke in če je organizacija nameščena za prikaz valutnih kod namesto simbolov valut.
- Končnemu datumu člana ekipe je dodan en dan, če delovni urnik traja 24 ur na dan.
- V časovnici projektov dodajanje kategorije transakcije v opravilo ne sproži samodejnega shranjevanja.
- Pri dodajanju člana ekipe v predlogo projekta se prikaže naslednja napaka: »Zahteve po virih je nemogoče povezati s predlogami projekta«. 
- Skript pravilnika traku "msdyn.Approval.CanApproveOrReject" prikaže napako časovne omejitve.

**Sales**

Odpravljene so naslednje težave:

- Sporočilo o napaki se ne prikaže, ko je v iskalnem polju cenika izbran stroškovni cenik v razdelku »Cenik nove ponudbe projekta«.
- Zapiranje ponudbe, kot da je pridobljena, ne povzroči premika do ustvarjene pogodbe, če je BPF, priložen ponudbi, v zaključni fazi.
- Storniranje vnosov v razdelku **Neobračunana prodaja** je povezano z izvirnimi stroški ob odpoklicu časovnega vnosa.
- Po izbiri gumba **Potrdi** se stanje računa ne spremeni v **Potrjeno**, razen če je račun osvežen.
