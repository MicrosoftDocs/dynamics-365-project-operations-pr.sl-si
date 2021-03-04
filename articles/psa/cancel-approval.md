---
title: Preklic odobrenih časovnih vnosov in vnosov stroškov
description: V tej temi najdete informacije o tem, kako prekličete potrjen čas projekta in transakcijo stroškov.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
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
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150598"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Preklic odobrenih časovnih vnosov ali vnosov stroškov

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V najnovejši različici rešitvi Dynamics 365 Project Service Automation lahko odobritelji prekličejo časovne vnose ali vnose stroškov, ki so jih predhodno odobrili.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Preklic predhodno potrjenega časovnega vnosa ali vnosa stroškov

Če želite preklicati že odobren časovni vnos ali vnos stroškov, sledite spodnjim korakom.

1. Odprite **Projekti** \> **Moje delo** \> **Odobritve**.
2. Na strani s seznamom **Odobritve** spremenite pogled na **Moje pretekle odobritve**. Prikaže se seznam časovnih vnosov in vnosov stroškov, ki ste jih odobrili.
3. Izberite enega ali več vnosov in nato **Prekliči odobritev**. Prikaže se opozorilo.
4. Če želite preklicati odobritev, izberite **V redu**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Razumevanje vpliva preklica odobritve časovnega vnosa ali vnosa stroškov

Preklic odobritve ima operativni in finančni učinek.

### <a name="operational-impact"></a>Operativni učinek

Ko je odobritev preklicana, se stanje zapisa ponastavi na **Osnutek** in odobritev ni več prikazana v pogledu **Moje pretekle odobritve**. Namesto tega je preklicana odobritev prikazana v pogledu **Časovni vnosi za odobritev** ali **Vnosi stroškov za odobritev**, odvisno od tega, ali je šlo za časovni vnos ali vnos stroškov. Poleg tega se stanje povezanega vnosa časa ali stroškov spremeni v **Poslano**, tako da je povezan vnos skladen z odobritvami, ki imajo stanje **Osnutek**.

Kot odobritelj lahko urejate nekatera polja odobritve s stanjem **Osnutek**. Med ta polja spadata **Vrsta obračunavanja** in **Ure za obračunavanje za vnose časa**. Ko naredite spremembe, lahko zapis znova odobrite. Lahko pa tudi zavrnete vnos. Če zavrnete odobritev časovnega vnosa, se stanje postavke spremeni v **Vrnjeno**. Če zavrnete odobritev vnosa stroškov, se stanje spremeni v **Zavrnjeno**. Vrnjeni in zavrnjeni vnosi delujejo enako kot vnos s stanjem **Osnutek**. Član projektne ekipe lahko naredi vse potrebne spremembe vnosa in ga nato znova predloži v odobritev ali v celoti izbriše vnos.

### <a name="financial-impact"></a>Finančni učinek

Ko je odobritev preklicana, to tudi finančno vpliva na projekt. Ustrezne dejanske vrednosti za stroške in prodajne cene se posodobijo tako:

- Stanje prilagoditve je nastavljeno na **Prilagojeno**.
- Stanje obračunavanja je nastavljeno na **Preklicano**.

Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja. Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti. Edine vrednosti, ki niso prekopirane, so vrednosti količin. Te vrednosti se stornirajo. Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**. Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, stanje obračunavanja pa je nastavljeno na **Preklicano**.

Po teh spremembah se znesek, ki je zabeležen kot porabljen za projekt, in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.
