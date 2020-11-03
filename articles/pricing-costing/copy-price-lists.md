---
title: Kopiranje cenikov
description: Ta tema vsebuje informacije o tem, kako se v aplikaciji Project Operations kopirajo ceniki.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084795"
---
# <a name="copy-price-lists"></a>Kopiranje cenikov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko ustvarite kopije cenikov. Ustvarite lahko na primer cenike za prihajajoče leto z uporabo cenika za tekoče leto.  Iz cenikov za stroške lahko kopirate tudi cenik za deleže obračunavanja in prodajne cene. 

Če želite kopirati cenik, izvedite naslednje korake.

1. Odprite cenik, ki ga želite kopirati, in izberite možnost **Kopiraj**.
2. Vnesite vse potrebne podatke za kopiranje cenika. Naslednja tabela prikazuje, kaj je treba upoštevati pri vnosu podatkov.

| Polje | Ustreznost, namen in smernice | Nadaljnji vpliv |
| --- | --- | --- |
| Imenu | Ime izvornega cenika s pripeto oznako **-kopija**. | Cenik je s to vrednostjo prikazan na vseh straneh s seznami in v spustnih seznamih. |
| Kontekst | Vnesite želeni kontekst za ciljni cenik. | Cenik, nastavljen na kontekst **Strošek** , se uporablja za iskanje cen za ocene stroškov in dejanske vrednosti stroškov. Cenik, nastavljen na kontekst **Prodaja** , se uporablja za iskanje cen za ocene prodaje in dejanske vrednosti prodaje. Samo cenike, katerih kontekst je nastavljen na možnost **Prodaja** , je mogoče priložiti cenikom projektov za stranke, ponudbe in pogodbe. |
| Datum začetka | Datum začetka obdobja, za katerega velja cenik | V polju **Končni datum** in tem polju je določeno, kateri cenik se uporablja za posamezno vrstico za oceno ali dejansko vrednost. |
| Končni datum | Datum konca obdobja, za katerega velja cenik. | V polju **Začetni datum** in tem polju je določeno, kateri cenik se uporablja za posamezno vrstico za oceno ali dejansko vrednost. |
| Valuta | Valuta izvornega cenika Mogoče jo je spremeniti. | Če je valuta spremenjena, se med kopiranjem vse cenovne vrstice za delo, stroške in elementi kataloga izdelkov pretvorijo v valuto ciljnega cenika. |
| Časovna enota | Valuta izvornega cenika Mogoče jo je spremeniti. | Če je enota spremenjena, se med kopiranjem vse cenovne vrstice za delo, stroške in elementi kataloga izdelkov pretvorijo v enoto ciljnega cenika. Uporabljeni sta pretvorbi iz nastavitve enote za časovno enoto izvornega cenika in časovno enoto ciljnega cenika. |
| Opis | Opis izvornega cenika s pripeto oznako **-kopija**. V tem besedilnem polju lahko navedete opis cenika v več vrsticah. | To polje je prikazano v pogledih **Povezani** na cenikih v različnih entitetah s povezanimi ceniki. |

3. Shranite cenik. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Posodabljanje cenika z uporabo pribitka za vse cene

1. Na zavihkih cenika **Vloga** , **Kategorija** in **Element cenika** lahko izberete možnost **Posodobi cene** , da uveljavite pribitek za vse cene v podmreži. 
2. V pogovornem oknu, ki se odpre, vnesite pribitek. Vnesete lahko tudi negativni odstotek pribitka, da za določen odstotek znižate cene. 
3. V pogovornem oknu izberite možnost **V redu** in nato preverite, ali cene v podmreži odražajo vaše spremembe.
