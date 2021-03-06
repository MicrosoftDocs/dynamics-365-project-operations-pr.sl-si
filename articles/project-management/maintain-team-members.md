---
title: Vzdrževanje članov ekipe
description: Ta tema vsebuje informacije o rezervaciji poimenovanih virov projektne ekipe in njihovi dodelitvi opravilom.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961949"
---
# <a name="maintain-team-members"></a>Vzdrževanje članov ekipe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Poimenovani vir lahko v projektno ekipo dodate tako, da ga neposredno rezervirate v ekipi.

1. V storitvi Dynamics 365 Project Operations odprite možnost **Projekti**in odprite projekt, za katerega želite izvesti rezervacijo.
2. Na strani **Projekt** na zavihku **Ekipa** izberite **Novo**. 
3. V pogovornem oknu **Hitro ustvarjanje člana projektne ekipe** izberite vir, ki ga je mogoče rezervirati. Polje **Vloga** bo izpolnjeno s privzeto vlogo vira, če ima dodeljeno. Vlogo lahko spremenite. 
4. Izberite začetni in končni datum obdobja, v katerem potrebujete vir, in izberite način dodeljevanja zmogljivosti vira. 
5. V polju **Odobritelj projekta** izberite **Da**, če želite članu ekipe dodeliti vlogo odobritelja projekta. Član ekipe bo tako lahko odobril poslane časovne vnose in vnose stroškov za ta projekt. 
6. Izberite **Shrani**.

Rezervirani vir lahko sedaj dodelite opravilom za projekt. Na strani **Projekt** na zavihku **Razpored** dodelite opravila novemu viru. V polju **Viri** na mreži opravil se odpre izbirnik za vire, v katerem so prikazani člani ekipe, ki jih lahko izberete.


V storitvi Project Operations rezervacije virov in dodelitve opravil niso tesno povezane. Pri uporabi izbirnika virov v razporedu lahko članom ekipe dodelite opravila za več ur, kot jih je zajetih v rezervacijah za projekt.

Razlike med rezervacijami in dodelitvami članov ekipe so prikazane na zavihkih **Ekipa** in **Uskladitev virov**. Razlike med rezervacijami in dodelitvami virov lahko tudi uskladite na podrobnejši ravni.

Izbirnik za vire na zavihku **Razpored** lahko uporabite za iskanje in izbiro virov, ki jih je mogoče rezervirati, vendar še niso del projektne ekipe. Ti viri so v izbirniku virov prikazani kot **Drugi viri**.

Ko opravite izbor, je vir dodan projektni ekipi in dodeljen opravilu, vendar se pri tem ne ustvari rezervacija.

Za rezervacijo zmogljivosti vira za projekt lahko uporabite funkcijo razširjanja rezervacij na zavihku **Uskladitev** ali **ploščo razporeda**.

Ko je član ekipe rezerviran za vaš projekt, lahko uporabite možnost **Upravljanje rezervacij** ali **Plošča razporeda** ter neposredno urejate njegove rezervacije.
