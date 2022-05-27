---
title: Opombe za razvijalce za odobritve
description: V tej temi so na voljo dodatne informacije o delu z odobritvami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579740"
---
# <a name="developer-notes-for-approvals"></a>Opombe za razvijalce za odobritve

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations vključuje logiko preverjanja veljavnosti, ki zagotavlja pravilen prehod zapisov po stopnjah odobritev. Pravilni prehodi zapisov zagotavljajo: 

  - Vse podporne vrstice so ustvarjene v povezanih tabelah, kot so dnevniki in dejanske vrednosti.
  - Odobritelj je označen kot **Odobritelj projekta** v projektu pred nadaljevanjem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]