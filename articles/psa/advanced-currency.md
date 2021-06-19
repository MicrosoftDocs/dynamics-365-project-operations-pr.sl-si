---
title: Scenariji z več valutami (različica 3.x)
description: Ta tema vsebuje informacije o scenarijih z več valutami.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 70f27d29c74a82f0307bd0724347960e5755e3a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014811"
---
# <a name="multiple-currency-scenarios"></a>Scenariji z več valutami

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 ima dva koncepta valut:

- **Valuta transakcije** – valuta, v kateri se izvede transakcija 
- **Osnovna valuta** – valuta primerka Dynamics 365 Ta valuta je nastavljena, ko je omogočena uporaba primerka Dynamics 365. Ni je mogoče spremeniti.

Contoso ZDA na primer proda 100 majic stranki v Združenem kraljestvu za 15 funtov (GBP) na kos. Spodnja tabela prikazuje, kako je ta transakcija zapisana v entiteti »Izdelek iz naročila«.

| Izdelek | Količina | Cena na enoto | Valuta | Znesek | Menjalni tečaj | Cena na enoto (osnova)| Znesek (osnova)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Majica | 100      | 15             | GBP      | 1500   | 0,94          | 17,25 USD               | 1.725 USD       |

Stolpec **Valuta** prikazuje valuto transakcije, torej valuto, v kateri je bila izvedena prodaja. Stolpec **Menjalni tečaj** prikazuje menjalni tečaj med valuto transakcije in osnovno valuto. Osnovna valuta je ameriški dolar (USD). Ta osnovna valuta je bila nastavljena, ko je bila omogočena uporaba primerka Dynamics 365.
Kot prikazuje tabela, se vsaka transakcija zapiše tako v valuti transakcije kot v osnovni valuti. Dynamics 365 za izračun zneskov v osnovni valuti uporabi menjalni.

## <a name="project-service-automation-extensions"></a>Razširitve za Project Service Automation

Dynamics 365 Project Service Automation vpliva na valuto transakcije, ker imajo poslovne transakcije običajno dve strani: strošek in prodajo.

Za poslovne transakcije veljajo naslednje entitete:

- Podrobnosti vrstic ponudbe
- Podrobnost vrstice projektne pogodbe
- Vrstica ocene
- Vrstica dnevnika
- Podrobnosti vrstice računa
- Dejansko

V vsaki od teh entitet je zapis, ki predstavlja znesek stroška ali prodajni znesek. Kot velja za vsako entiteto v Dynamics 365, ki polje **Znesek**, vsak zapis vključuje zneske v valuti transakcije in osnovni valuti. 

PSA razširja koncept valute transakcije za strošek in prodajo na naslednje načine:

- Valuta stroškovne transakcije za časovne transakcije vedno izvira iz valute organizacijske enote, ki ima projekt v lasti ali ga upravlja. Ta organizacijska enota se obravnava kot pogodbena enota.
- Valuta prodajne transakcije za časovne in stroškovne transakcije vedno izvira iz valute projektne pogodbe.
- Valuta stroškovne transakcije za stroške izvira iz valute, v kateri je bil ustvarjen vnos stroška.

## <a name="multiple-currency-scenario"></a>Scenarij z več valutami

V tem razdelku je opisan primer projekta, ki ga Contoso Združeno kraljestvo dostavi stranki z imenom Fabrikam, Japonska. Scenarij je sestavljen tako:

1. GBP in japonski jen (JPY) sta nastavljena v razdelku **Nastavitve** \> **Upravljanje poslovanja** \> **Valute**. 
2. Odpre se račun stranke z imenom **Fabrikam – Japonska** in JPY je izbran kot valuta za račun.
3. Nastavi se organizacijska enota, imenovana **Contoso Združeno kraljestvo**, za katero je izbrana valuta GBP.
4. Ustvarjena je projektna pogodba, v kateri je podjetje **Contoso Združeno kraljestvo** opredeljeno kot pogodbena enota, podjetje **Fabrikam – Japonska** pa je določeno kot stranka.
5. Ustvarijo se podrobnosti projektne pogodbe, in sicer na podlagi različnih razredov dogovorov za zaračunavanje v okviru projekta, npr. obračunavanje za čas v primerjavi z obračunavanjem za stroške.
6. Ustvari se projekt, v katerem je podjetje **Contoso Združeno kraljestvo** opredeljeno kot pogodbena enota. Ta projekt je ustvarjen in preslikan v vrstice projektne pogodbe.


Pri izvedbi ocene, ki uporablja podrobnosti vrstice ponudbe, podrobnosti vrstice projektne pogodbe ali vrstico ocene v razporedu, sta v entiteti vedno ustvarjena dva zapisa. En zapis je za strošek, drugi za prodajo.

- Valuta transakcije v zapisu stroška je privzeto nastavljena na valuto pogodbene enote projekta. V tem primeru je ta valuta GBP.
- Valuta transakcije v prodajnem zapisu je privzeto nastavljena na valuto projektne pogodbe. V tem primeru je ta valuta JPY.

Ko so ustvarjene dejanske vrednosti za čas z uporabo časovnega vnosa ali vrstice dnevnika, se zgodi naslednje:

- Valuta transakcije v zapisu stroška je privzeto nastavljena na valuto pogodbene enote projekta.
- Valuta transakcije v prodajnem zapisu je privzeto nastavljena na valuto projektne pogodbe.

Ko so ustvarjene dejanske vrednosti za stroške z uporabo vnosa stroška ali vrstice dnevnika, se zgodi naslednje:

- Znesek stroška lahko zapišete v kateri koli valuti. Izberite valuto z izbirnikom valut na strani **Vnos stroška** ali na strani **Vrstica dnevnika**. Valuta transakcije v zapisu stroška je privzeto nastavljena na valuto iz vnosa stroška. 
- Valuta transakcije za prodajni zapis je privzeto valuta projektne pogodbe. Če želite nastaviti to valuto, sistem najprej pretvori znesek transakcije v valuti, ki jo je uporabnik vnesel kot osnovno valuto. Nato pretvori znesek v valuto projektne pogodbe. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Izračun zbranih vrednosti, ko so dejanske vrednosti projekta zapisane v več valutah transakcij

Dynamics 365 samodejno izvede zbiranje zneskov v različnih valutah. Spodaj je primer tega.

| Razred transakcije | Vrsta transakcije| Datum   | Vir | Kategorija transakcije | Količina | Cena enote | Znesek      | Menjalni tečaj | Znesek v osnovni valuti |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Neobračunana prodaja   | 14. jun | Martin  |                      | 8 ur    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Neobračunana prodaja   | 15. jun | Martin  |                      | 8 ur    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Expense           | Neobračunana prodaja   | 16. jun | Martin  | Hotel                | 1 enota     | 250 EUR      | 250 EUR     | 0,94          | 265,95 USD     |
| Expense           | Neobračunana prodaja   | 17. jun | Martin  | Najem avtomobila           | 1 enota     | 150 EUR      | 150 EUR     | 0,94          | 159,57 USD     |

Če želite izračunati skupno vrednost neobračunanega prodajnega zneska za projekt, lahko ustvarite zbirno polje za polje **Znesek** za vse povezane dejanske vrednosti neobračunanih prodajnih zneskov. Zbirno polje je konstrukt v Dynamics 365, ki omogoča hitre izračune formule v sorodnih zapisih.


[!INCLUDE[footer-include](../includes/footer-banner.md)]