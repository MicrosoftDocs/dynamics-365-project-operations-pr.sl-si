---
title: Opombe za razvijalce za odobritve
description: V tej temi so na voljo dodatne informacije o delu z odobritvami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991686"
---
# <a name="developer-notes-for-approvals"></a>Opombe za razvijalce za odobritve

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations vključuje logiko preverjanja veljavnosti, ki zagotavlja pravilen prehod zapisov po stopnjah odobritev. Pravilni prehodi zapisov zagotavljajo: 

  - Vse podporne vrstice so ustvarjene v povezanih tabelah, kot so dnevniki in dejanske vrednosti.
  - Odobritelj je označen kot **Odobritelj projekta** v projektu pred nadaljevanjem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]