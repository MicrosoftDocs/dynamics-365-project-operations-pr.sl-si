---
title: Sinhroniziranje dejanskih vrednosti projekta neposredno iz rešitve Project Service Automation v dnevnik integracije projekta za objavo v rešitvi Finance and Operations
description: Ta tema opisuje predloge in osnovna opravila, ki se uporabljajo za sinhronizacijo dejanskih vrednosti projekta neposredno iz rešitve Microsoft Dynamics 365 Project Service Automation v Finance and Operations.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988131"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sinhroniziranje dejanskih vrednosti projekta neposredno iz rešitve Project Service Automation v dnevnik integracije projekta za objavo v rešitvi Finance and Operations

[!include[banner](../includes/banner.md)]

Ta tema opisuje predloge in osnovna opravila, ki se uporabljajo za sinhronizacijo dejanskih vrednosti projekta neposredno iz rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.

Predloga sinhronizira transakcije iz rešitve Project Service Automation v pripravljalno tabelo v rešitvi Finance. Po končani sinhronizaciji **morate** uvoziti podatke iz pripravljalne tabele v dnevnik integracije.

> [!NOTE]
> - Integracija dejanskih vrednosti projekta je na voljo od različice 8.0.1 naprej.
> - Če uporabljate različico Enterprise 7.3.0, boste po namestitvi KB 4132657 in KB 4132660 lahko predloge uporabili za integracijo projektnih opravil, kategorij stroškov transakcij, ocen delovnih ur, ocen stroškov in dejanskih vrednosti ter konfiguriranje zaklepanja funkcionalnosti. Če morate ponastaviti računovodsko porazdeljevanje, priporočamo, da namestite tudi KB 4131710.
> - Če uporabljate različico 7.3.0 in transakcije s pristojbinami pridobivate iz rešitve Project Service Automation, morate namestiti KB 4345320, da te pristojbine vključite v račun projekta.
> - Če vnašate zneske prometnega davka za časovne in stroškovne transakcije v rešitvi Project Service Automation, morate namestiti Project Service Automation Update 7. V nasprotnem primeru dejanske vrednosti davka ne bodo povezane z dejanskimi vrednostmi časa ali stroškov in ne bodo sinhronizirane v rešitev Finance. Za več informacij se obrnite na podporo.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Pretok podatkov za Project Service Automation v Finance

Rešitev za integracijo rešitve Project Service Automation v rešitev Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance. Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok podatkov o dejanskih vrednostih projekta iz rešitve Project Service Automation v Finance.

Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.

[![Podatkovni tok za integracijo rešitve Project Service Automation v rešitvi Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Dejanske vrednosti projekta iz rešitve Project Service Automation

### <a name="template-and-tasks"></a>Predloga in opravila

Za dostop do razpoložljivih predlog v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.

Naslednja predloga in osnovna opravila se uporabljajo za sinhronizacijo dejanskih vrednosti projekta iz rešitve Project Service Automation v Finance:

- **Ime predloge v integraciji podatkov:** dejanske vrednosti projekta (PSA v Fin in Ops)
- **Ime opravil v projektu:**

    - Dejanske vrednosti
    - TransactionConnections

### <a name="entity-set"></a>Nabor entitet

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Dejanske vrednosti                    | Integracijska entiteta za dejanske vrednosti projekta                   |
| Povezave transakcij    | Integracijska entiteta za odnose projektne transakcije |

### <a name="entity-flow"></a>Potek entitete

Dejanske vrednosti projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v dnevnik integracije projekta v rešitvi Finance. Računovodstvo se uporabi na podlagi privzetih finančnih razsežnosti in nastavitve knjiženja.

### <a name="prerequisites"></a>Zahteve

Preden se lahko izvede sinhronizacija dejanskih vrednosti, morate konfigurirati parametre integracije rešitve Project Service Automation ter sinhronizirati projekte, projektna opravila in kategorije transakcij stroškov projekta.

### <a name="power-query"></a>Power Query

V predlogi za dejanske vrednosti projekta morate uporabiti Microsoft Power Query za Excel, če želite dokončati naslednja opravila:

- Pretvorite vrsto transakcije v rešitvi Project Service Automation v pravilno vrsto transakcije v rešitvi Finance. Ta pretvorba je že določena v predlogi za dejanske vrednosti projekta (PSA v Fin in Ops).
- Pretvorite vrsto obračunavanja v rešitvi Project Service Automation v pravilno vrsto obračunavanja v rešitvi Finance. Ta pretvorba je že določena v predlogi za dejanske vrednosti projekta (PSA v Fin in Ops). Vrsta obračunavanja se nato preslika v lastnost vrstice glede na konfiguracijo na strani **Parametri integracije rešitve Project Service Automation**.
- Filtrirajte do določenih organizacijskih enot virov, ki jih je treba sinhronizirati s to predlogo.
- Če se dejanske vrednosti medpodjetniškega časa ali stroška sinhronizirajo v rešitev Finance, morate pogodbeno organizacijsko enoto pretvoriti v pravilno pravno osebo v rešitvi Finance. V predlogi za dejanske vrednosti projekta (PSA v Fin in Ops) je pogojni stolpec določen na podlagi predstavitvenih podatkov. Zadnji vstavljeni pogojni stolpec morate posodobiti na pravilne pravne osebe. V nasprotnem primeru lahko pride do napake pri integraciji ali pa se v rešitev Finance uvozijo napačne dejanske transakcije.
- Če se dejanske vrednosti medpodjetniškega časa ali stroška ne bodo sinhronizirale v rešitev Finance, morate iz predloge izbrisati zadnji vstavljeni pogojni stolpec. V nasprotnem primeru lahko pride do napake pri integraciji ali pa se v rešitev Finance uvozijo napačne dejanske transakcije.

#### <a name="contract-organizational-unit"></a>Pogodbena organizacijska enota
Če želite v predlogi posodobiti vstavljeni pogojni stolpec, kliknite puščico **Preslikava**, da odprete preslikavo. Izberite povezavo **Napredno pošiljanje poizvedb in filtriranje**, da odprete Power Query.

- Če uporabljate privzeto predlogo za dejanske vrednosti projekta (PSA v Fin in Ops), v rešitvi Power Query izberite zadnji **Vstavljen pogoj** v razdelku **Uporabljeni koraki**. V vnosu **Funkcija** zamenjajte **USSI** z imenom pravne osebe, ki jo želite uporabiti pri integraciji. Po želji dodajte dodatne pogoje v vnos **Funkcija** in posodobite pogoj **else** z **USMF** na pravilno pravno osebo.
- Če ustvarjate novo predlogo, morate dodati stolpec za medpodjetniški čas in stroške. Izberite **Dodaj pogojni stolpec** in vnesite ime novega stolpca, na primer **LegalEntity**. Vnesite pogoj za stolpec; če je **msdyn\_contractorganizationalunitid.msdyn\_name** \<organizational unit\>, potem je \<enter the legal entity\>; v nasprotnem primeru ju »null«.

### <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

Spodnja slika prikazuje primer preslikave predloge opravila v integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.

[![Preslikava predloge – dejanske vrednosti.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Preslikava predloge – povezave transakcij.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Uvoz iz pripravljalne tabele po integraciji iz rešitve Project Service Automation

Periodični postopek uvoza iz pripravljalne tabele morate zagnati po sinhronizaciji dejanskih vrednosti iz rešitve Project Service Automation v Finance. Ta postopek bo uvozil projektne transakcije iz pripravljalne tabele v dnevnik integracije rešitve Project Service Automation, kjer se uporabi računovodstvo in je mogoče knjižiti uvožene transakcije. Priporočamo, da ta postopek zaženete v paketnem načinu; po želji ga lahko nastavite tako, da se izvaja kot ponavljajoče se opravilo.

## <a name="update-actuals-from-finance"></a>Posodobitev dejanskih vrednosti iz rešitve Finance

### <a name="template-and-tasks"></a>Predloga in opravila

Naslednja predloga in osnovna opravila se uporabljajo za sinhronizacijo številke kupona in prometnih davkov za knjižene projektne transakcije iz rešitve Finance v Project Service Automation:

- **Ime predloge v integraciji podatkov:** posodobitev dejanskih vrednosti projekta (Fin in Ops v PSA)
- **Ime opravil v projektu:**

    - Dejanske vrednosti 
    - TransactionConnections

### <a name="entity-set"></a>Nabor entitet

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integracijska entiteta za dejanske vrednosti projekta                   | Dejanske vrednosti                    |
| Integracijska entiteta za odnose projektne transakcije | Povezave transakcij    |

### <a name="entity-flow"></a>Potek entitete

Dejanske vrednosti projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v dnevnik integracije projekta v rešitvi Finance. Ko so dejanske vrednosti objavljene v rešitvi Finance, so v rešitvi Project Service Automation posodobljene s številko kupona iz rešitve Finance. Če so bili v rešitvi Finance dodani prometni davki, se v rešitvi Project Service Automation ustvarijo nove dejanske vrednosti davka.

### <a name="power-query"></a>Power Query

V predlogi za posodobitev dejanskih vrednosti projekta morate uporabiti Power Query, če želite dokončati naslednja opravila:

- Pretvorite vrsto transakcije v rešitvi Finance v pravilno vrsto transakcije v rešitvi Project Service Automation. Ta pretvorba je že določena v predlogi za posodobitev dejanskih vrednosti projekta (Fin in Ops v PSA).
- Pretvorite vrsto obračunavanja v rešitvi Finance v pravilno vrsto obračunavanja v rešitvi Project Service Automation. Ta pretvorba je že določena v predlogi za posodobitev dejanskih vrednosti projekta (Fin in Ops v PSA).

### <a name="template-mapping-in-data-integration"></a>Preslikava predlog v Integraciji podatkov

Spodnje slike prikazujejo primere preslikav predlog opravil v Integracijo podatkov. Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Finance v Project Service Automation.

[![Preslikava predloge – posodobitev dejanskih vrednosti.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Preslikava predloge – posodobitev transakcij.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]