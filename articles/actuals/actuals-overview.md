---
title: Dejanske vrednosti
description: Ta tema vsebuje informacije o delu z dejanskimi vrednostmi v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a086fe0be67c21ed73793b6f3b58b47ad08eaa4e8a4c98870b4b2264562e3dce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991821"
---
# <a name="actuals"></a>Dejanske vrednosti 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dejanske vrednosti predstavljajo pregledane in odobrene finančne in časovne napredke projekta. Ustvarijo se kot rezultat odobritve časa, stroškov, vnosov porabe materiala ter vknjižb in računov.

## <a name="journal-lines-and-time-submission"></a>Vrstice dnevnikov in vnos časa

Za več informacij o vnosu časa glejte [Pregled vnosa časa](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Čas in materiali

Ko je predloženi vnos časa, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, sta v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.

### <a name="fixed-price"></a>Fiksna cena

Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.

### <a name="default-pricing"></a>Privzete cene

Logika za oblikovanje privzetih cen se nahaja v vrstici dnevnika. Vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika. Te vrednosti vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.

Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Enota vira**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika. Časovnemu vnosu lahko dodate polje po meri. Če želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v tabelah **Dejanske vrednosti** in **Vrstica dnevnika**. Uporabite kodo po meri, da z izvori transakcij prek vrstice dnevnika razširite izbrane vrednosti polja iz časovnega vnosa v dejanske podatke. Za več informacij o izvoru in povezavah transakcij in glejte stran [Povezava dejanskih podatkov z izvirnimi zapisi](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Oddaja vrstic dnevnika in osnovnih stroškov

Za več informacij o vnosu stroškov glejte [Pregled stroškov](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Čas in materiali

Ko je vnos osnovnega stiška, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, se v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.

### <a name="fixed-price"></a>Fiksna cena

Ko je poslan vnos osnovnega stroška povezan s projektom, ki je preslikan v podrobnosti pogodbe za fiksno ceno, sistem ustvari eno vrstico dnevnika za ceno.

### <a name="default-pricing"></a>Privzete cene

Logika vnosa privzetih cen za stroške temelji na kategoriji stroškov. Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika. Polja, ki vplivajo na privzete cene, kot sta **Kategorija transakcija** in **Enota vira**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika. Vendar to deluje le, če je v ceniku navedena metoda določanja cen **cena na enoto**. Če je metoda določanja cen **nabavna cena** ali **pribitek na ceno**, se za stroške uporabi cena, vnesena ob ustvarjanju vnosa stroškov, cena v vrstici dnevnika prodaje pa se izračuna na podlagi metode določanja cen. 

Vnosu stroškov lahko dodate polje po meri. Če želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v tabelah **Dejanske vrednosti** in **Vrstica dnevnika**. Uporabite kodo po meri, da z izvori transakcij prek vrstice dnevnika razširite izbrane vrednosti polja iz časovnega vnosa v dejanske podatke. Za več informacij o izvoru in povezavah transakcij in glejte stran [Povezava dejanskih podatkov z izvirnimi zapisi](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Vrstice dnevnika in oddaja dnevnika uporabe materiala

Za več informacij o vnosu stroškov glejte stran [Dnevnik uporabe materiala](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Čas in materiali

Ko je poslan vnos v dnevnik uporabe materiala povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in materiale, sistem ustvari dve vrstici dnevnika, eno za stroške in drugo za neobračunano prodajo.

### <a name="fixed-price"></a>Fiksna cena

Ko je poslan vnos v dnevnik uporabe materiala povezan s projektom, ki je preslikan v podrobnosti pogodbe za fiksno ceno, sistem ustvari eno vrstico dnevnika za ceno.

### <a name="default-pricing"></a>Privzete cene

Logika za vnos privzetih cen materiala temelji na kombinaciji izdelka in enote. Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika. Polja, ki vplivajo na privzete cene, kot sta **ID izdelka** in **Enota vira**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika. Vendar to deluje samo za izdelke iz kataloga. Za izdelke, ki niso v katalogu, se za stroške in prodajno ceno v vrsticah dnevnika uporablja cena, vnesena ob ustvarjanju vnosa v dnevnik uporabe materiala. 

Vnosu v **dnevnik uporabe materiala** lahko dodate polje po meri. Če želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v tabelah **Dejanske vrednosti** in **Vrstica dnevnika**. Uporabite kodo po meri, da z izvori transakcij prek vrstice dnevnika razširite izbrane vrednosti polja iz časovnega vnosa v dejanske podatke. Za več informacij o izvoru in povezavah transakcij in glejte stran [Povezava dejanskih podatkov z izvirnimi zapisi](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Uporaba dnevnikov vnosov za zapisovanje stroškov

V dnevnike lahko beležite stroške ali prihodke v razredih transakcij za material, dajatve, čas, stroške ali davke. Dnevniki se lahko uporabljajo v naslednje namene:

- Dejanske podatke o transakciji prenesite iz drugega sistema v aplikacijo Microsoft Dynamics 365 Project Operations.
- Beleženje stroškov, ki so nastali v drugem sistemu. Ti stroški lahko vključujejo stroške naročanja ali podizvajanja.

> [!IMPORTANT]
> Aplikacija ne preveri veljavnosti vrste vrstice dnevnika ali povezanih cen, ki so vnesene v vrstico dnevnika. Zato mora dnevnike vnosov za ustvarjanje dejanskih vrednosti uporabljati oseba, ki se popolnoma zaveda računovodskega vpliva dejanskih vrednosti na projekt. Zaradi vpliva te vrste dnevnika morate skrbno izbrati, kdo ima dostop do ustvarjanja dnevnikov vnosov.

## <a name="record-actuals-based-on-project-events"></a>Zapisovanje dejanskih vrednosti na podlagi projektnih dogodkov

Aplikacija Project Operations beleži finančne transakcije, do katerih pride med projektom. Te transakcije se zapišejo kot dejanske vrednosti. V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Vir pripada isti organizacijski enoti kot pogodbena enota projekta

<table>
<thead>
<tr>
<th rowspan="3">Dogodek</th>
<th colspan="4">Obračunan ali prodan projekt</th>
<th rowspan="3">Projekt v fazi predprodaje</th>
<th rowspan="3">Interni projekt</th>
</tr>
<tr>
<th colspan="2">Čas in materiali</th>
<th colspan="2">Fiksna cena</th>
</tr>
<tr>
<th>Opravljeno delo</th>
<th>Valuta transakcije</th>
<th>Fiksna cena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ustvari se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td>Pošlje se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td rowspan="2">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="2">Dejanska cena</td>
<td rowspan="2">Valuta pogodbene enote
<td rowspan="2">Dejanska cena</td>
<td rowspan="2">Dejanska cena</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za obračunavanje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="3">Dejanska cena</td>
<td rowspan="3">Valuta pogodbene enote</td>
<td rowspan="3">Dejanska cena</td>
<td rowspan="3">Dejanska cena</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="2">Obračunana prodaja za mejnik</td>
<td rowspan="2">Valuta projektne pogodbe</td>
<td rowspan="2">Ni na voljo</td>
<td rowspan="2">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je popravljen s povečano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="5">
<ul>
<li>Storniranje obračunane prodaje za mejnik</li>
<li>Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></li>
</ul>
</td>
<td rowspan="5">Valuta projektne pogodbe</td>
<td rowspan="5">Ni na voljo</td>
<td rowspan="5">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je popravljen z zmanjšano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Neobračunana prodaja – obračuna se za razliko</td>
<td>Valuta projektne pogodbe</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta

<table>
<thead>
<tr>
<th rowspan="3">Dogodek</th>
<th colspan="4">Obračunan ali prodan projekt</th>
<th rowspan="3">Projekt v fazi predprodaje</th>
<th rowspan="3">Interni projekt</th>
</tr>
<tr>
<th colspan="2">Čas in materiali</th>
<th colspan="2">Fiksna cena</th>
</tr>
<tr>
<th>Opravljeno delo</th>
<th>Valuta transakcije</th>
<th>Fiksna cena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ustvari se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td>Pošlje se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td rowspan="4">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="4">Dejanska cena</td>
<td rowspan="4">Valuta pogodbene enote</td>
<td rowspan="4">Dejanska cena</td>
<td rowspan="4">Dejanska cena</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za obračunavanje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Cena enote vira</td>
<td>Valuta enote vira</td>
</tr>
<tr>
<td>Prodaja znotraj organizacije</td>
<td>Valuta pogodbene enote</td>
</tr>
<tr>
<td rowspan="5">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="5">Dejanska cena</td>
<td rowspan="5">Valuta pogodbene enote</td>
<td rowspan="5">Dejanska cena</td>
<td rowspan="5">Dejanska cena</td>
</tr>
<tr>
<td>Cena enote vira</td>
<td>Valuta enote vira</td>
</tr>
<tr>
<td>Prodaja znotraj organizacije</td>
<td>Valuta pogodbene enote</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="2">Obračunana prodaja za mejnik</td>
<td rowspan="2">Valuta projektne pogodbe</td>
<td rowspan="2">Ni na voljo</td>
<td rowspan="2">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je popravljen s povečano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="5">
<ul>
<li>Storniranje obračunane prodaje za mejnik</li>
<li>Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></li>
</ul>
</td>
<td rowspan="5">Valuta projektne pogodbe</td>
<td rowspan="5">Ni na voljo</td>
<td rowspan="5">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je popravljen z zmanjšano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Neobračunana prodaja – obračuna se za razliko</td>
<td>Valuta projektne pogodbe</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
