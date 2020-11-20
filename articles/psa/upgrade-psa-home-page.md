---
title: Nadgradnja domače strani
description: Ta tema vsebuje informacije o tem, kje najdete pomembne informacije o novih in spremenjenih funkcijah aplikacije Dynamics 365 Project Service Automation, in o postopku za nadgradnjo na najnovejšo različico.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121778"
---
# <a name="upgrade-home-page"></a>Nadgradnja domače strani

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Nadgradnja storitve PSA, različice 2.x ali 1.x, na različico 3.x

### <a name="new-instances"></a>Novi primerki

Od 17. maja 2019, ko je bila rešitev Project Service Automation izbrana med pripravo novega primerka, se različica 3.x privzeto namesti.

### <a name="existing-instances"></a>Obstoječi primerki

V prejšnjih različicah so se morale stranke, ki imajo primerek PSA različice 2.x in ga morajo nadgraditi na različico 3.x, tj. različica PSA na podlagi poenotenega vmesnika odjemalca (UCI), obrniti na Microsoftovo podporo in podati podrobnosti o njihovem primerku, da lahko podpora omogoči primerek za nadgradnjo na različico 3.x. Od 1. marca 2020 bodo stranke, ki imajo primerek PSA različice 2.x in ga morajo nadgraditi na različico 3.x, lahko svoje primerke nadgradile neposredno s skrbniškega portala, ne da bi se morale obrniti na Microsoftovo podporo.  

> [!NOTE]
> PSA različice 3.x vključuje pomembne spremembe. Zgrajen je bil na osnovi ogrodja poenotenega vmesnika, da bi pomagal zagotoviti izboljšano uporabniško izkušnjo. Na novo zasnovana aplikacija zagotavlja skladen in enoten uporabniški vmesnik (UI), ki sledi odzivnim načelom oblikovanja za optimalen prikaz na zaslonu poljubne velikosti ali kateri koli napravi. V aplikaciji se je izvedlo še veliko drugih sprememb. Spremenila so se nekatera področja, na primer za oblikovanje cen, opravljanje rezervacij ter dodeljevanje virov, časa, stroškov in odobritev.

Priporočamo vam, da pred izvedbo postopka za nadgradnjo izvedete naslednja opravila:

- Preverite, ali sta v identificiranem primerku nameščeni tako Dynamics 365 Field Service kot Project Service Automation. Če sta nameščeni obe rešitvi, ju najprej nadgradite in šele nato nadaljujete z običajno uporabo primerka.
- Pozorno preglejte naslednje teme. Seznanjenje in razumevanje sprememb med različicami vam bo pomagalo pri postopku nadgradnje. Te teme zagotavljajo informacije o večjih spremembah v PSA, skupaj z nasveti in priporočili za načrtovanje nadgradnje na različico 3.x.

    - [Novosti ali spremembe v storitvi Project Service Automation različice 3](whats-new-changed-v3.md)
    - [Vidiki nadgradnje – nadgradnja storitve Project Service Automation različice 2.x ali 1.x na različico 3](upgrade-v3.md)

- Nadgradite različico za preizkusno okolje, da ocenite spremembe v uvedbi, preden nadgradite produkcijski primerek.

Ko boste pregledali zgoraj omenjene teme in boste pripravljeni na nadgradnjo na PSA različice 3.x ali različico na podlagi UCI, pošljite zahtevo Microsoftovi podpori, da bo ta omogočila nadgradnjo v skrbniškem središču. Vaša zahteva naj vsebuje tudi podrobnosti vašega primerka.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Starejše različice PSA (PSA različice 2.x) v novo ustvarjenem primerku

Od 17. maja 2019 bodo imeli vsi novi primerki privzetega odjemalca v obliki UCI. Za prilagoditev na to spremembo bosta privzeto omogočeni PSA različice 3.x in Field Service različice 8.x, saj sta ti različici zasnovani za delo z odjemalcem UCI.

Od 1. marca 2020 stranke, ki uporabljajo Dynamics PSA, ne bodo več mogle ustvarjati novih okolij s starejšimi različicami PSA, na primer PSA različice 2.x ali starejšimi. Vsako novo okolje bo razpoložljivo samo v različici PSA 3.x.

> [!NOTE]
> Za najboljšo izkušnjo pri uporabi starejših različic storitev Field Service in PSA, pojdite na stran **Sistemske nastavitve** in v polju **Uporabi samo nov poenoteni vmesnik (priporočeno)** izberite **Ne**, saj te različice niso zasnovane tako, da bi jih lahko pravilno naložili v UCI. Po izklopu UCI lahko odprete in zaženete te različice rešitev Field Service in PSA prek starega spletnega odjemalca. 
