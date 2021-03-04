---
title: Upravljanje cenikov za projekte v projektnih ponudbah – poenostavljeno
description: Ta tema vsebuje informacije o delu s ceniki projektov v ponudbah. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176001"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Upravljanje cenikov za projekte v projektnih ponudbah – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Projektne ponudbe so zasnovane tako, da podpirajo več cenikov z datumom začetka veljavnosti. V storitvi Dynamics 365 Project Operations se doda nova povezana entiteta, imenovana **Ceniki projektov**. Ta entiteta ima do projektne ponudbe odnos »ena proti mnogo«.

Ceniki projektov se uporabljajo za določanje časovnih in stroškovnih transakcij projekta. Če ima ponudba enega ali več cenikov projektov, se ti ceniki uporabljajo za določanje časovnih in stroškovnih ocen ter dejanskih podatkov za projekte, ki so povezani s ponudbo prek vrstic ponudbe.

Če v projektni ponudbi ni cenikov projektov, boste prejeli opozorilno sporočilo. V sporočilu je zapisano, da ker ne obstajajo ceniki projektov, ne bo podana cena za vaše ocenjeno in dejansko projektno delo ter stroške. Namesto tega bodo imeli za prodajne vrednosti ceno nič (0).

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Povežite ali ločite cenik projekta pri projektni ponudbi

Če želite ustvariti ali posamezen cenik za oceno projektnega dela in stroškov, opravite naslednje korake.

1. Pri ponudbi izberite zavihek **Cena projekta** in v podmreži izberite **+ Dodaj nov cenik projekta**.
2. Na strani »Hitro ustvarjanje« izberite cenik. Na spustnem seznamu so prikazani vsi ceniki, katerih kontekst je nastavljen na **Prodaja** in se valuta ujema z valuto v ponudbi.
4. Vnesite opis povezave s cenikom projekta in izberite **Shrani in zapri**.

Ustvari se povezava s cenikom projekta.

Ta postopek lahko ponovite, če želite v ponudbo projekta vključiti več kot en cenik projekta. Ustvarite več cenikov projekta samo, če imate različne datume začetka veljavnosti za vsakega od povezanih cenikov projekta.

> [!NOTE]
> Project Operations ne podpira prekrivajočih se datumov začetka veljavnosti pri cenikih projektov. Če obstaja več cenikov projektov za transakcijo z izbranim datumom, bo cena za to transakcijo privzeto nastavljena na nič (0).
Če želite odstraniti povezavo s cenikom projekta, izberite cenik projekta in nato izberite **Izbriši cenik projekta za ponudbo**. Cenik se odstrani iz cenikov projektov za ponudbo, sam cenik pa se ne izbriše. Izbriše se samo povezava s ponudbo.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Nastavitev privzetih cenikov projektov za ponudbo

Cenike projektov lahko privzeto nastavite za projektno ponudbo. Ta nastavitev zagotavlja, da se vse ponudbe v vaši organizaciji vedno začnejo s standardnim cenikom za to cenovno obdobje.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Nastavitev privzetih organizacijskih enot za cenike projektov

1. Odprite **Nastavitve** > **Splošno** > **Parametri**.
2. Na strani s seznamom **Aktivni parametri** poiščite zapis in dvokliknite, da ga odprete. 
3. Na strani **Parametri** izberite zavihek **Cenik**. Prikaže se seznam privzetih cenikov. To je seznam standardnih stroškov in prodajnih cenikov. Če imate tukaj povezani prodajni cenik za vsako valuto, v kateri prodajate, bo ta prodajni cenik privzet za katero koli ponudbo, ki jo ustvarite za stranke, ki poslujejo v tej valuti.

### <a name="set-up-customer-specific-project-price-lists"></a>Nastavitev cenikov projektov za posamezne stranke

Cenike projektov za posamezne stranke lahko nastavite tudi, ko se s strankami dogovorite za glavni dogovor o cenah.

Če želite nastaviti cenik projekta za posamezno stranko, izvedite naslednje korake.

1. V območju **Prodaja** izberite **Stranke**.
2. Na seznamu aktivnih računov izberite in odprite zapis stranke, za katero imate poseben cenik.
3. Na zavihku **Ceniki projektov** lahko ustvarite novo povezavo s cenikom, da pridobite cenik projekta, ki je specifičen za to stranko.

## <a name="create-custom-pricing-on-a-project-quote"></a>Ustvarjanje cen po meri za projektno ponudbo

Ko imate privzete organizacijske cenike in cenike projektov, specifične za stranke, bodo vaše projektne ponudbe samodejno ustvarjene s temi povezavami cenikov projektov. V nekaterih primerih pa boste morda morali ustvariti cene po meri za določeno ponudbo projekta. 

1. Pri možnosti **Projektna ponudba** se na zavihku **Cenik projekta** prepričajte, da v podmreži ni izbran noben specifičen zapis cenika.
2. Izberite **Ustvari cenik po meri**. S tem bodo ustvarjene kopije vseh standardnih cenikov, ki so trenutno povezani s ponudbo, in te kopije bodo povezane s ponudbo. Obstoječe povezave s standardnimi ceniki bodo odstranjene. Prodajalec lahko nato začne urejati cene teh kopij. Te spremenjene cene bodo veljale samo za to projektno ponudbo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]