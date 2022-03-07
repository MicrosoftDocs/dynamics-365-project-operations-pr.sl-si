---
title: Pogodbe za predplačila in honorarje
description: Ta tema vsebuje informacije o pogodbenih modelih za predplačila in honorarje v aplikaciji Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87e275cb72f1edc5a2a9913b4aa47d461d1f3d3d9bf177bf0ffba8b463f4ce01
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994431"
---
# <a name="advances-and-retainer-based-contracts"></a>Pogodbe za predplačila in honorarje


_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations podpira pogodbe za honorar. Pogodba za honorar je dogovorjeni nabor enakomerno porazdeljenih plačil, za katere bo stranki izdan račun ves čas trajanja projekta. Ta vrsta pogodbe se običajno uporablja za modele obračunavanja glede na čas in material ali porabo, kjer je treba stranki dati predvidljiv račun in razpored plačil. Dejanske vrednosti prihodkov vračunane za vsako obdobje, se uskladijo s plačili, ki ste jih prejeli od stranke na začetku obdobja. V skladu s konceptom modela obračunavanja časa in materiala se lahko vrednosti prihodkov, vračunane v posameznem obdobju, razlikujejo glede na nastale stroške. Če je vračunani prihodek večji od zneska, prejetega na začetku obdobja, bi lahko podjetje za izvedbo projektov:

- stranki izdalo samo račun za presežek 
- odložilo vire prihodkov na naslednje obdobje za zaračunavanje in na koncu projekta naredilo zadnji skupni račun za morebitne preostale neusklajene prihodke

Glavna razlika med pogodbenim modelom za honorarje in pogodbenim modelom s fiksno ceno v aplikaciji Project Operations je ta, da v pogodbenem modelu s fiksno ceno znesek računa ni povezan z nastalimi stroški ali vezan na njih. Zaračunavanje sledi pristopu, ki temelji na mejniku in je usklajen s stroški, nastalimi v tem obdobju. V pogodbi za honorarje se prihodki, za katere je mogoče izstaviti račun, zabeležijo v podrobnosti pogodbe na podlagi načina obračunavanja. Kadar je način obračunavanja glede na čas in material, je fakturirani prihodek vezan na stroške, nastale v katerem koli danem obdobju, in se lahko od obdobja do obdobja razlikuje. Vendar se stranki izda račun samo za znesek na periodičnem honorarju. Sistem na koncu obdobja uporabi drug račun za uskladitev fakturiranega prihodka, zabeleženega med obdobjem, z zneskom, za katerega je bil stranki izdan račun na začetku obdobja.

Prednost te metode je, da strankini stroški postanejo predvidljivi v urniku za honorar, za razliko od običajnega modela obračunavanja časa in materiala. Organizacija, ki izvaja projekt, ima tudi nekaj prostora za kritje tveganja izterjave stroškov, ki so nastali zaradi kakršnega koli povečanja obsega, katerega mu ga model s fiksno ceno ne bi omogočil.

Poleg periodičnega urnika za honorar lahko aplikacija Project Operations od stranke zabeleži enkratno predplačilo in ga uskladi z različnimi komponentami stroškov projekta.

honorar v aplikaciji Project Operations ni na voljo za uporabo, dokler ni izdan stranki. To označujejo naslednja polja na podmreži za predplačila in honorarje.

| Polje | Opis | Nadaljnji vpliv |
| --- | --- | --- |
| Razpoložljiv znesek | Znesek, ki je na voljo za uporabo v zapisu o honorarju ali predplačilu. | Dokler predplačilo ali honorar ni izdan, ga ni mogoče uporabiti, kar pomeni, da je razpoložljivi znesek enak nič. |
| Uporabljen znesek | Znesek, ki je že uporabljen v honorarju ali predplačilu. | Predplačilo ali honorar je mogoče na računu delno uskladiti z dejanskimi stroški, ki bodo imeli določen del označen kot »že porabljen« ali »porabljen«. Preostali znesek predplačila ali honorarja je na voljo za usklajevanje na prihodnjem računu z dejanskimi stroški. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]