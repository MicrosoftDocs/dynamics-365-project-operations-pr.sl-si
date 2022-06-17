---
title: Ustvarjanje projektne ekipe
description: Ta članek vsebuje informacije o ustvarjanju in upravljanju projektnih skupin.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927348"
---
# <a name="create-a-project-team"></a>Ustvarjanje projektne ekipe

[!include [banner](../includes/banner.md)]

Za uporabo vlog, ki so bile predhodno nastavljene v projektu, mora projektni vodja vloge povezati s projektom. Za projekt je mogoče dodeliti več vlog. Da bi preprečili zmedo, so te vloge med rezervacijo samodejno označene. Na primer, če projektni vodja zahteva tri inženirje programske opreme, so samodejno ustvarjene tri vloge inženirjev programske opreme, ki imajo kot oznake **inženir programske opreme 1**, **inženir programske opreme 2** in **inženir programske opreme 3**. Če so bile značilnosti vloge prej nastavljene za vlogo, so uporabljene kot filter med iskanji za vir. Po potrebi se lahko dodajo dodatne značilnosti za nadaljnje podrobneje določanje iskanja.

Nastavitve pogleda lahko prilagodite tudi za boljši pregled razpoložljivosti virov. Obstajajo možnosti prikaza urne, dnevne, tedenske, mesečne, četrtletne in letne razpoložljivosti. Obstaja tudi možnost prikaza razpoložljive in preostale zmogljivosti virov. Ta možnost je uporabna za upravljanje časa, ko ocenjujete razpoložljivi čas za dejavnosti ali razpoložljivost virov.

Projektni vodja lahko na strani izbere vlogo in nato, če je na voljo vir, ki ustreza zahtevi, izbere rezervacijo vira za zapolnitev vloge. Upoštevajte, da virov na tej točki v fazi načrtovanja ni treba rezervirati. Ko ustvarite SČD, lahko vloge nadomestite z zaposlenimi viri za projekt. Če se vloge v SČD nadomestijo z dodeljenimi viri, nastavitev virov samodejno posodobi seznam in razporejanje projektne skupine.

[![Seznam projektne ekipe, ki vključuje vloge in dejanske vire.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektni vodja ima različne možnosti za rezervacijo vira za projekt, npr. **Preostala zmogljivost**, **Polna zmogljivost**, **Odstotek zmogljivosti** in **Določanje ur**. Te možnosti rezervacije lahko kadar koli prekličete, če se dodelitve virov spremenijo. Podprti sta dve vrsti rezervacij:

- **Veljavna rezervacija** – Rezervacija vira je bila odobrena in potrjena za delo na angažmaju za navedeno trajanje.
- **Začasna rezervacija** – Rezervacija vira je bila okvirno nastavljena za delo na angažmaju za navedeno trajanje.

Naslednji postopek opisuje, kako ustvarite projektno ekipo.

## <a name="create-a-project-team"></a>Ustvarjanje projektne ekipe

1. Na strani seznama **Vsi projekti** izberite projekt, nato pa izberite **Uredi**.
2. Na zavihku **Projektna ekipa in načrtovanje** v polju **Končni datum urnika** vnesite začetni datum urnika plus en mesec. Na primer, če je začetni datum urnika 24. junij 2017 (24. 6. 2017), vnesite **24. 6. 2017**.
3. Izberite **Dodaj**.
4. V podoknu **Dodaj vloge v projekt** v polju **Vloga** izberite **Višji projektni vodja**.
5. Izberite **Zahtevane sposobnosti**.
6. Na strani **Izbira značilnosti** so značilnosti, ki ste jih prej nastavili za vlogo višjega projektnega vodje, privzeto izbrane. Izberite **V redu**.
7. Na strani **Dodaj vloge v projekt** v polje **Število virov** vnesite **1**.
8. V polju **Vir** iskanje prikaže vse vire, ki imajo zahtevane sposobnosti. Izberite **Daniel Goldschmidt**, nato pa izberite **Ustvari**.
9. Na strani **Projekt** izberite **Dodaj**.
10. V podoknu **Dodaj vloge v projekt** v polju **Vloga** izberite **Član ekipe**. V polje **Število virov** vnesite **5**.
11. Izberite **Ustvari**.
12. Na strani **Projekti** izberite **Zapolni vir**.

## <a name="monitor-project-teams"></a>Spremljanje projektnih ekip
1. Na strani **Vsi projekti** izberite povezavo **ID projekta** za projekt **2. faza nadgradnje XYZ**.
2. Na zavihku za hiter dostop **Projektna ekipa in načrtovanje** potrdite, da so viri projekta, ki so navedeni, pravilni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]