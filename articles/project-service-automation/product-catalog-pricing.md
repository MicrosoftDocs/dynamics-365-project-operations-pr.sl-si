---
title: Cene v katalogu izdelkov
description: Ta tema vsebuje informacije o tem, kako delujejo cene v katalogu izdelkov v aplikaciji Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f1a8b1af-0767-4d83-82ef-367aac7a630f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8f296f6af9f60f40b726fddb095785dfb9831dc3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755880"
---
# <a name="product-catalog-pricing"></a>Cene v katalogu izdelkov 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Entitete cenikov in elementov cenika podpirajo cene kataloga izdelkov. Večinoma se ta funkcija uporablja za vrstice, ki temeljijo na katalogu, v projektnih ponudbah in projektnih pogodbah.

Pri vrsticah, ki temeljijo na projektu, pogodba predstavlja sklenjeni posel. Ker postopek pogajanj običajno poteka pred sklenitvijo, se cena, ki je priložena ponudbi, v nov cenik vedno kopira takšna kot je in se priloži pogodbi. Tega novega cenika ni mogoče spremeniti izven okvira pogodbe. Ta omejitev pomaga zaščititi kartico s ceno, ki je bila izpogajana, pred spremembami cene v glavnem ceniku.

Izdelke morate nastaviti tako, da imajo v katalogu izdelkov privzete stroške in cenike. Če želite konfigurirati privzete stroške in cenike, morate uporabiti cenik, standardne stroške in trenutne stroške. Privzeti ceniki se v vrstici ponudbe ali v vrstici projektne pogodbe uporabljajo le, če sistem ne najde vrstice cenika za izdelek na ceniku izdelkov za ponudbo ali projektno pogodbo.

Lastno ceno v vrsticah kataloga izdelkov lahko spremenite v različnih ponudbah. Ta možnost je pomembna, saj ne morete določiti dobička iz poslovanja v projektnih obveznostih, če ne spremljate natančno stroškov. Kot lastna cena se privzeto uporablja standardna cena. Vendar pa privzeto lastno ceno lahko posodobite v vrstici ponudbe, če za to ponudbo obstaja druga lastna cena.

## <a name="price-list-items"></a>Elementi cenika

Izdelke iz kataloga izdelkov lahko dodajate različnim cenikom. Vrstice cenika za izdelke se vedno sklicujejo na določeno enoto. Ceno za izdelek v elementih cenika lahko konfigurirate kot znesek valute. Lahko pa jo konfigurirate kot funkcijo cenika, trenutnih stroškov ali standardnih stroškov.

PSA podpira različne načine zaokroževanja, ko so cene konfigurirane kot funkcija cenika, standardnih stroškov ali trenutnih stroškov. Izkoristite lahko več načinov oblikovanja cen in zaokroževanja ter tudi povežete sezname popustov z elementi cenika. 

> ![Dodajanje izdelkov iz kataloga izdelkov različnim cenikom](media/basic-guide-16.png)

Ko ustvarite nov cenik po meri za ponudbo tako, da izberete možnost **Ustvarjanje cen po meri** na strani **Projektna ponudba**, PSA naredi kopijo cenika in polje **Entiteta** v glavi novega cenika je nastavljeno na **Entiteta za prodajo**. Ime novega cenika je priloženo z imenom ponudbe in časovnim žigom. Ime novega cenika in ime ponudbe v potekih dela po meri lahko uporabite tudi za to, da sprožite dodaten pregled in odobritve za ponudbe, ki uporabljajo cene po meri.

 
## <a name="default-product-price-list"></a>Privzeti cenik izdelkov
Vsak zapis stranke ima polje **Privzeti cenik**, kjer lahko navedete cenik, ki ustreza valuti stranke. V polju PSA privzeta vrednost ni samodejno vnesena v to polje. Če imate z določeno stranko poseben dogovor o cenah, lahko uporabite to polje, da povežete cenik s to stranko.

Entitete »Priložnost«, »Ponudba« in »Projektna pogodba« uporabljajo spodnji vrstni red za vnos privzetih cenikov izdelkov. Isti vrstni red se uporablja za cenike projekta.

1.  Ponudba
2.  Priložnost
3.  Stranka
4.  Globalne nastavitve za PSA

Polje **Izdelek** v vrstici ponudbe privzeto navaja vse dejavne izdelke v ceniku izdelkov za ponudbo. Če je bil izdelek dezaktiviran ali če gre za osnutek izdelka, ga ni na seznamu, tudi če je na ceniku. 

Vrstice kataloga izdelkov se dodajo kot vrstice računa na prvem računu, ki je ustvarjen za projektno pogodbo. Na osnutku računa lahko izbrišete te vrstice računa. V tem primeru se vrstice prikažejo na naslednjem računu, dokler ni fakturiran oz. dokler se ne pošlje stranki. V PSA ne morete fakturirati delne količine vrstice računa izdelka. Ko so vrstice izdelka iz projektne pogodbe fakturirane, se ustvarijo dejanske vrednosti. Vendar pa te dejanske vrednosti niso povezane s povezano entiteto projekta. Z drugimi besedami, vrstice projektne pogodbe, ki temeljijo na izdelku, so neodvisne od uporabe, ki temelji na projektu. PSA ne sledi porabi materiala v projektih.
