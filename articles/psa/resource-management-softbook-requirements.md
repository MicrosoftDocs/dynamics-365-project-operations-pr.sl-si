---
title: Zahtevani pogoji za začasne rezervacije
description: Ta članek vsebuje informacije o tem, kako začasno rezervirati zahtevane pogoje.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8192047639823bc594803d6d10759be28f6db3ed
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928958"
---
# <a name="soft-book-requirements"></a>Zahtevani pogoji za začasne rezervacije

[!include [banner](../includes/psa-now-project-operations.md)]

Rezervacije zahtevanih pogojev za vir je mogoče potrditi. S potrjeno rezervacijo ustvarite predlog, ki porabi del zmogljivosti vira. Predlog se nato pošlje nazaj prosilcu za odobritev. Začasna rezervacija pogojno doda vir v projektno ekipo in ima drugačno stanje na plošči razporeda, vendar ne porabi zmogljivosti vira. Če želite vir s plošče razporeda začasno rezervirati, nastavite polje **Stanje rezervacije** na **Začasno**.

![Stanje rezervacije je nastavljeno na »Začasno«.](media/Resource-Management-image77.png)

Ko je zavihek **Ekipa** v pogledu **Poimenovani člani ekipe**, se tam prikaže tudi vir. Začasno rezervirane ure so zabeležene v stolpcu **Začasno rezervirane ure**.

![Začasno rezervirane ure v pogledu »Poimenovani člani ekipe«.](media/Resource-Management-image78.png)

Začasno rezervirane člane ekipe je mogoče dodeliti opravilom.

![Začasno rezerviran član ekipe, ki je dodeljen opravilu.](media/Resource-Management-image79.png)

V zavihku **Usklajevanje** ni prikazana nobena začasna rezervacija vira, saj zavihek **Usklajevanje** upošteva samo potrjene rezervacije.

![Začasno rezerviran vir brez rezervacije v zavihku »Uskladitev«.](media/Resource-Management-image80.png)

> [!NOTE]
> Vira ni mogoče začasno rezervirati na podlagi zahtevanega pogoja, ustvarjenega na podlagi splošnega člana ekipe.

Na plošči razporeda je za začasne rezervacije za vir uporabljena drugačna barva.

![Začasne rezervacije na plošči razporeda.](media/Resource-Management-image81.png)

Če želite pretvoriti začasno rezervacijo v potrjeno rezervacijo, na plošči razporeda z desno tipko miške kliknite začasno rezervacijo in izberite možnost **Spremeni stanje** \> **Potrjena rezervacija** \> **Potrjeno**.

![Spreminjanje stanja rezervacije na »Potrjeno«.](media/Resource-Management-image82.png)

Na plošči razporeda se spremeni tako rezervacija kot stanje. Ker se je stanje rezervacije spremenilo na **Potrjeno**, se vir prikaže kot rezerviran, njegova zmogljivost in razpoložljivost pa sta prilagojeni.

Na enak način lahko tudi prekličete potrjeno ali začasno rezervacijo na plošči razporeda.

Če želite pretvoriti vir z začasno rezervacijo na potrjeno rezervacijo v zavihku **Ekipa**, izberite vir in nato še možnost **Potrdi**.

![Potrditev ukaza.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
