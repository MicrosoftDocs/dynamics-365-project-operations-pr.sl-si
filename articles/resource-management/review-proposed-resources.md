---
title: Pregled predlaganih virov
description: Ta članek vsebuje informacije o tem, kako predlagati vire projekta.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183995"
---
# <a name="review-proposed-resources"></a>Pregled predlaganih virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Upravitelji virov lahko vodji projekta predlagajo vir prek zahteve za vir.

Za pregled predlaganih virov sledite naslednjim korakom:

1. V mreži **Zahteve** ali v sami zahtevi izberite možnost **Poišči vire**.
2. Na strani **Pomočnik za načrtovanje** izberite vir, nato pa potrdite, da so v predlagano rezervacijo vključene vse predlagane ure.
3. Polje **Stanje rezervacije** v podoknu **Ustvarjanje rezervacije vira** nastavite na **Predlagano** in izberite možnost **Rezervacija**.

    > [!NOTE]
    > Z nastavitvijo možnosti **Status rezervacije** na **Predlagano** ne bo izvedena veljavna rezervacija vira, splošni vir pa ne bo zamenjan s poimenovanim članom ekipe.

    Pojavijo se naslednje posodobitve stanja:

    - Na strani **Pomočnik za načrtovanje** se kazalniki stanja posodobijo in s tem sporočajo, da je rezervacija šele predlagana in da veljavna rezervacija ni bila izvedena.
    - Pri zahtevi za vir mora pregledovalec zahteve spremeniti status v **Potrebuje pregled**.
    - Na **Ekipa** zavihek projekta, generični član ekipe **Status zahteve** vrednost se samodejno spremeni v **Potrebuje pregled**.

Vodja projekta lahko predlog sprejme ali zavrne.

Upravitelji virov lahko za obdelavo zahtev za vire uporabijo katerega koli od spodaj navedenih pristopov:

- Predlagajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil zahtevane ure. Predlagane ure se nato razdelijo med več virov, ki lahko opravijo zahtevane ure. V tem primeru se ure ne morejo prekrivati.
- Predlagajo manj virov, kot jih zahtevajo. V tem primeru je predlagana zmogljivost vira manjša od zahtevanih ur, ki jih je določila oseba, ki je podala zahtevo. Ko oseba, ki je podala zahtevo, sprejme predlagane vire, se ustvari neizpolnjena zahteva za vir, ki zajema preostali del povpraševanja.
- Rezervirajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil delo.
- Rezervirajo manj virov, kot je zahtevano. V tem primeru bo število rezerviranih ur manjše od zahtevanih ur. Sistem vas usmeri k predlaganju virov, ne pa rezervacij, tako da lahko oseba, ki je podala zahtevo, preveri in spremlja preostali del povpraševanja.

## <a name="resource-availability"></a>razpoložljivosti vira

Upravitelji virov morajo imeti možnost ogleda razpoložljivosti virov in posodobitve rezervacij. V nekaterih primerih ni uradnega povpraševanja (zahteve za vir). Upravitelj virov se mora kljub temu odzvati na nenačrtovano povpraševanje iz drugih kanalov, kot so e-poštna sporočila, telefonski klici ali sprotna sporočila. Upraviteljem virov za posodabljanje virov in rezervacij služi **Plošča za načrtovanje**.

Delovni čas vira se uporablja kot osnova za izračun njegove razpoložljivosti. Rezervacije virov porabijo del zmogljivosti virov.

**Plošča za načrtovanje** rezervacije, razpoložljivost, prezasedenost in stanje rezervacij prikazuje s pomočjo različnih barv in senčenja. Nastavitev, ki jo ponuja **Plošča za načrtovanje**, vam omogoča prikaz legende.

Če **Plošča razporeda** ob posameznem viru, ki ga je mogoče rezervirati, prikazuje puščico v desno, lahko vir razširite in s tem prikažete podrobnosti o delu, za katerega je vir rezerviran.

Ker rešitev Dynamics 365 Project Operations uporablja mehanizem Universal Resource Scheduling, si lahko tudi vi ogledate podrobnosti o rezervacijah virov za projekte, delovne naloge in vse druge entitete, na katere ste razširili razporejanje, ob predpostavki, da imate nameščeno aplikacijo Dynamics 365 Field Service.

Če si želite ogledati dodatne podrobnosti o posameznem viru, ga kliknite z desno tipko miške, da odprete kartico vira.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
