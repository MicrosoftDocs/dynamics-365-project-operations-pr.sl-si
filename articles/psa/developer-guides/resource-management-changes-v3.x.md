---
title: Spremembe upravljanja virov (Project Service Automation 3.x)
description: Ta članek vsebuje informacije o spremembah področja upravljanja virov.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916032"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Spremembe upravljanja virov (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Razdelki tega članka zagotavljajo informacije o spremembah, ki so bile narejene na področju upravljanja virov Dynamics 365 Project Service Automation različica 3.x.

## <a name="project-estimates"></a>Projektne ocene

Namesto da bi bile projektne ocene narejene na podlagi entitete **msdyn\_projecttask** (**Projektno opravilo**), so narejene na podlagi entitete **msdyn\_resourceassignment** (**Dodelitev vira**). Dodelitve virov so postale »vir resničnosti« za razporejanje opravil in določanje cen.

## <a name="line-tasks"></a>Opravila vrstic

V PSA 3.x so opravila vrstic zastarela. Dodelitve zdaj kažejo na celotno opravilo in ne le na opravila vrstic.

Spodnji primer prikazuje, kako je opravilo, imenovano »Opravilo preizkusa«, dodeljeno članom skupine A in B v starejših različicah PSA in PSA 3.x.

- **Pred PSA 3.x:**

    - Opravilo preizkusa

        - Opravilo preizkusa – opravilo vrstice 1

            - Dodelitev skupini A

        - Opravilo preizkusa – opravilo vrstice 2

            - Dodelitev skupini B

- **PSA 3.x:**

    - Opravilo preizkusa

        - Dodelitev skupini A
        - Dodelitev skupini B

## <a name="unassigned-assignment"></a>Nedodeljena dodelitev

V različici PSA 3.x je nedodeljena dodelitev tista, ki je dodeljena članu ekipe z vrednostjo **NULL** in viru z vrednostjo **NULL**. Nedodeljene dodelitve se lahko pojavijo v spodaj naštetih primerih:

- Nedodeljena dodelitev se vedno ustvari, če je bilo opravilo ustvarjeno, vendar še ni bilo dodeljeno nobenemu članu ekipe. 
- Nedodeljena dodelitev se ponovno ustvari, če so odstranjeni vsi pooblaščenci posameznega opravila.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Polja za načrtovanje v entiteti »Projektno opravilo«

Polja v entiteti **msdyn\_projecttask** so zastarela ali premaknjena v entiteto **msdyn\_resourceassignment** oziroma se nanje sklicuje entiteta **msdyn\_projectteam** (**Član projektne ekipe**).

| Zastarelo polje v msdyn\_projecttask (projektno opravilo) | Novo polje v msdyn\_resourcedodelitve (dodelitev vira) | Pripomba |
|---|---|---|
| msdyn\_assignedresources | Ni priprav ali omejitev | |
| msdyn\_assignedteammembers | Ni priprav ali omejitev | |
| msdyn\_numberofresources | Ni priprav ali omejitev | |
| msdyn\_scheduledhours | Ni priprav ali omejitev | |
| msdyn\_effortcontour | msdyn\_plannedwork | Oblika podatkovne strukture JavaScript Object Notation (JSON), ki je shranjena v polju, je bila spremenjena. |

## <a name="schedule-contour"></a>Krivulja razporeda

Krivulja razporeda je shranjena v polju **Načrtovano delo** (**msdyn\_plannedwork**) za vsako entiteto **Dodelitev vira** posebej (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktura

Nova struktura krivulje razporeda je sestavljena iz prilagodljivih časovnih rezin, ki so definirane za vsak dan razporeda. Vsaka časovna rezina ima naslednje lastnosti:

- **Začetek** – začetek delovnega časa za posamezni dan glede na projektni koledar.
- **Konec** – konec delovnega časa za posamezni dan glede na projektni koledar.
- **Ure** – število dodeljenih ur za posamezni dan.

**Primer**

Ta primer uporablja projektni koledar, kjer delovni dan traja od 9.00 do 17.00 v časovnem pasu UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Samodejno in ročno razporejanje

Če je opravilo samodejno razporejeno, se ure naložijo vnaprej, trajanje opravila pa se lahko zmanjša.

**Primer**

Spodnji primer prikazuje opravilo, ki je bilo samodejno razporejeno za 18 ur v treh dneh (od 3. decembra 2018 do 5. decembra 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Če je opravilo ročno razporejeno, se ure enakomerno porazdelijo na vse datume.

**Primer**

Spodnji primer prikazuje opravilo, ki je bilo ročno razporejeno za 18 ur v treh dneh (od 3. decembra 2018 do 5. decembra 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Enota dodelitve

Enota dodelitve je bila v PSA 3.x opuščena. Ure potrebnega dela za opravilo se zdaj enakomerno porazdelijo po dneh za vse dodeljene vire.

**Primer**

V tem primeru je opravilo dodeljeno dvema viroma in samodejno razporejeno za 36 ur v treh dneh (od 3. decembra 2018 do 5. decembra 2018).

- Dodelitev 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Dodelitev 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Cenovne razsežnosti

V PSA 3.x so bila polja cenovnih razsežnosti za posamezne vire (kot sta **Vloga** in **Organizacijska enota**) odstranjena iz entitete **msdyn\_projecttask**. Ta polja je zdaj mogoče pridobiti od posameznega člana projektne skupine (**msdyn\_projectteam**) dodelitve vira (**msdyn\_resourceassignment**), ko so ustvarjene ocene projekta. Novo polje **msdyn\_organizationalunit** je bilo dodano entiteti **msdyn\_projectteam**.

| Zastarelo polje v msdyn\_projecttask (projektno opravilo) | Polje iz msdyn\_projectteam (Član projektne skupine), ki se uporablja v zameno |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Krivulje

Polja s krivuljami cen in ocen so bila opuščena v entiteti **msdyn\_projecttask**. Premaknjena so bila v entiteto **msdyn\_resourceassignment**.

| Zastarelo polje v msdyn\_projecttask (projektno opravilo) | Novo polje v msdyn\_resourcedodelitve (dodelitev vira) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Entiteti **msdyn\_resourceassignment** so bila dodana naslednja polja:

* msdyn\_plannedcost
* msdyn\_plannedsales

Entiteta **msdyn\_projecttask** ima nespremenjena spodaj našteta polja za načrtovane, dejanske in preostale stroške ter prodajo:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
