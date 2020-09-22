---
title: Izklop cenovne razsežnosti
description: Ta tema vsebuje informacije o tem, kako nastavite cenovne razsežnosti v rešitvi Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755834"
---
# <a name="turn-off-a-pricing-dimension"></a>Izklop cenovne razsežnosti

Morda boste morali vsakih nekaj let pregledati in posodobiti strategijo za oblikovanje cen. Vsaka izvedena posodobitev lahko zahteva, da izklopite obstoječo cenovno razsežnost in ustvarite novo. Prej ste morda na primer oblikovali ceno po elementu **Vloga**, zdaj pa ste se odločili, da boste oblikovali ceno po elementu **Delovne izkušnje**. Zaradi tega boste morda morali izklopiti element **Vloga** kot cenovno razsežnost in ustvariti **Delovne izkušnje** kot novo cenovno razsežnost. 

Cenovno razsežnost lahko izklopite tako, da polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** nastavite na **Ne**, ne glede na to, ali je cenovna razsežnost vnaprej pripravljena ali ustvarjena po meri.

Po tem se vam bo morda prikazalo to sporočilo o napaki.

![Napaka v poslovnem procesu, ki se lahko pojavi ob izklopu cenovne razsežnosti](media/Business-Process-Error.png)


To sporočilo o napaki pomeni, da obstajajo zapisi cen, ki so bili predhodno nastavljeni za razsežnost, ki jo želite izklopiti. Vse zapise **Cena vloge** in **Pribitki na ceno vloge**, ki se sklicujejo na razsežnost, je treba izbrisati, preden lahko uporabnost razsežnosti nastavite na **Ne**. To pravilo velja tako za vnaprej pripravljene cenovne razsežnosti kot za vse cenovne razsežnosti po meri, ki ste jih morda ustvarili. To preverjanje je potrebno zato, ker ima rešitev Project Service omejitev, zaradi katere mora imeti vsak zapis **Cena vloge** edinstveno kombinacijo razsežnosti. Na ceniku, imenovanem **Stroški v ZDA, 2018**, so naslednje vrstice **Cena vloge**. 

| Standardni naziv         | Organizacijska enota    |Enota   |Cena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemski inženir|Contoso, ZDA|Ura| 100|USD|
| Višji sistemski inženir|Contoso, ZDA|Ura| 150| USD|


Če izklopite **Standardni naziv** kot cenovno razsežnost, bo mehanizem za izračunavanje cen rešitve Project Service pri iskanju cene uporabil le vrednost **Organizacijska enota** iz konteksta vnosa. Če je **Organizacijska enota** za kontekst vnosa »Contoso, ZDA«, rezultata ne bo mogoče določiti, saj se bosta obe vrstici ujemali. Če se želite izogniti temu, naredite naslednje: ko ustvarite zapise **Cena vloge**, rešitev Project Service potrdi, da je kombinacija razsežnosti edinstvena. Če razsežnost po ustvarjanju zapisov **Cena vloge** izklopite, je to omejitev mogoče zaobiti. Zato morate pred izklopom razsežnosti izbrisati vse vrstice **Cena vlog** in **Pribitek na ceno vloge**, ki imajo izpolnjeno to vrednost razsežnosti.

