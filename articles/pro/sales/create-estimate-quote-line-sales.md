---
title: Ocenjevanje vrstice ponudbe, ki temelji na projektih
description: Ta tema vsebuje informacije o tem, kako ustvariti oceno za vrstico ponudbe, ki temelji na projektih.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273572"
---
# <a name="estimating-a-project-based-quote-line"></a>Ocenjevanje vrstice ponudbe, ki temelji na projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Vrstica ponudbe, ki temelji na projektu, vsebuje podrobnosti, ki pomagajo pri oceni stroškov in potencialnih prihodkov od dela, ki so povezani z uresničitvijo vrstice ponudbe.

Za oceno vrstice ponudbe, ki temelji na projektu, v vrstici izberite zavihek **Podrobnosti vrstice ponudbe**. Obstajata dva načina za izdelavo ocene za vrstici ponudbe, ki temelji na projektu:

- Oceno ročno ustvarite neposredno na vrstici ponudbe z uporabo podrobnosti vrstice ponudbe. 
- Ustvarite projekt in načrt projekta ter nato projekt in opravila na projektu povežite z vrstico ponudbe. Omogočen bo postopek uvoza ocen iz načrta projekta v vrstico ponudbe na podlagi podatkov, ki ste jih navedli.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Ustvarjanje ocen iz projekta neposredno v vrstici ponudbe, ki temelji na projektu

Če želite ustvariti oceno na vrstici ponudbe, ki temelji na projektu, izberite zavihek **Podrobnosti vrstice ponudbe**. V elementu vrstice, ki ga ustvarite na tem zavihku, bo povzeta ponudbena vrednost te vrstice ponudbe. 

Za ustvarjanje podrobnosti vrstice pogodbe izberite **+ Nove podrobnosti vrstice ponudbe** v podmreži **Podrobnosti vrstice ponudbe**. Odpre se drsnik za hitro ustvarjanje. Oblikujejo se naslednja polja na obrazcu **Vrstica ponudbe**:

| **Polje** | **Mesto** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Opis | Hitro ustvari | Opis posamezne ocene | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Razred transakcije | Hitro ustvari | Ta spustni seznam vsebuje razrede transakcij, ki so za vrstico ponudbe, ki temelji na projektu, vključeni na zavihku **Splošno**.  | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Vloga | Hitro ustvari | Oseba, ki bo opravila to delo ali bo povzročila ta strošek. | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Kategoriji | Hitro ustvari | Kategorija dela ali stroška | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Datum začetka | Hitro ustvari | Začetni datum dela | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Končni datum | Hitro ustvari | Končni datum dela | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Enota vira | Hitro ustvari | Enota vira, ki povzroči te stroške in zagotovil vire za delo. | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. To polje se uporablja tudi pri pridobivanju lastne cene. |
| Urnik enote | Hitro ustvari | Skupina enot dela ali stroškov. Enote pripadajo razporedu enot ali skupini enot. Na primer; milje in kilometri so enote, ki spadajo v skupino enot za merjenje razdalj. | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Enota | Hitro ustvari | Enota dela ali stroška | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Količina | Hitro ustvari | Količina enot dela ali stroškov | S tem poljem so privzeto povezane samodejno ustvarjene podrobnosti vrstice ponudbe za stroške. |
| Cena enote | Hitro ustvari | Obračunska stopnja vloge, ki opravlja delo, ali prodajna cena kategorije stroškov. To polje privzame čas na podlagi kombinacije vloge in enote vira v ceniku projekta, ki velja na datum začetka. Za stroške to polje privzame nastavitve cen za kategorijo transakcij v ceniku projekta, ki velja za datum začetka. Če način določanja cen za kategorijo transakcij ni »cena na enoto«, privzete vrednost ni in to polje ostane prazno. | Mera stroškov vloge, ki opravlja delo, ali »cena na enoto« za kategorijo stroškov To polje privzame čas na podlagi kombinacije vloge in enote vira glede na ceno v pogodbeni enoti cenika ponudbe, ki velja na datum začetka. Za stroške to polje privzame nastavitve cen za kategorijo transakcij v ceniku pogodbene enote, ki velja na datum začetka. Če način določanja cen za kategorijo transakcij ni »cena na enoto«, privzete vrednost ni in to polje ostane prazno. |
| Predvideni davek | Hitro ustvari | Za to delo ali strošek lahko ročno vnesete predvideni davek. | To polje nima nadaljnjega vpliva. |
| Znesek | Hitro ustvari | V to polje lahko ročno vnesete podatke, če sta polji **Količina** in **Cena** prazni. Če polji nista prazni, je to polje samo za branje in se izračuna z obrazcem (Količina \* Cena na enoto) + davek. | To polje nima nadaljnjega vpliva. |

## <a name="update-prices-on-quote-line-details"></a>Posodobitev cen v podrobnostih vrstice ponudbe

Če ste spremenili cene na ceniku projekta, ki je priložen ponudbi, ali na ceniku naročnika, lahko na strani **Ponudba** izberete možnost **Izračunaj znova**, da osvežite cene na podrobnostih posamezne vrstice ponudbe za odražanje vnesenih sprememb. Če izberete **Izračunaj znova**, se prikaže opozorilo, ki vas obvesti, da bodo ponastavljene cene na podrobnostih vrstice ponudbe za vse vrstice. Izberite možnost **Da**, da osvežite cene za prodajo in podrobnosti cen v vrstici ponudbe.

## <a name="access-quote-line-details-for-cost"></a>Dostop do podrobnosti vrstice ponudbe za cene

Na zavihku **Podrobnosti vrstice ponudbe** izberite vrstico v mreži za omogočanje dejanj na orodni vrstici podmreže. Prvo dejanje v orodni vrstici podmreže, ko so izbrane podrobnosti vrstice ponudbe, je **Odpri podrobnosti cene**. Izberite možnost **Odpri podrobnosti cene** če si želite ogledati pripadajočo stopnjo stroškov in znesek za to vrstico ponudbe.

> [!NOTE]
> Sprememba vrednosti virov enote, količine, datumov, vloge ali kategorije v podrobnostih vrstice ponudbe za stroške spremeni pripadajoče vrednosti podrobnosti v vrstici ponudbe za prodajo.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta v podrobnostih vrstice ponudbe za stroške in prodajo

Valuta na podrobnostih vrstice ponudbe za privzame prodajne vrednosti iz cenika projekta, ki velja za datum začetka podrobnosti vrstice ponudbe.

Valuta v podrobnostih vrstice ponudbe privzame prodajne vrednosti iz cenika enote naročnika iz ponudbe, ki velja na datum začetka podrobnosti vrstice ponudbe za ceno.

Izračuni donosnosti pretvorijo znesek v podrobnostih vrstice ponudbe za stroške in prodajo v osnovno valuto okolja za poročilo o celotni ocenjeni marži za ponudbo.

Tako lahko pride do napake pri zaokroževanju in spremembe marže, saj manjkajo menjalni tečaji, ki so občutljivi na datum. Te izračune za projektnih ponudbe uporabite samo kot približke in ne kot dejansko zakonsko ali drugo poročanje, ki zahteva večjo natančnost zaokroževanja in zavedanje pomembnosti datuma za menjalne tečaje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]