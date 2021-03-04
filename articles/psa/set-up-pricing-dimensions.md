---
title: Nastavitev polj po meri kot cenovnih razsežnosti
description: Ta tema vsebuje informacije o nastavitvi cenovnih razsežnosti po meri.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150373"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Nastavitev polj po meri kot cenovnih razsežnosti 

[!include [banner](../includes/psa-now-project-operations.md)]

Predpostavljamo, da ste pred začetkom tega postopka izvedli postopke v temah [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md) in [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md). Če teh postopkov še niste izvedli, se vrnite nazaj in jih dokončajte, preden se vrnete na to temo. 

Ta tema vsebuje informacije o nastavitvi cenovnih razsežnosti po meri. V spletnem vmesniku storitve Project Service so v zavihku **Cenovne razsežnosti na podlagi zneska** na strani **Parametri** prikazani zapisi v entitetah cenovnih razsežnosti. Ob namestitvi storitev Project Service privzeto ustvari 2 vrstici v mreži v tem zavihku:

- **msdyn_resourcecategory** (vloga)
- **msdyn_OrganizationalUnit** (organizacijska enota)

> [!IMPORTANT]
> Ne izbrišite teh vrstic. Če jih ne potrebujete, lahko določite, da jih ni mogoče uporabiti v določenem kontekstu, in sicer tako da možnosti **Mogoče uporabiti za ceno**, **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za nakup** nastavite na **Ne**. Nastavitev vrednosti teh atributov na **Ne** bo imela enak učinek, kot če polje s cenovno razsežnostjo ne bi obstajalo.

Če želite ustvariti polje s cenovno razsežnostjo, ga morate:

- ustvariti kot polje v entitetah **Cena vloge** in **Pribitek na ceno vloge**. Za več informacij o tem, kako to storite, glejte temo [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md).
- ustvariti kot vrstico v tabeli **Cenovna razsežnost**. Vrstice cenovnih razsežnosti lahko na primer dodate tako, kot je prikazano na spodnji grafiki. 

![Vrstice s cenovnimi razsežnostmi na podlagi zneska](media/Amt-based-PD.png)

V mrežo na zavihku **Cenovna razsežnost na podlagi pribitka** je bil dodan delovni čas vira (**msdyn_resourceworkhours**) kot ena od razsežnosti na podlagi pribitka.

![Vrstice s cenovnimi razsežnostmi na podlagi pribitka](media/Markup-based-PD.png)

> [!IMPORTANT]
> Vse spremembe obstoječih ali novih podatkov o cenovnih razsežnostih v tej tabeli se razširijo na poslovno logiko za oblikovanje cen v storitvi Project Service, vendar šele po osvežitvi predpomnilnika. Osveževanje predpomnilnika lahko traja do 10 minut. V tem času bodo uvedene spremembe v logiko za privzeto oblikovanje cen, ki morajo izhajati iz sprememb podatkov o cenovnih razsežnostih.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributi tabele za cenovne razsežnosti
Spodnji razdelki vsebujejo informacije o različnih atributih v tabeli za **Cenovne razsežnosti**.

### <a name="pricing-dimension-name"></a>Ime cenovne razsežnosti
Ta vrednost mora biti enaka imenu sheme polja, ki je dodano v tabelo **Cena vloge** za cenovne razsežnosti po meri. Za več informacij o dodajanju polj v tabelo **Cena vloge** glejte temo [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md).

### <a name="type-of-dimension"></a>Vrsta razsežnosti
Obstajata dve vrsti cenovnih razsežnosti:
  
  - **Razsežnost na podlagi zneska**: vrednosti razsežnosti iz konteksta vnosa so primerjane z vrednostmi razsežnosti v vrstici **Cena vloge**, vrednost cene/stroška pa se pridobi neposredno iz tabele **Cena vloge**.
  - **Razsežnosti na podlagi pribitka**: to so razsežnosti, za katere storitev Project Service izvede spodaj opisani 3-stopenjski postopek za pridobitev cene/stroška
 
    1. Storitev Project Service primerja vrednosti razsežnosti iz konteksta vnosa, ki ne temeljijo na pribitku, z vrstico »Cena vloge«, da pridobi osnovno postavko.
    2. Storitev Project Service primerja vse vrednosti razsežnosti iz konteksta vnosa z vrstico **Pribitek na ceno vloge**, da pridobi stopnjo pribitka.
    3. Storitev Project Service upošteva stopnjo pribitka iz drugega koraka pri osnovni postavki, ki jo je pridobila iz tabele **Cena vloge** v prvem koraku, in tako izračuna končno ceno/strošek.
   
   V spodnji tabeli je ponazorjen izračun cenovnih pribitkov.
  
| Vloga        | Organizacijska enota    |Lokacija dela      |Standardni naziv      |Delovni čas vira      |  Pribitek|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Indija|Na lokaciji            |                    |Nadure                 |15     |
|             | Contoso Indija|Lokalno             |                    |Nadure                 |10     |
|             | Contoso, ZDA   |Lokalno             |                    |Nadure                 |20     |


Če vir iz Contoso Indija, katerega osnovna postavka je 100 USD, deluje na licu mesta in v časovni vnos zabeleži 8 ur rednega dela in 2 uri nadur, bo cenovni mehanizem storitve Project Service uporabil osnovno postavko v višini 100 za 8 ur in zabeležil 800 USD. Za 2 uri nadur se bo upošteval pribitek v višini 15 % na osnovno postavko 100, s čimer se bo cenovna enota zvišala na 115 USD, skupni strošek pa bo znašal 230 USD.

### <a name="applicable-to-cost"></a>Mogoče uporabiti za ceno 
Če je ta možnost nastavljena na **Da**, to pomeni, da je treba uporabiti vrednost razsežnosti iz konteksta vnosa za uskladitev z vrednostma **Cena vloge** in **Pribitek na ceno vloge** pri pridobivanju postavke za ceno in stopnje pribitka.

### <a name="applicable-to-sales"></a>Mogoče uporabiti za prodajo
Če je ta možnost nastavljena na **Da**, to pomeni, da je treba uporabiti vrednost razsežnosti iz konteksta vnosa za uskladitev z vrednostma **Cena vloge** in **Pribitek na ceno vloge** pri pridobivanju obračunske stopnje in stopnje pribitka.

### <a name="applicable-to-purchase"></a>Mogoče uporabiti za nakup
Če je ta možnost nastavljena na **Da**, to pomeni, da je treba uporabiti vrednost razsežnosti iz konteksta vnosa za uskladitev z vrednostma **Cena vloge** in **Pribitek na ceno vloge** pri pridobivanju prodajne cene. Project Service trenutno ne podpira scenarijev, ki vključujejo podizvajalce, zato to polje ni uporabljeno. 

### <a name="priority"></a>Prioriteta
Določanje prioritete razsežnosti pomaga pri določanju cene v storitvi Project Service, tudi kadar ta ne najde točnega ujemanja med vhodnimi vrednostmi razsežnosti in vrednostmi iz tabel **Cena vloge** ali **Pribitek na ceno vloge**. V tem primeru bo storitev Project Service uporabila ničelne vrednosti za vrednosti razsežnosti brez ujemanja in bo razsežnosti razporedila glede na njihovo prioriteto.

- **Cenovna prioriteta**: vrednost cenovne prioritete razsežnosti, ki določa težo razsežnosti pri ugotavljanju ujemanja z nastavljenimi lastnimi cenami. Vrednost **Cenovna prioriteta** mora biti enaka za vse razsežnosti, za katere velja, da jih je **Mogoče uporabiti za ceno**.
- **Prodajna prioriteta**: vrednost prodajne prioritete razsežnosti, ki določa težo razsežnosti pri ugotavljanju ujemanja z nastavljenimi prodajnimi cenami ali obračunskimi stopnjami. Vrednost **Prodajna prioriteta** mora biti enaka za vse razsežnosti, za katere velja, da jih je **Mogoče uporabiti za prodajo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]