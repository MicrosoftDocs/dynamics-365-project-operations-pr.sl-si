---
title: Pregled dejanskih vrednosti
description: Ta tema vsebuje informacije o dejanskih podatkih za projekt.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084954"
---
# <a name="actuals-overview"></a>Pregled dejanskih vrednosti

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dejanski podatki se nanašajo na količino dela, ki je bilo opravljeno za projekt. Dejanske podatke za projekt je mogoče izslediti do njihovih izvornih dokumentov. Ti izvorni dokumenti vključujejo čas, stroške, dnevniške vnose in tudi račune.

![Kako se dejanske podatke za projekt izsledi v izvornih dokumentih](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Pošiljanje časovnega vnosa

Ko je v PSA poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za čas in materiale, se ustvarita dve vrstici dnevnika. Ena vrstica je za ceno, druga za neobračunano prodajo. Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se ustvari samo vrstica dnevnika za ceno. 

Logika za vnos privzetih cen uporablja vrstico dnevnika. Vse vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika. Ta polja vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom. 

Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Organizacijska enota** , povzročijo, da se v vrstico dnevnika privzeto vnese ustrezna cena. Če za časovni vnos dodate polje po meri in želite, da se vrednost polja razširi na dejanske podatke, ustvarite polje v entiteti »Dejanski podatki« in za kopiranje polja iz časovnega vnosa v dejanske podatke uporabite preslikave polj.

## <a name="submitting-an-expense-entry"></a>Pošiljanje vnosa stroška

Ko je v PSA poslan vnos stroška za projekt, ki je preslikan v podrobnosti pogodbe za čas in materiale, se ustvarita dve vrstici dnevnika. Ena vrstica je za ceno, druga za neobračunano prodajo. Ko je poslan vnos stroška za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se ustvari samo vrstica dnevnika za ceno.

Logika za vnašanje privzetih cen za stroške temelji na kategoriji stroška, ki je izbrana na strani **Vnos stroška**. Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika. Vendar pa je za ceno znesek, ki ga je uporabnik vnesel, privzeto nastavljen neposredno v povezani vrstici dnevnika stroškov za strošek in prodajo.

V trenutni različici aplikacije PSA vnos privzetih cen na enoto na podlagi kategorije za vnose stroška ni na voljo.

## <a name="using-entry-journals-to-record-costs"></a>Uporaba dnevnikov za zapisovanje stroškov

V aplikaciji PSA lahko v dnevnike beležimo stroške ali prihodke v razredih transakcij za material, provizijo, čas, stroške ali davke. Dnevnik vsebuje glavo, vrstice in ukaz za **potrditev**. Tukaj je nekaj scenarijev, v katerih lahko uporabite dnevnik:

- Za projekt morate zabeležiti dejanske stroške materiala in prodaje.
- V PSA morate prenesti dejanske podatke o transakcijah iz drugega sistema.
- Zabeležiti morate stroške, ki so nastali v drugem sistemu, npr. za stroške nabave ali podizvajalcev.

> [!IMPORTANT]
> Dnevnike za ustvarjanje dejanskih podatkov naj uporablja samo en uporabnik, ki je v celoti seznanjen z računovodskim vplivom, ki ga imajo dejanski podatki na projekt. Razlog je v tem, da aplikacija ne potrdi vrstice dnevnika ali s tem povezane cene, ki je vnesena v vrstico dnevnika. Zaradi vpliva teh vrst dnevnikov bodite previdni, komu omogočite dostop do ustvarjanja vknjižb.     


## <a name="recording-actuals-based-on-project-events"></a>Zapisovanje dejanskih podatkov na podlagi projektnih dogodkov

PDA zapiše finančne transakcije v okviru projekta. Te transakcije se zapišejo kot **dejanske vrednosti**. V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.

**Vir pripada isti organizacijski enoti kot pogodbena enota projekta**

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

**Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta**

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
