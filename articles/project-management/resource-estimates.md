---
title: Ocene virov
description: Ta tema vsebuje informacije o načinu izračuna ocene virov v storitvi Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928608"
---
# <a name="resource-estimates"></a>Ocene virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ocene virov izhajajo iz časovno razporejenega dela, ki je opredeljeno v strukturirani členitvi dela skupaj z veljavnimi razsežnostmi cen. Običajno je izračun naslednji: **hitrost/uro za vsako vlogo X število ur.** Časovno razporejeno delo za vsak vir je shranjeno v zapisu o dodelitvi vira. Cene so shranjene v vnaprej določenem ceniku. Pretvorba enot se uporablja na podlagi veljavnega cenika.

![Ocene virov](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Privzeta lastna cena in valuta cene

Lastne cene so privzeto nastavljene iz organizacijske enote.

## <a name="default-bill-rate-and-sales-currency"></a>Privzeti delež obračunavanja stroškov in valuta prodaje

Prodajne cene se uporabijo enkrat na posel. Hierarhija privzeto nastavljenega prodajnega cenika je naslednja:

1. Organizacija
2. Stranki
3. Ponudba/pogodba
