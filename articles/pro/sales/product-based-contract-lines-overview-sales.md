---
title: Pregled podrobnosti pogodb, ki temeljijo na izdelkih
description: V tej temi so na voljo informacije o podrobnostih pogodb, ki temeljijo na izdelkih.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084683"
---
# <a name="product-based-contract-lines-overview"></a>Pregled podrobnosti pogodb, ki temeljijo na izdelkih

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V storitvi Dynamics 365 Project Operations lahko ustvarite podrobnosti pogodb, ki temeljijo na izdelkih. Podrobnosti pogodb so lahko ročno ustvarjene vrstice ali pa artikli iz kataloga izdelkov.

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

Če nastavite polje **Cene** na **Preglasi oblikovanje cene** , privzeta cena ni nastavljena. Vnesite ceno za izdelek pri podrobnosti pogodbe. Če polje nastavite na **Uporabi privzeto** , se uporablja privzeta prodajna cena in polja ni mogoče urejati.

Ko namestite Project Operations, se privzete prodajne cene vnesejo v vrstice v pogodbi, ki temeljijo na izdelkih. Polje **Oblikovanje cen** je nastavljeno na **Preglasi oblikovanje cene** , tako da lahko uredite privzeto ceno v podrobnostih pogodbe. To je preglasitev vedenja podrobnosti, ki temeljijo na izdelkih, v storitvi Dynamics 365 Sales, ki je specifična za Project Operations.