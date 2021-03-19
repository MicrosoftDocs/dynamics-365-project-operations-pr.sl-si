---
title: Ocena prodaje in stroškov projekta, ko vir, ki ga je mogoče rezervirati, prevzame več vlog za projekt
description: V tej temi so informacije o tem, kako je mogoče uporabiti cenovne razsežnosti za podporo določanja cen in stroškov za vir, ki prevzame več vlog v projektu.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291009"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Ocena prodaje in stroškov projekta, ko vir, ki ga je mogoče rezervirati, prevzame več vlog za projekt 

[!include [banner](../includes/psa-now-project-operations.md)]

Podjetja, ki temeljijo na projektih, pogosto potrebujejo en sam vir, ki prevzame več vlog v projektu. Za vsako od teh vlog je mogoče določiti različne cene in stroške, kar pomeni, da lahko čas istega vira v projektu dobi različne finančne ocene, odvisno od deležev obračunavanja in stroškov za vsako od vlog. Project Service Automation omogoča nastavitev vrednosti v zapisu člana ekipe za imenovani vir in omogoča različne razveljavitve za vsako opravilo, kateremu je dodeljen član ekipe.

V naslednjem primeru je pojasnjeno, kako preprosta preglasitev te vrednosti omogoča viru, da ima v projektu več vlog z različnimi stroški in deleži obračunavanja.

## <a name="create-tasks"></a>Ustvarjanje opravil
Ustvarite dve projektni opravili po 40 ur, »Opravilo A« in »Opravilo B«. »Opravilo A« določite kot predhodnika opravila B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Nastavitev vloge in organizacijske enote za splošnega člana projektne ekipe

1. Na strani **Razpored** izberite vrstico **Opravilo** za opravilo A. 
2. V polju **Viri** na spustnem seznamu izberite možnost **Ustvari**.
3. Na strani **Hitro ustvarjanje člana ekipe** določite atribute splošnega člana ekipe, ki lahko izvaja to opravilo.
4. Izberite ustrezno vlogo in organizacijsko enoto, nato pa izberite **Shrani in zapri**. Za to opravilo je ustvarjen in dodeljen splošni član ekipe. 

Ponovite te korake za opravilo B in se prepričajte, da se vloga in organizacijska enota splošnega člana ekipe, ustvarjenega za opravilo B, razlikujeta od opravila A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Nastavitev vloge in organizacijske enote za projektno opravilo

1. Ko ustvarite opravilo A, ga izberite in nato izberite **Uredi opravilo**.
2. Na strani **Podrobnosti opravila** poiščite polji **Vloga** in **Organizacijska enota**, nato dodajte vrednosti, potrebne za vir, ki bi opravil to opravilo. 

  > [!NOTE]
  > Če ta scenarij izpolnjujete s predstavitvenimi podatki rešitve Project Service Automation, za vlogo izberite **Svetovalni vodja** in za organizacijsko enoto **Fabrikam ZDA**.

3. Izberite opravilo B in nato izberite **Uredi opravilo**.
4. Na strani **Podrobnosti opravila** poiščite polji **Vloga** in **Organizacijska enota**, nato dodajte vrednosti, potrebne za vir, ki bi opravil to opravilo. Prepričajte se, da se vrednosti v poljih **Vloga** in **Organizacijska enota** za opravilo B razlikujejo od vrednosti za opravilo A. 

  > [!NOTE]
  > Če ta scenarij izpolnjujete s predstavitvenimi podatki rešitve Project Service Automation, za vlogo izberite **Omrežni tehnik** in za organizacijsko enoto **Fabrikam ZDA**.

5. Shranite in zaprite stran **Podrobnosti opravila**. 

## <a name="team-member-and-estimates-behavior"></a>Član ekipe in vedenje ocen 

1. Na strani **Podrobnosti opravila** v razdelku **Član ekipe** izberite dva splošna člana ekipe, nato pa izberite možnost **Ustvari zahteve**. 
2. Izberite vrstico člana ekipe za vlogo **Svetovalni vodja** in nato izberite možnost **Rezerviraj**. Odpre se plošča razporeda in rezervira vir za to zahtevo.
3. Izberite vrstico člana ekipe za vlogo **Omrežni tehnik** in nato izberite možnost **Rezerviraj**. Odpre se plošča razporeda in rezervira isti vir za to zahtevo.

### <a name="team-member-grid"></a>Mreža člana ekipe 
V mreži **Član ekipe** boste opazili, da sta dva zapisa splošnega člana ekipe izbrisana, nadomestil pa ju je en sam vir. Ta vir ima en nabor vrednosti, ki prikazuje privzeti nabor vrednosti za možnosti **Vloga** in **Organizacijska enota**.
Ko razširite vrstico tega zapisa člana ekipe, lahko v zapisu člana ekipe vidite ločene dodelitve za obe opravili. V vsaki vrstici dodelitve so vrednosti, specifične za opravilo, za možnosti **Vloga** in **Organizacijska enota**. 

### <a name="estimates-grid"></a>Mreža ocen 
Ko se pomaknete do mreže **Ocene**, boste opazili, da sta za obe dodelitvi za isti vir določeni različni ceni.
Dodelitev za vir v opravilu A je ocenjena na podlagi vrednosti atributa **Vloga** za možnost **Svetovalni vodja**. Dodelitev za isti vir v opravilu B je ocenjena na podlagi vrednosti atributa **Vloga** za možnost **Omrežni tehnik**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]