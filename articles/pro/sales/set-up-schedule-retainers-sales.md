---
title: Nastavitev urnika za honorar – poenostavljeno
description: Ta tema vsebuje informacije o tem, kako nastaviti urnik za honorar za Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181292"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Nastavitev urnika za honorar – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Urniki za honorar so nastavljeni na strani **Projektna pogodba** v storitvi Dynamics 365 Project Operations.

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
