---
title: Upravljanje predračuna projekta
description: Ta tema vsebuje informacije o tem, kako delati s predračuni projekta.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2146e62bddc4a6286fa303ff2cc2c5622ea3133c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866926"
---
# <a name="manage-a-proforma-project-invoice"></a>Upravljanje predračuna projekta 

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations so predračuni zgrajeni kot razširitev računov v aplikaciji Dynamics 365 Sales. Vendar pa obstajajo številne razlike pri postopku izdajanja računov med aplikacijama Sales in Project Operations, ko gre za izdajanje računov. V aplikaciji Project Operations iz strani **Seznam računov** na primer ni mogoče ustvariti novega računa, kar pa je mogoče v aplikaciji Sales. Te razlike in razširitve obstajajo za podporo postopkov izdajanja računov za projekte, ki se razlikujejo od izdajanja običajnega računa za prodajni nalog.

> [!IMPORTANT]
> Zaradi teh razlik v aplikacijah Sales in Project Operations ne uporabljajte računov izmenično.

## <a name="invoice-header"></a>Glava računa

Naslednje informacije so na voljo v glavi predračuna v aplikaciji Project Operations.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **ID računa** | Zavihek **Povzetek** | ID se samodejno ustvari, ko je predračun ustvarjen. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje se uporablja kot sklic na vsak predračun. |
| **Ime** | Zavihek **Povzetek** | Privzeto nastavite na ime projektne pogodbe. To polje lahko ureja uporabnik. | &nbsp;  |
| **Valuta** | Zavihek **Povzetek** | Privzeto nastavite na valuto projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. |&nbsp; |
| **Cenik** | Zavihek **Povzetek** | Privzeto nastavite na cenik projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Priložnost** | Zavihek **Povzetek** | Sklic na povezano priložnost. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp;  |
| **Pogodba** | Zavihek **Povzetek** | Sklic na povezano projektno pogodbo. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Stranka** | Zavihek **Povzetek** | Sklic na povezano projektno pogodbo. Polje »samo za branje«, ki je zaklenjeno za urejanje. |&nbsp;  |
| **Opis** | Zavihek **Povzetek** | Besedilno polje, ki opisuje račun. To polje lahko ureja uporabnik. | &nbsp; |
| **Naslov plačnika** in povezana polja | **Zavihek »Povzetek«** | Stranka projektne pogodbe nastavi privzete nastavitve. To polje lahko ureja uporabnik.  | &nbsp; |
| **Stanje** | Zavihek **Povzetek** | Nastavi naslednje možnosti, ki jih lahko ureja uporabnik: **Dejavno**, **Zaprto**, **Plačano** in **Preklicano**. | Nepodprta stanja za aplikacijo Project Operations vključujejo **Zaprto** in **Preklicano**. </br> Ko je račun ustvarjen, je stanje nastavljeno na **Dejavno**. </br>Status naj bo nastavljen na **Plačano** šele po potrditvi računa. |
| **Stanje računa za projekt** | Zavihek **Povzetek** | Nastavi naslednje možnosti, ki jih lahko ureja uporabnik: **Osnutek**, **V pregledu** in **Potrjeno**. | V stanjih **Osnutek** in **V pregledu** je mogoče urejati račun. Po potrditvi računa ni mogoče urediti. |
| **Znesek podrobnosti** | Zavihek **Povzetek** | Vsota zneskov v vseh vrsticah računov po predplačilih in odbitkih. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje se uporablja za izračun končnega zneska. |
| **Popust (%)** | Zavihek **Povzetek** | To polje je mogoče urediti za vnos odstotka popusta. Funkcija aplikacije Project Operations tega polja ne podpira. | To je nepodprto polje. |
| **Znesek popusta** | Zavihek **Povzetek** | To polje je mogoče urediti za vnos zneska popusta. Funkcija aplikacije Project Operations tega polja ne podpira. | To je nepodprto polje. |
| **Znesek pred stroški prevoza** | **Zavihek »Povzetek«** | Skupni znesek računa po uveljavitvi popustov. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje se uporablja za izračun končnega zneska. |
| **Znesek prevoznine** | Zavihek **Povzetek** | To polje je mogoče urediti za vnos zneska stroškov prevoza. Funkcija aplikacije Project Operations tega polja ne podpira. | To je nepodprto polje. |
| **Skupni davki** | Zavihek **Povzetek** | Skupni davek iz vseh vrstic računa na računu. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Brez. |
| **Skupni znesek** | Zavihek **Povzetek** | Vsota zneska po popustih in davkih. | Vsota je znesek, ki ga mora kupec plačati. |
## <a name="project-based-invoice-lines"></a>Vrstice računov, ki temeljijo na projektu

V aplikaciji Project Operations je za vsako vrstico projektne pogodbe vedno ena vrstica računa. Vrstica računa se ustvari, tudi če ni dejanskega dela. Naslednje informacije so na voljo v vrstici predračuna.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **ID računa** | Zavihek **Splošno** | Sklic na ID računa. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Povezava ID računa se lahko uporabi za pomik nazaj v glavo računa. |
| **Ime** | Zavihek **Splošno** | Ime vrstice računa je privzeto nastavljeno iz imena podrobnosti pogodbe. To polje lahko ureja uporabnik. | &nbsp; |
| **Project** | Zavihek **Splošno** | Projekt v povezani vrstici projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Povezava projekta se lahko uporablja za pomik v projekt. |
| **Način obračunavanja** | Zavihek **Splošno** | Način obračunavanja v povezani vrstici projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Znesek vrstice pogodbe** | Zavihek **Splošno** | Znesek pogodbe v povezani vrstici projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Račun izdan do datuma** | Zavihek **Splošno** | Vsota zneskov v vseh podrobnostih vrstice računa na tem računu. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Znesek** | Zavihek **Splošno** | Vsota zneskov v vseh podrobnostih vrstice računa, ki so zaračunane, na tem računu. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje se uporablja za izračun končnega zneska v glavi računa. |
| **Davek** | Zavihek **Splošno** | Vsota davčnih zneskov v vseh podrobnostih vrstice računa na tej vrstici računa. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje se uporablja za izračun končnega davčnega zneska v glavi računa. |
| **Skupna vrednost postavk na računu** | Zavihek **Splošno** | Vsota skupnih zneskov (**Davek + zneski**) v vseh podrobnostih vrstice računa, ki se zaračunajo, na tej vrstici računa. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje se uporablja za izračun končnega zneska v glavi računa. |


## <a name="invoice-line-details"></a>Podrobnosti vrstice računa

Vsaka vrstica računa v računu projekta vključuje podrobnosti vrstice računa. Te podrobnosti vrstice se nanašajo na neobračunane dejanske vrednosti prodaje in mejnike, ki se nanašajo na podrobnosti pogodbe, na katere se sklicuje vrstica računa. Vse te transakcije so označene kot **Pripravljeno za izdajanje računov**.

Za vrstico **Račun za čas in material** so podrobnosti vrstice računa združene v možnosti **Plačljivo**, **Se ne zaračuna** in **Brezplačno** na strani **Vrstica računa**. Podatki **Vrstice računa, ki se zaračuna** se dodajo v skupno vrstico računa. **Brezplačno** in **Dejanske vrednosti, ki se ne zaračunaj** se ne štejejo v skupno vrstico računa.

Za vrstico **Račun s fiksno ceno** se podrobnosti vrstice računa ustvarijo iz mejnikov, ki so v povezanih podrobnostih pogodbe označeni kot **Pripravljen na račun**. Ko se iz mejnika ustvarijo podrobnosti vrstice računa, se stanje obračunavanja na mejniku posodobi na **Račun za stranko je ustvarjen**.

### <a name="edit-invoice-line-details"></a>Urejanje podrobnosti vrstice računa

Naslednja polja so na voljo v podrobnosti vrstice računa, ki temelji na dejanski prodajni vrednosti:

| Polje | Opis | Nadaljnji vpliv |
| --- | --- | --- |
| **Vrstica računa** | Sklic na **Vrstico ID računa**. Polje samo za branje, zaklenjeno za urejanje. | Ta povezava se lahko uporabi za pomik nazaj v glavo računa. |
| **Opis** | Opis podrobnosti vrstice računa. Privzeto nastavljeno iz polja **Interni komentarji** pod možnostjo **Vnos časa** in iz polja **Opis** pod možnostjo **Vnos stroškov**. To polje lahko ureja uporabnik.| &nbsp; |
| **Zunanji opis** | Opis podrobnosti vrstice računa. Privzeto nastavljeno iz polja **Zunanji komentarji** pod možnostjo **Vnos časa** in polje **Opis** pod možnostjo **Vnos stroškov**. To polje lahko ureja uporabnik. | Ta opis lahko uporabite, da določite, kaj naj bo na natisnjenem računu, ki bo poslan stranki. V aplikaciji Project Operations predračun nima vseh potrebnih funkcij za konfiguracijo nastavitev tiskanja za račun. |
| **Začetni datum** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela. |
| **Project** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Privzeto nastavljeno na projekt v povezani podrobnosti pogodbe. |
| **Opravilo** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | To polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela. Spustni seznam prikazuje vsa opravila, povezana s povezano vrstico projektne pogodbe.  |
| **Kategorija transakcije** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na dejanskemu viru. |
| **Vloga** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela. |
| **Vir, ki ga je mogoče rezervirati** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na dejanskemu viru. |
| **Enota vira** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela. |
| **Količina** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela. |
| **Urnik enote** | Za podrobnosti vrstice računa za čas je ta vedno nastavljen na čas in ga ni mogoče urejati. Za stroške je to privzeto nastavljeno iz vira stroškov dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Privzeto nastavljeno na **Čas** na novi podrobnosti vrstice računa, ki ne temelji na dejanskem delu. |
| **Enota** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela |
| **Cena** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Polje lahko uredite v novi podrobnosti vrstice računa, ki ne temelji na viru dejanskega dela. Če nobena vrednost ni vnesena, je privzeto nastavljena po **shranjevanju**. |
| **Valuta** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Privzeto nastavljeno iz glave računa pri ustvarjanju novih podrobnosti računa, ne da bi temeljile na dejanskem delu.  Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Znesek** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Izračunano kot **Količina \* Cena** pri ustvarjanju novih podrobnosti računa, ne da bi temeljile na dejanskem delu. Izračuna se po **shranjevanju**. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Davek** | Privzeto nastavljeno iz vira dejanskega dela. To polje lahko ureja uporabnik | Uporabni lahko polje ureja pri ustvarjanju novih podrobnosti računa, ne da bi temeljile na dejanskem delu. |
| **Skupna vrednost postavk na računu** | Polje z izračunom, izračunano kot **Znesek + davek**. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Vrsta obračunavanja** | Privzeto nastavljeno iz vira dejanskega dela. To polje lahko ureja uporabnik. | Izbira možnosti **Se zaračuna** doda vrstico v skupno vrstico računa. Možnosti **Brezplačno** in **Se ne zaračuna** jo izključita iz skupne vrstice računa. |
| **Izbira izdelka** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira. | Ko ustvarite novo podrobnost vrstice računa brez dejanske podpore, lahko to polje uredite. |
| **Izdelku** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira. | Ko ustvarite novo podrobnost vrstice računa brez dejanske podpore, lahko to polje uredite, če je polje **Izbira izdelka** nastavljeno na **Obstoječi izdelek**. |
| **Ime izdelka** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira. | V novi podrobnosti vrstice računa, kjer je ID izdelka izbran iz kataloga, je to polje nastavljeno na ime izdelka. Pri izdelku, ki ni v katalogu, je polje nastavljeno na ime, ki ni v katalogu. |
| **Opis izdelka, ki ni v katalogu** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira. | Ko ustvarite novo podrobnost vrstice računa brez dejanske podpore, lahko za izdelek dodate opis. |
| **Vrsta transakcije** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Privzeto nastavljeno na **Obračunana prodaja** in zaklenjeno pri ustvarjanju novih **Podrobnosti vrstice računa**, ne da bi temeljile na dejanskem delu.  |
| **Razred transakcije** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Privzeto nastavljeno glede na to, ali se uporabnik odloči ustvariti podrobnosti vrstice računa za **čas**, **stroške**, **material** ali **dajatve**, hkrati pa ustvari nove **podrobnosti vrstice računa** brez dejanske podpore. Zaklenjeno za urejanje. |

Naslednja polja so na voljo v podrobnosti vrstice računa, ki temelji na mejniku:

| Polje | Opis | Nadaljnji vpliv |
| --- | --- | --- |
| **Vrstica računa** | Sklic na **Vrstico ID računa**. Polje »samo za branje«, ki je zaklenjeno za urejanje. | Ta povezava se lahko uporabi za pomik nazaj v glavo računa. |
| **Opis** | Opis podrobnosti vrstice računa. Privzeto nastavljeno iz opisa vira mejnika. | &nbsp; |
|**Zunanji opis** | Opis podrobnosti vrstice računa, ki je privzeto nastavljena iz opisa vira mejnika. | To polje lahko uporabite, da določite, kaj naj bo na natisnjenem računu, ki bo poslan stranki. V aplikaciji Project Operations predračun nima vseh potrebnih funkcij za konfiguracijo nastavitev tiskanja za račun. |
| **Začetni datum** | Privzeto nastavljeno iz datuma **Mejnika** na podlagi vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Project** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Opravilo** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Kategorija transakcije** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Vloga** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Vir, ki ga je mogoče rezervirati** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Enota vira** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Urnik enote** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Enota** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Cena** | Privzeto nastavljeno iz zneska v viru mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Valuta** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. |&nbsp; |
| **Znesek** | Privzeto nastavljeno iz zneska v viru mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Davek** | Privzeto nastavljeno iz zneska davka v viru mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Skupna vrednost postavk na računu** | Privzeto nastavljeno iz skupne vrednosti postavk na računu v viru mejnika. To polje lahko ureja uporabnik | &nbsp; |
| **Vrsta obračunavanja** | Vedno privzeto nastavljeno na **Se zaračuna**. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Vrsta transakcije** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |
| **Razred transakcije** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Ustvarjanje novih podrobnosti vrstice računa

V vrsticah računa za čas in material lahko ustvarite nove podrobnosti vrstice računa. Te podrobnosti vrstice računa ne temeljijo na dejanskem delu. V vrstici računa vrstice računa za čas in material lahko izberete možnost **Novo**, da ustvarite novo podrobnost vrstice računa za razrede transakcij, ki so vključeni v podrobnosti pogodbe.

## <a name="refresh-invoice-transactions"></a>Osvežitev transakcij računa

Če imate podatke o dejanskem delu, ki ste jih dobili po ustvarjenem računu, lahko to dejansko delo vključite v račun.

1. V polju **Pogled nedokončanih opravil obračunavanja** podatke označite kot **Pripravljeno za izdajanje računov**.   
2. Odprite osnutek predračuna in na traku **Dejanja** kliknite **Osvežitev transakcij vrstice računa**.

  Tako ustvarite podrobnosti vrstice računa za vse dejansko delo, ki je že preteklo in je označeno kot **Pripravljeno za izdajanje računov**; vendar ni vključeno v račun.

## <a name="product-based-invoice-lines"></a>Vrstice računov, ki temeljijo na izdelkih

V aplikaciji Project Operations lahko ustvarite vrstice računov za izdelke, ki se ne nanašajo na noben projekt ali za vse projekte, skupaj z vrsticami računov, ki temeljijo na projektu. Te vrstice računov so ustvarjene kot podrobnosti pogodb, ki temeljijo na izdelkih, ko pa so označene kot pripravljene za izdajanje računov, so dodane kot vrstice računov, ki temeljijo na izdelkih.

Ko dodate vrstice računov, ki temeljijo na izdelkih, jih ni več mogoče spremeniti. Lahko pa jih izbrišete iz osnutka predračuna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
