---
title: Pogodbe za predplačila in honorarje
description: Ta tema vsebuje informacije o pogodbenih modelih za predplačila in honorarje v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088105"
---
# <a name="advances-and-retainer-based-contracts"></a>Pogodbe za predplačila in honorarje 


_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Dynamics 365 Project Operations podpira pogodbe za honorarje. Pogodba za honorar je dogovorjeni nabor enakomerno porazdeljenih plačil, za katere bo stranki izdan račun ves čas trajanja projekta. Ta vrsta pogodbe se običajno uporablja za modele obračunavanja glede na čas in material ali porabo, kjer je treba stranki dati predvidljiv račun in razpored plačil. Dejanske vrednosti prihodkov vračunane za vsako obdobje, se uskladijo s plačili, ki ste jih prejeli od stranke na začetku obdobja. V skladu s konceptom modela obračunavanja časa in materiala se lahko vrednosti prihodkov, vračunane v posameznem obdobju, razlikujejo glede na nastale stroške. Če je vračunani prihodek večji od zneska, prejetega na začetku obdobja, bi lahko podjetje za izvedbo projektov:

- stranki izdalo samo račun za presežek 
- odložilo vire prihodkov na naslednje obdobje za zaračunavanje in na koncu projekta naredilo zadnji skupni račun za morebitne preostale neusklajene prihodke

Glavna razlika med pogodbenim modelom za honorarje in pogodbenim modelom s fiksno ceno v aplikaciji Project Operations je ta, da v pogodbenem modelu s fiksno ceno znesek računa ni povezan z nastalimi stroški ali vezan na njih. Zaračunavanje sledi pristopu, ki temelji na mejniku in je usklajen s stroški, nastalimi v tem obdobju. V pogodbi za honorarje se prihodki, za katere je mogoče izstaviti račun, zabeležijo v podrobnosti pogodbe na podlagi načina obračunavanja. Kadar je način obračunavanja glede na čas in material, je fakturirani prihodek vezan na stroške, nastale v katerem koli danem obdobju, in se lahko od obdobja do obdobja razlikuje. Vendar se stranki izda račun samo za znesek na periodičnem honorarju. Sistem na koncu obdobja uporabi drug račun za uskladitev fakturiranega prihodka, zabeleženega med obdobjem, z zneskom, za katerega je bil stranki izdan račun na začetku obdobja.

Prednost te metode je, da strankini stroški postanejo predvidljivi v urniku za honorar, za razliko od običajnega modela obračunavanja časa in materiala. Organizacija, ki izvaja projekt, ima tudi nekaj prostora za kritje tveganja izterjave stroškov, ki so nastali zaradi kakršnega koli povečanja obsega, katerega mu ga model s fiksno ceno ne bi omogočil.

Poleg periodičnega urnika za honorar lahko aplikacija Project Operations od stranke zabeleži enkratno predplačilo in ga uskladi z različnimi komponentami stroškov projekta.

honorar v aplikaciji Project Operations ni na voljo za uporabo, dokler ni izdan stranki. To označujejo naslednja polja na podmreži za predplačila in honorarje.

| Polje | Ustreznost, namen in smernice | Nadaljnji vpliv |
| --- | --- | --- |
| Razpoložljiv znesek | Znesek, ki je na voljo za uporabo v zapisu o honorarju ali predplačilu. | Dokler predplačilo ali honorar ni izdan, ga ni mogoče uporabiti, kar pomeni, da je razpoložljivi znesek enak nič. |
| Uporabljen znesek | Znesek, ki je že uporabljen v honorarju ali predplačilu. | Predplačilo ali honorar je mogoče na računu delno uskladiti z dejanskimi stroški, ki bodo imeli določen del označen kot »že porabljen« ali »porabljen«. Preostali znesek predplačila ali honorarja je na voljo za usklajevanje na prihodnjem računu z dejanskimi stroški. |
