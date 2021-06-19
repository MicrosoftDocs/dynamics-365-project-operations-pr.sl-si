---
title: Uporaba kategorije transakcije kot cenovne razsežnosti
description: Ta tema vsebuje informacije o uporabi kategorije transakcije kot cenovne razsežnosti.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: db1d9ec0c99531344aed2e935441b43993f1e102
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014361"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Uporaba kategorije transakcije kot cenovne razsežnosti

[!include [banner](../includes/psa-now-project-operations.md)]

Ta tema opisuje, kako uporabiti kategorijo transakcije kot cenovno razsežnost. Preden začnete, morate ustvariti novo rešitev cenovne razsežnosti, če je še niste. Če že imate rešitev cenovne razsežnosti, lahko izvedete spremembe kar v tisti rešitvi. Če še niste ustvarili nove rešitve cenovne razsežnosti za vašo organizacijo, najprej do konca izvedite postopke v temi [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Dodajanje kategorij transakcij v obrazce in poglede
Če želite kategorije transakcij prikazati v uporabniškem vmesniku rešitve za cenovne razsežnosti, boste morali odpreti vse obrazce in poglede v ključnih entitetah rešitve Project Service in ta polja dodati v obrazce in poglede teh entitet.
V spodnji tabeli je obsežen seznam vnaprej pripravljenih obrazcev in pogledov, razvrščenih po entitetah, ki jih boste morali posodobiti z novimi polji. Če imate v svojih prilagoditvah v teh entitetah kakršne koli dodatne poglede ali obrazce, dodajte nova polja tudi vanje.

|  Entiteta        | Obrazci     |Pogledi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena vloge|• Informacije |• Cene kategorij dejavnih virov<br> • Povezani pogled za ceno kategorije vira|
|  Pribitek na ceno vloge|• Informacije|• Dejavni pribitek na ceno vloge<br>• Povezani pogled za pribitek na ceno vloge|
|  Podrobnosti vrstic ponudbe|• Podatki o projektu<br>• Hitro ustvarjanje projekta|• Dejavne podrobnosti vrstice ponudbe<br>• Skupne podrobnosti vrstice ponudbe<br>• Povezani pogled za podrobnosti vrstice ponudbe|
|  Podrobnost vrstice projektne pogodbe|• Podatki o projektu<br>• Hitro ustvarjanje projekta|• Podrobnosti združenih pogodb<br>• Podrobnosti dejavnih pogodb<br>• Povezani pogled za podrobnosti pogodbe|
|  Projektno opravilo|• Informacije<br>• Novi obrazec||
|  Član projektne ekipe|• Informacije<br>• Novi obrazec|• Dejavni člani projektne ekipe<br>• Člani projektne ekipe<br>• Povezani pogled za člane projektne ekipe|
|  Časovni vnos|• Informacije<br>• Ustvari časovni vnos|• Moji časovni vnosi po datumu<br>• Moji časovni vnosi za ta teden<br>• Časovni vnosi za odobritev|
|  Vrstica dnevnika|• Informacije<br>• Hitro ustvarjanje|• Dejavne vrstice dnevnika<br>• Povezani pogled za vrstice dnevnika|
|  Podrobnosti vrstice računa|• Informacije<br>• Hitro ustvarjanje|• Dejavne podrobnosti vrstice računa<br>• Transakcije računa, ki se zaračunajo<br>• Brezplačne transakcije računa<br>• Povezani pogled za podrobnosti vrstice računa<br>• Transakcije računa, ki se ne zaračunajo|
|  Dejansko|• Informacije<br>• Dejavno opravljeno delo|• Povezani pogled za opravljeno delo|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Nastavitev kategorije transakcije kot cenovne razsežnosti

1. V spletnem vmesniku odprite **Project Service** > **Nastavitve** > **Parametri**. 
2. Na zavihku **Cenovne razsežnosti na podlagi zneska** na strani **Parametri** lahko vidite, da mreža na zavihku prikazuje zapise v entiteti **Cenovne razsežnosti**.
3. Dodajte možnost **Kategorija transakcije** na ta seznam in nastavite polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** na **Da**.
4. V polju **Vrsta razsežnosti** izberite **Na podlagi zneska** in nato izberite prioriteto za možnost **Kategorija transakcije**, povezano s ceno in prodajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]