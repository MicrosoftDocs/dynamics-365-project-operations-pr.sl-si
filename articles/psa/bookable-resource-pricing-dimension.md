---
title: Uporaba vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti
description: V tej temi so na voljo informacije o uporabi vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti
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
ms.openlocfilehash: 0ffbb1f7aa25e723c7842259f1c0127b3d2e26d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012111"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Uporaba vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti

[!include [banner](../includes/psa-now-project-operations.md)]

V tej temi so na voljo informacije o uporabi vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti Preden začnete, morate ustvariti novo rešitev cenovne razsežnosti, če je še niste. Če že imate rešitev cenovne razsežnosti, lahko izvedete spremembe kar v tisti rešitvi. Če še niste ustvarili nove rešitve cenovne razsežnosti za vašo organizacijo, najprej do konca izvedite postopke v temi [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Dodajanje vira, ki ga je mogoče rezervirati, v obrazce in poglede
Če želite polja prikazati v uporabniškem vmesniku rešitve za cenovne razsežnosti, boste morali odpreti vse obrazce in poglede v ključnih entitetah rešitve Project Service in ta polja dodati v obrazce in poglede teh entitet.
V spodnji tabeli je obsežen seznam vnaprej pripravljenih obrazcev in pogledov po entitetah, ki jih boste morali posodobiti. Če imate v svojih prilagoditvah v teh entitetah kakršne koli dodatne poglede ali obrazce, dodajte nova polja tudi vanje.
Odprite raziskovalca rešitev za rešitev cenovnih razsežnosti in nato kliknite **Objavi vse prilagoditve.**


|   Entiteta        | Obrazci   |Pogledi        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Nastavitev vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti

1. V spletnem vmesniku odprite **Project Service** > **Nastavitve** > **Parametri**. Na zavihku **Cenovne razsežnosti na podlagi zneska** na strani **Parameter** lahko vidite, da mreža na zavihku prikazuje zapise v entiteti cenovnih razsežnosti. 
2. Na ta seznam cenovnih razsežnosti dodajte **Vir, ki ga je mogoče rezervirati** kot **msdyn_bookableresource**. 
3. Navedite kontekst, v katerem vir, ki ga je mogoče rezervirati, deluje kot cenovna razsežnost, in nastavite vrednosti **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo**.
4. V polju **Vrsta cenovne razsežnosti** izberite možnost **Na podlagi zneska**. 
5. Izberite prioriteto cene in prodaje za vir, ki ga je mogoče rezervirati. Običajno ima vir, ki ga je mogoče rezervirati, najvišjo prioriteto, ko je vključen kot cenovna razsežnost; to lahko zagotovite tako, da nastavite vrednost na **1** (ali **0**: odvisno od vašega načina določanja prioritete).

## <a name="set-up-pricing-dimension-field-names"></a>Nastavitev imen polj cenovnih razsežnosti

Ko je ime polja cenovne razsežnosti v tabeli **Cena vloge** drugačno od imena polja v drugih entitetah, kjer mora delovati privzeto nastavljanje cene, je treba zapis cenovnih razsežnosti seznaniti z drugačnimi imeni.    
Entiteta **Člani projektne ekipe** ima nekoliko drugačno ime (**msdyn_bookableresourceid**) za vir, ki ga je mogoče rezervirati, od imena v entiteti **Cena vloge** (**msdyn_bookableresource**). S tem je treba seznaniti zapis cenovne razsežnosti za **msydn_bookableresource**. 
1. Če želite to narediti, dvokliknite vrstico v mreži **Cenovne razsežnosti**, da odprete stran razsežnosti imena **msdyn_bookableresource**.
2. Na zavihku **Povezano** strani razsežnosti kliknite **Imena polj cenovnih razsežnosti**.

 ![Zavihek z imeni polj cenovnih razsežnosti](media/PD-fieldname.png)

4. V povezanem pogledu, ki se odpre, kliknite možnost **Dodaj novo ime polja cenovne razsežnosti**.

 ![Dodajanje novih imen polj cenovnih razsežnosti](media/Add-NewPD-fieldname.png)


Odpre se stran **Novo ime polja cenovne razsežnosti** za **msdyn_bookableresource**. 

5. V polje **Logično ime entitete** dodajte ime **msdyn_projectteam**, v polje **Ime polja** pa **msdyn_bookableresourceid**. Shranite zapis.

 ![Oblika novega imena polja cenovne razsežnosti](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]