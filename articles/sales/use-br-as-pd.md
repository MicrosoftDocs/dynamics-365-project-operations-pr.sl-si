---
title: Uporaba vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti
description: V tej temi so na voljo informacije o uporabi vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti.
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b9fb7732f677a04272a556238b6c2acc1dcdfb9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277313"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Uporaba vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti

 _**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_ 

V tej temi so na voljo informacije o uporabi vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti. Če je vaša cenovna strategija nastavljena tako, da mora imeti vsak vir, ki ga je mogoče rezervirati, določeno cenovno ali stroškovno stopnjo, uporabite vir, ki ga je mogoče rezervirati, kot cenovno razsežnost.

## <a name="prerequisites"></a>Zahteve
Preden dokončate postopke v tej temi, morate imeti novo rešitev za cenovne razsežnosti za svojo organizacijo. Če je še niste ustvarili, glejte [Ustvarjanje polj in entitet po meri](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Dodajanje polja Vir, ki ga je mogoče rezervirati, v obrazce in poglede
Če želite narediti polje **Vir, ki ga je mogoče rezervirati** vidno v rešitvi za cenovne razsežnosti, morate polje dodati vsem obrazcem in pogledom v obliki entitete.

V spodnji tabeli so navedeni vsi vnaprej pripravljeni obrazci in pogledi, razvrščeni po entitetah. Novo polje boste morali dodati tudi v vse dodatne obrazce ali poglede v vaših entitetah po meri.

|   Entity        | Obrazci   |Pogledi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena vloge| Informacije | - Cene kategorij dejavnih virov<br> - Povezana cena kategorije vira |
|  Pribitek na ceno vloge| Informacije| - Dejavni pribitek na ceno vloge<br>- Povezani pribitek na ceno vloge |
|  Podrobnosti vrstic ponudbe| - Podatki o projektu<br>- Hitro ustvarjanje projekta| - Dejavne podrobnosti vrstice ponudbe<br>- Skupne podrobnosti vrstice ponudbe<br>- Povezane podrobnosti vrstice ponudbe |
|  Podrobnost vrstice projektne pogodbe| - Podatki o projektu<br>- Hitro ustvarjanje projekta| - Podrobnosti združenih pogodb<br>- Podrobnosti dejavnih pogodb<br>- Povezane podrobnosti pogodbe |
|  Projektno opravilo| - Informacije<br>- Novi obrazec| &nbsp; |
|  Član projektne ekipe| - Informacije<br>- Novi obrazec| - Dejavni člani projektne ekipe<br>- Člani projektne ekipe<br>- Povezani člani projektne ekipe |
|  Časovni vnos| - Informacije<br>- Ustvari časovni vnos| - Moji časovni vnosi po datumu<br>- Moji časovni vnosi za ta teden<br>- Časovni vnosi za odobritev|
|  Vrstica dnevnika| - Informacije<br>- Hitro ustvarjanje| - Dejavne vrstice dnevnika<br>- Povezane vrstice dnevnika |
|  Podrobnosti vrstice računa| - Informacije<br>- Hitro ustvarjanje| - Dejavne podrobnosti vrstice računa<br>- Transakcije računa, ki se zaračunajo<br>- Brezplačne transakcije računa<br>- Povezane podrobnosti vrstice računa <br>- Transakcije računa, ki se ne zaračunajo|
|  Dejansko| - Informacije<br>- Dejavno opravljeno delo| Povezano opravljeno delo |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Nastavitev vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti
Če želite nastaviti vir, ki ga je mogoče rezervirati, kot cenovno razsežnost, sledite spodnjim korakom:

1. Odprite **Nastavitve** > **Parametri**. 
2. Na zavihku **Cenovne razsežnosti na podlagi zneska** na strani **Parameter** preverite, ali mreža na zavihku prikazuje zapise v entiteti **Cenovne razsežnosti**. 
2. Na ta seznam cenovnih razsežnosti dodajte **Vir, ki ga je mogoče rezervirati** kot **msdyn_bookableresource**. 
3. V razdelkih **Velja za stroške** in **Velja za prodajo** izberite želeno vrednost.
4. V razdelku **Vrsta cenovne razsežnosti** izberite možnost **Na podlagi zneska**. 
5. Izberite prioriteto cene in prodaje za vir, ki ga je mogoče rezervirati. Običajno ima vir, ki ga je mogoče rezervirati, najvišjo prioriteto, če je vključen kot cenovna razsežnost. Nastavite prioriteto na **1** (ali **0**, odvisno od tega, kako štejete prioritete), da omogočite tako vedenje.

## <a name="set-up-pricing-dimension-field-names"></a>Nastavitev imen polj cenovnih razsežnosti

Če je ime polja cenovne razsežnosti v tabeli **Cena vloge** drugačno od imena polja v drugih entitetah, kjer je uporabljena privzeta cena, je treba zapis cenovnih razsežnosti seznaniti z drugačnimi imeni.  

Za vir, ki ga je mogoče rezervirati, ima entiteta **Člani projektne ekipe** nekoliko drugačno ime od imena v entiteti **Cena vloge**: 

 - Entiteta **Člani projektne ekipe** = **msdyn_bookableresourceid**
 - Entiteta **Cena vloge** = **msdyn_bookableresource**

O tej razliki je treba seznaniti zapis cenovne razsežnosti za **msydn_bookableresource**.

1. Dvokliknite vrstico v mreži **Cenovne razsežnosti**, da odprete stran razsežnosti imena **msdyn_bookableresource**.
2. Na zavihku **Povezano** strani razsežnosti izberite **Imena polj cenovnih razsežnosti**.

  ![Zavihek z imeni polj cenovnih razsežnosti](media/PD-fieldname.png)

3. V povezanem pogledu, ki se odpre, izberite možnost **Dodaj novo ime polja cenovne razsežnosti**.

  ![Dodajanje novih imen polj cenovnih razsežnosti](media/Add-NewPD-fieldname.png)

  Odpre se stran **Novo ime polja cenovne razsežnosti** za **msdyn_bookableresource**. 

4. Na strani **Novo ime polja cenovne razsežnosti** dodajte **msdyn_projectteam** v polje **Logično ime entitete**.
5. Dodajte **msdyn_bookableresourceid** v polje **Ime polja**.

 ![Oblika novega imena polja cenovne razsežnosti](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]