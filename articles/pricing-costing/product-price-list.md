---
title: Ceniki za izdelke
description: Ta tema vsebuje informacije o cenikih pri določanju cen v katalogu, ki se uporabljajo za ponudbe in pogodbe za projekte.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999246"
---
# <a name="product-price-lists"></a>Ceniki za izdelke

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

 V aplikaciji Project Operations **ceniki izdelkov** in s tem povezane entitete elementa cenika podpirajo funkcionalnost določanja cen izdelkov na podlagi ponudb in pogodbenih postavk izdelka. Za izdelke, ki se uporabljajo na projektih, se uporabljajo zapisi elementa cenika za cenike projekta. 

Izdelke morate nastaviti tako, da imajo v katalogu izdelkov privzete stroške in cenike. Če želite konfigurirati privzete stroške in cenike, uporabite cenik, standardne stroške in trenutne stroške. Privzeti ceniki se v vrstici ponudbe ali v vrstici projektne pogodbe uporabljajo le, če sistem ne najde vrstice cenika za izdelek na ceniku izdelkov za ponudbo ali projektno pogodbo.

Lastno ceno v vrsticah kataloga izdelkov lahko spremenite v različnih ponudbah. Ta možnost je pomembna, saj ne morete določiti dobička iz poslovanja v projektnih obveznostih, če ne spremljate natančno stroškov. Kot lastna cena se privzeto uporablja standardna cena. Vendar pa privzeto lastno ceno lahko posodobite v vrstici ponudbe, če za to ponudbo obstaja druga lastna cena.

## <a name="price-list-items"></a>Elementi cenika

Izdelke iz kataloga izdelkov lahko dodajate različnim cenikom. Vrstice cenika za izdelke se vedno sklicujejo na določeno enoto. Ceno za izdelek v elementih cenika lahko konfigurirate kot znesek valute. Lahko pa jo konfigurirate kot funkcijo cenika, trenutnih stroškov ali standardnih stroškov.

Funkcionalnost določanja cen podpira različne načine zaokroževanja, ko so cene izdelka konfigurirane kot funkcija cenika, standardnih stroškov ali trenutnih stroškov. Izkoristite lahko več načinov oblikovanja cen in zaokroževanja ter tudi povežete sezname popustov z elementi cenika. 

 
## <a name="default-product-price-list"></a>Privzeti cenik izdelkov
Vsak zapis stranke ima polje **Privzeti cenik**, kjer lahko navedete cenik, ki ustreza valuti stranke. Privzeta vrednost ni samodejno vnesena v to polje. Če imate z določeno stranko poseben dogovor o cenah, lahko uporabite to polje, da povežete cenik s to stranko.

Entitete »Priložnost«, »Ponudba« in »Projektna pogodba« uporabljajo spodnji vrstni red za vnos privzetih cenikov izdelkov. Isti vrstni red se uporablja za cenike projekta.

1.  Citat
2.  Priložnost
3.  Stranki
4.  Globalne nastavitve 

Polje **Izdelek** v vrstici ponudbe privzeto navaja vse dejavne izdelke v ceniku izdelkov za ponudbo. Če je bil izdelek dezaktiviran ali če gre za osnutek izdelka, ga ni na seznamu, tudi če je na ceniku. 

Vrstice kataloga izdelkov se dodajo kot vrstice računa na prvem računu, ki je ustvarjen za projektno pogodbo. Na osnutku računa lahko izbrišete te vrstice računa. V tem primeru se vrstice prikažejo na naslednjem računu, dokler ni fakturiran oz. dokler se ne pošlje stranki. Ne morete fakturirati delne količine vrstice računa izdelka. Ko so vrstice izdelka iz projektne pogodbe fakturirane, se ustvarijo dejanske vrednosti. Vendar pa te dejanske vrednosti niso povezane s povezano entiteto projekta. Z drugimi besedami, vrstice projektne pogodbe, ki temeljijo na izdelku, so neodvisne od uporabe, ki temelji na projektu. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
