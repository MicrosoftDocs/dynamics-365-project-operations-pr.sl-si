---
title: Projektne predloge
description: Ta članek vsebuje informacije o tem, kako uporabiti predloge projektov za hitro nastavitev projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 03cccf8f0201d82db57e52dc1175fcf9a7812a53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930890"
---
# <a name="project-templates"></a>Projektne predloge 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektna predloga je vnaprej določeno ogrodje, ki vam pomaga hitro in enostavno zagnati projekt. Uporabite lahko vnaprej določeno predlogo in ustvarite nov projekt z enim klikom. Enako kot pri projektih morate določiti pogoje za projektne predloge. Za vsako projektno predlogo morate določiti koledar projekta, vloge in ceniki pa morajo biti vnaprej določeni v organizaciji, tako da imajo komponente predloge uporabne podatke.

Projektna predloga je sestavljena iz treh komponent: razporeda, ocen projekta in članov projektne ekipe.

## <a name="schedule"></a>Urnik

Razpored v projektni predlogi ima enak nabor elementov kot razpored v projektu. Ustvarite lahko hierarhijo opravil, povežete vloge z opravili, določite atribute za razporejanje in nastavite odvisnosti. Razpored v projektni predlogi podpira tudi načine opravil za vsako opravilo. Zato podpira mehanizem razporejanja. Koledar projekta morate povezati s projektom. Ko ustvarite razpored dela, med projektno predlogo in projektom ni razlik.

## <a name="project-estimates"></a>Projektne ocene

Projektne ocene v projektni predlogi delujejo na enak način kot projektne ocene v projektu. Vendar pa se lastne in prodajne cene pridobijo iz privzetih cenikov z lastnimi in prodajnimi cenami, ki so določeni v parametrih.

## <a name="creating-a-project-from-a-template"></a>Ustvarjanje projekta iz predloge
 
Projekt lahko iz projektne naloge ustvarite na več načinov:

- Če ustvarite projekt iz ponudbe, lahko projektno predlogo izberete v pogovornem oknu **Hitro ustvarjanje: projekt**.

> ![Pogovorno okno »Hitro ustvarjanje: projekt«.](media/project-11.png)

- Če ustvarite projekt tako, da izberete **Nov projekt**, se stran **Projekt** prikaže, preden je zapis shranjen. V polju **Izberi predlogo** izberite eno od vnaprej določenih projektnih predlog v organizaciji.
- Uporabite **Ustvari projekt iz predloge** na strani **Entiteta predloge**.

## <a name="copying-components-of-template-to-project"></a>Kopiranje komponent predloge v projekt

Ko kopirate komponente projektne predloge v projekt, lahko pride do preglasitev, odvisno od nastavitev v projektu.

### <a name="copying-the-schedule"></a>Kopiranje razporeda

Če ima projekt drugačen projektni koledar kot predloga, bodo pri kopiranju razporeda iz projektne predloge za razpored opravil uporabljene delovne ure iz koledarja projekta. Tako se razpored prilagodi osnovnemu koledarju projekta. Podobno ima tudi prvo opravilo v razporedu začetni datum projekta, razpored za preostalo hierarhijo pa se posodobi glede na trajanje in odvisnosti, ki so navedene v predlogi. 

### <a name="copying-project-estimates"></a>Kopiranje projektnih ocen 

Ko kopirate v vrsticah ocen projekta, se ceniki posodobijo. Pri ceniku z lastnimi cenami te posodobitve temeljijo na lastniški enoti projekta. Pri prodajnem ceniku temeljijo na stranki. Pri projektih, ki so povezani z entiteto prodaje, se lastne in prodajne cene enote določijo na podlagi teh cenikov.

### <a name="copying-a-project-team"></a>Kopiranje projektne ekipe

Ko projektno ekipo kopirate iz projektne predloge v projekt, se prekopirajo tudi splošni viri skupaj z znanji in usposobljenostmi, opredeljenimi v predlogi. Ohranijo se tudi dodelitve splošnega vira iz projektne predloge. Poimenovani viri niso podprti v projektnih predlogah.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
