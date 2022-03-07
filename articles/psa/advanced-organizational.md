---
title: Organizacijske enote
description: Ta tema vsebuje informacije o organizacijskih enotah v aplikaciji Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: dccb01e5d1c032039cac980061d93b443ef0f9e1296cdd2d8efd7b1bf7338ce0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005096"
---
# <a name="organizational-units"></a>Organizacijske enote 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V aplikaciji Dynamics 365 Project Service Automation je organizacijska enota ločena skupina ali oddelek v podjetju za strokovne storitve, ki zaposluje vire, katerih delo se obračunava po cenah.

Za podjetja za strokovne storitve, ki uporabljajo tehnične vire na različnih področjih ali poslovnih panogah, se lahko cena za zapolnitev vloge na enem področju ali v poslovni panogi razlikuje od cene za zapolnitev vloge na drugem področju ali poslovni panogi. Koncept organizacijskih enot v tem scenariju zagotavlja način za združevanje nabora vlog, za katere se delo obračuna, v delitvi podjetja, ki ima posebno stroškovno strukturo za te vloge.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Ključni atributi in povezave organizacijskih enot

V PSA imajo organizacijske enote ločene valute in posebne cenike z lastnimi cenami.

Valuta organizacijske enote je glavna valuta, ki se uporablja za sledenje stroškom.

Vsaki organizacijski enoti je mogoče priložiti enega ali več cenikov z lastnimi cenami. Za cenike, ki jih je mogoče priložiti organizacijski enoti, v PSA veljajo naslednje omejitve:

- ceniki morajo imeti enako valuto kot organizacijska enota,
- ceniki morajo biti ceniki z lastnimi cenami.

Poleg tega je v entiteti »Vir« atribut za organizacijsko enoto. Vsak vir je lahko dodeljen eni organizacijski enoti.

## <a name="roles-of-organizational-units"></a>Vloge organizacijskih enot

Organizacijska enota ima v PSA dve vlogi:

- **Pogodbena enota** – organizacijska enota, ki predstavlja skupino ali oddelek podjetja, ki je primarno odgovoren za izvedbo prodaje in upravljanje zagotavljanja dela in storitev za stranke. Pogodbena enota je identificirana s poljem **Pogodbena enota** v razdelku glave na straneh **Priložnost**, **Ponudba**, **Projektna pogodba** in **Projekt**.
- **Enota vira** – organizacijska enota, ki ji pripada vir ali ji je dodeljen. Ta organizacijska enota lahko zagotovi svoje vire za nekatere vloge za nekatere vloge v izjavah o delu (SOW) in projektih, ki so v lasti pogodbene enote.

> ![Pogodbene enote in enote vira.](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Pogosta vprašanja o organizacijskih enotah

Spodaj so odgovori na nekatera od najpogostejših vprašanj o organizacijskih enotah.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kako je entiteta »Organizacijska enota« v PSA povezana z entiteto »Organizacija«, ki že obstaja v Dynamics 365?

Entiteta »Organizacija« v Microsoft Dynamics 365 predstavlja ime globalnega primerka Dynamics 365. To ime je običajno ime globalnega podjetja.

Entiteta »Organizacijska enota« predstavlja skupino ali oddelek v globalnem podjetju. Ta skupina ali oddelek ima nabor vlog in seznam cenikov z lastnimi cenami za te vloge, te vloge in cenik pa se razlikujejo od vlog in cenikov drugih skupin ali oddelkov v podjetju.

Ko je aplikacija PSA nameščena, se ustvari privzeta organizacijska enota, ki temelji na organizaciji. Vsi obstoječi viri so dodeljeni privzeti organizacijski enoti. Če so v Dynamics 365 uvozijo novi imenika Active Directory ali viri, jih proces uvoza uporabnikov dodeli privzeti organizacijski enoti v PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kako se entiteta »Organizacijska enota« razlikuje od entitete »Poslovna enota«?

V Dynamics 365 je entiteta »Poslovna enota« varnostni konstrukt. Povezava uporabnika s poslovno enoto določa entitete in zapise entitet, do katerih ima uporabnik dostop. Določa tudi dovoljenja (ustvarjanje, branje, pisanje, brisanje, dodajanje, prilaganje, dodeljevanje ali skupna raba), ki jih ima uporabnik za te zapise entitet.

Entiteta »Organizacijska enota« predstavlja skupino ali oddelek podjetja, ki ima ločene cene za zaposlene, ki so ji dodeljeni. Povezava vira z organizacijsko enoto določa strošek tega vira za dejavnost v okviru projekta.

Ko uvedete Dynamics 365, optimizirajte varnostna pooblastila za hierarhijo poslovnih enot in dodeljevanje uporabnikov poslovnim enotam. V isto poslovno enoto dodelite vse uporabnike, ki morajo običajno dostopati do istega nabora zapisov. Organizacijska enota ne vpliva na varnostna pooblastila ali dostop.

#### <a name="example-of-organizational-units-and-business-units"></a>Primer organizacijskih enot in poslovnih enot

Contoso, Ltd. ima uspešno ekipo za Microsoftove tehnologije. Martin in Nina sta razvijalca za C\#, vendar je Nina v Združenih državah Amerike, medtem ko je Martin v Indiji. Večina projektnih obveznosti zahteva vire iz podružnic Contoso Indija in Contoso ZDA, poleg tega pa Martin in Nina potrebujeta enako varnostno raven za dostop do projektov na tem področju. Vendar pa se cena razvijalcev iz podružnice Contoso Indija precej razlikuje od cene razvijalcev v podružnici Contoso ZDA.

Tukaj je optimalen način za obravnavo tega scenarija z uporabo Dynamics 365 in aplikacije PSA.

1. Oddelek za Microsoftove tehnologije ustvarite kot poslovno enoto in z njo povežite Martina in Nino. Na ta način zagotovite, da imata oba zaposlena enako varnostno raven za dostop do vseh projektov na tem področju delovanja. Oba bosta lahko spremljala napredek in prijavljala čas, stroške in posodobitve o opravilih. 
2. Ustvarite dve organizacijski enoti, s katerima zagotovite, da se stroški za projekt pravilno obračunajo. 
3. Nino povežite v Contoso ZDA, Martina pa v Contoso Indija.
4. Vsaki organizacijski enoti dodelite ustrezne cenike z lastnimi cenami. S tem zagotovite, da stroški, ki so zabeleženi za projekt za Martina in Nino natančno odražajo razliko v cenah med podružnicama Contoso ZDA in Contoso Indija.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Ali so organizacijske enote v Dynamics 365 povezane s prodajnimi območji?

Med območji prodaje in organizacijskimi enotami ni nobene povezave ali odnosa. Območje podaje je običajno geografsko območje, kjer pride do prodaje. Prodajni cenik je mogoče povezati s posameznim območjem prodaje.

Organizacijska enota je notranja skupina ali oddelek v podjetju, ki sledi stroškom za sklop vlog, ki jih proda drugim oddelkom ali zunanjim strankam.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Primer organizacijskih enot in območij prodaje

Contoso, Ltd ima dve razvojni središči: Contoso ZDA in Contoso Indija. Stroški virov v teh razvojnih središčih se precej razlikujejo.

Contoso svoje storitve za IT prodaja na številnih mednarodnih trgih, kot so Latinska Amerika, Severna Amerika, Azija/Pacifik, zahodna Evropa in Bližnji vzhod. Cene za obračunavanje se za enake projektne vloge med temi trgi zelo razlikujejo.

Contoso ZDA in Contoso Indija morata biti nastavljena kot organizacijski enoti, in vsaka organizacijska enota mora imeti svoj cenik z lastnimi cenami. Azija/Pacifik, Latinska Amerika, Severna Amerika, zahodna Evropa in Bližnji vzhod pa morajo biti nastavljeni kot območja prodaje, pri čemer mora vsako območje prodaje imeti svoj cenik z lastnimi cenami.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Zakaj obstaja omejitev glede povezavo cenikov z organizacijskimi enotami? 

Prodajne cene so običajno razlikujejo glede na geografska območja ali trge, kjer se storitve prodajajo. Notranji oddelki podjetja običajno nimajo lastnih prodajnih cen za isto vrsto storitev. Vendar pa imajo notranji oddelki imajo različne cene prodajnega blaga, ki so odvisne od sposobnosti zaposlenih oseb in pogojev dela v regiji, kjer poslujejo. Ker so organizacijske enote oblikovane kot notranji oddelki podjetja, lahko imajo samo cenike z lastnimi cenami.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Zakaj prodajnih cenikov ni mogoče povezati z organizacijskimi enotami?

V PSA je mogoče prodajne cenike povezati s strankami in območji za prodajo. Transakcijske entitete, kot so »Priložnost«, »Ponudba«, »Projektna pogodba« in »Projekt«, uporabljajo prodajne cenike, ki so priloženi računu stranke ali območju za prodajo, da lahko določijo zneske računov in mogoče prihodke dejavnosti v okviru projekta.

Ceniki z lastnimi cenami so povezani z organizacijskimi enotami. Transakcijske entitete, kot so »Priložnost«, »Ponudba«, »Projektna pogodba« in »Projekt«, uporabljajo cenike z lastnimi cenami, ki so priloženi pogodbeni enoti, da lahko določijo cene za dejavnosti v okviru projekta.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Ali so organizacijske enote v PSA hierarhične?

Ne. V trenutni izdaji aplikacije PSA organizacijske enote niso hierarhične. To pomeni, da ni mogoče:

- konfigurirati vzorca za privzemanje lasnih cen, ki bi prehajal po hierarhiji, 
- poročanje o prihodkih ali cenah, združenih z različnih ravni hierarhije organizacijskih enot.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Smo veliko mednarodno podjetje z zapleteno večplastno hierarhijo stroškovnih centrov, oddelkov in obračunskih pisarn. Kako lahko najučinkovitejše uporabimo koncept organizacijskih enot v tej različici aplikacije Project Service?

Če imate kompleksno hierarhijo stroškovnih centrov, oddelkov, obračunskih pisarn itd., nastavite listna vozlišča v tej hierarhiji kot ločene organizacijske enote.
Ta primer prikazuje običajno hierarhijo:

**ContosoIndija**

  - Oddelek za SAP 

    - Tehnični svetovalci 
    - Svetovalci za funkcionalnosti 
    
  - Oddelek za Microsoftove tehnologije 

    - Tehnični svetovalci
    - Svetovalci za funkcionalnosti 
    
**Contoso ZDA**

 - Oddelek za SAP 

    - Tehnični svetovalci 
    - Svetovalci za funkcionalnosti 
    
 - Oddelek za Microsoftove tehnologije 

    - Tehnični svetovalci 
    - Svetovalci za funkcionalnosti 
 
Če je vaša hierarhija podobna, jo morate nastaviti kot nerazvrščeni seznam tako, kot je prikazano tukaj:
- Contoso Indija – Oddelek za SAP – Tehnični svetovalci 
- Contoso Indija – Oddelek za SAP – Svetovalci za funkcionalnosti       
- Contoso Indija – Oddelek za Microsoftove tehnologije – Svetovalci za funkcionalnosti 
- Contoso Indija – Oddelek za Microsoftove tehnologije – Svetovalci za funkcionalnosti 
- Contoso ZDA – Oddelek za SAP – Tehnični svetovalci  
- Contoso ZDA – Oddelek za SAP – Svetovalci za funkcionalnosti  
- Contoso ZDA – Oddelek za Microsoftove tehnologije – Tehnični svetovalci 
- Contoso ZDA – Oddelek za Microsoftove tehnologije – Svetovalci za funkcionalnosti

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Smo majhno podjetje za strokovne storitev, ki posluje kot samo en oddelek. Kako lahko najbolje uporabimo koncept organizacijske enote v trenutni različici aplikacije PSA?

Če podjetje deluje kot ena sama enota z enim cenikom z lastnimi cenami, vam ni treba nastaviti nobenih organizacijskih enot. Med namestitvijo aplikacije PSA Dynamics 365 ustvari eno privzeto organizacijsko enoto, ki ima enako ime kot organizacija. Vsi uporabniki so privzeto dodeljeni v to organizacijsko enoto. Kadar sistem zahteva, da mora biti izbrana organizacijska enota, je privzeto izbrana ta organizacijska enota.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Če je projekt ustvarjen iz vrstice ponudbe ali projektne pogodbe, privzeta pogodbena enota izvira iz ponudbe ali projektne pogodbe. Kaj je privzeta pogodbena enota, če je projekt ustvarjen pred prodajnimi entitetami, kot sta ponudba ali projektna pogodba?

Ko je projekt ustvarjen samostojno, privzeta pogodbena enota projekta odvisna od uporabnika, ki ga ustvari. Ta uporabnik je tudi privzeti vodja projekta. Če je projekt preslikan v prodajno entiteto, kot je ponudba ali projektna pogodba, pa je pogodbena enota projekta odvisna od prodajne entitete. V tem primeru se lahko ocene za projekt znova izračunajo, ker se cenik z lastnimi cenami, uporabljen za izračun ocenjene cene spremeni, če je spremenjena pogodbena enota. Prodajni cenik se uporablja za izračun ocen prodaje, ki bodo spremenjene tako, da bodo usklajene s cenikom projekta v ponudbi.

Polji **Pogodbena enota** in **Valuta** v projektu so zaklenjeni in ju ni mogoče urejati, ker morata biti usklajeni z vrednostmi v prodajni entiteti (ponudbi ali projektni pogodbi), v katero je projekt preslikan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]