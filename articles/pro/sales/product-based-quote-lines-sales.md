---
title: Pregled podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno
description: V tej temi so na voljo informacije o delu z vrsticami ponudb, ki temeljijo na izdelkih.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178208"
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