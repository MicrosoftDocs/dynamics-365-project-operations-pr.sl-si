---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 18, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v posodobitvi Project Service Automation, izdaja 18, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918884"
---
# <a name="project-service-automation-update-release-18-v3"></a>Izdaja posodobitve 18 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, posodobitev izdaja 18. Številka graditve te različice je V3.10.8.12 in je na splošno na voljo prek samostojne posodobitve v aprilu 2020.

## <a name="update-release-18"></a>Izdaja posodobitve 18

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

- Popravljeno: postopki **Preklic**, **Zahteva** in **Preklic odobritve** naletijo na izjeme z nejasnimi sporočili o napakah.
- Popravljeno: ko za določen strošek postopek **Preklic odobritve** ne uspe, ne pride do napake ustrezne izjeme.
- Popravljeno: mreža časovnih vnosov nepravilno obravnava dela proste dneve v Avstraliji po oktobrskem preklopu na poletni čas.
- Popravljeno: nepravilna logika privzetih nastavitev preprečuje oddajo stroškov.
- Popravljeno: če odobritev časovnega vnosa ne uspe, odobritev ostane v stanju **V teku**.
- Popravljeno: napake strežnika SQL pri množičnih odobritvah (zamuda/časovna omejitev).
- Popravljeno: večje težave z uporabniško izkušnjo, ki jih povzroči posodabljanje članov ekipe pri odobravanju časovnih vnosov.

**Vodenje projektov**

- Popravljeno: obvestilo o časovnem pasu se je premaknilo s pogleda **Uskladitev** na glavni obrazec **Projekt**.
- Popravljeno: predloga koledarja nima pravilnih privzetih nastavitev, ko se odpre nov obrazec projekta.
- Popravljeno: uporabniki brskalnikov, ki temeljijo na programski opremi Chromium, ne morejo preprosto izbrati predhodnih opravil za izbris.
- Popravljeno: ustvarjanje ali kopiranje **projekta iz prazne predloge** pridobi nepovezane dodelitve.
- Popravljeno: v določenih robnih primerih se pri ustvarjanju nove naloge iz mreže opravil ustvarijo podvojeni zapisi.
- Popravljeno: v ročnem načinu uporabniki ne morejo spremeniti začetnih datumov opravil na poznejše od trenutno shranjenega datuma.

**Upravljanje virov**

- Popravljeno: v pogled **Uskladitev** vrstica delne vsote napačno izračuna razlike pri rezervacijah po podaljšanju rezervacij.
- Popravljeno: pogled **Uskladitev** napačno prikaže dodelitve virov, ko ima vir, ki ga je mogoče rezervirati, koledar, ki se ne ujema s koledarjem projekta.

**Sales**

- Opravljeno: ko so časovni vnosi ponovno odobreni (**Odobri > Prekliči >** ponovno odobri), se ustvari podvojeni dejanski znesek, ki se ne zaračuna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
