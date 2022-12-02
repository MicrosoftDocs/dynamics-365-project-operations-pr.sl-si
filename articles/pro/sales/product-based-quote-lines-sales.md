---
title: Pregled podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno
description: V tem članku so na voljo informacije o delu z vrsticami ponudb, ki temeljijo na izdelkih.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: db0700e789202a8fdd0ef3b49959421ac54fb9ad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914330"
---
# <a name="product-based-quote-lines-overview---lite"></a>Pregled podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko ustvarite vrstice ponudb, ki temeljijo na izdelku. Vrstice ponudb, ki temeljijo na izdelkih, lahko ročno dodate ali pa izberete izdelke iz kataloga izdelkov.

## <a name="product-catalog"></a>Katalog izdelkov

Vsak izdelek v katalogu izdelkov ima privzeto enoto in skupino enot. Če ima več izdelkov enak nabor atributov, lahko ustvarite družino izdelkov, ki ima prav tako te atribute. 

Podjetje na primer prodaja naročniške licence za različne vrste programske opreme. Vsa naročniška programska oprema ima ta dva atributa:

- Število uporabnikov
- Trajanje naročnine, merjene v mesecih

To vrsto kataloga upravljajte tako, da ustvarite družino izdelkov, ki se imenuje **Naročniška programska oprema**, in kot atributa dodate število uporabnikov in trajanje naročnine. Nato lahko posamezne elemente dodate v družino izdelkov **Naročniška programska oprema**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Dodajanje elementov kataloga izdelkov v projektno ponudbo

Strani **Ponudba za projekt** in **Projektna pogodba** imata razdelke za vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih. Pri vrsticah, ki temeljijo na izdelku, spustni seznam v vrstici ponudbe ali vrstici projekte pogodbe vključuje vse izdelke in enote na ceniku izdelkov. Dodajate lahko tudi izdelke, ki niso del cenika izdelkov.

Poleg tega lahko izberete izdelke iz drugih cenikov ali pa neposredno iz kataloga izdelkov. Ko izberete izdelke neposredno iz kataloga izdelkov, se za prikaz prodajne cene izdelka uporabi privzeti cenik tega izdelka. Če privzeti cenik ni nastavljen, je cena nastavljena na nič (0).

Če vrstica ponudbe temelji na katalogu izdelkov, lahko prodajno ceno preglasite neposredno v vrstici ponudbe. Vrstica ponudbe v polju **Cene** z dvema razpoložljivima vrednostma:

- **Preglasi oblikovanje cene**
- **Uporabi privzeto**

Če izberete možnost **Preglasi oblikovanje cene**, privzeta cena ni nastavljena. Namesto tega morate ceno za izdelek vnesti v vrstici ponudbe. Če izberete možnost **Uporabi privzeto**, je uporabljena privzeta prodajna cena in polje je zaklenjeno za urejanje.

Privzete prodajne cene se vnesejo v vrstice, ki temeljijo na izdelkih, v ponudbi. Polje **Oblikovanje cen** je nato nastavljeno na **Preglasi oblikovanje cene**, tako da lahko uredite privzeto ceno v vrsticah ponudbe. Ta preglasitev vedenja podrobnosti, ki temeljijo na izdelkih, v aplikaciji Dynamics 365 Sales je značilna za aplikacijo Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]