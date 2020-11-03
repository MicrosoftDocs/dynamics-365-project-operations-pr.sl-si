---
title: Ustvarjanje ponudb za projekte iz priložnosti
description: V tej temi najdete informacije o ustvarjanju ponudbe za projekt iz priložnosti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084668"
---
# <a name="create-project-quotes-from-opportunities"></a>Ustvarjanje ponudb za projekte iz priložnosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ponudbe je mogoče ustvariti iz priložnosti za projekte na naslednje načine:

- V zavihku **Ponudbe** na strani **Priložnost za projekt**
- Iz poteka prodajnega postopka za priložnost
- S posodobitvijo sklica priložnosti pri obstoječi ponudbi

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>V zavihku Ponudbe na strani Priložnost za projekt

Če želite iz priložnosti ustvariti ponudbo za projekt, upoštevajte naslednje korake.

1. Odprite stran **Priložnost za projekt** in izberite zavihek **Ponudbe**. 
2. Na podmreži **Ponudbe** izberite **+** , da na podlagi priložnosti ustvarite ponudbo za nov projekt. Vse vrstice priložnosti in z njimi povezani ceniki za projekte se kopirajo v novo ponudbo iz priložnosti.

## <a name="from-the-opportunity-sales-process-flow"></a>Iz poteka prodajnega postopka za priložnost

Če želite iz poteka prodajnega postopka za priložnost ustvariti ponudbo, upoštevajte naslednje korake.

1. Pri poteku prodajnega postopka za priložnost odprite priložnost.
2. Izberite stopnjo **Potrdi**. 
3. Izberite **Naprej** in nato izberite **+ Ustvari** , da ustvarite novo ponudbo. Večina informacij na zavihku **Povzetek** za to novo ponudbo bo privzeto nastavljenih prek priložnosti. 
4. Vnesite morebitne zahtevane podatke, ki manjkajo, ali po potrebi posodobite privzete vrednosti na zavihku **Povzetek**.
5. Izberite **Shrani**. Nova ponudba se ustvari in poveže s priložnostjo. Zdaj si lahko ogledate podatke o ponudbi na zavihku **Ponudbe** na strani **Priložnost**. 

   Prodajni postopek za priložnost preide na naslednjo stopnjo: **Predlagaj**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>S posodobitvijo sklica priložnosti pri obstoječi ponudbi

Obstoječo ponudbo lahko povežete s priložnostjo. Upoštevajte naslednje korake za posodobitev podatkov o priložnosti pri obstoječi ponudbi.

1. Odprite stran **Ponudba** in izberite zavihek **Povzetek**.
2. V polju **Priložnost** izberite priložnost, ki jo želite povezati s ponudbo. Ponudbo si lahko ogledate na mreži **Ponudbe** priložnosti. 
3. S prodajnim postopkom za priložnost lahko priložnost premaknete na naslednjo stopnjo: **Predlagaj**. 

   Ko priložnost premaknete na to stopnjo, lahko to ponudbo izberete s seznama ponudb, povezanih s to priložnostjo. Izbira te ponudbe pomeni, da jo boste v nadaljevanju postopka uporabljali še naprej.

   Vse druge ponudbe, povezane s priložnostjo, bodo še vedno na voljo in bodo aktivne, dokler ne pridobite ene od njih. Prodajni postopek lahko premaknete nazaj na prejšnjo stopnjo **Potrdi** in izberete drugo ponudbo, s katero želite nadaljevati.
