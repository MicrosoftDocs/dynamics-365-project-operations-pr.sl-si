---
title: Razporejanje virov za projekt
description: Kako razporejati vire za projekt v rešitvi Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150463"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Razporejanje virov za projekt (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Preverite lahko razpoložljivost virov za hiter pregled nad rezerviranostjo vaših virov, lahko pa filtrirate pogled glede na znanja, ekipo, lokacijo in druge možnosti.  
  
Na plošči razporeda je prikazan seznam virov in njihova razpoložljivost. Izberite način pogleda za prikaz razpoložljivosti glede na **Ure**, **Dan**, **Teden** ali **Mesec**.  
  
Preden uporabite ploščo razporeda, je pomembno, da jo nastavite. Za več informacij glejte [Konfiguriranje plošče razporeda (storitve Field Service ali storitve Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Če uporabljate starejšo različico, za razpoložljivost virov glejte [Ogled razpoložljivosti virov](../psa/view-resource-availability.md).  

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
 [Priročnik za upravitelje virov](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]