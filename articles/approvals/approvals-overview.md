---
title: Pregled odobritev
description: Ta tema vsebuje informacije o delu z odobritvami v aplikaciji Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084616"
---
# <a name="approvals-overview"></a>Pregled odobritev

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Oddaje za čas in stroške se dodeljujejo prek potek dela za odobritev. Po odobritvi vnosov se transakcije zabeležijo v dejanske vrednosti ali pa se v urnik vpiše čas.

## <a name="approvals-workflow"></a>Potek dela za odobritve
Ko ustvarite in oddate vnos časa ali stroškov, se ustvari vnos odobritve. Odobritelj projekta ali vaš upravitelj pregleda in odobri vaš vnos. Če je vnos povezan s projektom, bodo po odobritvi ustvarjene dejanske vrednosti. To omogoča sledenje stroškom in obračunom. 

## <a name="approve-an-entry"></a>Odobritev vnosa
Obrazec za **odobritve** omogoča preklapljanje med različnimi pogledi, tako da si lahko ogledate različne vrste odobritev.
  
1. Na obrazec **Odobritve** izberite možnost **Stroški** , **Čas** ali **Preklic**.
2. Preglejte vsako odobritev in izberite tiste, ki jih želite odobriti.
3. Izberite možnost **Odobri** za odobritev izbranih vnosov.
V sistemu bodo vnosi obdelani in ustvarjene bodo dejanske vrednosti ali rezervacije.

## <a name="reject-an-entry"></a>Zavrnitev vnosa
Kot odobritelj projekta boste morda morali uporabniku poslati vnos v popravek.
  
1. Na obrazcu **Odobritve** izberite vnos, ki ga želite zavrniti. 
2. Izberite možnost **Zavrni**.
3. Neobvezno – dodajte komentar v pogovorno okno **Komentarji ob zavrnitvi** , ki uporabnika obvesti o razlogu za zavrnitev.
4. Izberite **V redu**. Vnos bo vrnjen uporabniku.
  
## <a name="recall-entries"></a>Preklic vnosov
Enkrat boste morda morali preklicati oddani vnos. Če vnos ni odobren, je takoj vrnjen. Odobreni vnos pa ima lahko pomemben vpliv. Odobritelj projekta mora odobriti odpoklic, da bo storniral transakcijo v dejanskih vrednostih.

## <a name="specify-project-approvers"></a>Določitev odobriteljev projekta
Vsak projekt ima več članov projektne skupine. Določite lahko, kdo od članov ekipe je tudi odobritelj projekta.

1. Na obrazcu **Projekti** s seznama odprite projekt.
2. Na zavihku **Ekipa** izberite člana ekipe, ki bo odobritelj projekta, in nato izberite možnost **Uredi**.
3. Polje **Odobritelj projekta** nastavite na možnost **Da**.
4. Izberite **Shrani**.
5. Ponovite drugi, tretji in četrti korak, da dodate dodatne odobritelje projekta.

## <a name="configure-the-users-manager"></a>Konfiguracija upravitelja izbranega uporabnika

1. Odprite **Nastavitve** > **Varnost** > **Uporabniki**.
2. Izberite uporabnika, ki mu želite dodeliti upravitelja, in v območju **Podatki o organizaciji** s seznama izberite upravitelja. 
3. Izberite **Shrani**.


