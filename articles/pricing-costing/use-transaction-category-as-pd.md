---
title: Uporaba kategorije transakcije kot cenovne razsežnosti
description: Ta članek vsebuje informacije o tem, kako uporabiti polje Kategorija transakcije kot dimenzijo cene.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911723"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Uporaba kategorije transakcije kot cenovne razsežnosti


_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Ta članek pojasnjuje, kako uporabljati **Kategorija transakcije** polje kot dimenzijo cene. 

## <a name="prerequisites"></a>Zahteve
Preden dokončate postopke v tem članku, morate imeti novo rešitev za cenovno dimenzijo za svojo organizacijo. Če je še niste ustvarili, glejte [Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Dodajanje polja Kategorija transakcije v obrazce in poglede
Če želite narediti polje **Kategorija transakcije** vidno v rešitvi za cenovne razsežnosti, morate polje dodati vsem obrazcem in pogledom v obliki entitete.

V spodnji tabeli so navedeni vsi vnaprej pripravljeni obrazci in pogledi, razvrščeni po entitetah. Novo polje boste morali dodati tudi v vse dodatne obrazce ali poglede v vaših entitetah po meri.

|  Entity        | Obrazci     |Pogledi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena vloge| Informacije |- Cene kategorij dejavnih virov<br> - Povezana cena kategorije vira |
|  Pribitek na ceno vloge| Informacije|- Dejavni pribitek na ceno vloge<br>- Povezani pribitek na ceno vloge |
|  Podrobnosti vrstice ponudbe|- Podatki o projektu<br>- Hitro ustvarjanje projekta| - Dejavne podrobnosti vrstice ponudbe<br>- Skupne podrobnosti vrstice ponudbe<br>- Povezane podrobnosti vrstice ponudbe |
|  Podrobnost vrstice projektne pogodbe|- Podatki o projektu<br>- Hitro ustvarjanje projekta|- Podrobnosti združenih pogodb<br>- Podrobnosti dejavnih pogodb<br>- Povezane podrobnosti pogodbe |
|  Projektno opravilo|- Informacije<br>- Novi obrazec| &nbsp; |
|  Član projektne ekipe|- Informacije<br>- Novi obrazec|- Dejavni člani projektne ekipe<br>- Člani projektne ekipe<br>- Povezani člani projektne ekipe |
|  Časovni vnos|- Informacije<br>- Ustvari časovni vnos|- Moji časovni vnosi po datumu<br>- Moji časovni vnosi za ta teden<br>- Časovni vnosi za odobritev|
|  Vrstica dnevnika|- Informacije<br>- Hitro ustvarjanje|- Dejavne vrstice dnevnika<br>- Povezane vrstice dnevnika|
|  Podrobnosti vrstice računa|- Informacije<br>- Hitro ustvarjanje|- Dejavne podrobnosti vrstice računa<br>- Transakcije računa, ki se zaračunajo<br>- Brezplačne transakcije računa<br>- Povezane podrobnosti vrstice računa <br>- Transakcije računa, ki se ne zaračunajo|
|  Dejansko|- Informacije<br>- Dejavno opravljeno delo| Povezano opravljeno delo |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Nastavitev polja kategorije transakcije kot cenovne razsežnosti

1. Odprite **Nastavitve** > **Parametri**. 
2. Na zavihku **Cenovne razsežnosti na podlagi zneska** na strani **Parametri** preverite, ali mreža na zavihku prikazuje zapise v entiteti **Cenovne razsežnosti**.
3. Dodajte možnost **Kategorija transakcije** na ta seznam in nastavite polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** na **Da**.
4. V polju **Vrsta razsežnosti** izberite **Na podlagi zneska** in nato izberite prioriteto za možnost **Kategorija transakcije**, saj je povezana s ceno in prodajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]