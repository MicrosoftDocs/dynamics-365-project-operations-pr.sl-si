---
title: Ocenjevanje podrobnosti projektne ponudbe
description: Ta tema vsebuje informacije, kako ustvariti oceno podrobnosti projektne ponudbe.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003971"
---
# <a name="estimate-a-project-quote-line"></a>Ocenjevanje podrobnosti projektne ponudbe

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Vrstica ponudbe, ki temelji na projektu, vsebuje podrobnosti, ki pomagajo pri oceni stroškov in potencialnih prihodkov od dela, ki so povezani z uresničitvijo vrstice ponudbe.

Za oceno vrstice ponudbe, ki temelji na projektu, v vrstici ponudbe izberite zavihek **Podrobnosti vrstice ponudbe**. Obstajata dva načina za izdelavo ocene vrstice ponudbe, ki temelji na projektu:

   - Oceno ročno ustvarite neposredno na vrstici ponudbe z uporabo podrobnosti vrstice ponudbe. 
   - Ustvarite projekt in načrt projekta ter nato projekt in opravila na projektu povežite z vrstico ponudbe. Omogočen bo postopek uvoza ocen iz načrta projekta v vrstico ponudbe na podlagi podatkov, ki ste jih navedli.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Ustvarjanje ocen iz projekta neposredno v vrstici ponudbe, ki temelji na projektu

Za ustvarjanje ocen neposredno na v vrstici ponudbe, ki temelji na projektu, upoštevajte naslednje korake:

1. Če želite ustvariti oceno na vrstici ponudbe, ki temelji na projektu, izberite zavihek **Podrobnosti vrstice ponudbe**. V elementu vrstice, ki ga ustvarite na tem zavihku, bo povzeta ponudbena vrednost te vrstice ponudbe. 
2. Za ustvarjanje podrobnosti vrstice pogodbe izberite **Nove podrobnosti vrstice ponudbe** v podmreži **Podrobnosti vrstice ponudbe**. Odpre se drsnik za hitro ustvarjanje. Naslednja polja na strani **Vrstica ponudbe**.

| **Polje** | **LOkacija** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Opis | Hitro ustvari | Opis posamezne ocene | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Razred transakcije | Hitro ustvari | Ta spustni seznam vsebuje razrede transakcij, ki so za vrstico ponudbe, ki temelji na projektu, vključeni na zavihku **Splošno**.  | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Izbira izdelka | Hitro ustvari | Velja, ko je razred transakcije **Material**. Določite lahko, da je ta vrstica ocene predvidena za **obstoječ** izdelek (iz kataloga) ali izdelek, **ki ni v katalogu**. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Izdelku | Hitro ustvari | ID izdelka iz kataloga izdelkov. To polje je omogočeno le, ko izberete **Obstoječ izdelek** v polju **Izberite izdelek**. ID se uporablja za pridobivanje prodajne cene iz cenika projekta na ponudbi. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Izdelek, ki ni v katalogu | Hitro ustvari | Besedilno polje za zapis imena izdelka. To polje je omogočeno le, če izberete **Izdelek, ki ni v katalogu** v polju **Izberite izdelek**.| Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Vloga | Hitro ustvari | Vloga osebe, ki bo opravila to delo ali povzročila te stroške. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Kategoriji | Hitro ustvari | Kategorija dela ali stroška. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Datum začetka | Hitro ustvari | Začetni datum dela. | To polje privzeto pripiše podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Datum konca | Hitro ustvari | Končni datum dela. | To polje privzeto pripiše podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Podjetje, ki zagotavlja vire | Hitro ustvarjanje | Podjetje, ki zagotavlja vire, ali pravna oseba, ki ima te stroške in zagotavlja vire za delo na njih. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške in se uporabi za pridobivanje lastne cene. |
| Enota vira | Hitro ustvari | Enota vira, ki ima te stroške in zagotavlja vire za delo na njih. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške in se uporabi za pridobivanje lastne cene. |
| Urnik enote | Hitro ustvari | Skupina enot dela, izdelka ali stroška. Enote pripadajo razporedu enot ali skupini enot. Na primer milje in kilometri (km) so enote, ki spadajo v skupino enot, ki opisuje razdaljo. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Enota | Hitro ustvari | Skupina enot dela, izdelka ali stroška. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Količina | Hitro ustvari | Količina dela, izdelkov ali stroškov. | Ta vrednost privzeto pripiše povezane podrobnosti vrstice ponudbe za samodejno ustvarjene stroške. |
| Cena enote | Hitro ustvarjanje |Obračunska stopnja vloge, ki opravlja delo, cena na enoto izdelka ali prodajna cena izdelka ali kategorije stroškov. Privzeta vrednost za **Čas** temelji na kombinaciji vrednosti cenovne razsežnosti za cenovno vrstico vloge v ceniku projekta, ki začne veljati z datumom začetka. Privzeta vrednost za **stroške** se pridobi iz nastavitev cene za kategorijo transakcij v ceniku projekta, ki začne veljati z datumom začetka. Če način določanja cen za kategorijo transakcij ni »cena na enoto«, privzete vrednost ni in to polje ostane prazno. Pri izdelkih privzeta vrednost tega polja temelji na vrstici **Elemente cenika** v ceniku projekta, ki začne veljati z datumom začetka.| Mera stroškov vloge, ki opravlja delo, cena na enoto kategorije stroškov ali izdelka. Privzeta vrednost za **Čas** temelji na kombinaciji vrednosti cenovne razsežnosti za cenovno vrstico vloge v ceniku z lastnimi cenami, ki je priložen pogodbeni enoti in začne veljati z datumom začetka. Privzeta vrednost za stroške temelji na kategoriji cenovne vrstice za cenik z lastnimi cenami, ki je priložen pogodbeni enoti in začne veljati z datumom začetka. Če način določanja cen za kategorijo transakcij ni cena na enoto, ni privzete vrednosti, to polje pa ostane prazno. Za izdelke privzeta vrednost za polje temelji na vrstici **Elementa cenika** v ceniku z lastnimi cenami, ki je priložen pogodbeni enoti in začne veljati z datumom začetka.|
| Predvideni davek | Hitro ustvari | Za to delo ali strošek lahko ročno vnesete predvideni davek. | To polje nima nadaljnjega vpliva. |
| Znesek | Hitro ustvari | V to polje lahko ročno vnesete podatke, če sta polji **Količina** in **Cena** prazni. Če polji nista prazni, je to polje samo za branje in se izračuna z obrazcem (Količina \* Cena na enoto) + davek. | To polje nima nadaljnjega vpliva. |

## <a name="update-prices-on-quote-line-details"></a>Posodobitev cen v podrobnostih vrstice ponudbe

Če ste spremenili cene na ceniku projekta, ki je priložen ponudbi, ali na ceniku naročnika, lahko na strani **Ponudba** izberete možnost **Izračunaj znova**, da osvežite cene na podrobnostih posamezne vrstice ponudbe za odražanje vnesenih sprememb. Ko izberete možnost **Preračunaj**, se prikaže opozorilo, ki vas obvesti, da bodo cene na podrobnostih vrstic ponudbe za vse postavke ponudb ponastavljene. Izberite možnost **Da**, da osvežite cene za prodajo in podrobnosti cen v vrstici ponudbe.

## <a name="access-quote-line-details-for-cost"></a>Dostop do podrobnosti vrstice ponudbe za cene

Za dostop do podrobnosti vrstice ponudbe upoštevajte te korake:

1. V zavihku **Podrobnosti vrstice ponudbe** izberite vrstico v mreži, da v orodni vrstici podmreže omogočite dejanja. 
2. Izberite možnost **Odpri podrobnosti cene** če si želite ogledati pripadajočo stopnjo stroškov in znesek za to vrstico ponudbe.

> [!NOTE]
> Sprememba vrednosti virov enote, količine, datumov, vloge ali kategorije v podrobnostih vrstice ponudbe za stroške spremeni pripadajoče vrednosti podrobnosti v vrstici ponudbe za prodajo.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta v podrobnostih vrstice ponudbe za stroške in prodajo

Valuta na podrobnostih vrstice ponudbe za privzete prodajne vrednosti iz cenika projekta, ki začne veljati z datumom začetka podrobnosti vrstice ponudbe.

Valuta na podrobnostih vrstice ponudbe za privzete cene iz cenika pogodbene enote za ponudbo, ki začne veljati z datumom začetka podrobnosti vrstice ponudbe za ceno.

> [!NOTE]
> Izračuni donosnosti pretvorijo znesek v podrobnostih vrstice ponudbe za stroške in prodajo v osnovno valuto okolja za poročilo o celotni ocenjeni marži za ponudbo. Pride lahko do napak pri zaokroževanju valut in spremenjenih marž zaradi pomanjkanja menjalnih tečajev, veljavnih na datum. Te izračune uporabljajte samo za projektne ponudbe, saj gre za približke in ne za dejansko zakonsko ali drugo poročanje, ki zahteva večjo natančnost zaokroževanja in zavedanje datuma začetka veljave za menjalne tečaje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
