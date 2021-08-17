---
title: Izklop cenovne razsežnosti
description: Ta tema vsebuje informacije o tem, kako nastavite cenovne razsežnosti v rešitvi Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9f690dfdb40e962ef329f323716f3f755493805d764dbfaa2d4f9d042231cee7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006806"
---
# <a name="turn-off-a-pricing-dimension"></a>Izklop cenovne razsežnosti

[!include [banner](../includes/psa-now-project-operations.md)]

Morda boste morali vsakih nekaj let pregledati in posodobiti strategijo za oblikovanje cen. Vsaka izvedena posodobitev lahko zahteva, da izklopite obstoječo cenovno razsežnost in ustvarite novo. Prej ste morda na primer oblikovali ceno po elementu **Vloga**, zdaj pa ste se odločili, da boste oblikovali ceno po elementu **Delovne izkušnje**. Zaradi tega boste morda morali izklopiti element **Vloga** kot cenovno razsežnost in ustvariti **Delovne izkušnje** kot novo cenovno razsežnost. 

Cenovno razsežnost lahko izklopite tako, da polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** nastavite na **Ne**, ne glede na to, ali je cenovna razsežnost vnaprej pripravljena ali ustvarjena po meri.

Po tem se vam bo morda prikazalo to sporočilo o napaki.

![Napaka v poslovnem procesu, ki se lahko pojavi ob izklopu cenovne razsežnosti.](media/Business-Process-Error.png)


To sporočilo o napaki pomeni, da obstajajo zapisi cen, ki so bili predhodno nastavljeni za razsežnost, ki jo želite izklopiti. Vse zapise **Cena vloge** in **Pribitki na ceno vloge**, ki se sklicujejo na razsežnost, je treba izbrisati, preden lahko uporabnost razsežnosti nastavite na **Ne**. To pravilo velja tako za vnaprej pripravljene cenovne razsežnosti kot za vse cenovne razsežnosti po meri, ki ste jih morda ustvarili. To preverjanje je potrebno zato, ker ima rešitev Project Service omejitev, zaradi katere mora imeti vsak zapis **Cena vloge** edinstveno kombinacijo razsežnosti. Na ceniku, imenovanem **Stroški v ZDA, 2018**, so naslednje vrstice **Cena vloge**. 

| Standardni naziv         | Organizacijska enota    |Enota   |Cena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemski inženir|Contoso US|Ura| 100|USD|
| Višji sistemski inženir|Contoso US|Ura| 150| USD|


Če izklopite **Standardni naziv** kot cenovno razsežnost, bo mehanizem za izračunavanje cen rešitve Project Service pri iskanju cene uporabil le vrednost **Organizacijska enota** iz konteksta vnosa. Če je **Organizacijska enota** za kontekst vnosa »Contoso ZDA«, rezultata ne bo mogoče določiti, saj se bosta obe vrstici ujemali. Če se želite izogniti temu, naredite naslednje: ko ustvarite zapise **Cena vloge**, rešitev Project Service potrdi, da je kombinacija razsežnosti edinstvena. Če razsežnost po ustvarjanju zapisov **Cena vloge** izklopite, je to omejitev mogoče zaobiti. Zato morate pred izklopom razsežnosti izbrisati vse vrstice **Cena vlog** in **Pribitek na ceno vloge**, ki imajo izpolnjeno to vrednost razsežnosti.



[!INCLUDE[footer-include](../includes/footer-banner.md)]