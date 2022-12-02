---
title: Projektne pogodbe
description: Ta članek vsebuje primere projektnih pogodb, ki jih lahko ustvarite za različne vrste projektov in vire financiranja, in načine za upravljanje pogodb in izdajanje računov strankam projektov.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14ff17bb070a44d8f3962e08f67d4c95bd8a26f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919666"
---
# <a name="project-contracts"></a>Projektne pogodbe

[!include [banner](../includes/banner.md)]

Ta članek vsebuje primere projektnih pogodb, ki jih lahko ustvarite za različne vrste projektov in vire financiranja, in načine za upravljanje pogodb in izdajanje računov strankam projektov.

Vrsta projekta, ki ga ustvarite za projektno pogodbo, določa metodo za izdajo računov projektnim strankam. Projektno pogodbo in z njo povezan projekt lahko spremenite, vendar ne morete spremeniti vrste projekta. 

Z uporabo projektne pogodbe lahko izdate račun za en ali več projektov hkrati. Projektna pogodba pomaga tudi pri doslednem izdajanju računov za vsak podprojekt v projektni strukturi. 

Vsak projekt, za katerega bo izdan račun, mora biti povezan s projektno pogodbo. Nastavitve za projektno pogodbo veljajo za vse projekte in podprojekte, ki so povezani s to projektno pogodbo. 

Projektna pogodba lahko določa enega ali več virov financiranja. Zato lahko obračun razdelite na več vlagateljev in nastavite omejitve financiranja, tako da viri financiranja ne bodo zaračunani nad določenim zneskom, in nastavite pravila financiranja za zaračunavanje izdatkov.

## <a name="funding-for-project-contracts"></a>Financiranje za projektne pogodbe
Nekatere projektne pogodbe določajo, da je več strank odgovornih za financiranje stroškov projekta. Tukaj je nekaj primerov:

-   Velika stranka z več oddelki zahteva, da se financiranje projekta razdeli po oddelkih.
-   Vaše podjetje si stroške velikega projekta deli z zunanjo organizacijo.
-   Projekt za cesto sofinancirata dve občini.
-   Projekt za most financira javna uprava z nepovratnimi sredstvi in zasebna družba.

V rešitvi Dynamics 365 Finance lahko račun za eno transakcijo ali celoten projekt razdelite na več strank, nepovratnih sredstev ali organizacij. 

V projektih z več vlagatelji se vse strani, ki prispevajo k financiranju projekta z naprednim financiranjem, imenujejo viri financiranja. Ko so stranka, organizacija ali nepovratna sredstva opredeljena kot vir financiranja, se lahko dodelijo enemu ali več pravilom financiranja. Pravila financiranja vsebujejo merila, ki določajo, kako se stroški razdelijo različnim virom financiranja za projekt. 

Ker izdelkov na zalogi, na primer tistih, ki se pojavijo v zahtevah za nakup in naročilnicah, ni mogoče razdeliti, zneska stroškov v času distribucije ni mogoče razdeliti med več virov financiranja. Zato vrednost vira financiranja ostane 0 (nič), dokler se ne vknjiži težava z zalogo. Ko je težava z zalogo vknjižena, se znesek stroškov porazdeli v skladu s pravili o razdelitvi računov za projekt.

Tu je nekaj korakov, s katerimi boste lažje razdelili stroške med več virov financiranja:

-   Navedite, da vse transakcije, ki so vnesene za projekt, uporabljajo isto prodajno valuto kot projektna pogodba.
-   Določite omejitve financiranja, tako da se viru financiranja za projekt ne zaračuna več kot določen znesek.
-   Konfigurirajte pravila financiranja in omejitve financiranja za vsakega delavca, izdelek, kategorijo, skupino kategorij in vrsto transakcije (ali za vse vrste transakcij).
-   Izberite izbirni začetni in končni datum, da določite obdobje veljavnosti posameznega pravila financiranja.
-   Navedite delež, ki pripada posameznemu viru financiranja.
-   Navedite, kateri vir financiranja je odgovoren za zaokroževanje razlik, ki so posledica izračunov pri dodeljevanju sredstev.
-   Nastavite pravila, ki določajo, kako se stroški projekta zaračunavajo zunanjim strankam in internim organizacijam.
-   Transakcije beležite na začasnem računu financiranja, dokler ni mogoče pridobiti dodatnega financiranja ali dokler se ne odločite za interno kritje stroškov.

Če želite določiti, katero davčno skupino bi povezali s transakcijo, poiščite dodelitev davčne skupine v projektu. Če na ravni projekta ni bila ustvarjena nobena davčna skupina, je treba poiskati projektno pogodbo.

### <a name="example-multiple-funding-sources-simple"></a>Primer: več virov financiranja (enostavno)

Spodnja tabela vsebuje scenarije za upravljanje dodeljevanja sredstev med več virov financiranja. Ti scenariji temeljijo na naslednjih predpostavkah:

-   Prednostne nastavitve se upoštevajo pri dodeljevanju sredstev pred drugimi merili, ki določajo pravila financiranja.
-   Za določitev obdobja d, za katerega velja pravilo financiranja, ni določeno nobeno časovno obdobje.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenarij</strong></td>
<td><strong>Vir financiranja</strong></td>
<td><strong>Delež dodelitve</strong></td>
<td><strong>Prednost pri dodeljevanju</strong></td>
</tr>
<tr class="even">
<td>Stroške dodelite enemu viru financiranja, dokler se njegova sredstva ne izčrpajo, nato drugemu viru financiranja, dokler se sredstva ne izčrpajo, preostale stroške pa tretjemu viru financiranja.</td>
<td><ul>
<li>Vir　financiranja　1</li>
<li>Vir　financiranja　2</li>
<li>Vir　financiranja　3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>75 odstotkov stroškov želite dodeliti enemu viru financiranja, 25 odstotkov pa drugemu viru financiranja. Ko je eden od teh virov financiranja izčrpan, plačajte preostale stroške iz tretjega vira financiranja.</td>
<td><ul>
<li>Vir　financiranja　1</li>
<li>Vir　financiranja　2</li>
<li>Vir　financiranja　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>75 odstotkov stroškov želite dodeliti enemu viru financiranja, 25 odstotkov pa drugemu viru financiranja. Ko je eden od teh virov financiranja izčrpan, razdelite preostale stroške med tretji in četrti vir financiranja.</td>
<td><ul>
<li>Vir　financiranja　1</li>
<li>Vir　financiranja　2</li>
<li>Vir　financiranja　3</li>
<li>Vir　financiranja　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Prvih 25 odstotkov stroškov želite dodeliti enemu viru financiranja, preostanek pa drugemu viru financiranja.</td>
<td><ul>
<li>Vir　financiranja　1</li>
<li>Vir　financiranja　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Primer: več virov financiranja (napredno)

Na voljo imate tri vire financiranja, ki jih želite uporabiti v naslednjem vrstnem redu:

1.  Vir financiranja 2 in 3 uporabljajte enako, dokler se vir 2 ne izčrpa.
2.  Še naprej uporabljajte vir financiranja 3, dokler ga ne izčrpate.
3.  Ko izčrpate vir financiranja 3, uporabite vir financiranja 1.

Za dosego tega cilja morate najprej storiti naslednje:

-   Določite omejitve financiranja za vir financiranja 2 in 3 v skladu z njihovima zneskoma.
-   Ustvarite naslednja pravila financiranja:
    -   1. pravilo (prednost 1): 50 odstotkov transakcij dodelite viru financiranja 2, 50 odstotkov pa viru financiranja 3.
    -   2. pravilo (prednost 2): 100 odstotkov transakcij dodelite viru financiranja 3.
    -   3. pravilo (prednost 3): 100 odstotkov transakcij dodelite viru financiranja 1.

Ta nastavitev deluje, ker se transakcije preverjajo glede na pravila in omejitve, da se ugotovi, ali katera od njih velja za transakcijo. Če za transakcijo ne veljajo nobena posebna pravila ali omejitve, velja pravilo za vse transakcije. Pravilo za vse transakcije se ujema z vsemi transakcijami. 

Če najdemo pravilo, ki se ujema s transakcijo, je najprej uporabljen delež, ki je bil dodeljen v tem pravilu, vendar šele potem, ko se preverijo ujemanja glede na nastavljene omejitve. Če je bila omejitev dosežena in so sredstva vira financiranja izčrpana, se pravilo financiranja, povezano z omejitvijo financiranja, ne upošteva in program preveri naslednje veljavno pravilo. 

V nekaterih primerih je mogoče pravilu dodeliti le del transakcije. To se lahko zgodi, ker je pri dodelitvi transakcije dosežena omejitev. V tem primeru se v skladu s tem pravilom dodeli le določen znesek, na primer 50 odstotkov za vsak vir financiranja. To velja za 1. pravilo, ki je opisano v prejšnjih odstavkih tega razdelka. Preostanek se dodeli v skladu z naslednjim pravilom v zaporedju. 

Spodnja tabela vsebuje podroben pregled tega scenarija.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Podrobnosti</strong></td>
</tr>
<tr class="even">
<td>Pravila financiranja</td>
<td><ul>
<li>1. pravilo (prednost 1): Vse transakcije. 50 % dodelite viru financiranja 2, 50 % pa viru financiranja 3.</li>
<li>2. pravilo (prednost 2): Vse transakcije. Viru financiranja 3 dodelite 100 %.</li>
<li>3. pravilo (prednost 2): Vse transakcije. Viru financiranja 1 dodelite 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Omejitve financiranja</td>
<td><ul>
<li>Omejitev vira financiranja 1 = 10.000,00</li>
<li>Omejitev vira financiranja 2 = 500,00</li>
<li>Omejitev vira financiranja 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakcija 1</td>
<td><strong>Znesek transakcije:</strong> 100,00<strong>Financiranje:</strong> Transakcija se plača samo v skladu s 1. pravilom, ker se transakcija plača v celoti po uporabi 1. pravila. Transakcija je financirana z viroma financiranja 2 in 3 v enakovrednih deležih.
<ul>
<li>Vir financiranja 2: 50,00</li>
<li>Vir financiranja 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakcija 2</td>
<td><strong>Znesek transakcije:</strong> 5.000,00<strong>Financiranje:</strong> Transakcija se plača v skladu z vsemi tremi pravili. <strong>1. pravilo</strong>
<ul>
<li>Vir financiranja 2: 450,00</li>
<li>Vir financiranja 3: 450,00</li>
</ul>
<strong>2. pravilo</strong>
<ul>
<li>Vir financiranja 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>3. pravilo</strong>
<ul>
<li>Vir financiranja 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Skupna sredstva, ki se razdelijo za vsak vir financiranja</td>
<td><ul>
<li>Vir financiranja 1: 3.850,00</li>
<li>Vir financiranja 2: 500,00</li>
<li>Vir financiranja 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Pravila za obračunavanje
Ko se s stranko dogovarjate za projektno pogodbo, določite, kako in kdaj lahko stranki zaračunate za delo na projektu. Ko nastavite projektno pogodbo in projekt, lahko nastavite tudi obračunska pravila za projekt. Obračunska pravila temeljijo na projektnih pogojih, ki so določeni v projektni pogodbi. Obračunska pravila, ki jih lahko ustvarite, so odvisna od pogojev projektne pogodbe in vrste projekta, kot sta »Čas in material« ali »Fiksna cena«, ki ju povežete z obračunskim pravilom. Za projektno pogodbo lahko ustvarite več obračunskih pravil. Obračunsko pravilo lahko dodelite tudi več projektom, ki so povezani z isto projektno pogodbo in imajo podobne pogoje za obračunavanje. 

Nastavite lahko naslednje vrste obračunskih pravil:

-   **Dostavna enota** – stranki izdajte račun, ko dokončate dostavno enoto. Dostavne enote določite v pogodbi.
-   **Napredek** – stranki izdajte račun, ko dokončate določen delež projekta. Obračunsko pravilo lahko nastavite tako, da bo samodejno izračunalo delež opravljenega dela, lahko pa ročno izračunate delež opravljenega dela in znesek, ki ga boste zaračunali stranki.
-   **Mejnik** – stranki izdajte račun za celoten znesek projektnega mejnika, ko je ta dosežen.
-   **Provizija** – stranki izdajte račun za vaše storitve plus provizijo za upravljanje, ki je običajno v obliki odstotka stroškov storitev.
-   **Čas in material** – stranki izdajte račun za vrednost časa in materialov, ki se uporabljajo pri projektu.

Za vse vrste obračunskih pravil lahko določite delež zadržanega plačila, ki se odšteje od računov za stranke, dokler projekt ne doseže dogovorjene stopnje. Delež zadržanega plačila je določen v projektni pogodbi. Znesek se izračuna na podlagi in odšteje od skupne vrednosti vrstic na računu za stranko. 

Za obračunska pravila **Čas in material** in **Napredek** lahko dodelite plačljive kategorije. Plačljive kategorije označujejo transakcije, ki naj bi bile vključene v račune za stranke. 

Ko ste pripravljeni stranki izdati račun, se znesek, ki ga boste zaračunali za projekt, izračuna na podlagi obračunskih pravil, in ustvari predlog za račun projekta. 

Naslednji razdelki vsebujejo primere, ki prikazujejo, kako nastaviti in upravljati obračunska pravila za projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Primer: ustvarite obračunsko pravilo na podlagi števila izvedenih enot

Vaša organizacija sklene pogodbo, po kateri bo strankinim zaposlenim zagotovila pet usposabljanj po ceni 10.000 na usposabljanje. Stranki izdate račun po vsakem usposabljanju. 

Pri nastavljanju obračunskih pravil za pogodbo uporabite naslednje vrednosti:

-   Dostavna enota označuje eno usposabljanje.
-   Cena enote je 10.000 na usposabljanje.
-   Skupno število enot je pet usposabljanj.

Ko zaključite eno usposabljanje, ustvarite račun za 10.000 za prvo enoto, ki je bila izvedena, in pošljite račun stranki.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Primer: ustvarite obračunsko pravilo na podlagi določenega deleža dokončanosti projekta (ročni izračun)

Vaša organizacija, svetovalno podjetje za programsko opremo, s stranko sklene dogovor o razvoju dela izdelka, ki ga stranka razvija. Vaša organizacija se strinja, da bo programsko kodo dostavila v šestih mesecih. Stranka se strinja, da bo vaši organizaciji za delo plačala skupno 100.000. Obračunsko pravilo ustvarite tako, da stranki izdate račun na podlagi deleža dokončanega dela na projektu, kot je navedeno v pogodbi.

-   Konec prvega meseca se sestanite s stranko, da določite delež dokončanega dela. Ko s stranko pregledate projekt, ugotovite, da je projekt dokončan do 15 odstotkov.
-   Ustvarite račun za 15.000 (15 odstotkov od 100.000) in ga pošljite stranki.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Primer: ustvarite obračunsko pravilo na podlagi določenega deleža dokončanosti projekta (samodejni izračun)

Vaša organizacija, podjetje za razvoj programske opreme, se strinja, da bo za stranko razvila paket za obračun plač za 30.000. Stranka se strinja, da bo vaši organizaciji za delo plačala za delež dokončanega dela. Po vaši oceni znašajo stroški projekta 20.000. Projektna pogodba določa kategorije del, ki jih uporabljate v postopku zaračunavanja. Nastavite obračunska pravila, ki samodejno izračunajo zneske računov za delež opravljenega dela za posamezno kategorijo. Za vsako kategorijo nastavite proračun:

-   **Razvoj** – stroški v višini 15.000 in prihodki v višini 20.000
-   **Namestitev** – stroški v višini 5.000 in prihodki v višini 10.000

Ko prvič ustvarite račun za stranko, se znesek računa samodejno izračuna na podlagi naslednjih informacij:

-   Po enem mesecu delavec na projektu predloži časovni list za projekt. Strošek delovnega časa delavca je 5.000 za razvoj in 1.000 za namestitev. Razvojna dela so končana v 33 odstotkih (5.000 dejanskih stroškov/15.000 proračunskih stroškov), namestitvena dela pa v 20 odstotkih (1.000 dejanskih stroškov/5.000 proračunskih stroškov).
-   Znesek računa v višini 8.667 se samodejno izračuna (33 odstotkov od 20.000 + 20 odstotkov od 10.000).
-   Ustvarite račun za 8.667 in ga pošljite stranki.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Primer: Ustvarite obračunsko pravilo na podlagi dogovorjenih mejnikov

Vaša organizacija, svetovalno podjetje za upravljanje, se zavezuje izvesti tržno raziskavo za potrošniški izdelek, ki ga stranka namerava prodati. Stranka se strinja, da bo vaše storitve uporabljala tri mesece z začetkom marca in da plača vaši organizaciji 50.000. Projekt ima tri mejnike:

-   1. mejnik: zbiranje podatkov o potrošnikih – 31. marec
-   2. mejnik: analiza podatkov o potrošnikih – 30. april
-   3. mejnik: predstavitev predloga za preživetje izdelka – 31. maj

Stranka se strinja, da bo vaši organizaciji plačala 10.000 za prvi mejnik, 20.000 za drugi mejnik in 20.000 za tretji mejnik. 

Ko določite projektno pogodbo, se strinjate, da boste stranki izdali račun na podlagi opravljenega mejnika. Nastavitev obračunskega pravila vključuje naslednje korake:

-   Določitev mejnikov projekta.
-   Določitev zneska, ki bo stranki zaračunan ob izpolnitvi posameznega mejnika.

Ko dosežete prvi mejnik 31. marca, ga označite kot izpolnjenega, nato pa ustvarite račun za 10.000 in ga pošljite stranki. Računa za mejnik ne morete ustvariti, dokler mejnika ne označite kot zaključenega.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Primer: Ustvarite pravilo za obračunavanje na podlagi storitev in provizije za upravljanje

Vaša organizacija, svetovalno podjetje za upravljanje, se zavezuje, da bo izvedla tržne raziskave, da bi ocenila sposobnost preživetja izdelka, ki ga razvija stranka – maloprodajno podjetje. Pogoji sporazuma določajo, da boste zagotovili storitve svojih treh vodilnih svetovalcev, ki bodo raziskave izvajali v časovnem in materialnem sorazmerju. Stranka se strinja, da bo plačala 100 na uro plus 10-odstotno provizijo za upravljanje za svetovalne ure, ki se zaračunajo projektu. 

Ko določate projektno pogodbo, ustvarite obračunsko pravilo, s katerim se svetovalnim uram, ki se zaračunajo projektu, doda 10-odstotno provizijo za upravljanje. 

Ko ustvarite račun za stranko, ji zaračunajte 10-odstotno provizijo za upravljanje plus stroške svetovalnih ur. Primer: če so omenjeni trije svetovalci na projektu delali skupno 200 ur, je treba na podlagi spodnjega izračuna ustvariti račun za 22.000:

-   200 ur po 100 na uro = 20.000
-   10-odstotna provizija za upravljanje = 2.000
-   Skupni znesek računa = 22.000

Če so provizije za stranko obdavčene in v projektni pogodbi izberete skupino prometnega davka, se skupina prometnega davka samodejno vnese v obračunsko pravilo za provizije.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Primer: Ustvarite obračunsko pravilo za vrednost časa in materialov

Vaša organizacija, svetovalno podjetje za programsko opremo, se zavezuje, da bo v naslednjih šestih mesecih zagotovila pet tehničnih svetovalcev, ki bodo delali na projektu za razvoj programske opreme za stranko. Stranka se strinja, da bo plačala 150 za vsako svetovalno uro plus stroške pisarniškega materiala. Vaša organizacija stranki konec vsakega meseca pošlje račun. 

Ob zasnovi projektne pogodbe se zavežete, da boste kupcu vsak mesec zaračunali trajanje in pisarniški material za projekt. Ustvarite obračunsko pravilo, ki vključuje naslednje informacije:

-   Pogodbeno obdobje traja šest mesecev.
-   Svetovalni čas se izračuna po postavki 150 na uro.
-   Pisarniški material se zaračuna po nabavni vrednosti, skupni stroški projekta pa ne smejo presegati 10.000.
-   Med trajanjem projekta morate ustvariti račun za stranko na koncu vsakega koledarskega meseca.

V prvem mesecu so svetovalci na projektu zabeležili skupno 800 ur. Strošek pisarniškega materiala, ki je zaračunan projektu, znaša 2.000. Konec meseca torej ustvarite račun za 122.000, tj. 800 delovnih ur po 150 na uro plus 2.000 za pisarniški material.





[!INCLUDE[footer-include](../includes/footer-banner.md)]