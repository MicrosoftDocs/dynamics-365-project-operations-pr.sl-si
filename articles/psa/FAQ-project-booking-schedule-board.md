---
title: Ustvarjanje rezervacije projekta na plošči razporeda
description: V tem članku so na voljo informacije o tem, kako ustvarite rezervacijo projekta na plošči razporeda.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: f231f7a862420fc4f20b4eb86e4067cbf2ed3425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930936"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Ustvarjanje rezervacije projekta na plošči razporeda

[!include [banner](../includes/psa-now-project-operations.md)]

Vir lahko rezervirate za projekt neposredno na zavihku **Ekipa** projekta ali tako, da v dodelitvi generičnega člana ekipe ustvarite zahtevo za vir in nato ustvarjeno zahtevo izpolnite s članom projektne ekipe.

Prav tako lahko vir rezervirate za projekt neposredno na plošči razporeda. To lahko naredite na tri načine:

- **Rezervacija v ustvarjeni zahtevi za vir:** zahtevo za vir lahko ustvarite po tem, ko ustvarite splošni vir in dodelite opravila znotraj projekta.

- **Rezervacija v primarni zahtevi:** primarne zahteve se prikažejo na plošči razporeda na zavihku **Projekt**. 

- **Rezervacija v novi zahtevi za vir:** ustvarite lahko povsem novo zahtevo za vir in jo povežete s projektom. Na plošči razporeda se zahteva za vir prikaže na zavihku **Odprte zahteve**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervacije v ustvarjeni zahtevi za vir

Ustvarite lahko splošni vir in mu dodelite eno ali več opravil znotraj projekta. Nato lahko pri generičnem članu ekipe ustvarite zahtevo za vir. 

1.  Na plošči razporeda se bo ta vir prikazal na zavihku **Odprte zahteve**. Če imate veliko odprtih zahtev, boste morda morali uporabiti filtre stolpcev v mreži. 

    ![Zavihek "Odprte zahteve na plošči razporeda".](media/FAQ-Project-Booking-Schedule-Board-1.png "Posnetek zaslona tabele rezervacij in dodelitev")

2. Izberite zahtevo. Na vrhu izbrane vrstice se prikaže zavihek **Poišči razpoložljivost**.
 
3. Ko izberete zavihek, se na plošči razporeda odpre način pomočnika za razporejanje, ki nato filtrira razpoložljive vire, ki izpolnjujejo zahtevo za vir. Nato lahko rezervirate vir.

4. Prav tako lahko izbrano vrstico povlečete z dna plošče razporeda in jo spustite v celico vira v mreži zgoraj. Ko jo spustite, se na desni strani odpre plošča **Ustvarjanje rezervacije vira**.

    Če izberete možnost **Rezerviraj**, rezervirate vir za projektno ekipo.

![Plošča »Ustvarjanje rezervacije vira«.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervacija v primarni zahtevi

Če v storitvi Project Service ustvarite projekt, se samodejno ustvari zahteva za vir, imenovana primarna zahteva. To je prazna zahteva, ki se uporablja za hitro rezervacijo vira na plošči razporeda, pri čemer ni treba ustvariti (povsem nove) zahteve. Ker je zahteva prazna, boste morali določiti datume in način dodelitve ter ure, če so na voljo. 

1. Če želite rezervirati vir s primarno zahtevo, na plošči razporeda izberite zavihek **Projekt**. Če imate veliko projektov, boste morda morali uporabiti filter stolpca v stolpcu **Projekt**.

   ![Filtri stolpca na plošči za načrtovanje.](media/FAQ-Project-Booking-Schedule-Board-2.png "Posnetek zaslona tabele rezervacij in dodelitev")

2. Izberite zahtevo, ki ima v svojem imenu samo ime projekta, vrednost njenega trajanja pa je nič (0).

3. Izberite zavihek **Poišči razpoložljivost**, ki se prikaže v vrstici. Plošča razporeda preide v način pomočnika za razporejanje in prikaže razpoložljive vire, ki jih je mogoče rezervirati za projekt.

4. Ker je **Primarna zahteva** prazna zahteva z vrednostjo trajanja nič (0), boste morali pri izbiri in rezervaciji vira na plošči **Ustvarjanje rezervacije vira** določiti trajanje.

5. Lahko izberete tudi možnost **Primarna zahteva projekta** na dnu plošče razporeda ter jo povlečete in spustite v vir, da ga rezervirate.
 
    Ker je **Primarna zahteva** prazna zahteva z vrednostjo trajanja nič (0), boste morali pri izbiri in rezervaciji vira na plošči **Ustvarjanje rezervacije vira** določiti trajanje.
 
    Če vir rezervirate prek možnosti **Primarna zahteva** na plošči razporeda, ga dodate projektni ekipi brez kakršnih koli dodelitev.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervacije v novi zahtevi za vir
Za rezervacijo iz nove zahteve za vir dokončajte spodnje korake. 

1. Odprite **Zahteve za vir** in nato izberite **Novo**, da ustvarite novo zahtevo za vir.

2. Na zavihku **Projekt** izberite projekt, da povežete zahtevo s projektom.
 
    Ta novo ustvarjena zahteva se na plošči razporeda prikaže kot **Odprta zahteva**, ki jo lahko izpolnite.

3. Rezervirajte vir, da ga dodate projektni ekipi.

4. Zdaj, ko je vir rezerviran, morate ročno dodeliti opravila.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
