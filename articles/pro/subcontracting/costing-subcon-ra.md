---
title: Ocena stroškov dodelitev virov s podizvajalsko pogodbo
description: Ta članek pojasnjuje, kako Microsoft Dynamics 365 Project Operations izračuna oceno stroškov podizvajalskih dodelitev virov.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262080"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Ocena stroškov dodelitev virov s podizvajalsko pogodbo

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Stroški dodelitve nalog podizvajalskih članov projektne skupine so ovrednoteni z uporabo **Nakup** cenik, ki je priložen podizvajalski pogodbi na pripadajočem zapisu članov ekipe. To se razlikuje od tega, kako se ovrednotijo stroški dodelitev virov zaposlenih, kjer se dodelitve nalog virov zaposlenih ovrednotijo z uporabo **Stroški** cenik, ki je priložen naročniku projekta. 

Za generične člane projektne skupine, ki so sklenjeni s podizvajalci, se dodelitve ovrednotijo z nastavitvijo cene na podlagi vloge v nabavnem ceniku, priloženem podizvajalski pogodbi. Nakupne cene je mogoče nastaviti tudi posebej za vsak vir. Te cene, specifične za vire, bodo imele prednost, če so dodelitve nalog imenovanih članov projektne skupine pogodbeni delavci. 

Prednost uporabe nakupne cene, specifične za vlogo, v primerjavi s specifično za vir določa nastavitev prioritete dimenzije cen v **Parametri > Razsežnosti oblikovanja cen na podlagi zneska**.

Ta funkcionalnost dinamičnega izpeljanja cen na podlagi nastavitve razsežnosti za nakupne cene podizvajalcev je podobna izpeljavi stroškov in stopenj računov za zaposlene s polnim delovnim časom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Izdelava nalog za pridobitev ocene stroškov virov podizvajalcev

Naloge za podizvajalce se lahko ustvarijo na dva načina: 
- Uporabljati **Naloge** zavihek.
- Uporabljati **Ekipa** zavihek.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ustvarjanje dodelitev virov z uporabo zavihka Naloge
Uporabljati **Viri** seznam v **Naloge** za določeno nalogo, lahko ustvarite dodelitev naloge za imenovan vir ali generični vir. Če izberete imenovani vir iz **Dodeljeni viri** spustni meni na opravilu in je ta vir pogodbeni delavec, je imenovani vir dodeljen opravilu in ustvarjen je ustrezen zapis člana projektne skupine z vrsto delavca, nastavljeno na **Pogodbeni delavec** in **Veljavnost** nastavljena **Neveljavno**. Kot naslednji korak boste morali odpreti zapis člana projektne skupine in izbrati podizvajalsko pogodbo in vrstico podizvajalske pogodbe. To bo posodobilo dodelitev naloge, da se bo sklicevalo na podizvajalsko pogodbo in podizvajalsko linijo, posodobilo pa bo tudi status člana ekipe na **Veljavno**.

Če se odločite ustvariti generičnega člana ekipe iz **Dodeljeni viri** spustni meni za nalogo, **Generično ustvarjanje članov ekipe** pogovorno okno vam bo omogočilo izbiro podizvajalske pogodbe in vrstice podizvajalske pogodbe. Ko je generični vir dodeljen opravilu in je ustvarjen ustrezen zapis člana projektne skupine, boste opazili, da je zapis člana projektne skupine ustvarjen z vrsto delavca, nastavljeno na **Pogodbeni delavec** in **Veljavnost** nastavljena **Veljavno**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Ustvarjanje članov projektne skupine z uporabo zavihka Ekipa
Z uporabo zavihka Ekipa v projektu lahko ustvarite splošnega ali imenovanega člana ekipe. Pri ustvarjanju člana ekipe lahko izberete podizvajalsko pogodbo in vrstico podizvajalske pogodbe. Ko je član ekipe ustvarjen, ga boste morali dodeliti nalogi z uporabo **Dodeljeni viri** spustni meni na nalogi. 

## <a name="updating-estimates"></a>Posodabljanje ocen
Ko boste člane projektne skupine dodelili nalogam, se boste morali pomakniti do **Ocene** na projektu in izberite **Posodobite cene** zagotoviti, da so stroški dodelitve sredstev podizvajalcem posodobljeni na podlagi nabavnega cenika, priloženega podizvajalski pogodbi. Ocene se ne ustvarijo za nedodeljena opravila v Microsoftu Dynamics 365 Project Operations. Posledično boste morali ustvariti dodelitve nalog za ceno in stroške različnih nalog v vašem projektu. 

> [OPOMBA!] Člani projektne skupine, ki so **Delavski tip** kot **Pogodbeni delavec** vendar nimajo reference podizvajalca, so označeni kot **Neveljavno** na **Člani projektne skupine** mreža. Če obstajajo člani projektne skupine s tem statusom, odprite zapis člana projektne skupine in ročno posodobite polja podizvajalske pogodbe in vrstice podizvajalske pogodbe, tako da bo ocena finančnih stroškov natančno odražala stroške podizvajalca na **Ocene** zavihek. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
