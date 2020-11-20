---
title: Opredelitev pravilnikov o stroških
description: Opredelite lahko pravilnike o stroških, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128438"
---
# <a name="define-expense-policies"></a>Opredelitev pravilnikov o stroških

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Opredelite lahko pravilnike, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot.         
Izvajanje pravilnikov o stroških vam lahko pomaga učinkovito upravljati stroške.         

Tako lahko na primer nastavite pravilnik za hotelske stroške v New Yorku, ki določa, da strošek na nočitev ne sme presegati 250 USD.       
Če delavec predloži poročilo o stroških ali zahtevo za pot, kjer cena sobe presega ta znesek, sistem obvesti         
delavca, da je bil znesek pravilnika za strošek presežen. Lahko konfigurirate sporočilo, ki ga bo delavec prejel, ko        
opredelite pravilnik.      
        
Opredelite lahko tri vrste pravilnikov:         
        
- **Opozorilo**: dovoli delavcu, da predloži poročilo o stroških ali zahtevo za pot, vendar bodo stroški označeni za vse odobritelje in         
  za poznejše poročanje.        

- **Napaka**: od delavca zahteva, da revidira strošek v skladu s pravilnikom, preden predloži poročilo o stroških ali zahtevo za pot.        
 
 - **Utemeljitev**: zahteva, da delavec ali vodja pred predložitvijo poročila o stroških ali zahteve za pot vnese utemeljitev za preseganje zneska pravilnika.        

## <a name="policy-tips"></a>Nasveti glede pravilnikov
Tu je nekaj predlogov, ki vam lahko pomagajo pri ustvarjanju novih pravilnikov za upravljanje stroškov: 

- Pravilniki veljajo z datumom začetka veljavnosti, kar pomeni, da pravilnik ne bo začel veljati, če bo ustvarjen z datumom po datumu nastanka stroška. Na primer, danes ustvarite nov pravilnik, s katerim uveljavite največji strošek obroka v višini 50 $. Vsi obstoječi stroški, vneseni do včeraj, ne bodo preverjeni v skladu s tem pravilnikom.
- Pri ustvarjanju pravilnika za kategorijo stroška, ki jo je mogoče razčleniti, razmislite o dodajanju pogoja za vrsto vrstice stroška. Nekateri pravilniki, na primer zahtevanje potrdila, morda niso smiselni za razčlenjene vrstice. V tem primeru se pravilnik uporablja samo za vrstico glave ali nerazčlenjeno vrstico. 
- Pravilniki upravljanja stroškov se privzeto ovrednotijo glede na izvorno entiteto. Za medpodjetniške scenarije lahko nastavite, da se pravilnik namesto tega vrednoti glede na ciljno entiteto (entiteta izposojevalka). Če želite izvajati pravilnike glede na ciljno entiteto, vklopite funkcijo **Ocena pravilnika o stroških glede na pravno osebo izposojevalko** v delovnem prostoru **Upravljanje funkcij**.

## <a name="when-to-evaluate-policies"></a>Kdaj oceniti pravilnike

V parametrih upravljanja stroškov lahko izberete, da ocenite pravilnike upravljanja stroškov, ko se vrstica shrani ali ko se predloži poročilo o stroških. Če se odločite, da boste ocenili, ko je vrstica shranjena, bodo uporabniki prej videli, kaj morajo storiti, da naenkrat izpolnijo poročilo o stroških. V nasprotnem primeru lahko odložite oceno pravilnika in prihranite čas s preverjanjem na koncu med predložitvijo v potek dela.
