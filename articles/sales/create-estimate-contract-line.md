---
title: Ocenjevanje podrobnosti pogodbe, ki temelji na projektu
description: V tej temi so na voljo informacije o ocenjevanju podrobnosti pogodbe, ki temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cdc8984e080d995e3a0b667fe662291b499235b2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278528"
---
# <a name="estimate-a-projectbased-contract-line"></a>Ocenjevanje podrobnosti pogodbe, ki temelji na projektu

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_ 

V storitvi Dynamics 365 Project Operations imajo podrobnosti pogodbe, ki temelji na projektu, podrobnosti, ki pomagajo oceniti strošek in možne prihodke dela, vključenega v zagotavljaje podrobnosti pogodbe.

Za ocenjevanje podrobnosti pogodbe, ki temelji na projektu, odprite zavihek **Podrobnosti vrstice pogodbe** za **Podrobnosti pogodbe**, ki temelji na projektu.  Obstajata dva načina za ustvarjanje ocene za podrobnosti pogodbe, ki temelji na projektu:

   - Ustvarjanje ocene neposredno na podrobnostih pogodbe z ročnim dodajanjem podrobnosti vrstice pogodbe.
   - Ustvarjanje projekta in projektnega načrta, nato pa povezovanje projekta in opravila s podrobnostmi pogodbe. To omogoča proces, po katerem lahko uvozite oceno projektnega načrta v podrobnost pogodbe na podlagi komponent, vključenih v podrobnosti pogodbe.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Ustvarjanje ocene neposredno v podrobnostih pogodbe, ki temelji na projektu

1. Pojdite v podrobnosti pogodbe in izberite zavihek **Podrobnost vrstice pogodbe**. Vrstice, ki jih ustvarite v tem zavihku, so povzete in prikazane kot **Pogodbena vrednost** za to možnost **Podrobnosti pogodbe**. 
2. V podmreži **Podrobnosti pogodbe** izberite **+ Nove podrobnosti vrstice pogodbe**. Odpre se drsnik za hitro ustvarjanje. Naslednja polja so na voljo na obrazcu **Podrobnosti vrstice pogodbe**:

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **Opis** | **Hitro ustvarjanje** | Opis posamezne ocene | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Razred transakcije** | **Hitro ustvarjanje** | Ta spustni seznam je seznam razredov transakcij, vključen na zavihku **Splošno** podrobnosti pogodbe, ki temelji na projektu. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Vloga** | **Hitro ustvarjanje** | Vloga osebe, ki opravlja to delo ali ima ta strošek. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Kategorija** | **Hitro ustvarjanje** | Kategorija dela ali stroška. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Začetni datum** | **Hitro ustvarjanje** | Začetni datum dela. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Končni datum** | **Hitro ustvarjanje** | Končni datum dela. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za strošek, ki je samodejno ustvarjen. |
| **Podjetje, ki zagotavlja vire** | **Hitro ustvarjanje** | Podjetje, ki zagotavlja vire, ali pravna entiteta, ki ima ta strošek in zagotavlja vir za delo na njem. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. To polje se uporablja tudi pri pridobivanju lastne cene. |
| **Enota vira** | **Hitro ustvarjanje** | Enota vira, ki ima ta strošek in zagotavlja vir za delo na njem. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. To polje se uporablja tudi pri pridobivanju lastne cene. |
| **Urnik enote** | **Hitro ustvari** | Skupina enot za delo ali strošek. Enote pripadajo razporedu enot ali skupini enot. Na primer, *milje* in *km* so enote, ki spadajo v skupino enot, ki opisujejo razdaljo. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Enota** | **Hitro ustvarjanje** | Enota za delo ali strošek. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Količina** | **Hitro ustvarjanje** | Količina za delo ali strošek. | To polje se privzeto nastavi na povezane podrobnosti vrstic pogodbe za stroške, ki so samodejno ustvarjeni. |
| **Cena enote** | **Hitro ustvarjanje** | Delež obračunavanja za vlogo, ki izvaja delo ali prodajno ceno kategorije stroška. To polje se privzeto nastavi za **Čas** na podlagi kombinacije vloge in enote vira v ceniku projekta, ki velja na datum začetka. Za stroške je privzeto za to polje iz nastavitve cene za kategorijo transakcij v projektnem ceniku, ki je veljaven na začetni datum. Če način določanja cen za kategorijo transakcij ni **cena na enoto**, privzete vrednost ni in to polje ostane prazno. | Mera stroškov za vlogo, ki izvaja delo ali strošek na enoto kategorije stroška. To polje se privzeto nastavi za **Čas na podlagi vloge** in kombinacija enote vira na vrstici cene vloge stroškovnega cenika, priloženega pogodbeni enoti z veljavnostjo za začetni datum. Za stroške privzeto za to polje temelji na vrstici cene kategorije stroškovnega cenika, priloženega k pogodbeni enoti, ki je veljavna na začetni datum. Če način določanja cen za kategorijo transakcij ni »cena na enoto«, privzete vrednost ni in to polje ostane prazno. |
| **Predvideni davek** | **Hitro ustvarjanje** | Predvideni davek za to delo ali strošek vnese uporabnik. | Predvideni davek za to delo ali strošek vnese uporabnik. |
| **Znesek** | **Hitro ustvarjanje** | To vrednost v tem polju lahko doda uporabnik, če sta polji **Količina** in **Cena** puščeni prazni. Če sta polji **Količina** in **Cena** izpolnjeni je polje **Znesek** samo za branje in je izračunano kot **(Količina\*cena enote) + davek**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Posodobitev cen na podrobnostih vrstic pogodbe

Če spremenite cene na projektnem ceniku, ki je priložen pogodbi ali stroškovnem ceniku pogodbene enote, lahko osvežite cene na posameznih podrobnostih vrstice postavke, da odražajo spremembo. Na strani **Pogodba** izberite **Preračunavanje**. Odpre se opozorilo, ki vas obvesti, da so cene za vse podrobnosti pogodbe v tej pogodbi ponastavljene. Izberite **Da** za osvežitev cen za prodajne in stroškovne podrobnosti vrstice pogodbe.

## <a name="access-contract-line-details-for-cost"></a>Dostop do podrobnosti vrstice pogodbe za strošek

Na zavihku **Podrobnosti vrstice pogodbe** izberite vrstico v mreži za prikaz dejanj na orodni vrstici podmreže. Prvo dejanje v orodni vrstici podmreže je **Odpri podrobnosti cene**. Če si želite ogledati povezano mero stroškov in znesek za to podrobnost vrstice pogodbe, izberite **Odpri podrobnosti cene**. 

> [!NOTE]
> Spreminjanje vrednosti podjetja, ki zagotavlja vire, enote vira, količine, datumov, vloge ali kategorije na podrobnosti vrstice pogodbe za **Strošek** spremeni tudi pripadajoče vrednosti na podrobnostih vrstice pogodbe za možnost **Prodaja**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta na podrobnostih vrstice pogodbe za strošek in prodajo

Podrobnosti vrstice pogodbe za možnost **Prodaja** nastavi privzeto valuto iz projektnega cenika, ki je veljaven za začetni datum podrobnosti vrstice pogodbe.

Podrobnosti vrstice pogodbe za možnost **Strošek** nastavi privzeto valuto iz projektnega cenika pogodbene enote pogodbe, ki je veljavna za začetni datum podrobnosti vrstice pogodbe za **Strošek**.

Izračuni dobičkonosnosti pretvorijo zneske za podrobnosti vrstice pogodbe za možnost **Strošek** in **Prodaja** v osnovno valuto okolja za poročanje splošne dejanske in ocenjene marže pogodbe.

> [!NOTE]
> Pride lahko do napak pri zaokroževanju valut in spremenjenih marž zaradi pomanjkanja menjalnih tečajev, veljavnih na datum. Uporabite te izračune za projektne pogodbe samo kot približke in ne za dejansko zakonito ali drugačno poročanje, za katerega je potrebna večja natančnost zaokroževanje in ozaveščenosti o datumski veljavnosti za menjalne tečaje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]