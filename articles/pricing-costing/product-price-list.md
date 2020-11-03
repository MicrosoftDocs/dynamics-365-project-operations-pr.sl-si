---
title: Ceniki za izdelke
description: Ta tema vsebuje informacije o cenikih pri določanju cen v katalogu, ki se uporabljajo za ponudbe in pogodbe za projekte.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 504aa90bfb478207059b5e2894a3990f9a4a5e9e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084824"
---
# <a name="product-price-lists"></a>Ceniki za izdelke

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Entitete cenikov in elementov cenika podpirajo cene kataloga izdelkov. Večinoma se ta funkcija uporablja za vrstice, ki temeljijo na katalogu, v projektnih ponudbah in projektnih pogodbah.

Pri vrsticah, ki temeljijo na projektu, pogodba predstavlja sklenjeni posel. Ker postopek pogajanj običajno poteka pred sklenitvijo, se cena, ki je priložena ponudbi, v nov cenik vedno kopira takšna kot je in se priloži pogodbi. Tega novega cenika ni mogoče spremeniti izven okvira pogodbe. Ta omejitev pomaga zaščititi kartico s ceno, ki je bila izpogajana, pred spremembami cene v glavnem ceniku.

Izdelke morate nastaviti tako, da imajo v katalogu izdelkov privzete stroške in cenike. Če želite konfigurirati privzete stroške in cenike, uporabite cenik, standardne stroške in trenutne stroške. Privzeti ceniki se v vrstici ponudbe ali v vrstici projektne pogodbe uporabljajo le, če sistem ne najde vrstice cenika za izdelek na ceniku izdelkov za ponudbo ali projektno pogodbo.

Lastno ceno v vrsticah kataloga izdelkov lahko spremenite v različnih ponudbah. Ta možnost je pomembna, saj ne morete določiti dobička iz poslovanja v projektnih obveznostih, če ne spremljate natančno stroškov. Kot lastna cena se privzeto uporablja standardna cena. Vendar pa privzeto lastno ceno lahko posodobite v vrstici ponudbe, če za to ponudbo obstaja druga lastna cena.

## <a name="price-list-items"></a>Elementi cenika

Izdelke iz kataloga izdelkov lahko dodajate različnim cenikom. Vrstice cenika za izdelke se vedno sklicujejo na določeno enoto. Ceno za izdelek v elementih cenika lahko konfigurirate kot znesek valute. Lahko pa jo konfigurirate kot funkcijo cenika, trenutnih stroškov ali standardnih stroškov.

PSA podpira različne načine zaokroževanja, ko so cene konfigurirane kot funkcija cenika, standardnih stroškov ali trenutnih stroškov. Izkoristite lahko več načinov oblikovanja cen in zaokroževanja ter tudi povežete sezname popustov z elementi cenika. 

Ko ustvarite nov cenik po meri za ponudbo tako, da izberete možnost **Ustvarjanje cen po meri** na strani **Projektna ponudba** , se ustvari kopija cenika in polje **Entiteta** v glavi novega cenika je nastavljeno na **Entiteta za prodajo**. Ime novega cenika je priloženo z imenom ponudbe in časovnim žigom. Ime novega cenika in ime ponudbe v potekih dela po meri lahko uporabite tudi za to, da sprožite dodaten pregled in odobritve za ponudbe, ki uporabljajo cene po meri.

 
## <a name="default-product-price-list"></a>Privzeti cenik izdelkov
Vsak zapis stranke ima polje **Privzeti cenik** , kjer lahko navedete cenik, ki ustreza valuti stranke. Privzeta vrednost ni samodejno vnesena v to polje. Če imate z določeno stranko poseben dogovor o cenah, lahko uporabite to polje, da povežete cenik s to stranko.

Entitete »Priložnost«, »Ponudba« in »Projektna pogodba« uporabljajo spodnji vrstni red za vnos privzetih cenikov izdelkov. Isti vrstni red se uporablja za cenike projekta.

1.  Citat
2.  Priložnost
3.  Stranki
4.  Globalne nastavitve 

Polje **Izdelek** v vrstici ponudbe privzeto navaja vse dejavne izdelke v ceniku izdelkov za ponudbo. Če je bil izdelek dezaktiviran ali če gre za osnutek izdelka, ga ni na seznamu, tudi če je na ceniku. 

Vrstice kataloga izdelkov se dodajo kot vrstice računa na prvem računu, ki je ustvarjen za projektno pogodbo. Na osnutku računa lahko izbrišete te vrstice računa. V tem primeru se vrstice prikažejo na naslednjem računu, dokler ni fakturiran oz. dokler se ne pošlje stranki. Ne morete fakturirati delne količine vrstice računa izdelka. Ko so vrstice izdelka iz projektne pogodbe fakturirane, se ustvarijo dejanske vrednosti. Vendar pa te dejanske vrednosti niso povezane s povezano entiteto projekta. Z drugimi besedami, vrstice projektne pogodbe, ki temeljijo na izdelku, so neodvisne od uporabe, ki temelji na projektu. Porabi materiala v projektih se ne sledi.
