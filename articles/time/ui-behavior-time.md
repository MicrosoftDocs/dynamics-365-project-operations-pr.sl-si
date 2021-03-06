---
title: Vedenje uporabniškega vmesnika za časovni vnos
description: Ta tema vsebuje informacije o vedenju uporabniškega vmesnika za časovni vnos.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961749"
---
# <a name="time-entry-ui-behavior"></a>Vedenje uporabniškega vmesnika za časovni vnos

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Nova mreža **Tedenski časovni vnosi** kontrolnik po meri z dvema glavnima razdelkoma – **Razsežnosti** in **Trajanje**.

## <a name="dimensions"></a>Razsežnosti
Razdelek **Razsežnosti** prikazuje vse razsežnosti, ki jih je mogoče uporabiti za vnos časa. Vnaprej so podprte spodaj navedene razsežnosti:

  - Project
  - Projektno opravilo
  - Vloga
  - Vnesi
  - Stanje vnosa

V razdelku **Razsežnosti** urejanje v vrstici ni mogoče. Ta razdelek je podprt s pogledom, ki omogoča dodajanje polj po meri v tedensko mrežo časovnih vnosov.

## <a name="duration"></a>Trajanje
Razdelek »Trajanje« prikazuje dneve v tednu kot glave stolpcev. Ta razdelek omogoča urejanje v vrstici. Ko je ustvarjena vrstica za časovni vnos z ustreznimi razsežnostmi, lahko uporabniki hitro vnesejo količino časa, ki so ga porabili za te razsežnosti.

## <a name="create-a-new-time-entry"></a>Ustvarjanje novega časovnega vnosa

1. V mreži tedenskih časovnih vnosov izberite možnost **Novo**. 
2. V pogovornem oknu **Hitro ustvarjanje časovnega vnosa** izberite datum vnosa časa.
3. Vnesite podatke za razsežnosti **Projekt**, **Projektno opravilo**, **Vloga** in **Trajanje**. Te podatke je treba dodati v minutah, urah ali dneh s črkami **h**, **m** ali **d** ter številko. 
4. Vnesite opis za časovni vnos in morebitne komentarje o časovnem vnosu, ki jih je mogoče dati v skupno javno rabo. 

Ko shranite vnos, se vnesene vrednosti prikažejo v razdelku **Razsežnosti**. Informacije, vnesene v **Trajanje**, se prikažejo v tistem datumu, za katerega je bil ustvarjen časovni vnos.

Polja za iskanje so podprta s sistemskimi pogledi. Ko uporabnik na primer vnese projekt, se polje **Projektno opravilo** privzeto nastavi na pogled **Kopiraj**. Če želite ustvariti časovne vnose za opravila, ki niso dodeljena uporabniku, v pogovornem oknu za iskanje izberite **Spremeni pogled** in nato še pogled **Vsa dejavna projektna opravila**.

## <a name="edit-a-time-entry"></a>Urejanje časovnega vnosa 
Podrobnosti iz nekaterih polj na strani časovnega vnosa, kot so **Opis** in **Zunanji komentarji**, niso prikazane v tedenski mreži časovnih vnosov. Namesto tega se v celicah **Trajanje**, ki imajo te dodatne podrobnosti, pojavi majhen trikotni kazalnik. 

1. Če želite urediti časovni vnos, v vnosu časa izberite celico, ki jo želite posodobiti.
2. Izberite možnost **Uredi podrobnosti** za posodobitev podatkov v podoknu **Glavni obrazec za vnos časa**. 

## <a name="copy-a-time-entry-row"></a>Kopiranje vrstice časovnega vnosa
Po tem, ko je ustvarjena vrstica, lahko izberete možnost **Kopiraj vrstico**, če želite kopirati celotno vrstico v novo vrstico. Ko vrstico kopirate na ta način, se pri tem kopirajo tudi razsežnosti in trajanje. Izberete lahko izberejo tudi možnost **Uredi vrstico**, da posodobite vrednosti razsežnosti in trajanja v razdelku **Trajanje**.

## <a name="open-a-time-entry-behavior"></a>Odpiranje vedenja časovnega vnosa
Za podporo optimalnega in hitrega vnašanja v najbolj uporabljenih poljih je v tedenski mreži časovnih vnosov prikazana podmnožica izbranih razsežnosti in časovnih obdobij. Če si želite ogledati vse podrobnosti posameznega časovnega vnosa, v razdelku **Urejanje vnosa** izberite **Odpri**.

## <a name="submit-a-time-entry"></a>Pošiljanje časovnega vnosa
Pošljete lahko en sam časovni vnos ali skupino časovnih vnosov, tako da izberete blok celic ali celotno vrstico časovnega vnosa in nato izberete **Pošlji**. Poslani časovni vnosi se prikažejo kot vnosi, ki čakajo na odobritev na strani potrjevalcev za **Odobritev**. Ko so časovni vnosi uspešno poslani, jih ni več mogoče urejati.

## <a name="recall-a-time-entry"></a>Preklic časovnega vnosa
Poslane časovne vnose lahko tudi prekličete. Prekličete lahko posamezen časovni vnos, blok časovnih vnosov ali celotno vrstico časovnih vnosov. Preklicane časovne vnose je mogoče urejati.

## <a name="time-entry-status"></a>Stanje časovnega vnosa

- **Osnutek**: novim časovnim vnosom je samodejno dodeljeno stanje **Osnutek**. Izbrisati je mogoče le časovne vnose s stanjem **Osnutek**.
- **Poslano**: ko je časovni vnos poslan, se stanje posodobi na **Poslano**. 
- **Odobreno**: ko je poslan časovni vnos odobren, se stanje posodobi na **Odobreno**. 
- **Vrnjeno**: če je časovni vnos zavrnjen, se stanje posodobi na **Vrnjeno**, vnos pa je nato mogoče popraviti in ponovno poslati. 

## <a name="view-rejection-comments"></a>Ogled komentarjev ob zavrnitvi
Ko potrditelj zavrne časovni vnos, lahko potrditelj doda komentarje, da vir lahko lažje razume razlog za zavrnitev. Če si želite ogledati komentar zavrnitve časovnega vnosa, izberite **Odpri vnos**. Komentarji zavrnitve bodo prikazani na časovnici. Uporabnik se lahko odzove na komentarje ob zavrnitvi, preden znova pošlje vnos.

## <a name="copy-week"></a>Kopiraj teden
Ko je ustvarjenih nekaj časovnih vnosov, lahko uporabniki hkrati ustvarijo več časovnih vnosov.

1. V obrazcu **Časovni vnosi** izberite možnost **Kopiraj teden** za množično ustvarjanje dodatnih časovnih vnosov. 
2. V pogovornem oknu **Kopija** v razdelku **Od obdobja** uporabite polji **Začetni datum** in **Končni datum**, da določite datumski obseg za kopiranje časovnih vnosov. 
3. V razdelku **Do obdobja** v polju **Začetni datum** določite datum, za katerega želite ustvariti časovne vnose. 
4. Izberite **Kopiraj**. V razdelku **Do obdobja** se za izbran datum ustvari kopija časovnih vnosov za ustrezen dan v tednu v razdelku **Od obdobja**. Ponedeljkov časovni vnos iz prejšnjega tedna bo kopiran v ponedeljek za teden, ki je označen kot možnost **Do obdobja**.

## <a name="import"></a>Uvozi
Isti osnovni postopek se uporablja za uvoz iz rezervacij, dodelitev in izmenjav. Določite lahko datumski obseg za uvoz rezervacij in nato izberete točno tiste rezervacije, ki jih je treba kopirati v osnutke časovnih vnosov. 
