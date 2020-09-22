---
title: Ustvarjanje časovnih vnosov
description: Ta tema vsebuje informacije o ustvarjanju časovnih vnosov.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755838"
---
# <a name="create-time-entries"></a>Ustvarjanje časovnih vnosov

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V prejšnjih različicah aplikacije Dynamics 365 Project Service Automation je bilo treba časovne vnose vnašati na tedenski ravni. V različici 3 rešitve Project Service Automation se vnosi vnesejo vsakodnevno. Po tem, ko ste ustvarili že nekaj časovnih vnosov, jih lahko množično ustvarite ali kopirate.

## <a name="create-a-time-entry"></a>Ustvarjanje časovnega vnosa

Za ustvarjanje časovnega vnosa sledite tem korakom.

1. Na strani **Časovni vnosi** izberite možnost **Novo**.
2. V pogovorno okno **Hitro ustvarjanje: časovni vnos** vnesite trajanje časovnega vnosa v minutah, urah ali dnevih. Trajanje morate vnesti v naslednji obliki: *x* minut, *x* ur ali *x* dni. Ure in dneve lahko vnesete tudi kot decimalne vrednosti, na primer *x,x* ur ali *x,x* dni.
3. Izberite vrsto časovnega vnosa in projekt, za katerega vnašate časovni vnos.
4. V polju **Projektno opravilo** poiščite opravilo za ta časovni vnos.

    > [!NOTE]
    > Če ustvarjate časovni vnos za opravilo, ki ni dodeljeno uporabniku, v polju **Projektno opravilo** izberite gumb **Iskanje**, nato izberite **Spremeni pogled** in nato še **Vsa dejavna projektna opravila**, da se prikaže seznam vseh opravil.

5. Vnesite opis, če je to potrebno, in nato izberite možnost **Shrani in zapri**.

Ko ste ustvarili in shranili časovni vnos, ga lahko uredite v mreži časovnega vnosa. Mreža časovnega vnosa podpira dve obliki zapisa:

- Časovne vnose lahko vnesete v obliki zapisa **hh:mm**. Ta oblika zapisa se nato pretvori v ure in decimalne vrednosti.
- Ure in decimalne vrednosti lahko vnesete neposredno.

Upoštevajte, da decimalne vrednosti ene ure niso enake minutam. To pomeni, da 1,5 ure predstavlja 1 uro in 30 minut. Enako pravilo velja za decimalne vrednosti dneva. En dan traja 24 ur, zato 0,5 dneva predstavlja 12 ur.

## <a name="bulk-create-time-entries"></a>Množično ustvarjanje časovnih vnosov

Ko ustvarite nekaj časovnih vnosov, jih lahko kopirate in s tem množično ustvarite dodatne časovne vnose.

1. Na strani **Časovni vnosi** izberite možnost **Kopiraj teden**.
2. Določite datumski obseg za kopiranje časovnih vnosov v poljih **Začetni datum** in **Končni datum** v skupini polj **Od obdobja**.
3. Določite datum, za katerega želite ustvariti časovne vnose, v polju **Začetni datum** v skupini polj **Do obdobja**.
4. Izberite **Kopiraj**, če želite ustvariti kopijo časovnih vnosov, ki ustrezajo dnevu v tednu, ki je določen v skupini polj **Do obdobja**. Časovni vnos za prejšnji ponedeljek bo na primer kopiran v ponedeljek za teden, ki je označen v skupini polj **Do obdobja**.

## <a name="import-data-for-time-entries"></a>Uvažanje podatkov za časovne vnose

Podatke lahko uvozite iz projektnih rezervacij in dodelitev. Ko uvažate podatke, lahko določite datumski obseg rezervacij za uvoz in nato izberite točno tiste rezervacije, ki jih je treba ustvariti kot **Osnutke** časovnih vnosov.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Združevanje po, razvrščanje, iskanje in zmogljivosti filtriranja

Časovne vnose lahko združite in filtrirate po razsežnostih, ki so določene v stolpcih. V polju **Združi po** izberite razsežnost, ki jo želite uporabiti za filtriranje časovnih vnosov. Zapise časovnih vnosov lahko razvrstite v naraščajočem ali padajočem vrstnem redu, tako da kliknete puščico za razvrščanje v glavi stolpca. Poleg tega lahko tudi prikažete ali skrijete vnose, tako da izberete gumb **Filter** v glavi stolpca, nato pa v polje **Iskanje** vnesete besedilo, ki ga je treba uporabiti za iskanje časovnih vnosov glede na ime projekta, projektno opravilo, časovni vnos ali vir.
