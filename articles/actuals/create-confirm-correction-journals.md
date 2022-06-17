---
title: Ustvarjanje in potrjevanje dnevnikov popravkov
description: Ta članek vsebuje informacije o tem, kako ustvariti in potrditi dnevnik popravkov.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928084"
---
# <a name="create-and-confirm-correction-journals"></a>Ustvarjanje in potrjevanje dnevnikov popravkov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Včasih je lahko vnos časa ali stroškov napačno vpisan. Na primer, svetovalec lahko izbere napačen datum, ko ustvari vnos časa, ali pa izbere napačen projekt, ko vnese strošek. Če svetovalec ne more posodobiti predloženih vnosov, lahko zaledni skrbnik neposredno popravi dejanske podatke za projekt.

## <a name="correct-approved-time-entries"></a>Popravek odobrenih časovnih vnosov     

Za popravljanje posameznega ali več časovnih vnosov za projekt izvedite naslednje korake.

1. V območju **Prodaja** izberite **Transakcije** in nato izberite **Odobren čas**. 

2. Na seznamu **Odobren čas** poiščite in izberite enega ali več odobrenih časovnih vnosov, ki jih želite popraviti. S filtrom lahko poiščete povezane vnose. filtrirate lahko na primer po ID-ju projekta in izberete vse odobrene časovne vnose s tem ID-jem projekta.

3. Izberite **Popravi vnose**. Samodejno se ustvari nov dnevnik popravkov z dodeljeno vrsto **Popravek časa**. Vnosi, ki ste jih izbrali, so dodani v dnevnik. 

4. Na strani **Novi dnevnik** vnesite **Opis** za svoj dnevnik za popravke in nato izberite zavihek **Popravki časovnih vnosov**.  

5. V razdelku **Nove vrednosti za časovne vnose** po potrebi posodobite polja s pravilnimi informacijami. Lahko na primer spremenite dodeljeni projekt ali vir, ki ga je mogoče rezervirati.

6. Izberite **Predogled**. V pogovornem oknu izberite **V redu**. Na zavihku **Vrstice dnevnika** si lahko ogledate seznam prvotnih dejanskih vrednosti, povezanih z izbranimi časovnimi vnosi, ki so bili razveljavljani, ter popravljene ustrezne vrstice, ki so bile ustvarjene. Če je treba izvesti dodatne popravke, ponovite 5. in 6. korak. 

    > [!NOTE]
    > Vse popravljene dejanske vrednosti bodo imele iste vrednosti, kot ste jih izbrali v razdelku **Nove vrednosti za časovne vnose**.

7. Če se popravki prikažejo po pričakovanjih, izberite **Potrdi**. V pogovornem oknu izberite **V redu**.

8. Vrnite se na območje **Prodaja**, izberite **Projekti** in nato odprite projekt, za katerega ste pravkar posodobili časovne vnose. 

9. Na strani **Projekti** v zavihku **Opravljeno delo** si oglejte spremembe, ki ste jih izvedli. 

    > [!NOTE]
    > Če zavihek **Opravljeno delo** ni viden, izberite **Povezano** > **Opravljeno delo**.  

10. Na seznamu **Povezani pogled za opravljeno delo** lahko vidite, da so prvotni časovni vnosi, ki so bili razveljavljeni, še vedno navedeni, navedeni pa so tudi ustrezni popravljeni časovni vnosi. 

 
## <a name="correct-approved-expense-entries"></a>Popravek odobrenih vnosov stroškov

Za popravljanje enega ali več vnosov stroškov opravite naslednje korake. 

1. V območju **Prodaja** v levem podoknu za krmarjenje pri možnosti **Transakcije** izberite **Odobreni stroški**.

2. Na seznamu **Odobreni stroški** izberite projekt, ki ga želite popraviti, nato pa izberite **Popravi vnose**. Novi dnevnik popravkov bo ustvarjen samodejno z dodeljeno vrsto **Popravek stroška**. 

3. Na strani **Novi dnevnik** vnesite **Opis** za popravek in na zavihku **Popravek stroška** v razdelku **Nove vrednosti za stroške** izberite podatkovna polja, ki jih želite popraviti za izbrane vrstice stroškov. Strošek lahko na primer dodelite za drug **Projekt** ali popravite možnosti **Kategorija stroška**, **Datum stroška** ali **Vir, ki ga je mogoče rezervirati**.

4. Izberite **Predogled**. V pogovornem oknu izberite **V redu**. 

5. Na zavihku **Vrstice dnevnika** preverite popravke. Lahko si ogledate seznam prvotnih dejanskih vrednosti, povezanih z izbranimi vnosi stroškov, ki so bili razveljavljani, ter popravljene ustrezne vrstice, ki so bile ustvarjene.

6. Če so popravljene vrednosti v skladu s pričakovanji, izberite **Potrdi**. V pogovornem oknu izberite **V redu**. Če vrednosti niso prikazane v skladu s pričakovanji, izberite **Prekliči**, da se vrnete na seznam **Odobreni stroški**. Ponovite korake od 2. do 5. 

7. Ko potrdite dnevnik popravkov, se vrnite na projekt ali projekte, ki ste jih posodobili, da si ogledate svoje spremembe.

8. Na strani projekta, na **Dejansko stanje** zavihek, preglejte **Dejanski povezani pogled** seznam. Izvirni vnosi in popravljeni vnosi so navedeni.


## <a name="correct-approved-material-usage-logs"></a>Popravite odobrene dnevnike uporabe materiala

Izvedite naslednje korake, da popravite enega ali več vnosov v dnevnik porabe materiala.

1. V **Prodaja** območje, v levem podoknu za krmarjenje, pod **Transakcije**, izberite **Dejansko stanje**.

2. V **Dejansko stanje** seznamu, uporabite filtre stolpcev, da izberete **Material** transakcijski razred, tako da so prikazani samo dejanski podatki za materiale. Uporabite druge filtre stolpcev, da dodatno omejite prikazane dejanske vrednosti. Ko najdete želeni niz dejanskih vrednosti, izberite dejanske vrednosti in nato izberite **Pravilni vnosi**. Nov dnevnik popravkov se samodejno ustvari in **Popravek materiala** vrsta je dodeljena.

3. Na **Novi časopis** strani, v **Opis** vnesite opis popravka. Nato na **Popravek materiala** zavihek, v **Nove vrednosti za materiale** razdelku izberite podatkovna polja, ki jih želite popraviti za izbrane vrstice materiala. Gradivo lahko na primer dodelite drugemu projektu ali popravite izdelek, datum materiala ali pogodbo s podizvajalcem.

4. Izberite **Predogled**. Nato v pogovornem oknu izberite **v redu**.

5. Na **Dnevniške vrstice** zavihek, preverite popravke. Ogledate si lahko seznam prvotnih dejanskih dejstev, ki se nanašajo na izbrane vnose materiala, ki so bili obrnjeni, in popravljene ustrezne vrstice, ki so bile ustvarjene.

6. Če so popravljene vrednosti v skladu s pričakovanji, izberite **Potrdi**. Nato v pogovornem oknu izberite **v redu**. Če vrednosti niso po pričakovanjih, izberite **Prekliči** da se vrnem na **Dejansko stanje** seznam. Nato ponovite korake od 2 do 5.

7. Ko potrdite dnevnik popravkov, se vrnite na projekt ali projekte, ki ste jih posodobili, da si ogledate svoje spremembe.

8. Na strani projekta, na **Dejansko stanje** zavihek, preglejte **Dejanski povezani pogled** seznam. Izvirni vnosi in popravljeni vnosi so navedeni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
