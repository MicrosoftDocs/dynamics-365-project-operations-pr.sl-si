---
title: Izdelki
description: Ta tema vsebuje informacije o katalogu izdelkov, s katerimi lahko strankam posredujete informacije o izdelkih in cenah, ki jih ponuja vaša organizacija.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121283"
---
# <a name="products"></a>Izdelki

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Izdelki so hrbtenica vašega podjetja. Katalog izdelkov v storitvi Dynamics 365 Sales Professional je zbirka informacij o izdelkih in njihovih cenah. Olajšajte predstavnikom prodaje povečanje prodaje tako, da hitro ustvarite katalog izdelkov.

## <a name="add-a-product"></a>Dodajanje izdelka

1.  Preverite, ali imate vlogo skrbnika sistema ali vodje prodaje, s katero lahko dodajate izdelke v storitev Dynamics 365 Sales Professional.
2.  Na zemljevidu mesta pod možnostjo **Nastavitev** izberite **Izdelki**.
3.  Izberite **Dodaj izdelek** in vnesite naslednje informacije:

    -  **Ime**
    -  **ID izdelka**
    -  **Nadrejeno**: izberite nadrejeno družino izdelkov za izdelek. Če ustvarjate podrejeni izdelek v družini izdelkov, sem vnesite ime nadrejene družine izdelkov. Tega ni mogoče spremeniti, ko je zapis shranjen.
    -  **Veljavno od**/**Veljavno do**: določite obdobje veljavnosti izdelka tako, da izberete datum pri možnosti **Veljavno od** in **Veljavno do**.
    -  **Skupina enot**: izberite skupino enot. Skupina enot je zbirka različnih enot, v katerih se prodaja izdelek, in določa, kako se posamezne elemente združuje v večje količine. Če kot izdelek na primer dodajate semena, ste morda ustvarili skupino enot »Semena« in kot njeno primarno enoto določili »paket«.
    -  **Privzeta enota**: izberite najbolj običajno enoto, v kateri boste prodajali izdelek. Enote so količine ali meritve, v katerih prodajate svoje izdelke. Če na primer kot izdelek dodate semena, lahko izdelek prodajate v paketih, v škatlah ali na paletah. Vsaka od teh enot postane enota izdelka. Če se semena večinoma prodajajo v paketih, to izberite kot enoto.
    -  **Privzeti cenik**: če je izdelek nov, je to polje na voljo samo za branje. Če želite izbrati privzeti cenik, morate najprej izpolniti vsa obvezna polja in zapis shraniti. Čeprav privzeti cenik ni obvezen, vam priporočamo, da ga nastavite za posamezen izdelek, potem ko shranite zapis o izdelku. Če v zapisu o stranki ni cenika, lahko prodajna ekipa za oblikovanje ponudb, naročil in računov uporabi privzeti cenik.
    -  **Podprte decimalke**: vnesti morate celo število med 0 in 5. Če izdelka ni mogoče razdeliti po delih, vnesite 0. Natančnost polja **Količina** v ponudbi, naročilu ali zapisku zmnožka računa je preverjena z vrednostjo v tem polju, če za izdelek ni povezanega cenika.
    -  **Zadeva**: povežite ta izdelek z zadevo. Z zadevami lahko razvrstite izdelke v kategorije in filtrirate poročila.

4.  Izberite **Shrani**.
5.  Na zavihku **Dodatne podrobnosti** v razdelku **Elementi cenika** izberite **Več ukazov** in nato izberite **Dodaj nov element cenika**.
7.  Na zavihku **Dodatne podrobnosti**, v razdelku **Odnos izdelka** izberite ikono **Več ukazov** in nato izberite **Dodaj nov odnos izdelka**.
8.  Na obrazcu **Nov odnos med izdelki** vnesite naslednje podrobnosti in v ukazni vrstici izberite **Shrani in zapri**:

    -   **Sorodni izdelek**: izberite izdelek, ki ga želite dodati kot sorodni izdelek obstoječemu zapisu izdelka, s katerim delate.
    -   **Vrsta prodajnih odnosov**: izberite, ali želite dodati izdelek kot izdelek za povečano prodajo, izdelek za navzkrižno prodajo, dodatek ali nadomestek.
    -   **Smer**: izberite, ali bo odnos med izdelki enosmeren ali dvosmeren. Ko izberete enosmeren, bo izdelek, ki ga izberete v možnosti **Sorodni izdelek**, prikazan kot priporočilo za obstoječi izdelek, ne pa tudi obratno.

9.  Na obrazcu izdelka izberite **Shrani**.

## <a name="import-products"></a>Uvozni izdelki

S predlogami za uvoz lahko podatke o izdelku v storitvi Dynamics 365 Sales vnesete v velikem obsegu.

## <a name="revise-a-product"></a>Revidiranje izdelka

Ohranite seznam izdelkov posodobljen tako, da glede na zahteve hitro izboljšate lastnosti izdelkov in znova objavite informacije, tako da si prodajni zastopniki lahko ogledajo najnovejše spremembe seznama izdelkov.

1.  Preverite, ali imate eno od naslednjih varnostnih vlog ali enakovredno dovoljenje: sistemski skrbnik, prilagojevalec sistema, direktor prodaje, namestnik direktorja prodaje, namestnik direktorja trženja ali izvršni direktor – poslovni direktor.
2.  Na zemljevidu mesta izberite **Izdelki**.
3.  Odprite dejaven izdelek, ki ga želite spremeniti, in v ukazni vrstici kliknite **Preglej**.
4.  V pogovornem oknu **Potrditev revizije** izberite **Potrdi**. To bo spremenilo stanje izdelka za **V reviziji**.
5.  Ko opravite spremembe, v ukazni vrstici izberite **Objavi**.

    > [!TIP]
    > Če želite povrniti spremembe in nadaljevati z zadnjo aktivno različico izdelka, izberite **Povrni**. To spremeni stanje izdelka nazaj na **Aktivno**.

## <a name="clone-a-product"></a>Kloniranje izdelka 

Pri ustvarjanju novega izdelka lahko nekaj časa prihranite tako, da klonirate obstoječega. S tem ustvarite kopijo izvornega zapisa z vsemi podrobnostmi razen imena in ID-ja.

1.  Preverite, ali imate eno od naslednjih varnostnih vlog ali enakovredno dovoljenje: sistemski skrbnik, prilagojevalec sistema, direktor prodaje, namestnik direktorja prodaje, namestnik direktorja trženja ali izvršni direktor – poslovni direktor.
2.  Na zemljevidu mesta izberite **Izdelki**.
3.  Izberite zapis izdelka, ki ga želite klonirati, in nato v ukazni vrstici izberite **Kloniraj**. Prikaže se potrditveno pogovorno okno.
4.  Izberite **Potrdi**.

Odpre se nov zapis izdelka z istimi podrobnostmi, kot jih ima izvorni zapis, drugačna boste le ime in ID.

## <a name="retire-a-product"></a>Umik izdelka 

Če vaša organizacija določenega izdelka ne prodaja več, ga umaknite, da ne bo več na voljo vašim prodajnim zastopnikom.

1.  Preverite, ali imate vlogo skrbnika sistema ali upravitelja za Sales Professional oz. enakovredno dovoljenje.
2.  Na zemljevidu mesta izberite **Izdelki**.
3.  Odprite dejaven izdelek, ki ga želite umakniti, in v ukazni vrstici kliknite **Umakni**.
4.  V pogovornem oknu **Potrditev umika** izberite **Potrdi**.


## <a name="delete-a-product"></a>Brisanje izdelka

Če želite ustaviti prodajo izdelka, ga izbrišite.

> [!IMPORTANT]
> Izbrisanega zapisa ne morete obnoviti.

1.  Preverite, ali imate vlogo skrbnika sistema ali upravitelja za Sales Professional oz. enakovredno dovoljenje.
2.  Na zemljevidu mesta izberite **Izdelki**.
3.  Izberite zapis izdelka, ki ga želite izbrisati, in nato v ukazni vrstici izberite **Izbriši**.
4.  V pogovornem oknu **Potrditev brisanja** izberite **Nadaljuj**.
 
 ## <a name="quantity-factors-for-products"></a>Količniki za količino za izdelke

Količniki za količino podpirajo prodajo naročniških izdelkov. Pri naročniških izdelkih je količina v vrstici ponudbe ali projektne pogodbe izražena kot število mesecev uporabe.

Običajno je cena naročniške programske opreme shranjena v katalogu kot cena na uporabnika na mesec. Vendar pa lahko namesto tega uporabite druge opise časa. Med prodajnim postopkom je cena v vrstici ponudbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent za IT. Vsak posel ima različno število uporabnikov in različno število naročniških mesecev. Količina, ki se uporablja za izračun zneska vrstice ponudbe, je produkt števila uporabnikov in števila mesecev naročnine.

Količniki za količino temeljijo na atributih izdelka. Ko konfigurirate določene lastnosti za izdelek, lahko označite podmnožico teh lastnosti ali vseh lastnosti kot količnike za količino.

Sistem preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom. Ko je izdelek, za katerega so konfigurirani količniki za količino, dodan v vrstico ponudbe, polje **Količina** v vrstici ponudbe postane polje samo za branje. Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, se izračuna količina vrstice ponudbe.

Na primer, če obstajajo naslednje lastnosti: 

- **Št. uporabnikov**: število uporabnikov. 
- **Št. mesecev**: število mesecev naročnine.
- **Inventarna številka izdelka** 

Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]