---
title: Novosti za julij 2021 – poenostavljeno uvajanje storitve Project Operations
description: V tej temi so na voljo informacije o posodobitvah kakovosti, ki so na razpolago v julijski (2021) izdaji poenostavljenega uvajanja storitve Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 475ceea3a6c6db9fe63e3950eaca5d9074faa766
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583972"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Novosti za julij 2021 – poenostavljeno uvajanje storitve Project Operations

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

  - Aplikacija Project Operations v okolju Dataverse (različica 4.12.0.148 ali 4.12.0.152).

## <a name="quality-updates"></a>Posodobitve kakovosti
| **Območje funkcij**              | **Številka sklica** | **Posodobitev kakovosti**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zaračunavanje in oblikovanje cen           | 2224046              | Polje **Razred transakcije** je mogoče urejati na zavihku **Podrobnosti vrstice ponudb**, ki pa je zaklenjeno, če delate na strani **Podrobnosti vrstice ponudb**.                                                                     |
| Zaračunavanje in oblikovanje cen           | 2224400              | Dejanje **Zapri ponudbo kot pridobljeno** ni uspešno, ko ponudba nima določenega datuma mejnikov.                                                                                                                                    |
| Zaračunavanje in oblikovanje cen           | 2234089              | Ko ročno vnesete opis izdelka, se ta počisti, in sicer potem, ko vnesete količino za oceno materiala.                                                                                                                         |
| Zaračunavanje in oblikovanje cen           | 2234100              | Mreža **Nastavitev obračunavanja opravil** ne vključuje stolpca **Material** in njegove vrednosti na zavihku **Obračunavanje opravil** projekta.                                                                                                       |
| Zaračunavanje in oblikovanje cen           | 2277409              | ID izdelka ni na voljo v podrobnostih pogodbe za vrstico z vrsto materiala.                                                                                                                                        |
| Zaračunavanje in oblikovanje cen           | 2281728              | Z ustvarjanjem podrobnosti pogodbe se po nepotrebnem ponovno ocenijo dejanske vrednosti, kar znatno poveča količino podatkov, posledično pa vpliva na uspešnost.                                                                                |
| Zaračunavanje in oblikovanje cen           | 2298668              | Vrstice dnevnika, povezane s preklicanimi in izbrisanimi stroški, se ne odstranijo.                                                                                                                                     |
| Zaračunavanje in oblikovanje cen           | 2300192              | Če račun ureja več uporabnikov, se lahko na potrjenem računu ustvari nova podrobnost vrstice računa.                                                                                   |
| Zaračunavanje in oblikovanje cen           | 2301569              | Računov ni mogoče popraviti, če je bil zadržan znesek v višini 0 \$.                                                                                                                                        |
| Zaračunavanje in oblikovanje cen           | 2307965              | Napaka se pojavi, če je ustvarjena cena kategorije z manjkajočimi vrednostmi.                                                                                                                           |
| Zaračunavanje in oblikovanje cen           | 2326870              | Do napake v storitvi **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** pride, če je vrednost **producttypecode** enaka nič.                                                                            |
| Zaračunavanje in oblikovanje cen           | 2332732              | Napaka se pojavi, če je mejnik podrobnosti pogodbe ustvarjen brez vrstice naročila.                                                                                                                |
| Načrtovanje in sledenje projektov | 2181094              | API razporejanja projektov zdaj podpira dnevnike PSS in dnevnike storitve Operations, ki so shranjeni 90 dni.                                                                                                                  |
| Načrtovanje in sledenje projektov | 2254201              | Oznaka **Način načrtovanja** je posodobljena s podrobnostmi, ki opisujejo privzeto logiko.                                                                                                                                      |
| Načrtovanje in sledenje projektov | 2300252              | Predpomnilnik odzivov vmesnika **openProject** je posodobljen in v ključu predpomnilnika vključuje lastnika žetona **osnovni URL** in **Segment URL**, tako da je vedno mogoče ponovno ustvariti možnost **Zahtevek za URL** v spremembah **osnovni URL**. |
| Načrtovanje in sledenje projektov | 2301312              | Element **msdyn_membershipstatus** je bil odstranjen iz pogleda **Član projektne skupine**.                                                                                                                                        |
| Načrtovanje in sledenje projektov | 2302759              | Izdelki se po nepotrebnem prenašajo na zavihke **Dodelitve vira**, **Ocene** in **Ocene stroškov**.                                                                                                        |
| Načrtovanje in sledenje projektov | 2308050              | Element **CopyProject** ni uspešen, pri čemer se prikaže napaka: »Žetona za pogovor z oddaljeno storitvijo ni bilo mogoče pridobiti«.                                                                                                                           |
| Načrtovanje in sledenje projektov | 2322650              | Pregled **Seznam projektnih nalog** je bil posodobljen tako, da samodejno prikaže datum opravila.                                                                                                            |
| Načrtovanje in sledenje projektov | 2327266              | Element **CopyProject** ustvari napako: »Ključa ni mogoče najti v slovarju«.                                                                                                      |
| Načrtovanje in sledenje projektov | 2328123              | Element **CopyProject** ustvari napako: »Žetona za pogovor z oddaljeno storitvijo ni bilo mogoče pridobiti«.                                                                                                                          |
| Načrtovanje in sledenje projektov | 2336258              | Element **CopyProject** napačno kopira imena položajev za vire.                                                                                                                                                 |
| Zaračunavanje in oblikovanje cen           | 2224476              | Polje **Vir, ki ga je mogoče rezervirati** ni pravilno privzeto za prijavljene uporabnike na strani **Uporaba materiala**.                                                                                                            |
| Upravljanje virov           | 2277249              | Napaka se pojavi, ko je posodobljen zahtevani pogoja za vir, ki ne temelji na projektu.                                                                                                            |
| Upravljanje virov           | 2323869              | Uporaba virov filtriranih virov ne prepozna pravilno.                                                                                                                                             |
| Čas in strošek              | 2176538              | Za kontrolnik **Časovni vnos** so uporabljeni napačni operatorji filtrov.                                                                                                                                                   |
| Čas in strošek              | 2177462              | Če izbrišete časovni vnos v mreži, stanje gumbov **Pošlji**, **Prekliči**, **Izbriši** in **Urejanje vnosa** ne bo posodobljeno, kot je bilo pričakovano.                                                                                        |
| Čas in strošek              | 2299985              | **TimeEntriesImportFromResourceAssignment** ne ohrani začetnega/končnega časa iz krivulj dodelitve.                                                                                                  |
| Čas in strošek              | 2318426              | Ko je časovni vnos poslan, je še vedno mogoče urejati zaklenjena polja.                                                                                                                                   |
| Čas in strošek              | 2323749              | Napaka se pojavi, ko se iz zavihka **Povezano** ustvari strošek za vir, ki ga je mogoče rezervirati.                                                                                                      |
| Čas in strošek              | 2327678              | Ko iz zavihka **Povezan** ustvarite časovni vnos za vir, ki ga je mogoče rezervirati, nadrejeni vir ni poslan kontrolniku za časovni vnos.                                                                            |
| Splošno                       | 2296857              | Sledenje napredku za dolgotrajne posle.                                                                                                                                                                        |
| Splošno                       | 2253682              | Rešitve dvojnega zapisovanja storitve Project Operations ne smemo nameščati, če je osnova dvojnega zapisovanja nameščena v okolju brez rešitve za organiziranje z dvojnim zapisovanjem.                                                |
| Splošno                       | 2316420              | Jedro aplikacije Project Service ni omogočeno, če je poslovna enota uporabnika aplikacije spremenjena.                                                                                                                     |
| Splošno                       | 2376405              | Odpravljena težava s posodobitvami, ki jih vodi izdajatelj (posodobitev kakovosti je na voljo v različici 4.12.0.152)                                                                                                                     |
