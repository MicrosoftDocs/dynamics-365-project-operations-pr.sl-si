---
title: Podrobnosti priložnosti, ki temeljijo na projektih
description: Ta tema vsebuje informacije o delu s podrobnostmi priložnosti, ki temeljijo na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898416"
---
# <a name="project-based-opportunity-lines"></a>Podrobnosti priložnosti, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Podrobnosti priložnosti, ki temeljijo na projektih, so na voljo samo za priložnosti, ki temeljijo na projektih. Zapisi priložnosti, ki temeljijo na projektih, imajo vrednost polja **Vrsta** nastavljeno na **Temelji na delu**.

Podrobnosti priložnosti, ki temeljijo na projektih, so vrstične postavke, ki bodo stranki dostavljene prek projekta. Vendar projekta ni mogoče povezati s podrobnostjo priložnosti, ki temelji na projektu. Projekti so lahko vezani na vrstične postavke od stopnje **Ponudba** naprej, ker običajno priložnost nastane v zgodnji stopnji posla. Določitev števila projektov, ki se bodo uporabljali za izvedbo del za stranko, je odločitev, ki se sprejme pozneje, v stopnji prodaje. Stopnjo priložnosti uporabite za določitev ločenih komponent dostave za stranko. Odločitve v zvezi z dejanskim številom projektov, ki se uporabljajo za dostavo teh komponent, je mogoče odložiti, dokler ni znanih več informacij o samem delu.

Spodaj so polja, ki jih najdete pri podrobnosti priložnosti, ki temelji na projektu:

| **Polje** | **Mesto** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Tip izdelka | Zavihek »Splošno« (skrito) | To je polje za nabor možnosti. Če ste namestili storitev Dynamics 365 Operations, je ena od možnosti, ki je na voljo, **Storitev na osnovi projekta**.  | Vrednost tega polja je nastavljena na **Storitev na osnovi projekta**, ko pri priložnosti iz mreže podrobnosti, ki temeljijo na projektu, ustvarite podrobnost priložnosti, ki temelji na projektu. <br> Če spremenite ali preglasite to vrednost, funkcija projekta ne bo omogočena za vaše vrstične postavke, ki temeljijo na projektu. |
| Priložnost | Zavihek Splošno | To polje je samo za branje in se sklicuje na nadrejeni zapis »Priložnost«, ki mu pripada ta vrstična postavka. | To polje nima nadaljnjega vpliva. |
| Imenu | Zavihek Splošno | To besedilno polje, ki ga je mogoče urejati, lahko uporabite za podajanje kratkega opisa te vrstične postavke. | Ko ustvarite ponudbo iz te priložnosti, se ta vrednost prenese v podrobnost ponudbe. |
| Proračun stranke | Zavihek Splošno | To polje »Valuta«, ki ga je mogoče urejati, lahko uporabite za sledenje znesku, ki ga je stranka pripravljena porabiti za to vrstično postavko. | Ko ustvarite ponudbo iz te priložnosti, se ta vrednost prenese v ustrezno polje pri podrobnosti ponudbe. |
| Način obračunavanja | Zavihek Splošno | To polje, ki ga je mogoče urejati, ima naslednje vrednosti:</br>- čas in material</br>- fiksna cena | Ko ustvarite ponudbo iz te priložnosti, se ta vrednost prenese v ustrezno polje pri podrobnosti ponudbe. Ko je podrobnost ponudbe ustvarjena, je polje zaklenjeno in ga ni mogoče spremeniti. To vrednost polja dodelite čim natančneje. Če morate spremeniti vrednost tega polja pri podrobnosti ponudbe, izbrišite in znova ustvarite podrobnost ponudbe. |
