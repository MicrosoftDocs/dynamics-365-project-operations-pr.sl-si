---
title: Odstranjevanje projektne ocene
description: Ta tema vsebuje informacije o odstranjevanju projektne ocene, ko je ta končana.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684110"
---
# <a name="eliminate-a-project-estimate"></a>Odstranjevanje projektne ocene

[!include [banner](../includes/banner.md)]

Projektne ocene omogočajo finančni pregled za predvideno in načrtovano delo za projekt. Če želite delati z ocenami za projekt, morate projekt priložiti projektni oceni. Projektna ocena vedno temelji na obstoječem projektu, vendar se lahko več projektov nanaša na eno samo projektno oceno. Projektnim ocenam je mogoče priložiti samo projekte s fiksno ceno in naložbene projekte, ki morajo pripadati isti projektni skupini kot projektna ocena.

Če želite odpraviti projektno ocena, mora biti ta popolna. Spodnji koraki pojasnjujejo, kako odpraviti oceno.

1. Odprite **Vodenje projekta in računovodstvo** > **Vsi projekti** in odprite projekt. 
2. V zavihku **Upravljanje** izberite **Ocene** in na strani **Oceni** izberite **Odpravi**.
3. Na strani **Odpravi oceno** v zavihku **Splošno** nastavite naslednje možnosti:

   - **Koda obdobja**: izberite kodo obdobja, da izberete ustrezne projektne ocene. 
   - **Predvideni datum**: izberite ustrezen predvideni datum za odstranjevanje.
   - **Odstranjevanje z opozorili WIP**: izberite to možnost, da omogočite obveščanje, ko bo odstranjena ocena, ki je povezana z delom v teku (WIP). Če ta možnost ni omogočena, se odpravljanje ne bo nadaljevalo, če obstajajo kakršne koli neocenjene transakcije. 
   > [!NOTE]
   > Ta možnost je na voljo samo, če se odpravljanje uporabi za projektno oceno. Funkcija ni na voljo, če uporabljate periodično knjiženje. Ta nastavitev začne delovati, če jo nastavite v zavihku **Ocena** na strani **Projektni parametri** v skupini polj **Dovoli odpravljanje v primeru neocenjenih transakcij**.
   - **Nastavi stopnjo na končano**: omogočite to možnost, da nastavite stopnjo projektne ocene na **Končano** po izvedbi odstranjevanja.
   - **Natisni seznam ocen**: izberite informacije, ki jih želite vključiti pri tiskanju seznama ocen.
   - **Pokaži dnevnik podatkov**: omogočite to možnost za prikaz dnevnika podatkov.
   - **Datum knjiženja**: izberite datum knjiženja ocene v glavni knjigi.

4.  Izberite **V redu**.
5. Po zaključku postopka odstranjevanja se odstranjena projektna ocena prikaže z negativno vrednostjo. 

Če ocene niste nameravali odstraniti, jo lahko izberete in kliknete **Povrni postopek odstranjevanja**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]