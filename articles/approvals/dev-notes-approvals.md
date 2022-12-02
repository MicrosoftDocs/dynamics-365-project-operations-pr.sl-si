---
title: Opombe za razvijalce za odobritve
description: V tem članku so na voljo dodatne informacije o delu z odobritvami.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924772"
---
# <a name="developer-notes-for-approvals"></a>Opombe za razvijalce za odobritve

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations vključuje logiko preverjanja veljavnosti, ki zagotavlja pravilen prehod zapisov po stopnjah odobritev. Pravilni prehodi zapisov zagotavljajo: 

  - Vse podporne vrstice so ustvarjene v povezanih tabelah, kot so dnevniki in dejanske vrednosti.
  - Odobritelj je označen kot **Odobritelj projekta** v projektu pred nadaljevanjem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]