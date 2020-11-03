---
title: Izklop cenovne razsežnosti
description: Ta tema vsebuje informacije o tem, kako izklopiti cenovne razsežnosti.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a7c91ef70b1dd3697f6a8b5044c6ad4a14c4e74
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084852"
---
# <a name="turning-off-a-pricing-dimension"></a>Izklop cenovne razsežnosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Morda boste morali vsakih nekaj let pregledati in posodobiti strategijo za oblikovanje cen. Vsaka izvedena posodobitev lahko zahteva, da izklopite obstoječo cenovno razsežnost in ustvarite novo. Prej ste morda na primer oblikovali ceno po elementu **Vloga** , zdaj pa ste se odločili, da boste oblikovali ceno po elementu **Delovne izkušnje**. Zaradi tega boste morda morali izklopiti element **Vloga** kot cenovno razsežnost in ustvariti **Delovne izkušnje** kot novo cenovno razsežnost. 

Cenovno razsežnost lahko izklopite tako, da polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** nastavite na **Ne** , ne glede na to, ali je cenovna razsežnost vnaprej pripravljena ali ustvarjena po meri.

Ko pa to storite, boste morda prejeli sporočilo o napaki **Cenovne razsežnosti ni mogoče posodobiti ali izbrisati, če obstajajo povezani zapisi cen**.

To sporočilo o napaki pomeni, da obstajajo zapisi cen, ki so bili predhodno nastavljeni za razsežnost, ki jo želite izklopiti. Vse zapise **Cena vloge** in **Pribitki na ceno vloge** , ki se sklicujejo na razsežnost, je treba izbrisati, preden lahko uporabnost razsežnosti nastavite na **Ne**. To pravilo velja tako za vnaprej pripravljene cenovne razsežnosti kot za vse cenovne razsežnosti po meri, ki ste jih morda ustvarili. To preverjanje je potrebno zato, ker mora imeti vsak zapis **Cena vloge** edinstveno kombinacijo razsežnosti. Na ceniku, imenovanem **Stroški v ZDA, 2018** , so naslednje vrstice **Cena vloge**. 

| Standardni naziv         | Organizacijska enota    |Enota   |Cena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemski inženir|Contoso, ZDA|Ura| 100|USD|
| Višji sistemski inženir|Contoso, ZDA|Ura| 150| USD|


Če izklopite **Standardni naziv** kot cenovno razsežnost, bo mehanizem za izračunavanje cen pri iskanju cene uporabil le vrednost **Organizacijska enota** iz konteksta vnosa. Če je **Organizacijska enota** za kontekst vnosa »Contoso, ZDA«, rezultata ne bo mogoče določiti, saj se bosta obe vrstici ujemali. Če se želite izogniti temu, naredite naslednje: ko ustvarite zapise **Cena vloge** , sistem potrdi, da je kombinacija razsežnosti edinstvena. Če razsežnost po ustvarjanju zapisov **Cena vloge** izklopite, je to omejitev mogoče zaobiti. Zato morate pred izklopom razsežnosti izbrisati vse vrstice **Cena vlog** in **Pribitek na ceno vloge** , ki imajo izpolnjeno to vrednost razsežnosti.
