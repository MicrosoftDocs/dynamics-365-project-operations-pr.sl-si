---
title: Ocena stroškov dodelitev virov s podizvajalsko pogodbo
description: Ta članek pojasnjuje, kako program Microsoft Dynamics 365 Project Operations izračuna oceno stroškov dodelitev virov s podizvajalsko pogodbo.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522676"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Ocena stroškov dodelitev virov s podizvajalsko pogodbo

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Stroški dodelitve opravil podizvajalskih članov projektne ekipe se obračunajo s cenikom **Nakup**, ki je priložen podizvajalski pogodbi na povezanem zapisu člana ekipe. To se razlikuje od tega, kako se obračunajo stroški dodelitev virov zaposlenih, kjer se dodelitve opravil virov zaposlenih obračunajo s cenikom **Cena**, ki je priložen pogodbeni enoti projekta. 

Opravila splošnih članov projektne ekipe, ki so podizvajalci, se obračunajo z nastavitvijo cene, ki temelji na vlogi, v ceniku nabave, ki je priložen podizvajalski pogodbi. Nakupne cene je mogoče nastaviti tudi posebej za vsak vir. Te cene, povezane z viri, bodo imele prednost pri obračunavanju stroškov dodelitve opravil imenovanih članov projektne ekipe, ki so pogodbeni delavci. 

Prednost uporabe nakupne cene, povezane z vlogo, v primerjavi s ceno, povezano z viri, je odvisna od nastavitve prioritete cenovne razsežnosti v razdelku **Parametri > Cenovna razsežnost na podlagi zneska**.

Ta funkcionalnost dinamičnega določanja cen na podlagi nastavitve razsežnosti za nakupne cene podizvajalcev je podobna izpeljavi cen in deležev obračunavanja za zaposlene s polnim delovnim časom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Ustvarjanje dodelitev opravil za pridobitev ocen stroškov virov podizvajalcev

Dodelitve opravil za podizvajalce se lahko ustvarijo na dva načina: 
- Z izbiro zavihka **Opravila**.
- Z izbiro zavihka **Ekipa**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ustvarjanje dodelitev virov z uporabo zavihka »Opravila«
Z uporabo seznama **Viri** v zavihku **Opravila** za določeno nalogo lahko ustvarite dodelitev opravila za poimenovani vir ali splošni vir. Če izberete poimenovani vir iz spustnega seznama **Dodeljeni viri** na opravilu in je ta vir pogodbeni delavec, je poimenovani vir dodeljen opravilu in ustvarjen je ustrezen zapis člana projektne ekipe z vrsto delavca, nastavljeno na **Pogodbeni delavec**, in možnostjo **Veljavnost**, nastavljeno na **Neveljavno**. V naslednjem koraku boste morali odpreti zapis člana projektne ekipe in izbrati podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe. S tem boste posodobili dodelitev opravila, da se bo sklicevalo na podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe, prav tako pa boste posodobili stanje člana ekipe na **Veljavno**.

Če se odločite ustvariti splošnega člana ekipe iz spustnega seznama **Dodeljeni viri** na opravilu, vam bo pogovorno okno **Ustvarjanje splošnega člana ekipe** omogočilo izbiro podizvajalske pogodbe in podrobnosti podizvajalske pogodbe. Ko je splošni vir dodeljen opravilu in je ustvarjen ustrezen zapis člana projektne ekipe, boste opazili, da je zapis člana projektne ekipe ustvarjen z vrsto delavca, nastavljeno na **Pogodbeni delavec**, in možnostjo **Veljavnost**, nastavljeno na **Veljavno**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Ustvarjanje članov projektne ekipe z uporabo zavihka »Ekipa«
Z uporabo zavihka »Ekipa« v projektu lahko ustvarite splošnega ali poimenovanega člana ekipe. Pri ustvarjanju člana ekipe lahko izberete podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe. Ko je član ekipe ustvarjen, ga boste morali dodeliti opravilu z uporabo spustnega seznama **Dodeljeni viri** v opravilu. 

## <a name="updating-estimates"></a>Posodabljanje ocen
Ko boste člane projektne ekipe dodelili opravilom, se boste morali pomakniti do zavihka **Ocene** v projektu in izbrati možnost **Posodobi cene**, da zagotovite, da so mere stroškov dodelitve virov podizvajalcem posodobljene na podlagi nabavnega cenika, priloženega podizvajalski pogodbi. Ocene se ne ustvarijo za nedodeljena opravila v programu Microsoft Dynamics 365 Project Operations. Posledično boste morali ustvariti dodelitve opravil za ceno in stroške različnih opravil v vašem projektu. 

> [OPOMBA!] Člani projektne ekipe, ki imajo možnost **Vrsta delavca** nastavljeno kot **Pogodbeni delavec**, vendar nimajo sklica na podizvajalsko pogodbo, so v mreži **Člani projektne ekipe** označeni kot **Neveljavno**. Če obstajajo člani projektne ekipe s tem stanjem, odprite zapis člana projektne ekipe in ročno posodobite polja podizvajalske pogodbe in podrobnosti podizvajalske pogodbe tako, da bo ocena finančnih stroškov natančno odražala stroške podizvajalca v zavihku **Ocene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
