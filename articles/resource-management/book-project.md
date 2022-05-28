---
title: Rezervacija v projekt
description: Ta tema vsebuje informacije o tem, kako rezervirati vir v projekt.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591409"
---
# <a name="book-to-a-project"></a>Rezervacija v projekt

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Včasih mora vodja projektov ali upravitelj virov dodeliti vir projektu, ne da bi bila določena posebna zahteva splošnega člana ekipe. To lahko dosežete na enega od treh načinov.

- Dodajanje rezervacij na mreži člana ekipe
- Dodajanje rezervacij na plošči razporeda
- Dodajanje rezervacij iz obrazca **projekta**

## <a name="book-from-the-team-member-grid"></a>Dodajanje rezervacij na mreži člana ekipe

Če vaša organizacija deluje v hibridnem načinu dodeljevanja virov, lahko upravitelj projekta vir rezervira neposredno v projekt tako, da izvede naslednje korake.

1. V projektu pojdite na mrežo članov ekipe in izberite možnost **Novo**.
2. Določite ime položaja in vlogo vira.
3. S seznama izberite vir, ki ga je mogoče rezervirati.
4. Ko izberete vir, določite vrednosti za naslednja polja, da ga rezervirate:

    - Začetni datum
    - Datum zaključka
    - Način dodelitve
    - Ure, če je primerno
    - Odobritelj projekta

6. Izberite možnost **Shrani in zapri**.

## <a name="book-from-the-schedule-board"></a>Dodajanje rezervacij na plošči razporeda

Kadar mora upravitelj virov vir rezervirati neposredno v projekt, lahko uporabi ploščo razporeda in zahtevo za projekt. Zahteva projekta je zahteva za vire, katero je vedno mogoče rezervirati. Za rezervacijo vira neposredno v obrazec projekta na plošči razporeda dokončajte spodnje korake.

1. Pomaknite se do plošče razporeda in na levi strani filtrirajte vire, ki so primerni za zahtevo.
2. V spodnjem podoknu izberite zavihek **Projekt** za ogled seznama projektnih zahtev.
3. Povlecite zahtevo na vir in določite vrednost naslednjih podatkov:

    - Datum začetka
    - Datum zaključka
    - Stanje rezervacije
    - Način rezervacije
    - Trajanje
   
   > [!NOTE]
   > trenutno Dynamics 365 Project Operations ne podpira razporedne plošče.   

## <a name="book-from-the-project-form"></a>Dodajanje rezervacij iz obrazca projekta

Kot vodja projekta boste morda morali rezervirati vir za projekt, za katerega poznate le merila, ne pa tudi imena. Dokončajte naslednje korake, če želite s pomočjo pomočnika za razporejanje poiskati vir na podlagi katerih koli razpoložljivih atributov vira. 

1. Pomaknite se do projekta in izberite možnost **Rezerviraj**, da odprete pomočnika za razporejanje.
2. S filtri na levi strani pomočnika za razporejanje zožite merila in izberite možnost **Išči.**
3. Na podlagi virov, vrnjenih v rezultatih iskanja, lahko rezervirate vir.

> [!NOTE]
> Ta način ne ustvari nobenih rezervacij za vir. Namesto tega je vir dodan v ekipo. Potem ko je član ekipe dodan v projekt, lahko vodja projekta z vzdrževanjem rezervacij ali podaljšanjem rezervacij doda zahtevane rezervacije v vir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
