---
title: Upravljanje predračuna, ki temelji na projektu
description: Ta tema vsebuje informacije o tem, kako upravljati in delati s predračuni, ki temeljijo na projektu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989346"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Upravljanje predračuna, ki temelji na projektu

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

V aplikaciji Dynamics 365 Project Operations so predračuni zgrajeni kot razširitev računov v aplikaciji Dynamics 365 Sales. Vendar pa obstajajo številne razlike pri postopku izdajanja računov med aplikacijama Sales in Project Operations, ko gre za izdajanje računov. V aplikaciji Project Operations iz strani **Seznam računov** na primer ni mogoče ustvariti novega računa, kar pa je mogoče v aplikaciji Sales. Te razlike in razširitve obstajajo za podporo postopkov izdajanja računov za projekte, ki se razlikujejo od izdajanja običajnega računa za prodajni nalog.

> [!IMPORTANT]
> Zaradi teh razlik v aplikacijah Sales in Project Operations ne uporabljajte računov izmenično.

## <a name="invoice-header"></a>Glava računa

Naslednje informacije so na voljo v glavi predračuna v aplikaciji Project Operations.

| Polje | LOkacija | Opis |
| --- | --- | --- | 
| **ID računa** | Zavihek **Povzetek** | ID se samodejno ustvari, ko je predračun ustvarjen. Polje »samo za branje«, ki je zaklenjeno za urejanje. To polje se uporablja kot sklic na vsak predračun. |
| **Ime** | Zavihek **Povzetek** | Privzeto nastavite na ime projektne pogodbe. To polje lahko uredite. | 
| **Valuta** | Zavihek **Povzetek** | Privzeto nastavite na valuto projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Cenik** | Zavihek **Povzetek** | Privzeto nastavite na cenik projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Priložnost** | Zavihek **Povzetek** | Sklic na povezano priložnost. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Pogodba** | Zavihek **Povzetek** | Sklic na povezano projektno pogodbo. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Stranka** | Zavihek **Povzetek** | Sklic na povezano projektno pogodbo. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Opis** | Zavihek **Povzetek** | Besedilno polje, ki opisuje račun. To polje lahko uredite. | 
| **Naslov plačnika** in povezana polja | **Zavihek »Povzetek«** | Stranka projektne pogodbe nastavi privzete nastavitve. To polje lahko uredite.  | 
| **Stanje** | Zavihek **Povzetek** | Nastavi naslednje možnosti: **Aktivno**, **Zaprto**, **Plačano** ter **Prekinjeno** in jih je mogoče urejati. Nepodprta stanja za aplikacijo Project Operations vključujejo **Zaprto** in **Preklicano**. </br> Ko je račun ustvarjen, je stanje nastavljeno na **Dejavno**. </br>Status naj bo nastavljen na **Plačano** šele po potrditvi računa.  | 
| **Stanje računa za projekt** | Zavihek **Povzetek** | Nastavi naslednje možnosti: **Osnutek**, **V pregledu** ter **Potrjeno** in jih je mogoče urejati. V stanjih **Osnutek** in **V pregledu** je mogoče urejati račun. Po potrditvi računa ni mogoče urediti. | 
| **Znesek podrobnosti** | Zavihek **Povzetek** | Vsota zneskov v vseh vrsticah računov po predplačilih in odbitkih. Polje »samo za branje«, ki je zaklenjeno za urejanje.  To polje se uporablja za izračun končnega zneska. | 
| **Popust (%)** | Zavihek **Povzetek** | To polje je mogoče urediti za vnos odstotka popusta. Funkcija aplikacije Project Operations tega polja ne podpira. To je nepodprto polje.|  
| **Znesek popusta** | Zavihek **Povzetek** | To polje je mogoče urediti za vnos zneska popusta. Funkcija aplikacije Project Operations tega polja ne podpira. To je nepodprto polje. |  
| **Znesek pred stroški prevoza** | **Zavihek »Povzetek«** | Skupni znesek računa po uveljavitvi popustov. Polje »samo za branje«, ki je zaklenjeno za urejanje. To polje se uporablja za izračun končnega zneska.  | 
| **Znesek prevoznine** | Zavihek **Povzetek** | To polje je mogoče urediti za vnos zneska stroškov prevoza. Funkcija aplikacije Project Operations tega polja ne podpira. To je nepodprto polje. |
| **Skupni davki** | Zavihek **Povzetek** | Skupni davek iz vseh vrstic računa na računu. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Skupni znesek** | Zavihek **Povzetek** | Vsota zneska po popustih in davkih. Vsota je znesek, ki ga mora kupec plačati. | 

## <a name="project-based-invoice-lines"></a>Vrstice računov, ki temeljijo na projektu

V aplikaciji Project Operations je za vsako vrstico projektne pogodbe vedno ena vrstica računa. Vrstica računa se ustvari, tudi če ni dejanskega dela. Naslednje informacije so na voljo v vrstici predračuna.

| Polje | LOkacija | Opis | 
| --- | --- | --- |
| **ID računa** | Zavihek **Splošno** | Sklic na ID računa. Polje »samo za branje«, ki je zaklenjeno za urejanje. Povezava ID računa se lahko uporabi za pomik nazaj v glavo računa. | 
| **Ime** | Zavihek **Splošno** | Ime vrstice računa je privzeto nastavljeno iz imena podrobnosti pogodbe. To polje lahko uredite. |
| **Project** | Zavihek **Splošno** | Projekt v povezani vrstici projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. Povezava projekta se lahko uporablja za pomik v projekt. | 
| **Način obračunavanja** | Zavihek **Splošno** | Način obračunavanja v povezani vrstici projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Znesek vrstice pogodbe** | Zavihek **Splošno** | Znesek pogodbe v povezani vrstici projektne pogodbe. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Račun izdan do datuma** | Zavihek **Splošno** | Vsota zneskov v vseh podrobnostih vrstice računa na tem računu. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Znesek** | Zavihek **Splošno** | Vsota zneskov v vseh podrobnostih vrstice računa, ki so zaračunane, na tem računu. Polje »samo za branje«, ki je zaklenjeno za urejanje. To polje se uporablja za izračun končnega zneska v glavi računa. | 
| **Davek** | Zavihek **Splošno** | Vsota davčnih zneskov v vseh podrobnostih vrstice računa na tej vrstici računa. Polje »samo za branje«, ki je zaklenjeno za urejanje. To polje se uporablja za izračun končnega davčnega zneska v glavi računa. | 
| **Skupna vrednost postavk na računu** | Zavihek **Splošno** | Vsota skupnih zneskov (**Davek + zneski**) v vseh podrobnostih vrstice računa, ki se zaračunajo, na tej vrstici računa. Polje »samo za branje«, ki je zaklenjeno za urejanje. To polje se uporablja za izračun končnega zneska v glavi računa. |

## <a name="invoice-line-details"></a>Podrobnosti vrstice računa

Vsaka vrstica računa v računu projekta vključuje podrobnosti vrstice računa. Te podrobnosti vrstice se nanašajo na neobračunane dejanske vrednosti prodaje in mejnike, ki se nanašajo na podrobnosti pogodbe, na katere se sklicuje vrstica računa. Vse te transakcije so označene kot **Pripravljeno za izdajanje računov**.

Za vrstico **Račun za čas in material** so podrobnosti vrstice računa združene v možnosti **Plačljivo**, **Se ne zaračuna** in **Brezplačno** na strani **Vrstica računa**. Podatki **Vrstice računa, ki se zaračuna** se dodajo v skupno vrstico računa. Možnosti **Brezplačno** in **Dejansko delo, ki se ne zaračuna** se ne seštejejo v skupno vrstico računa.

Za vrstico **Račun s fiksno ceno** se podrobnosti vrstice računa ustvarijo iz mejnikov, ki so v povezanih podrobnostih pogodbe označeni kot **Pripravljen na račun**. Ko se iz mejnika ustvarijo podrobnosti vrstice računa, se stanje obračunavanja na mejniku posodobi na **Račun za stranko je ustvarjen**.

### <a name="edit-invoice-line-details"></a>Urejanje podrobnosti vrstice računa

Naslednja polja so na voljo v podrobnosti vrstice računa, ki temelji na neobračunani dejanski prodaji.

| Polje | Opis |
| --- | --- | 
| **Vrstica računa** | Sklic na **Vrstico ID računa**. To polje je samo za branje in zaklenjeno za urejanje. Ta povezava se lahko uporabi za pomik nazaj v glavo računa. | 
| **Opis** | Opis podrobnosti vrstice računa. Privzeto nastavljeno iz polja **Interni komentarji** pod možnostjo **Vnos časa** in iz polja **Opis** pod možnostjo **Vnos stroškov**. Polje lahko uredite.| 
| **Zunanji opis** | Opis podrobnosti vrstice računa. Privzeto nastavljeno iz polja **Zunanji komentarji** pod možnostjo **Vnos časa** in polje **Opis** pod možnostjo **Vnos stroškov**. Polje lahko uredite. Ta opis lahko uporabite, da določite, kaj naj bo na natisnjenem računu, ki bo poslan stranki. V aplikaciji Project Operations predračun nima vseh potrebnih funkcij za konfiguracijo nastavitev tiskanja za račun. | 
| **Datum začetka** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira. |
| **Project** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira do projekta v povezanih podrobnostih pogodbe. |  
| **Opravilo** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Kategorija transakcije** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Vloga** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |  
| **Vir, ki ga je mogoče rezervirati** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Podjetje, ki zagotavlja vire** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Enota vira** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Količina** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |  
| **Razpored enote** | Za podrobnosti vrstice računa za čas je ta vedno nastavljen na čas in ga ni mogoče urejati. Za stroške je to privzeto nastavljeno iz vira stroškov dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Enota** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |  
| **Cena** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Valuta** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Znesek** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Davek** | Privzeto nastavljeno iz vira dejanskega dela. Polje lahko uredite.| 
| **Skupna vrednost postavk na računu** | Polje z izračunom, izračunano kot **Znesek + davek**. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Vrsta obračunavanja** | Privzeto nastavljeno iz vira dejanskega dela. Polje lahko uredite. Izbira možnosti **Se zaračuna** doda vrstico v skupno vrstico računa. Možnosti **Brezplačno** in **Se ne zaračuna** jo izključita iz skupne vrstice računa.| 
| **Izbira izdelka** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Izdelku** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Ime izdelka** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |  
| **Opis izdelka, ki ni v katalogu** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Vrsta transakcije** | To polje je samo za branje, ki je privzeto nastavljeno iz dejanskega vira do **obračunanih prodaj**. |  
| **Razred transakcije** | Privzeto nastavljeno iz vira dejanskega dela. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 

Naslednja polja so na voljo v podrobnosti vrstice računa, ki temelji na mejniku.

| Polje | Opis |
| --- | --- | 
| **Vrstica računa** | Sklic na **Vrstico ID računa**. Polje »samo za branje«, ki je zaklenjeno za urejanje. Ta povezava se lahko uporabi za pomik nazaj v glavo računa.  | 
| **Opis** | Opis podrobnosti vrstice računa. Privzeto nastavljeno iz opisa vira mejnika. | 
|**Zunanji opis** | Opis podrobnosti vrstice računa, ki je privzeto nastavljena iz opisa vira mejnika. To polje lahko uporabite, da določite, kaj naj bo na natisnjenem računu, ki bo poslan stranki. V aplikaciji Project Operations predračun nima vseh potrebnih funkcij za konfiguracijo nastavitev tiskanja za račun. | 
| **Začetni datum** | Privzeto nastavljeno iz datuma **Mejnika** na podlagi vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Project** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Opravilo** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Kategorija transakcije** | Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Vloga** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Vir, ki ga je mogoče rezervirati** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Enota vira** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Urnik enote** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Enota** | Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Cena** | Privzeto nastavljeno iz zneska v viru mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Valuta** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Znesek** | Privzeto nastavljeno iz zneska v viru mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Davek** | Privzeto nastavljeno iz zneska davka v viru mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Skupna vrednost postavk na računu** | Privzeto nastavljeno iz skupne vrednosti postavk na računu v viru mejnika. Polje lahko uredite. | 
| **Vrsta obračunavanja** | Vedno privzeto nastavljeno na **Se zaračuna**. Polje »samo za branje«, ki je zaklenjeno za urejanje. |
| **Vrsta transakcije** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 
| **Razred transakcije** | Privzeto nastavljeno iz vira mejnika. Polje »samo za branje«, ki je zaklenjeno za urejanje. | 

## <a name="refresh-invoice-transactions"></a>Osvežitev transakcij računa

Če imate podatke o dejanskem delu, ki ste jih dobili po ustvarjenem računu, lahko to dejansko delo vključite v račun.

1. V polju **Pogled nedokončanih opravil obračunavanja** podatke označite kot **Pripravljeno za izdajanje računov**.   
2. Odprite osnutek predračuna in na traku **Dejanja** izberite **Osveži transakcije v vrstici računa**.

  Podrobnosti vrstice računa se ustvarijo za vse pretekle dejanske vrednosti, ki so označene kot **Pripravljen na račun**, vendar niso vključene v račun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
