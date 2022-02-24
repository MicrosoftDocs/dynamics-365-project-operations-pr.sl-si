---
title: Nastavitev pravilnikov o stroških
description: Nastavite lahko pravilnike o stroških, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot v aplikaciji Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271283"
---
# <a name="set-up-expense-policies"></a>Nastavitev pravilnikov o stroških

Opredelite lahko pravilnike, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot.         
Izvajanje pravilnikov o stroških vam lahko pomaga učinkovito upravljati stroške.         

Tako lahko na primer nastavite pravilnik za hotelske stroške v New Yorku, ki določa, da strošek na nočitev ne sme presegati 250 USD.       
Če delavec predloži poročilo o stroških ali zahtevo za pot, kjer cena sobe presega ta znesek, sistem obvesti        
delavca, da je bil znesek pravilnika za strošek presežen. Lahko konfigurirate sporočilo, ki ga bo delavec prejel, ko        
opredelite pravilnik.      
        
Opredelite lahko tri vrste pravilnikov:         
        
- Opozorilo – dovoli delavcu, da predloži poročilo o stroških ali zahtevo za pot, vendar bodo stroški označeni za vse odobritelje in        
  za poznejše poročanje.        

- Napaka – od delavca zahteva, da revidira strošek v skladu s pravilnikom, preden predloži poročilo o stroških ali zahtevo za pot.       
 
 - Utemeljitev – zahteva, da delavec ali vodja pred predložitvijo poročila o stroških ali zahteve za pot vnese utemeljitev za preseganje zneska pravilnika.        

## <a name="policy-tips"></a>Nasveti glede pravilnikov
Tu je nekaj predlogov, ki vam lahko pomagajo pri ustvarjanju novih pravilnikov za upravljanje stroškov. 
* Pravilniki veljajo z datumom začetka veljavnosti in ne bodo začel veljati, če je pravilnik ustvarjen z datumom po datumu nastanka stroška. Če na primer danes ustvarite nov pravilnik, s katerim uveljavite največji strošek obroka v višini $50, vsi obstoječi stroški, vneseni do včeraj, ne bodo preverjeni v skladu s tem pravilnikom.
* Pri ustvarjanju pravilnika za kategorijo stroška, ki jo je mogoče razčleniti, razmislite o dodajanju pogoja za vrsto vrstice stroška. Nekateri pravilniki, na primer zahtevanje potrdila, morda niso smiselni za razčlenjene vrstice in se uporabljajo samo za vrstico glave ali nerazčlenjeno vrstico. 
* Pravilniki upravljanja stroškov se privzeto ovrednotijo glede na izvorno entiteto. Za medpodjetniške scenarije lahko nastavite, da se pravilnik namesto tega vrednoti glede na ciljno entiteto (entiteta izposojevalka). Če želite izvajati pravilnike glede na ciljno entiteto, vklopite funkcijo »Ocena pravilnika o stroških glede na pravno osebo izposojevalko« v delovnem prostoru **Upravljanje funkcij**.

## <a name="when-to-evaluate-policies"></a>Kdaj oceniti pravilnike

V parametrih upravljanja stroškov imate možnost, da ocenite pravilnike upravljanja stroškov, ko se vrstica shrani ali ko se predloži poročilo o stroških. Če se odločite, da boste ocenili, ko je vrstica shranjena, s tem zagotovite, da bodo uporabniki prej videli, kaj morajo storiti, da naenkrat izpolnijo poročilo o stroških. V nasprotnem primeru lahko odložite oceno pravilnika in prihranite čas s preverjanjem na koncu med predložitvijo v potek dela.


[!INCLUDE[footer-include](../includes/footer-banner.md)]