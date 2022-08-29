---
title: Možnosti za oddajo del podizvajalcem za člane projektne ekipe
description: Ta članek pojasnjuje možnosti podizvajalcev za člane projektne skupine v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261627"
---
# <a name="subcontracting-options-for-project-team-members"></a>Možnosti za oddajo del podizvajalcem za člane projektne ekipe

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V Microsoftu Dynamics 365 Project Operations, lahko ocenite možnosti podizvajalcev, ki so na voljo za enega ali več članov projektne skupine. Razpoložljive možnosti podizvajalcev vam omogočajo, da:

- Ustvarite novo podizvajalsko pogodbo in/ali ustvarite nove vrstice v obstoječi podizvajalski pogodbi za izbrane člane projektne skupine. 
- Rezervacija za že obstoječo podizvajalsko pogodbo in podizvajalsko linijo. 

Izbirate lahko med razpoložljivimi podizvajalskimi možnostmi za generične člane projektne skupine ali med člani projektne skupine, ki so zaposleni z imenovanim virom, ki je pogodbeni delavec. 

Možnosti podizvajalcev niso na voljo za naslednje:

- Člani projektne skupine, ki so bili zaposleni z zaposlenim. 
- Člani projektne skupine, ki so že povezani s podizvajalsko pogodbo in podizvajalsko linijo. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Sklenitev pogodbe s podizvajalcem za člana projektne skupine brez osebja

Če želite pregledati in izbrati med razpoložljivimi podizvajalskimi možnostmi za splošnega člana ali člana projektne skupine brez osebja, sledite tem korakom:

1. Izberite enega ali več zapisov članov projektne skupine, kjer je vir generični vir.
2. Prepričajte se, da nobeden od izbranih zapisov članov projektne skupine ni že podizvajalec. 
3. Izberite **Možnosti podizvajalcev** na podmreži članov projektne skupine. The **Možnosti podizvajalcev** odpre se pogovorno okno. 
4. Če ste v 1. koraku izbrali samo en zapis člana projektne skupine, bodo na voljo naslednje možnosti:
    - Ustvarite nove podizvajalske vrstice. 
    - Rezervacija za obstoječo podizvajalsko pogodbo Če ste v 1. koraku izbrali več zapisov članov projektne skupine, je edina razpoložljiva možnost, da ustvarite nove podizvajalske vrstice.
5. Možnost rezervacije za obstoječo podizvajalsko linijo vam omogoča, da izberete podizvajalsko pogodbo in podizvajalsko linijo, za katero želite rezervirati. Ko izbirate podizvajalsko linijo za rezervacijo zmogljivosti, morate zagotoviti, da je izbrana podizvajalska linija za čas in da se zahtevana vloga za člana projektne skupine ujema z vlogo, ki je bila kupljena na podizvajalski liniji.
6. Ko izberete ustvarjanje novih podizvajalskih vrstic za člane projektne skupine, vam bo sistem omogočil, da izberete podizvajalsko pogodbo, za katero želite ustvariti te vrstice. Podizvajalska pogodba, ki jo izberete za ustvarjanje novih vrstic, mora biti v **Osnutek** stanje. S to možnostjo ustvarjanja novih podizvajalskih vrstic za izbrane člane projektne skupine bo sistem ustvaril eno podizvajalsko vrstico za čas za vsakega člana projektne skupine. Vloga, ure in datumi bodo kopirani od člana projektne skupine v vsako vrstico podizvajalca, ki je ustvarjena. 
7. Ko je generični član skupine povezan s podizvajalcem in podizvajalsko linijo, **Delavski tip** polje v vrstici s splošnimi člani ekipe bo posodobljeno na **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** vrednost bo nastavljena na **Veljavno**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Sklenitev pogodbe s podizvajalcem zaposlenega člana projektne skupine

Tako kot generični člani skupine ali člani ekipe brez osebja si lahko ogledate tudi možnosti podizvajalcev za člana projektne skupine z osebjem, če je član ekipe s zaposlenimi pogodbeni delavec. Če želite pregledati in izbrati med razpoložljivimi podizvajalskimi možnostmi za zaposlenega ali imenovanega člana projektne skupine, sledite tem korakom:

1. Izberite enega ali več zapisov članov projektne skupine, kjer je vir imenovan pogodbeni delavec.
2. Prepričajte se, da nobeden od izbranih zapisov članov projektne skupine ni že podizvajalec. 
3. Izberite **Možnosti podizvajalcev** na podmreži članov projektne skupine. The **Možnosti podizvajalcev** odpre se pogovorno okno. 
4. Če ste v 1. koraku izbrali samo en zapis člana projektne skupine, bodo na voljo naslednje možnosti:
      - Ustvarite nove podizvajalske vrstice.
      - Rezervacija za obstoječo podizvajalsko pogodbo.
  Če ste v 1. koraku izbrali več zapisov članov projektne skupine, je edina razpoložljiva možnost ustvarjanje novih podizvajalskih vrstic.
5. Možnost rezervacije za obstoječo podizvajalsko linijo vam omogoča, da izberete podizvajalsko pogodbo in podizvajalsko linijo, za katero želite rezervirati. Pri izbiri podizvajalske linije za rezervacijo zmogljivosti morate zagotoviti naslednje:
      - Izbrana podizvajalska linija je za čas. 
      - Zahtevana vloga za člana projektne skupine se ujema z vlogo, ki je bila kupljena v liniji podizvajalcev. 
      - Prodajalec, s katerim je povezan pogodbeni delavec, je isti kot prodajalec v podizvajalski pogodbi.
6. Ko izberete ustvarjanje novih podizvajalskih vrstic za člane projektne skupine, vam bo sistem omogočil, da izberete podizvajalsko pogodbo, za katero želite ustvariti te vrstice. Pri tej možnosti bi morali zagotoviti, da je prodajalec, ki mu pripada pogodbeni delavec, isti kot prodajalec na podizvajalski pogodbi. 
7. Podizvajalska pogodba, ki jo izberete za ustvarjanje novih vrstic, mora biti v **Osnutek** stanje. S to možnostjo ustvarjanja novih podizvajalskih vrstic za izbrane člane projektne skupine bo sistem ustvaril eno podizvajalsko vrstico za čas za vsakega člana projektne skupine. Vloga, ure in datumi bodo kopirani od člana projektne skupine v vsako vrstico podizvajalca, ki je ustvarjena.  
8. Ko je imenovani član skupine povezan s podizvajalcem in podizvajalsko linijo, **Delavski tip** polje v vrstici imenovanega člana ekipe bo posodobljeno na **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** vrednost bo nastavljena na **Veljavno**.

## <a name="re-costing-subcontractor-assignments"></a>Prevrednotenje dodelitev podizvajalcem

Ko je član projektne skupine (splošen ali imenovan) povezan s podizvajalskimi linijami z uporabo **Možnosti podizvajalcev** morebitne dodelitve nalog, ki jih ima član ekipe, bodo preračunane na podlagi nabavnega cenika, priloženega podizvajalski pogodbi. Na **Ocene** zavihek na **Podrobnosti projekta** strani izberite **Posodobite cene** gumb za ogled posodobljenih cen in/ali stroškov, ki izhajajo iz odločitve o podizvajalcu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
