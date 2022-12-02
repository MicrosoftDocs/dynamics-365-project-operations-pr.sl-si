---
title: Možnosti za oddajo del podizvajalcem za člane projektne ekipe
description: Ta članek pojasnjuje možnosti podizvajalskih za člane projektne ekipe v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522299"
---
# <a name="subcontracting-options-for-project-team-members"></a>Možnosti za oddajo del podizvajalcem za člane projektne ekipe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikaciji Microsoft Dynamics 365 Project Operations lahko ocenite možnosti podizvajalske pogodbe, ki so na voljo za enega ali več članov projektne ekipe. Razpoložljive možnosti podizvajalske pogodbe omogočajo naslednje:

- Ustvarite novo podizvajalsko pogodbo in/ali ustvarite nove vrstice v obstoječi podizvajalski pogodbi za izbrane člane projektne ekipe. 
- Rezervirate za obstoječo podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe. 

Izbirate lahko med razpoložljivimi možnostmi podizvajalske pogodbe za splošne člane projektne ekipe ali med člani projektne ekipe, ki so zaposleni z imenovanim virom, ki je pogodbeni delavec. 

Za naslednje ni na voljo možnosti podizvajalske pogodbe:

- Člani projektne ekipe, ki so imeli zaposlene. 
- Člani projektne epike, ki so že povezani s podizvajalsko pogodbo in podrobnostmi podizvajalske pogodbe. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Oddaja del podizvajalcu, ki je član projektne ekipe brez osebja

Če želite pregledati in izbrati med razpoložljivimi možnostmi podizvajalske pogodbe za splošnega člana ali člana projektne ekipe brez osebja, sledite tem korakom:

1. Izberite enega ali več zapisov člana projektne ekipe, kjer je vir splošen.
2. Prepričajte se, da nobeden od izbranih zapisov člana projektne ekipe ni že podizvajalec. 
3. V podmreži članov projektne ekipe izberite možnost **Možnosti podizvajalske pogodbe**. Odpre se pogovorno okno **Možnosti podizvajalske pogodbe**. 
4. Če ste v 1. koraku izbrali samo en zapis člana projektne ekipe, bodo na voljo naslednje možnosti:
    - Ustvarjanje novih podrobnosti podizvajalske pogodbe. 
    - Rezervirajte za obstoječe podizvajalske pogodbe. Če ste v 1. koraku izbrali več zapisov članov projektne ekipe, je edina razpoložljiva možnost ustvarjanje novih podrobnosti podizvajalske pogodbe
5. Možnost rezervacije za obstoječe podrobnosti podizvajalske pogodbe omogoča, da izberete podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe, za katere želite rezervirati. Ko izbirate podrobnosti podizvajalske pogodbe za rezervacijo zmogljivosti, morate zagotoviti, da so izbrane podrobnosti podizvajalske pogodbe namenjene za čas in da zahtevana vloga za člana projektne ekipe ustreza vlogi, ki je bila kupljena v podrobnostih podizvajalske pogodbe.
6. Ko izberete ustvarjanje novih podrobnosti podizvajalske pogodbe za člane projektne ekipe, bo sistem omogočil, da izberete podizvajalsko pogodbo, za katero želite ustvariti te vrstice. Podizvajalska pogodba, ki jo izberete za ustvarjanje novih vrstic, mora biti v stanju **Osnutek**. S to možnostjo ustvarjanja novih podrobnosti podizvajalske pogodbe za izbrane člane projektne ekipe bo sistem ustvaril eno podrobnost podizvajalske pogodbe za čas za vsakega člana projektne ekipe. Vloga, ure in datumi bodo kopirani od člana projektne ekipe v vsako podrobnost podizvajalske pogodbe, ki je ustvarjena. 
7. Ko je splošni član ekipe povezan s podizvajalcem in podrobnostmi podizvajalske pogodbe, bo polje **Vrsta delavca** v vrsti splošnega člana ekipe posodobljeno na **Pogodbeni delavec**, vrednost **Veljavnost podizvajalske pogodbe** pa bo nastavljena na **Veljavno**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Oddaja del podizvajalcu, ki je član projektne ekipe z osebjem

Tako kot splošni člani ekipe ali člani ekipe brez osebja si lahko ogledate tudi možnosti podizvajalske pogodbe za člana projektne ekipe z osebjem, če je član ekipe z osebjem pogodbeni delavec. Če želite pregledati in izbrati med razpoložljivimi možnostmi podizvajalske pogodbe za člana projektne ekipe z osebjem ali imenovanega člana projektne ekipe, sledite tem korakom:

1. Izberite enega ali več zapisov člana projektne ekipe, kjer je vir imenovan pogodbeni delavec.
2. Prepričajte se, da nobeden od izbranih zapisov člana projektne ekipe ni že podizvajalec. 
3. V podmreži članov projektne ekipe izberite možnost **Možnosti podizvajalske pogodbe**. Odpre se pogovorno okno **Možnosti podizvajalske pogodbe**. 
4. Če ste v 1. koraku izbrali samo en zapis člana projektne ekipe, bodo na voljo naslednje možnosti:
      - Ustvarjanje novih podrobnosti podizvajalske pogodbe.
      - Rezervacija za obstoječo podizvajalsko pogodbo.
  Če ste v 1. koraku izbrali več zapisov članov projektne ekipe, je edina razpoložljiva možnost ustvarjanje novih podrobnosti podizvajalske pogodbe.
5. Možnost rezervacije za obstoječe podrobnosti podizvajalske pogodbe omogoča, da izberete podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe, za katere želite rezervirati. Pri izbiri podrobnosti podizvajalske pogodbe za rezervacijo zmogljivosti morate zagotoviti naslednje:
      - Izbrane podrobnosti podizvajalske pogodbe so namenjene za čas. 
      - Zahtevana vloga za člana projektne ekipe se ujema z vlogo, ki je bila kupljena v podrobnostih podizvajalske pogodbe. 
      - Dobavitelj, s katerim je povezan pogodbeni delavec, je isti kot dobavitelj v podizvajalski pogodbi.
6. Ko izberete ustvarjanje novih podrobnosti podizvajalske pogodbe za člane projektne ekipe, bo sistem omogočil, da izberete podizvajalsko pogodbo, za katero želite ustvariti te vrstice. Ko je ta možnost omogočena, morate zagotoviti, da je dobavitelj, kateremu pripada pogodbeni delavec, isti kot dobavitelj v podizvajalski pogodbi. 
7. Podizvajalska pogodba, ki jo izberete za ustvarjanje novih vrstic, mora biti v stanju **Osnutek**. S to možnostjo ustvarjanja novih podrobnosti podizvajalske pogodbe za izbrane člane projektne ekipe bo sistem ustvaril eno podrobnost podizvajalske pogodbe za čas za vsakega člana projektne ekipe. Vloga, ure in datumi bodo kopirani od člana projektne ekipe v vsako podrobnost podizvajalske pogodbe, ki je ustvarjena.  
8. Ko je imenovani član ekipe povezan s podizvajalcem in podrobnosti podizvajalske pogodbe, bo polje **Vrsta delavca** v vrsti imenovanega člana ekipe posodobljeno na **Pogodbeni delavec**, vrednost **Veljavnost podizvajalske pogodbe** pa bo nastavljena na **Veljavno**.

## <a name="re-costing-subcontractor-assignments"></a>Ponoven izračun stroškov dodelitev podizvajalcem

Ko je član projektne ekipe (splošen ali imenovan) povezan s podrobnostmi podizvajalske pogodbe s pogovornim oknom **Možnosti podizvajalskih pogodb**, bo za morebitne dodelitve opravil, ki jih ima član ekipe, znova izračunan strošek na podlagi nabavnega cenika, priloženega podizvajalski pogodbi. V zavihku **Ocene** na strani **Podrobnosti projekta** izberite gumb **Posodobitev cene**, da si ogledate posodobljene cene in/ali stroške, ki izhajajo iz odločitve o podizvajalski pogodbi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
