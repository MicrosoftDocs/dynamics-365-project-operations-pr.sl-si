---
title: Ustvarjanje in potrjevanje dnevnikov popravkov
description: Ta tema vsebuje informacije o tem, kako ustvariti in potrditi dnevnik popravkov.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127793"
---
# <a name="create-and-confirm-correction-journals"></a>Ustvarjanje in potrjevanje dnevnikov popravkov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Občasno je vnos za čas ali strošek vnesen napačno. Svetovalec lahko na primer pri ustvarjanju časovnega vnosa izbere napačen datum ali pa prenese številke pri vnosu stroška. Če svetovalec ne more posodobiti poslanih vnosov, lahko skrbnik neposredno popravi vnos za projekt.

Za dokončanje postopkov v tej temi boste potrebovali skrbniška dovoljenja.

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

Na naslednji grafiki sta na primer dve vrstični postavki s količino 8,00, ki imata bremena, navedena v stolpcu »Znesek«. Poleg tega sta v stolpcu »Znesek« prikazani dve vrstici s količino –8,00, ki prikazujeta znesek, knjižen v dobro. S temi popravki se količina zmanjša na nič.

 
## <a name="correct-approved-expense-entries"></a>Popravek odobrenih vnosov stroškov

Za popravljanje enega ali več vnosov stroškov opravite naslednje korake. 

1. V območju **Prodaja** v levem podoknu za krmarjenje pri možnosti **Transakcije** izberite **Odobreni stroški**.

2. Na seznamu **Odobreni stroški** izberite projekt, ki ga želite popraviti, nato pa izberite **Popravi vnose**. Novi dnevnik popravkov bo ustvarjen samodejno z dodeljeno vrsto **Popravek stroška**. 

3. Na strani **Novi dnevnik** vnesite **Opis** za popravek in na zavihku **Popravek stroška** v razdelku **Nove vrednosti za stroške** izberite podatkovna polja, ki jih želite popraviti za izbrane vrstice stroškov. Strošek lahko na primer dodelite za drug **Projekt** ali popravite možnosti **Kategorija stroška**, **Datum stroška** ali **Vir, ki ga je mogoče rezervirati**.

4. Izberite **Predogled**. V pogovornem oknu izberite **V redu**. 

5. Na zavihku **Vrstice dnevnika** preverite popravke. Lahko si ogledate seznam prvotnih dejanskih vrednosti, povezanih z izbranimi vnosi stroškov, ki so bili razveljavljani, ter popravljene ustrezne vrstice, ki so bile ustvarjene.

6. Če so popravljene vrednosti v skladu s pričakovanji, izberite **Potrdi**. V pogovornem oknu izberite **V redu**. Če vrednosti niso prikazane v skladu s pričakovanji, izberite **Prekliči**, da se vrnete na seznam **Odobreni stroški**. Ponovite korake od 2. do 5. 

> [!NOTE]
> Popravljene dejanske vrednosti bodo imele iste vrednosti, kot ste jih izbrali v razdelku **Nove vrednosti za stroške**.

7. Ko potrdite dnevnik za popravke, se pomaknite nazaj do projekta ali projektov, ki ste jih posodobili, da si ogledate spremembe.  

8. Na strani projekta, na zavihku **Opravljeno delo** preglejte **Povezani pogled za opravljeno delo**. Izvirni vnosi in popravljeni vnosi so navedeni. Naslednji grafični prikaz prikazuje izvirne zneske za vnos stroška in ustrezne popravljene zneske za vnos stroška. 


