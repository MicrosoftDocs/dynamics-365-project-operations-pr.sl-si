---
title: Dodajanje zahtevanih polj po meri v entitete za nastavitev cene in transakcijske entitete
description: Ta tema vsebuje informacije o tem, kako dodati zahtevane sklice na polja po meri entitetam ter obrazcem in pogledom.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 36c95913cc72e293c3015e1b9d3055aac476eebb4cf7d7993741d3cb61de0e13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006188"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Dodajanje zahtevanih polj po meri v entitete za nastavitev cene in transakcijske entitete

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ta tema predpostavlja, da ste zaključili postopke v temi [Ustvarjanje polj in entitet po meri za uporabo kot cenovne razsežnosti](create-custom-fields-entities-pricing-dimensions.md). Če teh postopkov še niste izvedli, se vrnite nazaj in jih dokončajte, preden se vrnete na to temo. 

V tej temi je s postopki prikazano, kako dodate zahtevane sklice na polja po meri entitetam in elementom uporabniškega vmesnika, kot so obrazci in pogledi.

## <a name="add-custom-pricing-dimension-fields"></a>Dodajanje polj cenovne razsežnosti po meri 
Ko ustvarite polja in entitete po meri, morate nastaviti entitete za nastavitev cene in transakcijske entitete tako, da vključijo entitete ali nabore možnosti po meri. To naredite tako, da ustvarite sklicno polje. Glede na to, ali seznam cenovnih razsežnosti vključuje razsežnosti na osnovi nabora možnosti ali razsežnosti na osnovi entitete oz. oboje, sledite le korakom v razdelku **Cenovne razsežnosti po meri na osnovi nabora možnosti** ali **Cenovne razsežnosti po meri na osnovi entitete** oz. v obeh.

### <a name="option-set-based-custom-pricing-dimensions"></a>Cenovne razsežnosti po meri na osnovi nabora možnosti
Če cenovna razsežnost po meri temelji na naboru možnosti, jo dodajte kot polje v ključne entitete. V spodnjem postopku se za cenovne razsežnosti na osnovi nabora možnosti uporabljata možnosti **Lokacija dela vira** in **Delovni čas vira**. Najprej ju morate dodati kot polji v entiteti za določanje cene **Cena vloge** in **Pribitek na ceno vloge**.

1. V storitvi Project Operations izberite **Nastavitve** > **Rešitve**, nato pa dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete > Cena vloge**.
3. Razširite entiteto **Cena vloge** in izberite **Polja**.
4. Izberite **Novo**, da ustvarite novo polje z imenom **Lokacija dela vira**, in kot vrsto polja izberite **Nabor možnosti**. 
5. Izberite **Uporabi obstoječi nabor možnosti** in nabor možnosti **Lokacija dela vira** ter nato izberite **Shrani**.
6. Ponovite korake od 1 do 5, da dodate to polje v entiteto **Pribitek na ceno vloge**. 
7. Ponovite korake od 1 do 5 za nabor možnosti **Delovni čas vira**.

> [!IMPORTANT]
> Če dodate polje v več entitet, uporabite isto ime polja v vseh entitetah. 

> ![Dodajanje lokacije vira dela v ceno vloge.](media/RWL-Field.png)

V fazah prodaje in ocenjevanja za projekt se za oceno vrednosti ponudbe/projekta uporabijo ocene obsega dela, ki je potreben za dokončanje dela z oznako **Lokalno** in **Na lokaciji**, in sicer z vrednostma **Redni delovni čas** in **Nadure**. Polji **Lokacija dela vira** in **Delovni čas vira** bosta dodani entitetam ocenjevanja **Podrobnost vrstice ponudbe**, **Podrobnost vrstice pogodbe**, **Član projektne ekipe** in **Vrstica ocene**.

1. V storitvi Project Operations izberite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete > Podrobnost vrstice ponudbe**.
3. Razširite entiteto **Podrobnost vrstice ponudbe** in izberite **Polja**.
4. Izberite **Novo**, da ustvarite novo polje z imenom **Lokacija dela vira**, in izberite vrsto polja **Nabor možnosti**. 
5. Izberite **Uporabi obstoječi nabor možnosti** in **Lokacija dela vira** ter nato izberite **Shrani**.
6. Ponovite korake od 1 do 5, da dodate to polje v entitete **Podrobnost vrstice projektne pogodbe**, **Član projektne ekipe** in **Vrstica ocene**.
7. Ponovite korake od 1 do 6 za nabor možnosti **Delovni čas vira**. 

> ![Dodajanje lokacije dela vira v vrstico ocene.](media/RWL-Default-Value.png)

Za namene dostave in izdajanja računov je treba za opravljeno delo natančno določiti ceno. V opravljenih delih projekta izberite, ali je bilo izvedeno **lokalno** ali **na lokaciji** in ali je bilo opravljeno med **rednim delovnim časom** ali **nadurami**. Polji **Lokacija dela vira** in **Delovni čas vira** morata biti dodani v entitete **Časovni vnos**, **Dejansko**, **Podrobnosti vrstice računa** in **Vrstica dnevnika**.

1. Izberite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete > Časovni vnos**.
3. Razširite entiteto **Podrobnost vrstice ponudbe** in nato izberite **Polja**.
4. Izberite **Novo**, da ustvarite novo polje z imenom **Lokacija dela vira**, in kot vrsto polja izberite **Nabor možnosti**. 
5. Izberite **Uporabi obstoječi nabor možnosti** in nabor možnosti **Lokacija dela vira** ter nato izberite **Shrani**.
6. Ponovite korake od 1 do 5, da dodate to polje v entitete **Dejansko**, **Podrobnost vrstice računa** in **Vrstica dnevnika**.
7. Ponovite korake od 1 do 6 za nabor možnosti **Delovni čas vira**. 

> ![Dodajanje lokacije dela vira v časovni vnos.](media/RWL-time-entry.png)

S tem dokončate spremembe sheme, ki so potrebne za razsežnosti po meri na osnovi nabora možnosti.

## <a name="entity-based-custom-pricing-dimensions"></a>Cenovne razsežnosti po meri na osnovi entitete

Če je cenovna razsežnost po meri entiteta, dodate odnose 1: N med entiteto razsežnosti in ključnimi entitetami. Pri uporabi zgornjega primera za standardni naziv je razumno pričakovati, da je vsakemu zaposlenemu dodeljen standardni naziv. Zato potrebujete odnos 1:N za standardni naziv proti viru, ki ga je mogoče rezervirati, ali odnos N:1 za vir, ki ga je mogoče rezervirati, proti standardnemu nazivu.

1. V storitvi Project Operations izberite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete > Standardni naziv**.
3. Razširite entiteto **Standardni naziv** in izberite **Odnosi 1: N**.
4. Izberite **Novo**, da ustvarite nov odnos 1: N, ki se imenuje **Standardni naziv proti viru, ki ga je mogoče rezervirati**. Vnesite zahtevane informacije in izberite **Shrani**.

> ![Dodajanje standardnega naziva kot sklicnega polja v vir, ki ga je mogoče rezervirati.](media/ST-BR.png)

Standardni naziv morate dodati tudi entitetam za določanje cene **Cena vloge** in **Pribitek na ceno vloge**. Tudi to zaključite z uporabo odnosov 1: N med entitetama **Standardni naziv** in **Cena vloge** ter entitetama **Standardni naziv** in **Pribitek na ceno vloge**.

1. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete > Standardni naziv**.
2. Razširite entiteto **Standardni naziv** in izberite **Odnosi 1: N**.
3. Izberite **Novo**, da ustvarite nov odnos 1: N, ki se imenuje **Standardni naziv proti ceni vloge**. Vnesite zahtevane informacije in izberite **Shrani**.
4. Ponovite korake od 1 do 4, da ustvarite odnose 1: N med entitetama **Standardni naziv** in **Pribitek na ceno vloge**.

V fazah prodaje in ocenjevanja za projekt so za določanje cene ponudbe/projekta pri vsakem standardnem nazivu potrebne ocene obsega dela. To pomeni, da so potrebni odnosi 1: N od standardnega naziva proti vsaki od teh entitet ocenjevanja: 

- **Podrobnost vrstice ponudbe**
- **Podrobnost vrstice projektne pogodbe**
- **Član projektne ekipe**
- **Vrstica ocene**

5. Ponovite korake od 1 do 5, da ustvarite odnose 1: N med entiteto **Standardni naziv** in entitetami **Podrobnost vrstice ponudbe**, **Podrobnost vrstice projektne pogodbe**, **Član projektne ekipe** in **Vrstica ocene**.

> ![Dodajanje standardnega naziva kot sklicnega polja v vrstico ocene.](media/ST-Estimate-Line.png)

  V fazah dostave in izdajanja računov mora biti v opravljenih delih projekta za delo, ki ga opravi posamezni standardni naziv, natančno določena cena. To pomeni, da potrebujete odnos 1: N med entiteto **Standardni naziv** in entitetami **Časovni vnos**, **Dejansko**, **Podrobnost vrstice računa** in **Vrstica dnevnika**.

6. Ponovite korake od 1 do 6, da ustvarite odnos 1: N med entiteto **Standardni naziv** in entitetami **Časovni vnos**, **Dejansko**, **Podrobnost vrstice računa** in **Vrstica dnevnika**.

> ![Dodajanje standardnega naziva kot sklicnega polja v časovni vnos.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Nastavitev privzete vrednosti razsežnosti z uporabo funkcij preslikave v platformi
Pri časovnem vnosu je uporabno, če sistem nastavi privzeto vrednost standardnega naziva v časovnem vnosu iz vira, ki ga je mogoče rezervirati in ki beleži časovni vnos. Uporabite spodnje korake, da dodate preslikave polj v odnosu 1: N iz entitete **Vir, ki ga je mogoče rezervirati** v entiteto **Časovni vnos**.

1. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete > Standardni naziv**.
2. Razširite entiteto **Standardni naziv** in izberite **Odnosi 1: N**.
3. Dvokliknite **Vir, ki ga je mogoče rezervirati, v časovni vnos**. Na strani **Odnos** izberite **Uporabi preslikave polj**. 
4. Izberite **Novo**, da ustvarite novo preslikavo polja med poljem **Standardni naziv** v entiteti **Vir, ki ga je mogoče rezervirati** in sklicnim poljem **Standardni naziv** v entiteti **Časovni vnos**. 

> ![Nastavitev preslikav polj za omogočanje nastavljanja privzete vrednosti standardnega naziva iz entitete vira, ki ga je mogoče rezervirati, v entiteto časovnega vnosa.](media/ST-Mapping2.png)

S tem dokončate spremembe sheme, ki so potrebne za razsežnosti po meri na osnovi entitete.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Dodajanje polj po meri v obrazce, poglede in pravila poslovanja

Ko naredite vse potrebne spremembe sheme, morate polja dodati v obrazce in poglede, tako da so vidna v uporabniškem vmesniku.

1. Odprite obrazec ali pogled. V podoknu za krmarjenje na desni izberite polje in ga povlecite v delovno območje obrazca. 
2. Če urejate pogled, uporabite podokno za krmarjenje na desni, izberite **Dodaj polja** in v pogovornem oknu **Seznam polj** izberite polja, ki jih potrebujete, ter izberite **V redu**.

V spodnji tabeli je obsežen seznam vnaprej pripravljenih obrazcev in pogledov po entitetah, ki jih boste morali posodobiti z novimi polji. Če imate v svojih prilagoditvah v teh entitetah dodatne poglede ali obrazce, dodajte nova polja tudi vanje.

| Entity        | Obrazci, ki potrebujejo novo polje   |Pogledi, ki potrebujejo novo polje      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena vloge|• Informacije |• Cene kategorij dejavnih virov<br> • Povezani pogled za ceno kategorije vira|
|  Pribitek na ceno vloge|• Informacije|• Dejavni pribitek na ceno vloge<br>• Povezani pogled za pribitek na ceno vloge|
|  Podrobnosti vrstic ponudbe|• Podatki o projektu<br>• Hitro ustvarjanje projekta|• Dejavne podrobnosti vrstice ponudbe<br>• Skupne podrobnosti vrstice ponudbe<br>• Povezani pogled za podrobnosti vrstice ponudbe|
|  Podrobnost vrstice projektne pogodbe|• Podatki o projektu<br>• Hitro ustvarjanje projekta|• Podrobnosti združenih pogodb<br>• Podrobnosti dejavnih pogodb<br>• Povezani pogled za podrobnosti pogodbe|
|  Član projektne ekipe|• Informacije<br>• Novi obrazec|• Dejavni člani projektne ekipe<br>• Člani projektne ekipe<br>• Povezani pogled za člane projektne ekipe|
|  Časovni vnos|• Informacije<br>• Ustvari časovni vnos|• Moji časovni vnosi po datumu<br>• Moji časovni vnosi za ta teden<br>• Časovni vnosi za odobritev|
|  Vrstica dnevnika|• Informacije<br>• Hitro ustvarjanje|• Dejavne vrstice dnevnika<br>• Povezani pogled za vrstice dnevnika|
|  Podrobnosti vrstice računa|• Informacije<br>• Hitro ustvarjanje|• Dejavne podrobnosti vrstice računa<br>• Transakcije računa, ki se zaračunajo<br>• Brezplačne transakcije računa<br>• Povezani pogled za podrobnosti vrstice računa<br>• Transakcije računa, ki se ne zaračunajo|
|  Dejansko|• Informacije<br>• Dejavno opravljeno delo|• Povezani pogled za opravljeno delo|

Polja po meri je morda treba dodati tudi v pravila poslovanja, odvisno od vaših opredelitev. En vnaprej pripravljen primer je za pravilo poslovanja **Možnost urejanja časovnega vnosa na podlagi stanja**. To pravilo določa, katera polja je treba zakleniti, ko je časovni vnos v stanju, ki ga ni mogoče urejati, na primer **Odobreno**. Dodajte polja v to pravilo poslovanja, tako da so polja zaklenjena za urejanje, ko časovni vnos ni v stanju **Osnutek** ali **Vrnjen**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]