---
title: Organizacijske enote
description: Ta tema opisuje koncept organizacijskih enot in pojasnjuje, kako ustvariti in vzdrževati organizacijske enote v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581396"
---
# <a name="organizational-units-overview"></a>Pregled organizacijskih enot

V Microsoftu Dynamics 365 Project Operations, an *organizacijska enota* je posebna skupina ali oddelek v podjetju za strokovne storitve, ki zaposluje plačljiva sredstva, ki imajo stroškovne stopnje.

Za podjetja za strokovne storitve, ki zaposlujejo tehnične vire na različnih praktičnih področjih ali poslovnih področjih, se lahko stroški za zapolnitev vloge razlikujejo, odvisno od področja prakse ali poslovnega področja, kjer je vloga zasedena. V tem scenariju koncept organizacijskih enot pomaga z zagotavljanjem načina za združevanje nabora plačljivih vlog v oddelku podjetja, ki ima za te vloge posebno strukturo stroškov.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Koncept organizacijskih enot v projektnem poslovanju

Pri projektnem poslovanju ima organizacijska enota določeno valuto in posebne cenike.

Valuta organizacijske enote je glavna valuta, ki se uporablja za sledenje stroškom.

Vsaki organizacijski enoti je mogoče priložiti enega ali več cenikov z lastnimi cenami. Projektno poslovanje postavlja naslednje omejitve na cenike, ki jih je mogoče priložiti organizacijski enoti:

- Ceniki morajo biti v valuti organizacijske enote.
- Ceniki morajo biti ceniki.

Poleg tega entiteta Vir vključuje atribut za organizacijsko enoto. Vsak vir je lahko dodeljen eni organizacijski enoti.

### <a name="roles-of-organizational-units"></a>Vloge organizacijskih enot

Organizacijska enota ima pri projektnem delovanju dve vlogi:

- **Pogodbena enota** – organizacijska enota, ki predstavlja skupino ali oddelek podjetja, ki je primarno odgovoren za izvedbo prodaje in upravljanje zagotavljanja dela in storitev za stranke. Pogodbena enota je identificirana s poljem **Pogodbena enota** v razdelku glave na straneh **Priložnost**, **Ponudba**, **Projektna pogodba** in **Projekt**.
- **Enota vira** – organizacijska enota, ki ji pripada vir ali ji je dodeljen. Ta organizacijska enota lahko zagotovi svoje vire za nekatere vloge za nekatere vloge v izjavah o delu (SOW) in projektih, ki so v lasti pogodbene enote.

![Pogodbene enote in enote vira.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organizacijska enota Pogosta vprašanja

Spodaj so odgovori na nekatera od najpogostejših vprašanj o organizacijskih enotah.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kako je entiteta organizacijske enote v projektnih operacijah povezana s entiteto organizacije, ki že obstaja v Dynamics 365?

Entiteta organizacije v Dynamics 365 predstavlja ime globalnega primerka Dynamics 365. To ime je običajno ime globalnega podjetja.

Entiteta »Organizacijska enota« predstavlja skupino ali oddelek v globalnem podjetju. Ta skupina ali oddelek ima nabor vlog in seznam cenikov z lastnimi cenami za te vloge, te vloge in cenik pa se razlikujejo od vlog in cenikov drugih skupin ali oddelkov v podjetju.

Ko je Project Operations nameščen, se na podlagi organizacije ustvari privzeta organizacijska enota. Vsi obstoječi viri so dodeljeni privzeti organizacijski enoti. Če se v Dynamics 365 uvozijo novi uporabniki ali viri Active Directory, jih postopek uvoza uporabnikov dodeli privzeti organizacijski enoti v Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kako se subjekt organizacijske enote razlikuje od subjekta poslovne enote?

V Dynamics 365 je entiteta »Poslovna enota« varnostni konstrukt. Povezava uporabnika s poslovno enoto določa entitete in zapise entitet, do katerih ima uporabnik dostop. Določa tudi dovoljenja (ustvarjanje, branje, pisanje, brisanje, dodajanje, prilaganje, dodeljevanje ali skupna raba), ki jih ima uporabnik za te zapise entitet.

Entiteta »Organizacijska enota« predstavlja skupino ali oddelek podjetja, ki ima ločene cene za zaposlene, ki so ji dodeljeni. Povezava vira z organizacijsko enoto določa strošek tega vira za dejavnost v okviru projekta.

Ko uvedete Dynamics 365, optimizirajte varnostna pooblastila za hierarhijo poslovnih enot in dodeljevanje uporabnikov poslovnim enotam. V isto poslovno enoto dodelite vse uporabnike, ki morajo običajno dostopati do istega nabora zapisov. Organizacijska enota ne vpliva na varnostna pooblastila ali dostop.

**Primer, ki prikazuje eno potencialno razliko pri modeliranju organizacijskih enot in poslovnih enot**

Contoso, Ltd. ima uspešno ekipo za Microsoftove tehnologije. Martin in Nina sta razvijalca za C\#, vendar je Nina v Združenih državah Amerike, medtem ko je Martin v Indiji. Večina projektnih poslov zahteva sredstva iz Contoso Indije in Contoso ZDA, Prakash in Tricia pa zahtevata enako raven varnostnega dostopa do projektov na tem področju prakse. Vendar pa se cena razvijalcev iz podružnice Contoso Indija precej razlikuje od cene razvijalcev v podružnici Contoso ZDA.

Tukaj je optimalen način oblikovanja za ta scenarij z uporabo Dynamics 365 in Project Operations.

1. Oddelek za Microsoftove tehnologije ustvarite kot poslovno enoto in z njo povežite Martina in Nino. Na ta način pomagate zagotoviti, da imata oba zaposlena enako raven varnostnega dostopa do vseh projektov na tem področju prakse. Oba bosta lahko preverjala napredek in poročala o času, stroških, porabi materiala in posodobitvah opravil.
2. Ustvarite dve organizacijski enoti, da zagotovite, da se stroški projekta pravilno odražajo.
3. Poveži Tricia z Contoso ZDA in Prakash z Contoso Indija.
4. Vsaki organizacijski enoti dodelite ustrezne cenike z lastnimi cenami. Na ta način pomagate zagotoviti, da stroški, ki so zabeleženi v projektu za Prakash in Tricia, natančno odražajo razliko v stroških med Contoso ZDA in Contoso Indija.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Ali so organizacijske enote v Dynamics 365 povezane s prodajnimi območji?

Med območji prodaje in organizacijskimi enotami ni nobene povezave ali odnosa. Območje podaje je običajno geografsko območje, kjer pride do prodaje. Prodajni cenik je mogoče povezati s posameznim območjem prodaje.

Organizacijska enota je notranja skupina ali oddelek v podjetju, ki sledi stroškom za sklop vlog, ki jih proda drugim oddelkom ali zunanjim strankam.

**Primer, ki prikazuje eno potencialno razliko pri modeliranju organizacijskih enot in prodajnih območij**

Contoso, Ltd ima dve razvojni središči: Contoso ZDA in Contoso Indija. Stroški virov se med tema dvema razvojnima središčema zelo razlikujejo. Contoso svoje storitve informacijske tehnologije (IT) prodaja na številnih mednarodnih trgih, kot so Latinska Amerika, Severna Amerika, Azija-Pacifik, Zahodna Evropa in Bližnji vzhod. Cene za obračunavanje se za enake projektne vloge med temi trgi zelo razlikujejo. Contoso ZDA in Contoso Indija morata biti nastavljena kot organizacijski enoti, in vsaka organizacijska enota mora imeti svoj cenik z lastnimi cenami. Azija/Pacifik, Latinska Amerika, Severna Amerika, zahodna Evropa in Bližnji vzhod pa morajo biti nastavljeni kot območja prodaje, pri čemer mora vsako območje prodaje imeti svoj cenik z lastnimi cenami.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Zakaj obstaja omejitev glede povezavo cenikov z organizacijskimi enotami?

Prodajne cene so običajno razlikujejo glede na geografska območja ali trge, kjer se storitve prodajajo. Notranji oddelki podjetja običajno nimajo lastnih prodajnih cen za isto vrsto storitev. Vendar pa imajo notranji oddelki imajo različne cene prodajnega blaga, ki so odvisne od sposobnosti zaposlenih oseb in pogojev dela v regiji, kjer poslujejo. Ker so organizacijske enote oblikovane kot notranji oddelki podjetja, lahko imajo samo cenike z lastnimi cenami.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Zakaj prodajnih cenikov ne moremo povezati z organizacijskimi enotami?

V Project Operations se lahko prodajni ceniki povežejo s strankami in prodajnimi območji. Transakcijski subjekti, kot so Priložnost, Ponudba, Projektna pogodba in Projekt, uporabljajo prodajne cenike, ki so priloženi računu stranke ali prodajnemu območju, da določijo stopnje računov in potencialni prihodek za projektno dejavnost.

Ceniki z lastnimi cenami so povezani z organizacijskimi enotami. Transakcijski subjekti, kot so Priložnost, Ponudba, Projektna pogodba in Projekt, uporabljajo cenike stroškov, ki so priloženi pogodbeni enoti, da določijo stroške projektnega posla.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Ali so organizacijske enote hierarhičen v projektnem poslovanju?

Ne. V trenutni izdaji Project Operations organizacijske enote niso hierarhičen. Zato ne morete izvajati naslednjih nalog:

- Konfigurirajte vzorec za vnos privzetih stroškovnih cen, ki prečka hierarhijo navzgor.
- Poročaj o prihodkih ali stroških, ki so združeni na različnih ravneh hierarhije organizacijskih enot.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Smo veliko multinacionalno podjetje, ki ima zapleteno hierarhijo na več ravneh stroškovnih mest, oddelkov in računov. Kako lahko najbolje uporabimo koncept organizacijskih enot v trenutni različici Project Operations?

Ko imate zapleteno hierarhijo stroškovnih mest, oddelkov, računov itd., nastavite listna vozlišča te hierarhije kot ločene organizacijske enote.

Naslednji primer prikazuje tipično hierarhijo.

**Contoso Indija**

- Oddelek za SAP

    - Tehnični svetovalci
    - Svetovalci za funkcionalnosti

- Oddelek za Microsoftove tehnologije

    - Tehnični svetovalci
    - Svetovalci za funkcionalnosti

**Contoso, ZDA**

- Oddelek za SAP

    - Tehnični svetovalci
    - Svetovalci za funkcionalnosti

- Oddelek za Microsoftove tehnologije

    - Tehnični svetovalci
    - Svetovalci za funkcionalnosti

Če je vaša hierarhija podobna tem primeru, jo morate nastaviti kot ploski seznam, kot je prikazano tukaj:

- Contoso Indija – Oddelek za SAP – Tehnični svetovalci
- Contoso Indija – Oddelek za SAP – Svetovalci za funkcionalnosti
- Contoso Indija – Oddelek za Microsoftove tehnologije – Svetovalci za funkcionalnosti
- Contoso Indija – Oddelek za Microsoftove tehnologije – Svetovalci za funkcionalnosti
- Contoso ZDA – Oddelek za SAP – Tehnični svetovalci
- Contoso ZDA – Oddelek za SAP – Svetovalci za funkcionalnosti
- Contoso ZDA – Oddelek za Microsoftove tehnologije – Tehnični svetovalci
- Contoso ZDA – Oddelek za Microsoftove tehnologije – Svetovalci za funkcionalnosti

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Smo majhno podjetje za strokovne storitev, ki posluje kot samo en oddelek. Kako lahko najbolje uporabimo koncept organizacijskih enot v trenutni različici Project Operations?

Če podjetje deluje kot ena sama enota z enim cenikom z lastnimi cenami, vam ni treba nastaviti nobenih organizacijskih enot. Namestitev Project Operations ustvari eno privzeto organizacijsko enoto, ki ima isto ime kot organizacija. Vsi uporabniki so privzeto dodeljeni v to organizacijsko enoto. Kadar sistem zahteva, da mora biti izbrana organizacijska enota, je privzeto izbrana ta organizacijska enota.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Če je projekt ustvarjen iz vrstice ponudbe ali projektne pogodbe, privzeta pogodbena enota izvira iz ponudbe ali projektne pogodbe. Kakšna je privzeta pogodbena enota, če je projekt ustvarjen pred prodajnimi subjekti, kot sta ponudba ali projektna pogodba?

Ko je projekt ustvarjen samostojno, privzeta pogodbena enota projekta odvisna od uporabnika, ki ga ustvari. Ta uporabnik je tudi privzeti vodja projekta. Če je projekt preslikan na prodajni subjekt, kot je ponudba ali projektna pogodba, namesto tega pogodbena enota projekta temelji na prodajnem subjektu. V tem primeru se lahko ocene za projekt znova izračunajo, ker se cenik z lastnimi cenami, uporabljen za izračun ocenjene cene spremeni, če je spremenjena pogodbena enota. Prodajni cenik se uporablja za izračun prodajnih ocen, ki bodo spremenjene tako, da so usklajene s projektnim cenikom ponudbe.

The **Pogodbena enota** in **valuta** polja projekta so zaklenjena za urejanje, ker morajo biti sinhronizirana z vrednostmi prodajnega subjekta (predračun ali projektna pogodba), v katerega je projekt preslikan.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Ustvarite in vzdržujte organizacijske enote v projektnem poslovanju

Če želite ustvariti organizacijsko enoto v Project Operations, sledite tem korakom.

1. Pojdi do **Nastavitve \> Organizacijske enote**.
2. Izberite **Novo**.
3. V **General** območju, v **ime** v polje vnesite ime organizacijske enote. Nato po potrebi nastavite ostala polja.
4. Izberite **Shrani** ustvarite zapis, tako da ga lahko nadaljujete z urejanjem.
5. Spodaj **Cenik stroškov**, izberite znak plus (**+**), da dodate cenik. Dodate lahko samo cenike, ki imajo **Stroški** kontekst tukaj.
6. V **ime** polje, izberite **Iskanje** in izberite cenik, ki ga želite dati na voljo organizacijski enoti. Po potrebi še naprej dodajajte cenike.
7. Ko končate z dodajanjem cenikov, izberite **Shrani** v spodnjem desnem kotu strani.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
