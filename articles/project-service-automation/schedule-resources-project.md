---
title: Razporejanje virov za projekt
description: Kako razporejati vire za projekt v rešitvi Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755869"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Razporejanje virov za projekt (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Preverite lahko razpoložljivost virov za hiter pregled nad rezerviranostjo vaših virov, lahko pa filtrirate pogled glede na znanja, ekipo, lokacijo in druge možnosti.  
  
Na plošči razporeda je prikazan seznam virov in njihova razpoložljivost. Izberite način pogleda za prikaz razpoložljivosti glede na **Ure**, **Dan**, **Teden** ali **Mesec**.  
  
Preden uporabite ploščo razporeda, je pomembno, da jo nastavite. Za več informacij glejte [Konfiguriranje plošče razporeda (storitve Field Service ali storitve Project Service Automation)](../field-service/configure-schedule-board.md).
  
Če uporabljate starejšo različico, za razpoložljivost virov glejte [Ogled razpoložljivosti virov](../project-service/view-resource-availability.md).  

> [!IMPORTANT]
>  Če želite uporabljati funkcijo rezervacij plošče za načrtovanje, geokodiranje in lokacijske storitve, morate vklopiti zemljevide.  
> 
> 1. V glavnem meniju izberite **Razporejanje virov** > **Skrbništvo**.  
> 2. Kliknite **Parametri razporejanja**.  
> 3. Odprite zapis in se pomaknite navzdol do razdelka **Resource Scheduling Optimization**.  
> 4. V polju **Vzpostavi povezavo z zemljevidi** izberite **Da**.  
> 5. Sprejmite pogoje in shranite zapis.  
> 6. V glavnem meniju izberite **Project Service** > **Plošča razporeda**. Zdaj lahko zahtevo rezervacije ročno razporedite na več načinov. Izberite metodo, ki deluje za vas.
  
## <a name="find-available-resources"></a>Iskanje razpoložljivih virov

1.  Na seznamu **Zahteva rezervacije** z desno tipko miške kliknite nenačrtovano rezervacijo in izberite eno od naslednjih možnosti:  
  
- Če želite poiskati razpoložljiv vir s seznama na plošči razporeda, izberite možnost **Iskanje razpoložljivosti – trenutni viri**.  
- Če želite poiskati razpoložljiv vir med viri, ki so na voljo v sistemu, izberite možnost **Iskanje razpoložljivosti – vsi viri**  
   > [!NOTE]
   >  Ko izberete možnost, se prek filtrov prikažejo možnosti za izbrano zahtevo rezervacije.  
  
2. Ko vidite režo, ki je na voljo, z desno tipko miške kliknite časovni okvir na plošči razporeda in izberite možnost **Rezerviraj tukaj**. Ali pa zahtevo rezervacije povlecite in spustite v časovni okvir, ki je na voljo.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervacija vira prek dnevnega pogleda in iskanje oseb s premalo rezervacijami
  
1.  Na plošči razporeda izberite **Način pogleda** in izberite **Dnevi**.  
  
    Tukaj je prikazan pogled mreže, v katerem je navedeno število ur na dan, ko je vir rezerviran, in so navedeni dnevi, ko je vir prost.  
  
2.  Kliknite ime vira, ki ga želite rezervirati, in nato izberite **Rezerviraj**.  
  
3.  V pogovornem oknu **Rezervacija virov (ustvarjanje)** izberite projekt, za katerega želite rezervirati vir, način rezervacije ter začetni in končni čas rezervacije.  
  
4.  Ko končate, izberite **Rezerviraj**.  
  
## <a name="view-to-the-schedule-board"></a>Ogled plošče razporeda
  
1.  S seznama na dnu izberite nerazporejeno zahtevo rezervacije.  
  
2.  Povlecite zahtevo rezervacije do razpoložljivega vira/časovnega okvira na plošči razporeda.  
  
3.  Ko končate, izberite **Rezerviraj**.  
  
### <a name="additional-resources"></a>Dodatni viri  
 [Priročnik za upravitelje virov](../project-service/resource-manager-guide.md)
