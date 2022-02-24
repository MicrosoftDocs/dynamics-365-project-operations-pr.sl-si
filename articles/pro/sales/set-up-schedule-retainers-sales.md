---
title: Nastavitev urnika za honorarje
description: Ta tema vsebuje informacije o tem, kako nastaviti urnik za honorar za Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272314"
---
# <a name="set-up-a-retainer-schedule"></a>Nastavitev urnika za honorarje

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Urniki za honorarje so nastavljeni na strani **Projektna pogodba** v storitvi Dynamics 365 Project Operations.

1. Na strani **Projektna pogodba** na zavihku **Predujmi in honorarji** izberite **Nastavitev urnika za honorar**.
2. Na pogovornem oknu, ki se odpre, so prikazana polja, navedena v naslednji tabeli. Tabela daje predstavo o tem, kako vnesene vrednosti vplivajo na urnik za honorar, ki bo ustvarjen.

| Polje | Opis | Nadaljnji vpliv |
| --- | --- | --- |
| Stranka projektne pogodbe | Stranka v pogodbi, ki ji bo izdan račun za honorar ali predplačilo. | Če imate v pogodbi več strank in če morate vsaki od njih izdati račun za določen znesek honorarja ali predplačila, ročno ustvarite en račun za vsako stranko. |
| Začetek urnika za honorar | Vnesite začetni datum urnika za honorar. | Ta datum morda ni datum, ko je ustvarjen prvi honorar ali predplačilo. Na datum nastanka prvega honorarja ali predplačila vpliva tudi pogostost izdajanja računov. |
| Konec urnika za honorar | Vnesite končni datum urnika za honorar. | Ta datum morda ni datum, ko je ustvarjen zadnji honorar ali predplačilo. Na datum nastanka zadnjega honorarja ali predplačila vpliva tudi pogostost izdajanja računov. |
| Število honorarjev, ki jih želite ustvariti | Ko vnesete število honorarjev, ki jih želite ustvariti, sistem v tem polju uporabi začetni datum in pogostost. | Ko je to polje ročno posodobljeno, sistem prezre vrednost polja **Konec urnika za honorar** in namesto tega ustvari določeno število honorarjev ali predplačil. |
| Pogostost izdajanja računov | Kako pogosto bo aplikacija ustvarila honorarje in preplačila. | Ta vrednost neposredno vpliva na število honorarjev in predplačil ter ustvarjene datume. |
| Skupni znesek | Skupni znesek je znesek, razdeljen na posamezen račun za honorar ali predplačilo, ki bo ustvarjen. | To polje nima nadaljnjega vpliva. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]