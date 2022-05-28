---
title: Prenos proračunov projektov ob koncu proračunskega leta
description: Ta članek vsebuje informacije o tem, kako prenesti preostale proračunske zneske v prihodnja leta in ustvariti podrobnosti proračunskega registra.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5b4e768cb78d6a6cb76b3c338fd76363d5290ebd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684064"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Prenos proračunov projektov ob koncu proračunskega leta

[!include [banner](../includes/banner.md)]

Ko delate na večletnem projektu, vam bo morda ob koncu proračunskega leta ostalo nekaj proračunskih sredstev. Preostala proračunska sredstva lahko prenesete v prihodnje leto in ustvarite podrobnosti registra proračuna za zneske na povezanih računih glavne knjige. Preden prenesete preostale zneske, preglejte in analizirajte zneske preostalih proračunskih sredstev.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Preglejte in analizirajte preostale zneske proračunskih sredstev

Opravite naslednje korake za pregled proračunskih sredstev ob koncu leta za projekte, vendar zneskov ne prenesite naprej.

1. Odprite **Vodenje projektov in računovodstvo** > **Redno** > **Proračuni** > **Prenos proračunov**. 
2. Na strani **Postopek prenosa proračuna projekta** na zavihku **Možnosti ob koncu leta** preverite, ali možnost **Prenesi preostala proračunska sredstva za projekt** ni omogočena.
3. Na zavihku **Parametri** v polju **Proračunsko leto projekta** izberite proračunsko leto, za katero si želite ogledate znesek preostalih sredstev proračuna. 
4. V polje **Začetno proračunsko leto** izberite proračunsko leto, za katero si želite ogledate znesek preostalih sredstev proračuna. 
5. V polju **Od modela napovedi** izberite **Preostali proračun**. 
6. Če želite vključiti projekte, ki ustrezajo izbranim merilom in za katere je bil porabljen ves proračun, izberite **Prikaži porabljene proračune**.  
7. Na zavihku za **izbiro proračunov** izberite **Pridobi vse proračune**, da naložite vse proračune, ki ustrezajo izbranim merilom, in nato izberite **Obdelaj**. 
8. Če želite oblikovati poizvedbo zbirke podatkov, ki v podokno naloži določen nabor proračunov, izberite **Pridobi izbrane proračune**.

Če želite več informacij o določeni vrstici v podoknu, izberite vrstico in nato izberite **Prikaži podrobnosti proračuna** ali **Prikaži račune**.

## <a name="carry-forward-remaining-budget-amounts"></a>Prenos zneska preostalih proračunskih sredstev 

Ko obdelate znesek preostalih proračunskih sredstev, lahko ustvarite transakcije v glavni knjigi za zneske, ki jih želite prenesti. Če želite ustvariti transakcije glavne knjige, opravite korake v razdelku [Prenos zneskov proračuna in ustvarjanje transakcij glavne knjige](#carry-forward). 

> [!NOTE]
> Preneseni zneski proračuna se prenesejo v model napovedi, ki je izbran na strani **Modeli napovedi** kot model napovedi za prenos.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Prenos zneskov proračuna in ustvarjanje transakcij glavne knjige

1.  Izberite **Vodenje projektov in računovodstvo** > **Redno** > **Proračuni** > **Prenos proračunov**. 
2. Na strani **Postopek prenosa proračuna projekta** izberite **Konec leta** in nato omogočite **Prenesi preostala proračunska sredstva za projekt** in **Ustvari vnose v register proračuna v glavni knjigi**. 
3. Na zavihku **Parametri** pri skupini polj **Projektni parametri** izberite naslednje:

   - **Proračunsko leto projekta**: izberite začetek proračunskega leta, za katero si želite ogledate znesek preostalih sredstev proračuna. 
   - **Poslovni izid**: ustvarite transakcije poslovnega izida v glavni knjigi. 
   -  **Postavka za nedokončano storitev**: ustvarite transakcije za nedokončane storitve (WIP) v glavni knjigi.
   -  **Plačilna lista**: v glavni knjigi ustvarite transakcije za dodelitev plače. 

5. V skupini polj **Glavna knjiga** navedite naslednje podatke: 

   - V polje **Začetno proračunsko leto** izberite proračunsko leto, za katero želite prenesti znesek preostalih sredstev proračuna za projekte. Privzeta vrednost je eno leto po vrednosti v polju **Proračunsko leto projekta**.
   -  V polju **Obdobje za prenos** izberite obdobje, za katero želite v glavni knjigi ustvariti podrobnosti registra proračuna. To je običajno prvo obdobje na začetnem proračunskem letu.

6. V skupini polj **Kopiraj od/v** navedite naslednje podatke:

   - V polju **Od modela napovedi** izberite model napovedi za proračun projekta, povezan z zneski preostalega proračuna, ki jih želite prenesti za projekte. 
   - V polju **V model za proračun glavne knjige** izberite model za proračun glavne knjige, povezan z zneski proračuna, ki jih želite prenesti v glavno knjigo. 
   -  Izberite **Prenesi valuto prodaje**, da prodajno valuto projekta uporabite za transakcije glavne knjige, ki se ustvarijo, ko prenesete zneske proračuna za projekte. Če možnost ni izbrana, transakcije uporabljajo računovodsko valuto. 
   -  Izberite **Prikaži porabljene proračune**, da vključite projekte, za katere je bil porabljen že ves dodeljen proračun, vendar izpolnjujejo druga merila, ki ste jih izbrali pri projektih, prikazanih v spodnjem podoknu.

7. Na zavihku za **izbiro proračunov** izberite **Pridobi vse proračune**, da naložite vse proračune, ki ustrezajo izbranim merilom. Če želite oblikovati poizvedbo zbirke podatkov, ki v podokno naloži določen nabor proračunov projektov, izberite **Pridobi izbrane proračune**.
8. Za vsak projekt, ki ga želite obdelati, izberite možnost na začetku vrstice za projekt.

    > [!TIP]
    > Če želite izbrati vse projekte ali večino od njih, izberite kljukico v zgornjem levem kotu. Če želite izključiti obdelavo katerega koli projekta, počistite kljukico za ta projekt.

9. Če želite zneske preostalega proračuna za izbrane projekte prenesti na izbrano proračunsko leto in v glavni knjigi ustvariti podrobnosti registra proračuna, izberite **Obdelaj**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Prenos zneskov proračuna brez ustvarjanja transakcij glavne knjige

1. Odprite **Vodenje projektov in računovodstvo** > **Redno** > **Proračuni** > **Prenos proračunov**.
2. Na strani **Postopek prenosa proračuna projekta** v polju **Možnosti ob koncu leta** izberite možnost **Prenesi preostala proračunska sredstva za projekt**.
3. V skupini **Parametri** v polju **Proračunsko leto projekta** izberite proračunsko leto, za katero si želite ogledate znesek preostalih sredstev proračuna.
4. V skupini **Kopiraj od/v** navedite naslednje podatke:

   - V polju **Od modela napovedi** izberite model napovedi za proračun projekta, povezan z zneski preostalega proračuna, ki jih želite prenesti za projekte. 
   - Če želite vključiti projekte, za katere je bil porabljen ves proračun, vendar ustrezajo drugim izbranim merilom, izberite **Prikaži porabljene proračune**.
   - V skupini za **izbiro proračunov** izberite **Pridobi vse proračune**, da naložite vse proračune, ki ustrezajo izbranim merilom. Če želite oblikovati poizvedbo zbirke podatkov, ki v podokno naloži določen nabor proračunov projektov, izberite **Pridobi izbrane proračune**.

5. Za vsak projekt, ki ga želite obdelati, izberite možnost na začetku vrstice za projekt. 
6. Izberite **Obdelaj** za prenos preostalih zneskov proračuna za izbrane projekte na izbrano proračunsko leto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
