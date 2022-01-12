---
title: Možnosti podizvajalcev za člane projektne skupine
description: Ta tema pojasnjuje možnosti podizvajalcev za člane projektne skupine v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903104"
---
# <a name="subcontracting-options-for-project-team-members"></a>Možnosti podizvajalcev za člane projektne skupine

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V Microsoftu Dynamics 365 Project Operations, lahko ocenite možnosti podizvajalcev, ki so na voljo za enega ali več članov projektne skupine. Razpoložljive možnosti podizvajalcev vam omogočajo:

- Ustvarite novo podizvajalsko pogodbo in/ali ustvarite nove vrstice na obstoječi podizvajalski pogodbi za izbrane člane projektne skupine. 
- Rezervirajte za že obstoječo podizvajalsko in podizvajalsko linijo. 

Izbirate lahko med razpoložljivimi možnostmi oddaje pogodb s podizvajalci za splošne člane projektne skupine ali pa izbirate med člani projektne skupine, ki so bili zaposleni z imenovanim virom, ki je pogodbeni delavec. 

Za naslednje ni na voljo nobenih možnosti podizvajalcev:

- Člani projektne skupine, ki imajo zaposlenega. 
- Člani projektne skupine, ki so že povezani s podizvajalcem in podizvajalsko linijo. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Oddaja podizvajalskega člana projektne skupine brez osebja

Če želite pregledati in izbrati med razpoložljivimi možnostmi podizvajalcev za splošnega člana projektne skupine ali člana projektne skupine brez osebja, sledite tem korakom:

1. Izberite enega ali več zapisov članov projektne skupine, kjer je vir splošni vir.
2. Prepričajte se, da noben od izbranih zapisov članov projektne skupine ni že podizvajalec. 
3. Izberite **Možnosti podizvajalcev** na podmreži članov projektne skupine. The **Možnosti podizvajalcev** odpre se pogovorno okno. 
4. Če ste v 1. koraku izbrali samo en zapis člana projektne skupine, bodo na voljo naslednje možnosti:
    - Ustvarite nove vrstice podizvajalcev. 
    - Rezervacija za obstoječo podizvajalsko pogodbo Če ste v 1. koraku izbrali več zapisov članov projektne skupine, je edina razpoložljiva možnost, da ustvarite nove vrstice podizvajalcev.
5. Možnost rezervacije za obstoječo vrstico podizvajalcev vam omogoča, da izberete podizvajalsko in podizvajalsko vrstico, za katero želite rezervirati. Ko izberete vrstico podizvajalcev za rezervacijo zmogljivosti, morate zagotoviti, da je izbrana vrstica podizvajalcev za čas in da se zahtevana vloga za člana projektne skupine ujema z vlogo, ki je bila kupljena v vrstici podizvajalcev.
6. Ko izberete ustvarjanje novih vrstic podizvajalcev za člane projektne skupine, vam bo sistem omogočil, da izberete podizvajalsko pogodbo, za katero želite ustvariti te vrstice. Podizvajalska pogodba, ki jo izberete za ustvarjanje novih vrstic, mora biti v **Osnutek** stanje. S to možnostjo za ustvarjanje novih vrstic podizvajalcev za izbrane člane projektne skupine bo sistem ustvaril eno vrstico podizvajalcev za čas za vsakega člana projektne skupine. Vloga, ure in datumi bodo kopirani od člana projektne skupine v vsako ustvarjeno vrstico podizvajalcev. 
7. Ko je generični član ekipe povezan s podizvajalcem in podizvajalsko linijo, **Vrsta delavca** polje v vrstici splošnih članov ekipe bo posodobljeno v **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** vrednost bo nastavljena na **veljavno**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Oddajanje podizvajalskega dela za zaposlenega člana projektne skupine

Podobno kot splošni člani ekipe ali člani ekipe brez osebja, si lahko ogledate tudi možnosti podizvajalcev za člana projektne skupine z osebjem, če je član ekipe z osebjem pogodbeni delavec. Če želite pregledati in izbrati med razpoložljivimi možnostmi podizvajalcev za zaposlenega ali imenovanega člana projektne skupine, sledite tem korakom:

1. Izberite enega ali več zapisov članov projektne skupine, kjer je vir imenovan pogodbeni delavec.
2. Zagotovite, da noben od izbranih zapisov članov projektne skupine ni že sklenjen s podizvajalci. 
3. Izberite **Možnosti podizvajalcev** na podmreži članov projektne skupine. The **Možnosti podizvajalcev** odpre se pogovorno okno. 
4. Če ste v 1. koraku izbrali samo en zapis člana projektne skupine, bodo na voljo naslednje možnosti:
      - Ustvarite nove vrstice podizvajalcev.
      - Rezervirajte za obstoječo podizvajalsko pogodbo.
  Če ste v 1. koraku izbrali več zapisov članov projektne skupine, je edina na voljo možnost, da ustvarite nove vrstice podizvajalcev.
5. Možnost rezervacije za obstoječo vrstico podizvajalcev vam omogoča, da izberete podizvajalsko in podizvajalsko vrstico, za katero želite rezervirati. Pri izbiri podizvajalske linije za rezervacijo zmogljivosti morate zagotoviti naslednje:
      - Izbrana vrstica podizvajalcev je za čas. 
      - Zahtevana vloga za člana projektne skupine se ujema z vlogo, ki je bila kupljena v vrstici podizvajalcev. 
      - Prodajalec, s katerim je pogodbeni delavec povezan, je isti kot prodajalec v podizvajalski pogodbi.
6. Ko izberete ustvarjanje novih vrstic podizvajalcev za člane projektne skupine, vam bo sistem omogočil, da izberete podizvajalsko pogodbo, za katero želite ustvariti te vrstice. S to možnostjo bi morali zagotoviti, da je prodajalec, ki mu pripada pogodbeni delavec, isti kot prodajalec v podizvajalski pogodbi. 
7. Podizvajalska pogodba, ki jo izberete za ustvarjanje novih vrstic, mora biti v **Osnutek** stanje. S to možnostjo za ustvarjanje novih vrstic podizvajalcev za izbrane člane projektne skupine bo sistem ustvaril eno vrstico podizvajalcev za čas za vsakega člana projektne skupine. Vloga, ure in datumi bodo kopirani od člana projektne skupine v vsako ustvarjeno vrstico podizvajalcev.  
8. Ko je imenovani član ekipe povezan s podizvajalcem in podizvajalsko linijo, **Vrsta delavca** polje v vrstici imenovani član ekipe bo posodobljeno v **Pogodbeni delavec** in **Veljavnost podizvajalske pogodbe** vrednost bo nastavljena na **veljavno**.

## <a name="re-costing-subcontractor-assignments"></a>Preračunavanje stroškov podizvajalcev

Ko je član projektne skupine (generični ali imenovan) povezan s podizvajalskimi vrsticami z uporabo **Možnosti podizvajalcev** pogovornem oknu, bodo vse naloge, ki jih ima član ekipe, preračunane na podlagi nabavnega cenika, priloženega podizvajalski pogodbi. Na **Ocene** zavihek na **Podrobnosti o projektu** strani, izberite **Posodobite cene** gumb za ogled posodobljenih cen in/ali stroškov, ki izhajajo iz odločitve o podizvajalcu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
