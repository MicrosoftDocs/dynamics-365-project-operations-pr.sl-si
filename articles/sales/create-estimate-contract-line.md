---
title: Ocena podrobnosti projektne pogodbe
description: Ta članek vsebuje informacije o ocenah v vrstici projektne pogodbe.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 553f7e4a9e9f57732267a48da2b299c1751b0c0e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932040"
---
# <a name="estimate-a-project-contract-line"></a>Ocena podrobnosti projektne pogodbe

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_ 

V storitvi Dynamics 365 Project Operations imajo podrobnosti pogodbe, ki temelji na projektu, podrobnosti, ki pomagajo oceniti strošek in možne prihodke dela, vključenega v zagotavljaje podrobnosti pogodbe.

Za ocenjevanje podrobnosti pogodbe, ki temelji na projektu, odprite zavihek **Podrobnosti vrstice pogodbe** za **Podrobnosti pogodbe**, ki temelji na projektu.  Obstajata dva načina za ustvarjanje ocene za podrobnosti pogodbe, ki temelji na projektu:

   - Ustvarjanje ocene neposredno na podrobnostih pogodbe z ročnim dodajanjem podrobnosti vrstice pogodbe.
   - Ustvarjanje projekta in projektnega načrta, nato pa povezovanje projekta in opravila s podrobnostmi pogodbe. To omogoča proces, po katerem lahko uvozite oceno projektnega načrta v podrobnost pogodbe na podlagi komponent, vključenih v podrobnosti pogodbe.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Ustvarjanje ocen neposredno na projektu v podrobnosti pogodbe

Za ustvarjanje ocen neposredno na projektu v podrobnosti pogodbe, upoštevajte naslednje korake:

1. Pojdite v podrobnosti pogodbe in izberite zavihek **Podrobnost vrstice pogodbe**. Vrstice, ki jih ustvarite v tem zavihku, so povzete in prikazane kot **Pogodbena vrednost** za to možnost **Podrobnosti pogodbe**. 
2. V podmreži **Podrobnosti pogodbe** izberite **Nove podrobnosti pogodbe**. Odpre se drsnik za hitro ustvarjanje. Naslednja polja so na voljo na strani **Podrobnosti pogodbe**.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **Opis** | **Hitro ustvarjanje** | Opis posamezne ocene | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Razred transakcije** | **Hitro ustvarjanje** | Ta seznam razredov transakcij je vključen v zavihku **Splošno** pri podrobnostih pogodbe, ki temelji na projektu. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Izbira izdelka** | **Hitro ustvari** | Velja, ko je razred transakcije **Material**. Določite lahko, da je ta vrstica ocene predvidena za **obstoječ** izdelek (iz kataloga) ali izdelek, **ki ni v katalogu**. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Izdelku** | **Hitro ustvari** | ID izdelka iz kataloga izdelkov. To polje je omogočeno le, če izberete **Obstoječ izdelek** v polju **Izberite izdelek**. ID se uporablja za pridobivanje prodajne cene iz cenika projekta na pogodbi. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Izdelek, ki ni v katalogu** | **Hitro ustvari** | Besedilno polje za vnos imena izdelka. To polje je omogočeno le, če izberete **Izdelek, ki ni v katalogu** v polju **Izberite izdelek**.| Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Vloga** | **Hitro ustvarjanje** | Vloga osebe, ki opravlja to delo ali ima ta strošek. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške.|
| **Kategoriji** | **Hitro ustvarjanje** | Kategorija dela ali stroška. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške.|
| **Datum začetka** | **Hitro ustvarjanje** | Začetni datum dela. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Končni datum** | **Hitro ustvarjanje** | Končni datum dela. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Podjetje, ki zagotavlja vire** | **Hitro ustvarjanje** | Podjetje, ki zagotavlja vire, ali pravna oseba, ki ima te stroške in zagotavlja vire za delo na njih. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške in se uporabi za pridobivanje lastne cene. |
| **Enota vira** | **Hitro ustvarjanje** | Enota vira, ki ima te stroške in zagotavlja vire za delo na njih. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške in se uporabi za pridobivanje lastne cene. |
| **Urnik enote** | **Hitro ustvari** | Skupina enot dela, izdelka ali stroška. Enote pripadajo razporedu enot ali skupini enot. Na primer *milje* in *kilometri (km)* so enote, ki spadajo v skupino enot, ki opisujejo razdaljo. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Enota** | **Hitro ustvarjanje** | Skupina enot dela, izdelka ali stroška. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Količina** | **Hitro ustvarjanje** | Količina dela, izdelkov ali stroškov. | Ta vrednost privzeto pripiše povezane podrobnosti pogodbe za samodejno ustvarjene stroške. |
| **Cena enote** | **Hitro ustvarjanje** | Obračunska stopnja vloge, ki opravlja delo, cena na enoto izdelka ali prodajna cena izdelka ali kategorije stroškov. Privzeta vrednost za **Čas** temelji na kombinaciji vrednosti cenovne razsežnosti za cenovno vrstico vloge v ceniku projekta, ki začne veljati z datumom začetka. Privzeta vrednost za polje **Stroški** se pridobi iz nastavitev cene za kategorijo transakcij v ceniku projekta, ki začne veljati z datumom začetka. Če način določanja cen za kategorijo transakcij ni **cena na enoto**, privzete vrednost ni in to polje ostane prazno. Pri izdelkih privzeta vrednost tega polja temelji na vrstici **Elemente cenika** v ceniku projekta, ki začne veljati z datumom začetka.| Mera stroškov vloge, ki opravlja delo, ali cena na enoto kategorije stroškov ali izdelka. Privzeta vrednost za **Čas** temelji na kombinaciji vrednosti cenovne razsežnosti za cenovno vrstico vloge v ceniku z lastnimi cenami, ki je priložen pogodbeni enoti in začne veljati z datumom začetka. Privzeta vrednost za polje **Stroški** temelji na kategoriji cenovne vrstice za cenik z lastnimi cenami, ki je priložen pogodbeni enoti in začne veljati z datumom začetka. Če način določanja cen za kategorijo transakcij ni »cena na enoto«, privzete vrednost ni in to polje ostane prazno. Za izdelke privzeta vrednost za polje temelji na vrstici **Elementa cenika** v ceniku z lastnimi cenami, ki je priložen pogodbeni enoti in začne veljati z datumom začetka.|
| **Predvideni davek** | **Hitro ustvarjanje** | Predvideni davek za to delo ali strošek vnese uporabnik. | &nbsp; |
| **Znesek** | **Hitro ustvarjanje** | V tem polju je vrednost lahko dodana, če polji **Količina** in **Cena** ostaneta prazni. Če sta polji **Količina** in **Cena** izpolnjeni, je polje **Znesek** samo za branje in se izračuna kot **(količina \* cena na enoto) + davek**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Posodobitev cen na podrobnostih vrstic pogodbe

Če spremenite cene na projektnem ceniku, ki je priložen pogodbi ali stroškovnem ceniku pogodbene enote, lahko osvežite cene na posameznih podrobnostih vrstice postavke, da odražajo spremembo. Na strani **Pogodba** izberite **Preračunavanje**. Pojavi se opozorilo, ki vas obvešča, da so cene za vse podrobnosti pogodbe v tej pogodbi ponastavljene. Izberite **Da** za osvežitev cen za prodajne in stroškovne podrobnosti vrstice pogodbe.

## <a name="access-contract-line-details-for-cost"></a>Dostop do podrobnosti vrstice pogodbe za strošek

Na zavihku **Podrobnosti vrstice pogodbe** izberite vrstico v mreži za prikaz dejanj na orodni vrstici podmreže. Prvo dejanje v orodni vrstici podmreže je **Odpri podrobnosti cene**. Če si želite ogledati povezano mero stroškov in znesek za to podrobnost vrstice pogodbe, izberite **Odpri podrobnosti cene**. 

> [!NOTE]
> Spreminjanje vrednosti podjetja, ki zagotavlja vire, enote vira, količine, datumov, vloge ali kategorije na podrobnosti vrstice pogodbe za **Strošek** spremeni tudi pripadajoče vrednosti na podrobnostih vrstice pogodbe za možnost **Prodaja**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta na podrobnostih vrstice pogodbe za strošek in prodajo

Podrobnosti vrstice pogodbe za možnost **Prodaja** nastavi privzeto valuto iz projektnega cenika, ki je veljaven za začetni datum podrobnosti vrstice pogodbe.

Podrobnosti vrstice pogodbe za možnost **Strošek** nastavi privzeto valuto iz projektnega cenika pogodbene enote pogodbe, ki je veljavna za začetni datum podrobnosti vrstice pogodbe za **Strošek**.

Izračuni dobičkonosnosti pretvorijo zneske za podrobnosti vrstice pogodbe za možnost **Strošek** in **Prodaja** v osnovno valuto okolja za poročanje splošne dejanske in ocenjene marže pogodbe.

> [!NOTE]
> Pride lahko do napak pri zaokroževanju valut in spremenjenih marž zaradi pomanjkanja menjalnih tečajev, veljavnih na datum. Te izračune uporabljajte samo za projektne pogodbe, saj gre za približke in ne za dejansko zakonsko ali drugo poročanje, ki zahteva večjo natančnost zaokroževanja in zavedanje datuma začetka veljave za menjalne tečaje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
