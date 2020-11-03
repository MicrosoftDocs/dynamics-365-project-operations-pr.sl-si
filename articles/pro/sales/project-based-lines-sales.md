---
title: Podrobnosti priložnosti, ki temeljijo na projektih (Pro)
description: Ta tema vsebuje informacije o podrobnostih priložnosti, ki temeljijo na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084681"
---
# <a name="project-based-opportunity-lines-pro"></a>Podrobnosti priložnosti, ki temeljijo na projektih (Pro)

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podrobnosti priložnosti, ki temeljijo na projektih, so na voljo samo za priložnosti, ki temeljijo na projektih. Zapisi priložnosti, ki temeljijo na projektih, imajo vrednost polja **Vrsta** nastavljeno na **Temelji na delu**.

Podrobnosti priložnosti, ki temeljijo na projektih, so vrstične postavke, ki bodo stranki dostavljene prek projekta. Vendar projekta ni mogoče povezati s podrobnostjo priložnosti, ki temelji na projektu. Projekti so lahko vezani na vrstične postavke od stopnje **Ponudba** naprej, ker je običajno priložnost v zgodnji stopnji življenjskega cikla posla. Določitev števila projektov, ki se bodo uporabljali za izvedbo del za stranko, je odločitev, ki se sprejme pozneje, v stopnji prodaje. Stopnjo priložnosti lahko uporabite za določitev ločenih komponent dostave za stranko. Odločitve v zvezi z dejanskim številom projektov, ki se uporabljajo za dostavo teh komponent, je mogoče odložiti, dokler ni znanih več informacij o samem delu.

Spodaj so polja, ki jih najdete pri podrobnosti priložnosti, ki temelji na projektu:

| **Polje** | **Mesto** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Tip izdelka | Zavihek »Splošno« (skrito) | Izberite lahko eno od teh možnosti:</br>- storitev, ki temelji na projektu (na voljo samo, če je nameščena storitev Dynamics 365 Project Operations)</br>- izdelek (na voljo samo, če sta nameščeni storitvi Project Operations in Dynamics 365 Sales) | Vrednost tega polja je nastavljena na **Storitev na osnovi projekta** , ko pri priložnosti iz mreže podrobnosti, ki temeljijo na projektu, ustvarite podrobnost priložnosti, ki temelji na projektu. <br> Če spremenite ali preglasite to vrednost, funkcija projekta ne bo omogočena za vaše vrstične postavke, ki temeljijo na projektu. |
| Priložnost | Zavihek Splošno | To polje je samo za branje in se sklicuje na nadrejeni zapis »Priložnost«, ki mu pripada ta vrstična postavka. | S tega polja ni nadaljnjega vpliva. |
| Imenu | Zavihek Splošno | To besedilno polje, ki ga je mogoče urejati, lahko uporabite za podajanje kratkega opisa vrstične postavke. | Ko ustvarite ponudbo iz te priložnosti, se ta vrednost prenese v podrobnost ponudbe. |
| Proračun stranke | Zavihek Splošno | To polje »Valuta«, ki ga je mogoče urejati, lahko uporabite za sledenje znesku, ki ga je stranka pripravljena porabiti za to vrstično postavko. | Ko ustvarite ponudbo iz te priložnosti, se ta vrednost prenese v ustrezno polje pri podrobnosti ponudbe. |
| Način obračunavanja | Zavihek Splošno | To polje, ki ga je mogoče urejati, ima naslednje vrednosti:</br>- čas in material</br>- fiksna cena | Ko ustvarite ponudbo iz te priložnosti, se ta vrednost prenese v ustrezno polje pri podrobnosti ponudbe. Ko je podrobnost ponudbe ustvarjena, je polje zaklenjeno in ga ni mogoče spremeniti. To vrednost polja dodelite čim natančneje. Če morate spremeniti vrednost tega polja pri podrobnosti ponudbe, izbrišite in znova ustvarite podrobnost ponudbe. |
