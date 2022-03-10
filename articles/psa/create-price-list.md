---
title: Ustvarjanje cenika
description: Navodila za ustvarjanje cenika v rešitvi Project Service
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 049b36beed34ada5758d47a40a1126e0599e23e50afac83eb7ef0e37daaaaa65
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990921"
---
# <a name="create-a-price-list-project-service"></a>Ustvarjanje cenika (rešitev Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ceniki zagotavljajo predlogo, ki jo upravitelji kupcev lahko uporabijo za ustvarjanje ponudb in projektov ter določanje stroškov projekta. Zagotavljajo vrstični seznam vlog in stroškov s pripadajočimi cenami, ki jih boste zaračunali. Ustvarite lahko več cenikov, da lahko tako vzdržujete ločene cenovne strukture za različne regije, v katerih prodajate izdelke, ali različne prodajne kanale. Priporočamo, da ustvarite vsaj en cenik za vsako valuto, v kateri nameravate strankam izdajati račune.  
  
Če želite ustvariti finančne ocene za delo, ki bo opravljeno, poskrbite, da ima vsak projekt osnovni cenik stroškov in prodajnih cen. Nastavite privzeti cenik stroškov in prodaje, ki se uporablja za vse projekte, ustvarjene v organizaciji.  
  
Ceniki temeljijo na vlogah in kategorijah stroškov, zato poskrbite, da že pred ustvarjanjem cenika konfigurirate vloge in kategorije stroškov, ki jih želite uporabiti pri ustvarjanju cenika.  
  
1.  Odprite **Project Service > Ceniki**.  
  
2.  Kliknite **Novo**.  
  
3.  V polju **Kontekst** izberite kategorijo cenika: **Stroški**, **Nakup** ali **Prodaja**.  
  
4.  V polje **Ime** vnesite ime cenika.  
  
5.  V polju **Valuta** izberite valuto, ki jo boste uporabljali za obračunavanje ali razčlenitev stroškov.  
  
6.  V polju **Časovna enota** določite časovno obdobje, za katerega velja cena, npr. dan ali ura.  
  
7.  Vnesite **Začetni datum**, **Končni datum** in **Opis**.  
  
8.  Kliknite **Shrani**, da ustvarite zapis, ki ga nato lahko urejate.  
  
9. Če želite na cenik dodati ceno vloge, kliknite **+** v razdelku **Cene vlog**.  
  
10. V podoknu **Cena vloge** vnesite podrobnosti in nato kliknite **Shrani**. Po potrebi dodajate druge cene vlog. Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.  
  
11. Če želite na cenik dodati ceno kategorije stroška, kliknite **+** v razdelku **Cene kategorij**.  
  
12. V podoknu **Cena kategorije transakcije** vnesite podrobnosti in nato kliknite **Shrani**. Po potrebi dodajajte druge cene kategorij. Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.  
  
13. Če želite ceniku dodati elemente cenika, kliknite **+** v razdelku **Elementi cenika**.  
  
14. V podoknu **Elementi cenika** vnesite podrobnosti in nato kliknite **Shrani**. Po potrebi dodajate druge elemente cenika. Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.  
  
15. Če želite ceniku dodati odnose področja, kliknite **+** v razdelku **Odnosi področja**.  
  
16. V oknu **Nova povezava** vnesite podrobnosti in nato kliknite **Shrani**. Po potrebi dodajate druge odnose področja. Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.  
  
### <a name="see-also"></a>Glejte tudi  
 [Konfiguracija storitve Project Service Automation](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]