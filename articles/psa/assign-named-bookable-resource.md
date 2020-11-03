---
title: Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil
description: Ta tema vsebuje informacije o rezervaciji poimenovanih virov projektne ekipe in njihovi dodelitvi opravilom.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084875"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Poimenovan vir lahko v projektno ekipo lahko dodate tako, da ga neposredno rezervirate v ekipi. Pri tem upoštevajte spodnja navodila.

1. V aplikaciji Project Service Automation odprite možnost **Projekti** in odprite projekt, za katerega želite izvesti rezervacijo.
2. Na strani **Projekt** na zavihku **Ekipa** kliknite **Novo**. 

![Dodajanje člana ekipe na zavihku ekipe](media/RM-how-to-1.png)

3. V pogovornem oknu **Hitro ustvarjanje člana projektne ekipe** izberite vir, ki ga je mogoče rezervirati. Polje **Vloga** bo izpolnjeno s privzeto vlogo vira, če ima dodeljeno. Po potrebi lahko vlogo tudi spremenite. 
4. Izberite začetni in končni datum obdobja, v katerem potrebujete vir, in izberite način dodeljevanja zmogljivosti vira. 
5. Če želite, da je član ekipe odobritelj projekta, v polju možnosti **Odobritelj projekta** izberite **Da**. To pomeni, da lahko član ekipe odobri poslane časovne vnose in vnose stroškov za ta projekt. 
6. Kliknite **Shrani**.

![Dodajanje člana ekipe v obrazcu za hitro ustvarjanje](media/RM-how-to-2.png)


Rezervirani vir lahko sedaj dodelite opravilom za projekt. Na strani **Projekt** kliknite zavihek **Razpored** in dodelite opravila novemu viru. V polju **Viri** na mreži opravil se odpre izbirnik za vire, v katerem so prikazani člani ekipe, ki jih lahko izberete.

![Dodeljevanje člana ekipe opravilu na zavihku razporeda](media/RM-how-to-3.png)

V tretji različici aplikacije Project Service Automation (PSA) rezervacije virov in dodelitve opravil niso tesno povezane. To pomeni, da lahko pri uporabi izbirnika virov v razporedu članom ekipe dodelite opravila za več ur, kot jih je zajetih v rezervacijah za projekt.
Razlike med rezervacijami in dodelitvami člana ekipe lahko vidite na zavihku **Ekipa** ali na zavihku **Uskladitev virov**. Razlike med rezervacijami in dodelitvami virov lahko uskladite tudi na ravni s več podrobnostmi.

![Zavihek za uskladitev virov](media/RM-how-to-4.png)

Izbirnik za vire na zavihku **Razpored** lahko uporabite tudi za iskanje in izbiro virov, ki jih je mogoče rezervirati, vendar še niso del projektne ekipe. Ti so prikazani v izbirniku virov prikazani kot **Drugi viri**.

![Dodeljevanje vira, ki ni član ekipe, za opravilo](media/RM-how-to-5.png)

Ko to naredite, je vir dodan projektni ekipi in dodeljen opravilu, vendar se pri tem ne ustvari rezervacija.

![Član ekipe z dodelitvami in brez rezervacij](media/RM-how-to-6.png)

Za rezervacijo zmogljivosti vira za projekt lahko uporabite funkcijo razširjanja rezervacij na zavihku **Uskladitev** ali **ploščo razporeda**.

![Razširjanje rezervacij za člana ekipe na zavihku za uskladitev virov](media/RM-how-to-7.png)

Ko je član ekipe rezerviran za vaš projekt, lahko uporabite možnost »Upravljanje rezervacij« ali ploščo razporeda ter neposredno urejate njegove rezervacije.
