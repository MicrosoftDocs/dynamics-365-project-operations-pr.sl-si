---
title: Novosti za oktober 2022 – poenostavljeno uvajanje storitve Project Operations
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsoft Dynamics 365 Project Operations lite uvedbe iz oktobra 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806768"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novosti za oktober 2022 – poenostavljeno uvajanje storitve Project Operations

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.57.0.176. storitve Dataverse

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

| Območje funkcij | Ime funkcije | Več informacij |
| --- | --- | --- |
| Načrtovanje in sledenje projektov | **Zunanje razporejanje projektnih operacij**<br>Zunanji način razporejanja omogoča strankam izvorno ustvarjanje, posodabljanje in brisanje entitet, ki so povezane s strukturami razčlenitve dela (WBS) z uporabo izvornih Dataverse API-jev, brez trenutnih omejitev, ki jih uveljavlja Project for Web. | [Zunanje razporejanje](/dynamics365/project-operations/project-management/external-scheduling) |
| Uvajanje in konfiguracija | <p>**Omogočite strankam, da izberejo vrsto uvedbe**<br>Posodobitve, ki jih poganja izdelek (PDU-ji) za Project Operations, se uporabljajo za samodejno namestitev rešitve Project Operations Dual-write, ko so v okolju nameščene rešitve jedra in orkestracije Dual-write.</p><p>Ta funkcija uvaja nov parameter **Vedenje nadgradnje rešitve** v parametrih projekta. Ko je ta parameter nastavljen na **Lite only**, PUD-ji ne bodo več samodejno namestili rešitve za dvojno zapisovanje projektnih operacij, tudi če so v okolju nameščene jedrne in orkestracijske rešitve z dvojnim pisanjem. To vedenje bo koristilo strankam, ki nameravajo uporabiti rešitve dvojnega pisanja za integracijo prodajnih naročil v aplikacije za finance in operacije, vendar želijo uporabljati Project Operations v načinu Lite (to je brez integracije v aplikacije za finance in operacije).</p> | |

## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2316317 | Sistem omogoča ustvarjanje faktur, ki nimajo zaračunanih transakcij. |
| Zaračunavanje in oblikovanje cen | 2737300 | Pred dostopom do obrazca preverite razpoložljivost polja stranke. |
| Zaračunavanje in oblikovanje cen | 2744948 | Dodajte ničelno preverjanje za način obračunavanja. |
| Zaračunavanje in oblikovanje cen | 2763515 | Obravnava napake ničelne reference, ko manjka prodajna pogodba računa. |
| Zaračunavanje in oblikovanje cen | 2844301 | Ustvarjanje paketnega računa ne uspe zaradi napake. |
| Zaračunavanje in oblikovanje cen | 2845869 | Nepravilno shranjevanje organizacijske storitve. |
| Zaračunavanje in oblikovanje cen | 2853729 | Podrobnosti o vlogi in ceni se posodobijo, ko se spremeni vrsta obračunavanja. |
| Zaračunavanje in oblikovanje cen | 2940350 | Ko so cene dejanske, naj se samodejno vnesejo samo aktivni ceniki. |
| Uvajanje in konfiguracija | 3001206 | Entiteta msdyn\_ replaylogheader preprečuje nadgradnje strankinih organizacij. |
| Upravljanje priložnosti | 2755582 | Obravnava izjem ničelne reference v pomočniku za pravila razdeljenega obračunavanja. |
| Upravljanje priložnosti | 2761477 | Ko je uporabljeno deljeno obračunavanje, izbris mejnika (glave) pusti mejnike osirotele. |
| Upravljanje priložnosti | 2767595 | Ko se zapis o uporabi materiala odpre v glavnem obrazcu, se vir za rezervacijo za zapis spremeni v trenutno prijavljenega uporabnika. |
| Načrtovanje in sledenje projektov | 2790384 | Časovna omejitev Pending OperationSet je prekratka. |
| Upravljanje virov | 2751560 | Nedosledne prednostne organizacijske enote v zahtevah po virih. |
| Podizvajalske pogodbe | 2907231 | Faza obdelave računov dobavitelja ne more napredovati. |
| Čas in strošek | 2867363 | Zapisi ne izpadejo iz pogleda Odsotnosti/počitnice za odobritev, ko so v čakalni vrsti za odobritev. |
| Čas in strošek | 2894405 | TESA: Neuporabljen imenik POC povzroča težave s skladnostjo. |
