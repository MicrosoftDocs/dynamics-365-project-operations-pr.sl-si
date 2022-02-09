---
title: Ocena stroškov podizvajalskih dodelitev virov
description: Ta tema pojasnjuje, kako Microsoft Dynamics 365 Project Operations izračuna oceno stroškov podizvajalskih dodelitev virov.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903785"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Ocena stroškov podizvajalskih dodelitev virov

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Dodelitve nalog podizvajalskih članov projektne skupine se obračunavajo z uporabo **Nakup** cenik, ki je priložen podizvajalski pogodbi na evidenci povezanega člana ekipe. To se razlikuje od tega, kako se obračunavajo dodelitve virov zaposlenih, kjer se dodelitve nalog za vire zaposlenih vrednotijo z uporabo **Stroški** cenik, ki je priložen naročniku projekta. 

Za generične člane projektne skupine, ki so oddani podizvajalcem, se dodelitve obračunajo z uporabo cene na podlagi vlog v nabavnem ceniku, priloženem podizvajalski pogodbi. Nakupne cene je mogoče določiti tudi posebej za vsak vir. Te cene, specifične za vir, bodo imele prednost pri obračunavanju stroškov nalog imenovanih članov projektne skupine, ki so pogodbeni delavci. 

Prednost uporabe nakupne cene, specifične za vlogo, v primerjavi z virom, je odvisna od nastavitve prednostne razsežnosti cen v **Parametri > Razsežnosti cen na podlagi zneska**.

Ta funkcionalnost dinamičnega izpeljanja cen, ki temelji na nastavitvi dimenzij za nabavne cene podizvajalcev, je podobna načinu izpeljanja stroškov in obračunskih stopenj za redno zaposlene. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Izdelava nalog za pridobivanje ocen stroškov sredstev podizvajalcev

Dodelitve nalog za podizvajalce je mogoče izdelati na dva načina: 
- Uporabljati **Naloge** zavihek.
- Uporabljati **Ekipa** zavihek.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Ustvarjanje nalog virov z zavihkom Naloge
Uporabljati **Viri** seznam v **Naloge** na kartici za določeno nalogo, lahko ustvarite nalogo za imenovani vir ali splošni vir. Če izberete poimenovani vir iz **Dodeljeni viri** spustni meni za nalogo in ta vir je pogodbeni delavec, poimenovani vir je dodeljen nalogi in ustvarjen je ustrezen zapis člana projektne skupine z vrsto delavca, nastavljeno na **Pogodbeni delavec** in **Veljavnost** nastavljena **Neveljavno**. Kot naslednji korak boste morali odpreti zapis članov projektne skupine in izbrati vrstico podizvajalcev in podizvajalcev. To bo posodobilo dodelitev naloge tako, da bo imela sklic na vrstico podizvajalcev in podizvajalcev ter posodobilo tudi status člana ekipe na **veljavno**.

Če se odločite ustvariti splošnega člana ekipe iz **Dodeljeni viri** spustni meni za nalogo, **Ustvarjanje generičnega člana ekipe** pogovorno okno vam bo omogočilo izbiro podizvajalske in podizvajalske vrstice. Ko je generični vir dodeljen nalogi in je ustvarjen ustrezen zapis člana projektne skupine, boste opazili, da je zapis člana projektne skupine ustvarjen z vrsto delavca, nastavljeno na **Pogodbeni delavec** in **Veljavnost** nastavljena **veljavno**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Ustvarjanje članov projektne skupine z zavihkom Ekipa
Z uporabo zavihka Ekipa v projektu lahko ustvarite generičnega ali imenovanega člana ekipe. Ko ustvarjate člana ekipe, lahko izberete vrstico podizvajalcev in podizvajalcev. Ko je član ekipe ustvarjen, boste morali člana ekipe dodeliti nalogi z uporabo **Dodeljeni viri** spustni meni za nalogo. 

## <a name="updating-estimates"></a>Posodabljanje ocen
Ko dodelite člane projektne skupine nalogam, se boste morali pomakniti na **Ocene** zavihek na projektu in izberite **Posodobite cene** zagotoviti, da se stroškovne stopnje dodelitev virov podizvajalcem posodobijo na podlagi nabavnega cenika, priloženega podizvajalski pogodbi. Ocene se ne generirajo za nedodeljena opravila v Microsoftu Dynamics 365 Project Operations. Posledično boste morali ustvariti naloge za ceno in stroške različnih nalog v vašem projektu. 

> [OPOMBA!] Člani projektne skupine, ki imajo **Vrsta delavca** kot **Pogodbeni delavec** vendar nimajo reference podizvajalca, so označene kot **Neveljavno** na **Člani projektne ekipe** mreža. Če obstajajo člani projektne skupine s tem statusom, odprite zapis članov projektne skupine in ročno posodobite polja vrstice podizvajalcev in podizvajalcev, tako da ocena finančnih stroškov natančno odraža stroške podizvajalca na **Ocene** zavihek. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]