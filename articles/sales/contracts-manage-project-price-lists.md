---
title: Upravljanje projektnih cenikov v projektnih pogodbah
description: V tej temi so na voljo informacije o upravljanju projektnih cenikov v projektnih pogodbah.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278618"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Upravljanje projektnih cenikov v projektnih pogodbah

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Projektne pogodbe v storitvi Dynamics 365 Project Operations so zasnovane za podporo več prodajnih cenikov, veljavnih na datum, v pogodbi. V storitvi Project Operations obstaja nova povezana entiteta, imenovana **Projektni ceniki**. Ta entiteta ima odnos »ena proti mnogo« s projektno pogodbo.

Ceniki projektov se uporabljajo za določanje časovnih in stroškovnih transakcij projekta. Ko ima pogodba enega ali več cenikov projektov, se ti ceniki uporabijo za nastavitev cene za ocene časa in stroška ter dejanskih vrednosti za projekte, ki so povezani s pogodbo prek podrobnosti pogodbe.

Ko ni projektnih cenikov v projektni pogodbi, boste videli opozorilo, da ni projektnih cenikov ter za vaše ocene, dejansko projektno delo in stroške cena ne bo nastavljena. Ne bo cene za prodajne vrednosti.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Povezava ali odstranjevanje povezave cenika projekta v projektni pogodbi

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Ustvarjanje ali povezovanje specifičnih cenikov za ocenjevanje dela in stroškov, ki temeljijo na projektu

1. V projektni pogodbi izberite zavihek **Projektni ceniki**.
2. V podmreži izberite **+ Dodaj nov cenik projekta**.
3. Na drsniku **Hitro ustvarjanje** izberite cenik. 

  V spustnem seznamu so prikazani vsi ceniki, ki imajo kontekst nastavljen na **Prodaja**, kjer se valuta na ceniku ujema z valuto v pogodbi.
  
4. Vnesite opis za povezavo cenika projekta, izberite **Shrani**, nato pa zaprite drsnik **Hitro ustvarjanje**.

   Ustvari se povezava s cenikom projekta.
   
5. Ponovite korake 1–4, da povežete več kot en cenik s projektno pogodbo. Več projektnih cenikov ustvarite samo, če imate drugačen datum veljavnosti na vsakem od povezanih projektnih cenikov.

> [!NOTE]
> Project Operations ne podpira prekrivanja datumske veljavnosti projektnih cenikov. Če obstaja več projektnih cenikov za transakcijo z določenim datumom, bo cena za to transakcijo privzeto povrnjena na nič.

### <a name="remove-a-project-price-list-association"></a>Odstranitev povezave projektnega cenika

- Izberite projektni cenik in nato izberite **Brisanje pogodbenega projektnega cenika** v podmreži. 

  Cenik je odstranjen iz projektnih cenikov na pogodbi. Cenik sam ne bo izbrisan. Izbrisana bo samo povezava do cenika.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>V pogodbi nastavite samodejno povrnitev projektnih cenikov na privzeto

Projektni cenik je mogoče nastaviti kot privzeti cenik na projektni pogodbi. Ta nastavitev lahko pomaga zagotoviti, da vsi stiki v vaši organizaciji vedno začnejo s standardnim cenikom za to časovno obdobje.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Nastavitev organizacijske privzete nastavitve za projektne cenike

1. Odprite **Nastavitve** > **Splošno**, nato pa izberite **Parametri**.
2. Na strani s seznamom **Aktivni parametri** izberite in dvokliknite zapis, da ga odprete. Med dvoklikom se prepričajte, da ne klikate v vrednost polja, ki je hiperpovezava. 
3. Na strani **Aktivni parametri** izberite zavihek **Cenik**. Podmreža prikaže seznam privzetih cenikov. To je seznam standardnih cen in prodajnih cenikov. Če je tukaj povezan cenik **Prodaja** za vsako valuto, v kateri prodajate, to zagotavlja, da je prodajni cenik privzet za vsako pogodbo, ki jo ustvarite za stranke, ki izvajajo transakcije v tej valuti.

### <a name="set-up-a-customer-specific-project-price-list"></a>Nastavitev projektnega cenika, specifičnega za stranko

Nastavite lahko tudi projektne cenike za specifično stranko, ko ste se dogovorili za glavni dogovor o cenah s strankami.

1. Odprite **Prodaja** > **Stranke**.
2. Na seznamu aktivnih računov izberite stranko, za katero imate poseben cenik.
3. Izberite zapis stranke, da ga odprete in nato izberite zavihek **Projektni ceniki**. Podmreža prikaže seznam projektnih cenikov, specifičnih za to stranko. 
4. Tukaj ustvarite novo povezavo cenika za projektni cenik, specifičen za to stranko.

## <a name="custom-pricing-on-a-project-contract"></a>Cene po meri za projektne pogodbe

Ko imate organizacijske in privzete projekte cenike, specifične za stranko, bodo vaše projektne pogodbe samodejno ustvarjene s temi povezavami projektnih cenikov. Projektni ceniki na projektni pogodbi pa so vedno kopirani s pripetim datumom in imenom pogodbe. Upravitelji kupcev in projektni vodje lahko nato začnejo urejati cene za te kopije. Te spremenjene cene bodo veljale samo za to projektno pogodbo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]