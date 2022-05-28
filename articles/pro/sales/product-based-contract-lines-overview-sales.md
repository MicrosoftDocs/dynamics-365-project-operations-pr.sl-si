---
title: Pregled podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljeno
description: V tej temi so na voljo informacije o podrobnostih pogodb, ki temeljijo na izdelkih.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8006e90e0d4fdf02042f26b261775a92f87f47ca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598232"
---
# <a name="product-based-contract-lines-overview---lite"></a>Pregled podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko ustvarite podrobnosti pogodbe, ki temeljijo na izdelku. Podrobnosti pogodb so lahko ročno ustvarjene vrstice ali pa artikli iz kataloga izdelkov.

## <a name="product-catalog"></a>Katalog izdelkov

Izdelki v katalogu izdelkov imajo privzeto enoto in skupino enot. Če ima več izdelkov enak nabor atributov, lahko ustvarite družino izdelkov, ki ima prav tako te atribute. Vsi izdelki v eni družini izdelkov podedujejo isti nabor atributov.

Podjetje na primer prodaja naročniške licence za različne vrste programske opreme. Vsa naročniška programska oprema ima ta dva atributa:

- Število uporabnikov
- Trajanje naročnine (v mesecih)

Če želite vzdrževati to vrsto kataloga, ustvarite družino izdelkov z imenom **Programska oprema z naročnino**. V družino izdelkov dodajte atribute, **število uporabnikov** in **trajanje naročnine**. Nato dodajte posamezne izdelke v družino izdelkov **Programska oprema z naročnino**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Dodajanje elementov kataloga izdelkov v projektno pogodbo

Projektne pogodbe imajo razdelke za dve vrsti vrstic: vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih. Podrobnosti, ki temeljijo na izdelkih, vključujejo vse izdelke in enote v ceniku izdelkov v pogodbi. Dodajate lahko tudi izdelke, ki niso del cenika izdelkov v pogodbi.

Izberete lahko izdelke iz drugih cenikov ali pa neposredno iz kataloga izdelkov. Ko izberete izdelke neposredno iz kataloga izdelkov, se za prodajno ceno izdelka uporabi privzeti cenik tega izdelka. Če privzeti cenovni seznam ni nastavljen, je cena nastavljena na 0 (nič).

Če podrobnost pogodbe temelji na katalogu izdelkov, lahko prodajno ceno preglasite neposredno v podrobnosti pogodbe. Podrobnost pogodbe ima polje **Cene** z dvema vrednostma:

- **Preglasi oblikovanje cene**
- **Uporabi privzeto**

Če nastavite polje **Cene** na **Preglasi oblikovanje cene**, privzeta cena ni nastavljena. Vnesite ceno za izdelek pri podrobnosti pogodbe. Če polje nastavite na **Uporabi privzeto**, se uporablja privzeta prodajna cena in polja ni mogoče urejati.

Ko namestite Project Operations, se privzete prodajne cene vnesejo v vrstice v pogodbi, ki temeljijo na izdelkih. Polje **Oblikovanje cen** je nastavljeno na **Preglasi oblikovanje cene**, tako da lahko uredite privzeto ceno v podrobnostih pogodbe. To je preglasitev vedenja podrobnosti, ki temeljijo na izdelkih, v storitvi Dynamics 365 Sales, ki je specifična za Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]