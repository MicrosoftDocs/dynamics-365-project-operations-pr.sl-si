---
title: Nadgradnja vidikov za strukturirano členitev dela
description: Ta tema vsebuje informacije o nadgradnji strukturirane členitve dela iz storitve Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755832"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Nadgradnja vidikov za strukturirano členitev dela
Ta tema vsebuje informacije o nadgradnji strukturirane členitve dela iz storitve Project Service Automation 2.x na 3.x. Ta tema opisuje zdravo stanje projekta v rešitvi Project Service Automation (PSA), ki je potrebno za uspešno nadgradnjo. Vsebuje tudi informacije o pogostih razlogih za blokiranje, zaradi katerih bi bila nadgradnja neuspešna. Za več informacij o določanju projektnih opravil in njihovih funkcijah v okviru projektnega razporeda glejte temo [Projektni razporedi](project-creating.md).

## <a name="key-entities"></a>Ključne entitete
Za natančno strukturirano členitev dela, ki že ima naložene vire, so potrebne naslednje entitete:

- [Project](../developer/entities/msdyn_project.md)
- [Projektna ekipa](../developer/entities/msdyn_projectteam.md)
- [Projektno opravilo](../developer/entities/msdyn_projecttask.md)
- [Dodelitve virov](../developer/entities/msdyn_resourceassignment.md)
- [Odvisnost projektnega opravila](../developer/entities/msdyn_projecttaskdependency.md)
- [Viri, ki jih je mogoče rezervirati](../developer/entities/bookableresource.md)

Če želite določiti vir z naloženo strukturirano členitvijo dela, morate izvesti naslednje korake:

1. Ustvarite nov projekt. Za več informacij o tem, kako ustvarite nov projekt, glejte temo [msdyn_project](../developer/entities/msdyn_project.md).
2. Ustvarite eno ali več opravil. Za več informacij o tem, kako ustvarite opravilo, glejte temo [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).
3. Določite odvisnosti opravila. Za več informacij glejte [Odvisnost projektnega opravila](../developer/entities/msdyn_projecttaskdependency.md).
4. Dodelite člane projektne ekipe izbranemu projektu. Za več informacij glejte temo [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Dodelite člane projektne ekipe izbranim opravilom. Za več informacij glejte temo [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Odnosi projektnih ekip

Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:
- Vsi člani projektne ekipe morajo biti povezani z virom, ki ga je mogoče rezervirati.
- Vsi člani projektne ekipe morajo biti povezani z enakim projektom. 

## <a name="project-task-relationships"></a>Odnosi projektnih opravil
Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:

- Vsa povezana opravila morajo biti povezana z istim projektom.
- Vsako opravilo vrstice mora imeti nadrejeno opravilo.
- Vsako opravilo mora imeti nadrejeni projekt.

### <a name="valid-conditions"></a>Veljavni pogoji

- Vsa opravila morajo trajati točno ali dlje kot (> =) eno uro in manj kot 1.800.000 minut (1.250 dni).*
- Vsa opravila morajo imeti začetni datum od 1. 1. 2000.*
- Vsa opravila morajo imeti začetni datum najkasneje 17 let od današnjega dne.*
- Vsa opravila morajo imeti začetni datum pred končnim datumom ali na isti dan.
- Vse vrste transakcij za klasifikacije (stroški, material, davek in čas) morajo imeti določene vrednosti za **Privzeta enota** in **Skupina enot**.
- Izogibajte se črkovnem zapisu datuma.

### <a name="potential-mitigation-steps"></a>Možni koraki za ublažitev
- Z uporabo naprednega iskanja identificirajte projektna opravila, ki ne vsebujejo ID-ja projekta.
- Z uporabo naprednega iskanja identificirajte projektna opravila, kjer je načrtovano trajanje večje od > 1.800.000.
- Pred kakršnimi koli spremembami morate raziskati vse prilagoditve, povezane z entiteto, zaradi katerih bi lahko podatki prispeli v slabo stanje. Te prilagoditve je treba obravnavati, preden nadaljujete s kakršnimi koli posodobitvami, povezanimi s podatki.
- Pri identificiranih opravilih, ki so bila zapuščena, razmislite o brisanju teh opravil, če niso potrebna ali če bi morala biti povezana s pravilnim nadrejenim projektom.
- Za vsa opravila, kjer trajanje presega 1.250 dni, razmislite o dodajanju več opravil, ki predstavljajo skupno trajanje, če je izvedljivo.

> [!NOTE]
> Elementi, označeni z zvezdico (\*), so omejeni, ker sistem za upravljanje odnosov s strankami (CRM) podpira le 7.320 ponovitev razširitev. Ostati morate pod to omejitvijo.

## <a name="resource-assignment-relationships"></a>Odnosi dodelitev virov
Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:

- Vse dodelitve virov v strukturirani členitvi dela morajo biti povezane z istim projektom.
- Vse dodelitve virov v strukturirani členitvi dela morajo biti povezane s člani projektne ekipe v istem projektu.

### <a name="potential-mitigation-steps"></a>Možni koraki za ublažitev
- Identificirajte vsa opravila, ki so zunaj zgoraj opisanih pogojev.  
- Vse dodelitve virov, ki niso več veljavne, je treba izbrisati.

## <a name="project-task-dependency-relationships"></a>Odnosi pri odvisnostih projektnega opravila
Če želite zagotoviti uspešno nadgradnjo, morate ustrezno ohraniti naslednje odnose:

- Vse odvisnosti projektnih opravil morajo biti povezane z istim projektom.
- Opravilo ne more imeti več kot enega sklica na odvisnost.
