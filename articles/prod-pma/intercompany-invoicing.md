---
title: Zaračunavanje med podjetji
description: V tem članku so na voljo informacije in primeri zaračunavanja za projekte med podjetji.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76eba87e7cc78dcc14510a8fb53677d626bf204f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270788"
---
# <a name="intercompany-invoicing"></a>Zaračunavanje med podjetji

[!include [banner](../includes/banner.md)]

V tem članku so na voljo informacije in primeri zaračunavanja za projekte med podjetji.

Vaša organizacija ima lahko več oddelkov, podružnic in drugih pravnih subjektov, ki si za projekte izmenjujejo izdelke in storitve. Pravna oseba, ki zagotavlja storitev ali izdelek, se imenuje *pravna oseba, ki posoja*, pravna oseba, ki prejme storitev ali izdelek, pa se imenuje *pravna oseba, ki si izposoja*. 

Na spodnji sliki je prikazan tipičen primer, ko si dve pravni osebi, SI FR (pravna oseba, ki si izposoja) in SI USA (pravna oseba, ki posoja), delita sredstva za izvedbo projekta za stranko A. V tem primeru mora SI FR po pogodbi opraviti delo za stranko A. 

[![Primer zaračunavanja med podjetji](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Cilj je, da nadzor stroškov, upoštevanje prihodkov, davki in cena prenosa za projektne transakcije postanejo bolj prilagodljivi in zmogljivi. Poleg tega so na voljo naslednje zmogljivosti:

-   Ustvarite račune za stranke za projekt za pravno osebo, ki si izposoja, tako da uporabite časovne liste, stroške in račune dobaviteljev za uporabo med podjetji za pravno osebo, ki posoja.
-   Podprite izračune davkov in posredne stroške.
-   Odložite pripoznavanje prihodkov pri pravni osebi, ki posoja, in ko mora pravna oseba, ki si izposoja, pripoznati stroške.
-   Obračunajte prihodke dela v teku (WIP) za pravno osebo, ki posoja.
-   Nastavite cene prenosa, ki lahko temeljijo na različnih modelih oblikovanja cen. Tukaj je nekaj primerov:
    -   **Količina** – znesek, ki ga vnesete v polje **Oblikovanje cen**, je dejanski strošek na količino ali enoto.
    -   **Znesek stroškov** – cena/strošek na transakcijo plus znesek stroškov, ki ga vnesete v polje **Oblikovanje cen**.
    -   **Odstotek stroškov** – cena prenosa je cena/strošek na transakcijo, pomnoženo z odstotkom stroškov, ki ga vnesete v polje **Oblikovanje cen**.
    -   **Odstotek prodajne cene** – odstotek prodajne cene, ki se prenese na pravno osebo, ki posoja.
    -   **Znesek pod prodajno ceno** – znesek, ki ga pravna oseba, ki si izposoja, zadrži iz prodajnih cen pred prenosom pravni osebi, ki posoja.
    -   **Razmerje prispevkov** – številka, ki jo vnesete v polje **Oblikovanje cen** je razmerje prispevkov, ki je izraženo kot odstotek prodajne cene.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1. primer: Nastavitev parametrov za zaračunavanje med podjetji
V tem primeru je USSI pravna oseba, ki posoja, in njeni viri poročajo čas pravni osebi, ki si izposoja (FRSI), ki je lastnik pogodbe s končno stranko. Ure in stroški v poročilih zaposlenih pravne osebe USSI so lahko vključeni v račun za projekt, ki ga ustvari FRSI. Poleg tega obstaja tretji vir transakcij, ki lahko izvira iz pravne osebe, ki posoja (v tem primeru USSI), ko zagotavlja storitve skupnega dobavitelja podružnicam (kot je FRSI) in nato te stroške prenese v projekte v teh podružnicah. Vse povezane račune in izračune davkov izpolni rešitev Finance. 

V tem primeru mora biti FRSI stranka v pravni osebi USSI, USSI pa mora biti dobavitelj v pravni osebi FRSI. Nato lahko med pravnima osebama nastavite medpodjetniški odnos. Spodnji postopek prikazuje, kako nastavite parametre, tako da lahko obe pravni osebi sodelujeta pri zaračunavanju med podjetji.

1. Nastavite FRSI kot stranko v pravni osebi USSI in USSI kot dobavitelja v pravni osebi FRSI. Za korake, ki so potrebni za to opravilo, obstajajo tri vstopne točke.

   | Korak |                                                       Vstopna točka                                                        |                                                                                                                                                                                               Opis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | V USSI kliknite <strong>Terjatve</strong> &gt; <strong>Strank </strong> &gt; <strong>Vse stranke</strong>. |                                                                                                                                                                  Ustvarite nov zapis stranke za FRSI in izberite skupino strank.                                                                                                                                                                  |
   |  K   |    V FRSI kliknite <strong>Obveznosti</strong> &gt; <strong>Dobavitelji</strong> &gt; <strong>Vsi dobavitelji</strong>.     |                                                                                                                                                                    Ustvarite nov zapis dobavitelja za USSI in izberite skupino dobaviteljev.                                                                                                                                                                    |
   |  C   |                                  V FRSI odprite zapis dobavitelja, ki ste ga pravkar ustvarili.                                  | V podoknu za dejanja na zavihku <strong>Splošno</strong> v skupini <strong>Nastavitev</strong> kliknite <strong>Med podjetji</strong>. Na strani <strong>Med podjetji</strong> na zavihku <strong>Trgovinski odnos</strong> nastavite drsnik <strong>Dejavno</strong> na <strong>Da</strong>. V polju <strong>Podjetje stranke</strong> izberite zapis stranke, ki ste ga ustvarili v koraku A. |


2. Kliknite **Vodenje projektov in računovodstvo** &gt; **Nastavitev** &gt; **Vodenje projektov in računovodski parametri** in nato še zavihek **Med podjetji**. Način nastavitve parametrov je odvisen od tega, ali ste pravna oseba, ki si izposoja, ali pravna oseba, ki posoja.
   -   Če ste pravna oseba, ki si izposoja, izberite kategorijo nabave, ki naj se uporabi za povezovanje računov dobaviteljev, ki se samodejno ustvarijo.
   -   Če ste pravna oseba, ki posoja, za vsako pravno osebo, ki si izposoja, izberite privzeto kategorijo projekta za posamezno vrsto transakcije. Kategorije projektov se uporabljajo za konfiguracijo davka, če fakturirana kategorija v transakcijah med podjetji obstaja samo v pravni osebi, ki si izposoja. Izberete lahko obračun prihodkov za transakcije med podjetji. Ta obračun je narejen, ko so transakcije knjižene, ter nato storniran, ko je knjižen račun med podjetji.

3. Kliknite **Vodenje projektov in računovodstvo** &gt; **Nastavitev** &gt; **Cene** &gt; **Cena prenosa**.
4. Izberite valuto, vrsto transakcije in model cene prenosa. Valuta, ki se uporablja na računu, je valuta, ki je konfigurirana v zapisu stranke za pravno osebo, ki si izposoja, v pravni osebi, ki izposoja. Valuta se uporablja za povezovanje vnosov v tabeli cen prenosa.
5. Kliknite **Glavna knjiga** &gt; **Nastavitev knjiženja** &gt; **Medpodjetniško računovodstvo** in nastavite odnos za USSI in FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. primer: Ustvarjanje in objava časovnega lista za uporabo med podjetji
USSI (pravna oseba, ki posoja) mora ustvariti in objaviti časovni list za projekt iz FRSI (pravna oseba, ki si izposoja). Za korake, ki so potrebni za to opravilo, obstajata dve vstopni točki.

| Korak | Vstopna točka                                                                       | Opis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Vodenje projektov in računovodstvo** &gt; **Časovni listi** &gt; **Vsi časovni listi** | Ustvarite nov časovni list. V vrstici časovnega lista v polju **Pravna oseba** izberite **FRSI**. V polju **ID projekta** izberite projekt v FRSI. Vnesite ure za vsak dan v tednu. |
| K    | Stran **Časovni list**                                                                | Ko se potek dela zažene, objavite časovni list in si zapišite številko kupona.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. primer: Ustvarjanje in objava računa dobavitelja za uporabo med podjetji
USSI (pravna oseba, ki posoja) mora ustvariti in objaviti račun dobavitelja za uporabo med podjetji za projekt iz FRSI (pravna oseba, ki si izposoja). Ta račun dobavitelja predstavlja zunanje delo in strošek dobaviteljev, ki jih plača USSI. Za korake, ki so potrebni za to opravilo, obstajata dve vstopni točki.

| Korak | Vstopna točka                                                                                      | Opis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Obveznosti** &gt; **Računi** &gt; **Odprti računi dobaviteljev** &gt; **Nov račun dobavitelja** | Ustvarite nov račun dobavitelja in vnesite storitve, ki so bile naročene v imenu projekta pravne osebe FRSI.                                                                                                                                                                                  |
| K    | Stran **Račun dobavitelja**                                                                      | Vnesite vrstice, ki predstavljajo zunanje storitve v imenu pravne osebe FRSI. Na zavihku za hiter dostop **Podrobnosti vrstice** na zavihku **Projekt** za vrstico računa v polje **Projektno podjetje** vnesite **FRSI**. Vnesite projekt in ustrezne podatke. Nato knjižite račun dobavitelja. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. primer: Ustvarjanje in knjiženje računa med podjetji
USSI (pravna oseba, ki posoja) mora ustvariti in knjižiti račun med podjetji. Za korake, ki so potrebni za to opravilo, obstajata dve vstopni točki.

| Korak | Vstopna točka                                                                                             | Opis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Vodenje projektov in računovodstvo** &gt; **Računi za projekt** &gt; **Medpodjetniški račun stranke**  | Kliknite **Novo**, da odprete stran **Ustvarjanje medpodjetniškega računa**.                                                                                  |
| K    | **Vodenje projektov in računovodstvo** &gt; **Računi za projekt** &gt; **Medpodjetniški računi stranke** | Na strani **Ustvarjanje medpodjetniškega računa** vnesite pravno osebo, navedite transakcijo, ki jo želite vključiti, in kliknite **Iskanje**. |
| C    | **Vodenje projektov in računovodstvo** &gt; **Računi za projekt** &gt; **Medpodjetniški računi stranke** | Izberite transakcije za račun ali kliknite **Izberi vse** za fakturiranje vseh transakcij na seznamu in nato kliknite **V redu**.                  |
| D    | Stran **Medpodjetniški račun**                                                                       | Prikaže se predlog medpodjetniškega računa za stranko.                                                                                             |
| E    | Stran **Medpodjetniški račun**                                                                       | Kliknite **Knjiži**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. primer: Knjiženje računa dobavitelja in izdaja računa stranki
Ko USSI (pravna oseba, ki posoja) objavi medpodjetniški račun za stranko, se v FRSI (pravna oseba, ki si izposoja) ustvari ujemajoč se račun dobavitelja. Ko je ta račun dobavitelja knjižen, FRSI tudi izda račun za stranko projekta za ure, ki jih je vnesla pravna oseba USSI. Za korake, ki so potrebni za to opravilo, obstajajo tri vstopne točke.

| Korak | Vstopna točka                                                                                        | Opis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Obveznosti** &gt; **Računi** &gt; **Čakajoči računi dobavitelja**                            | Preglejte račun, da preverite, ali so vključene vrednosti časovnega lista, in nato knjižite račun dobavitelja.                  |
| K    | **Vodenje projektov in računovodstvo** &gt; **Računi za projekt** &gt; **Predlogi računa za projekt** | Ustvarite nov račun za projekt in preverite, ali so prikazane urne transakcije, ki so bile objavljene.            |
| C    | Stran **Račun za projekt**                                                                       | Izberite račun za projekt in kliknite **Prikaži podrobnosti** za pregled stroškov in zneska prodaje. Nato knjižite račun. |


Za več informacij glejte [Konfiguriranje zaračunavanja projektov med podjetji](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]