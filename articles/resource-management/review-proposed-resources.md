---
title: Pregled predlaganih virov
description: Ta tema vsebuje informacije o tem, kako predlagati projektne vire.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401193"
---
# <a name="review-proposed-resources"></a>Pregled predlaganih virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Upravitelji virov lahko vodji projekta predlagajo vir prek zahteve za vir.

1. V mreži zahtev ali sami zahtevi izberite **Poišči vire**.
2. Na strani **Pomočnik za razporejanje** izberite vir in nato v polju **Stanje rezervacije** v podoknu **Ustvari rezervacijo vira** izberite **Rezerviraj**.

Pojavijo se naslednje posodobitve stanja:

- Na strani **Pomočnik za razporejanje** se kazalniki stanja posodobijo in sporočajo, da je rezervacija šele predlagana in ne potrjena.
- V zahtevi za vir se stanje spremeni v **Potreben pregled**.
- Na zavihku **Ekipa** izbranega projekta se vrednost splošnega člana ekipe **Stanje zahteve** spremeni v **Potreben pregled**.

Vodja projekta lahko predlog sprejme ali zavrne.

Upravitelji virov lahko za obdelavo zahtev za vire uporabijo katerega koli od spodaj navedenih pristopov:

- Predlagajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil zahtevane ure. Predlagane ure se nato razdelijo med več virov, ki lahko opravijo zahtevane ure. V tem primeru se ure ne morejo prekrivati.
- Predlagajo manj virov, kot jih zahtevajo. V tem primeru je predlagana zmogljivost vira manjša od zahtevanih ur, ki jih je določila oseba, ki je podala zahtevo. Ko torej oseba, ki je podala zahtevo, sprejme predlagane vire, se ustvari neizpolnjena zahteva za vir, ki predstavlja preostalo povpraševanje.
- Rezervirajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil delo.
- Rezervirajo manj virov, kot jih zahtevajo. V tem primeru bo število rezerviranih ur manjše od zahtevanih ur. Sistem vas vodi k predlaganju virov namesto rezervacij, da lahko oseba, ki je podala zahtevo, preveri in spremlja preostalo povpraševanje.

## <a name="resource-availability"></a>razpoložljivosti vira

Upravitelji virov morajo imeti možnost ogleda razpoložljivosti virov in posodobitve rezervacij. V nekaterih primerih ni uradnega povpraševanja (zahteve za vir), vendar se mora upravitelj virov odzvati na nenačrtovano povpraševanje, ki prihaja prek različnih kanalov, na primer elektronske pošte, telefonskih klicev ali neposrednih sporočil. Upravitelji virov uporabljajo ploščo razporeda za posodabljanje virov in rezervacij.

Delovni čas virov se uporablja kot osnova za izračun razpoložljivosti vira. Rezervacije virov porabijo del zmogljivosti virov.

Na plošči razporeda so za prikaz rezervacij, razpoložljivosti, prezasedenosti in stanja rezervacij uporabljene različne barve in senčenje. Z izbiro ustrezne nastavitve v nastavitvah plošče razporeda lahko prikažete tudi legendo.

Če je ob posameznem viru, ki ga je mogoče rezervirati, na plošči razporeda prikazana puščica v desno, lahko vir razširite in s tem prikažete podrobnosti o delu, za katerega je vir rezerviran.

Ker Dynamics 365 Project Operations uporablja mehanizem Universal Resource Scheduling, si lahko tudi vi ogledate podrobnosti o rezervacijah virov za projekte, delovne naloge in vse druge entitete, na katere ste razširili razporejanje, ob predpostavki, da imate nameščeno aplikacijo Dynamics 365 Field Service.

Če si želite ogledati podrobnosti o posameznem viru, ga kliknite z desno tipko miške, da odprete kartico vira.

