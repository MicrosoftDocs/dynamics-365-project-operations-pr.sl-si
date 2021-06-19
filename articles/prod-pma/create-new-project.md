---
title: Ustvarite nov projekt
description: Ta tema vsebuje informacije o ustvarjanju novega projekta.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006261"
---
# <a name="create-a-new-project"></a>Ustvarite nov projekt

[!include [banner](../includes/banner.md)]

Dokončajte naslednje korake, da ustvarite nov projekt.

1. Na strani **Vodenje projektov** izberite **Nov projekt**, nato pa vnesite naslednje vrednosti:

    - **Vrsta projekta:** Čas in material
    - **Ime projekta:** 2. faza nadgradnje XYZ
    - **Projektna skupina:** TM\_WIP
    - **ID projektne pogodbe:** 00000002

2. Izberite **Ustvarjanje projekta**.

## <a name="assign-a-resource-to-a-project"></a>Dodeljevanje vira projektu

1. Na strani **Delavci** na seznamu **Delavci** izberite zapis za delavca, za katerega ste prej nastavili spodobnosti, in odprite zapis delavca.
2. V podoknu za dejanja na zavihku **Projekt** v skupini **Nastavitev** izberite **Dodelitve projektov**.
3. Na strani **Dodelitve projekta potrjevanja vira** na zavihku **Projekti** v polju **Dodaj projekt v izbrane projekte** filtrirajte na projekt **2. faza nadgradnje XYZ**.
4. V podoknu **Preostali projekti** izberite projekt in nato izberite gumb puščice, da ga dodate v podokno **Izbrani projekti**.

Prav tako lahko dodelite kategorije za vir, kot je potrebno. Vrsta kategorije je bodisi **Stroški** ali **Prihodki**. Vrsto kategorije določa vaša organizacija. Če za vir ni dodeljene nobene kategorije, storitev Finance poišče privzeto kategorijo urnih cen stroškov in prihodkov.

## <a name="set-up-project-resource-and-role-characteristics"></a>Nastavitev vira projekta in značilnosti vloge

Projektni vodja lahko uporabi funkcionalnost iskanja virov za projekt, da ustvari vloge, ki so potrebne za projekt. Vloge se lahko uporabijo, če so potrjeni viri še vedno neznani, ko se viri rezervirajo. Vloge so lahko začasno rezervirane kot načrtovani viri, da lahko nadaljujete faze načrtovanja projekta.

[![Primer vloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarij:** Contoso je bil najet za dokončanje projekta Čas in material, ki ima odobreno projektno listino. Mlajši projektni vodja še vedno izpolnjuje obseg projekta. Upravitelj virov trenutno prepoznava specifične vire, ki bodo rezervirani za delo na novem projektu. Zaradi kritične narave projekta je sponzor projekta za eno od vlog zahteval višjega projektnega vodjo. Upravitelj virov mora pridobiti nov vir in določiti vlogo v sistemu, če mlajši projektni vodja med načrtovanjem projekta zahteva informacije o viru.

Naslednji koraki prikazujejo, kako lahko upravitelj virov nastavi vlogo višjega projektnega vodje in z njo poveže značilnosti vira. Pozneje lahko vlogo uporabimo za iskanje razpoložljivih virov, ki se ujemajo z zahtevanimi sposobnostmi virov.

1. Na strani **Nastavitev vlog** izberite **Novo**, nato pa vnesite naslednje vrednosti:

    - **ID vloge:** Višji projektni vodja
    - **Opis:** Višji projektni vodja

2. Izberite **Ustvari**.
3. Izberite vlogo **Višji projektni vodja** in nato izberite **Konfiguracija značilnosti**.
4. V polju **Vrsta značilnosti** izberite **Znanje**.
5. V polju **Razpoložljive značilnosti** vnesite znanje, po katerem se išče.
6. V polju **Vrsta značilnosti** izberite **Potrdilo**.
7. V polju **Razpoložljive značilnosti** vnesite vrsto potrdila, po katerem se išče.

## <a name="assign-a-project-resource-to-a-project"></a>Dodeljevanje vira projekta projektu

1. Na strani **Vsi projekti** izberite projekt **2. faza nadgradnje XYZ**.
2. Na zavihku **Projektna ekipa in načrtovanje** izberite **Dodaj**.
3. V polju **Vloga** izberite **Član ekipe**.
4. Izberite **Rezervacija iz koledarja**.
5. Na strani **Razpoložljivost vira** izberite **Nastavitve pogleda**.
6. Na strani **Prilagajanje nastavitev pogleda** vnesite naslednje vrednosti:

    - **Oblika za pogled datumskega obsega:** Dan
    - **Prikaz opisov razpoložljivosti:** Da
    - **Prikaz preostale zmogljivosti:** Da

7. Na seznamu virov izberite vir.
8. Izberite **Veljavna rezervacija** in **Polna zmogljivost**.

## <a name="assign-a-resource-to-a-default-role"></a>Dodeljevanje vira privzeti vlogi

Kot pomoč lahko projektni vodje ali upravitelji virov prikažejo vire, ki jih je mogoče rezervirati za projekt, na ravni z več podrobnostmi. Privzeto vlogo lahko povežete z obstoječim virom ali novo pridobljenim virom. Na primer, Daniel je imel ob začetku sodelovanja izkušnje in znanja za zapolnitev vloge poslovnega analitika. Upravitelj virov je to vlogo določil kot privzeto vlogo za Daniela. Zato je upravitelj virov Daniela dodal v skupino poslovnih analitikov, ki so na voljo za delo na projektih.

Med rezervacijo virov lahko projektni vodje filtrirajo vire z vlogo, ki so na voljo za delo na projektih. Te informacije lahko uporabijo kot eno merilo, kadar med zapolnitvijo virov izvajajo analizo odločitev z več merili. V filter lahko dodajo tudi druge značilnosti virov za iskanje virov s posebnimi znanji, izobrazbo in izkušnjami za določen projekt.

**Scenarij:** Odobren projekt se je začel in vloga višjega projektnega vodje je bila rezervirana kot načrtovani vir v fazi načrtovanja projekta. Upravitelj virov je zdaj pridobil vir za zapolnitev vloge višjega projektnega vodje.

1. Na strani **Seznam virov** izberite **Daniel Goldschmidt**.
2. Na strani **Vloga vira** izberite **Novo**, nato pa vnesite naslednje vrednosti:

    - **Datum začetka veljavnosti:** Vnesite trenutni datum.
    - **Datum poteka:** Vnesite **Nikoli**.
    - **Vloga:** Vnesite **Višji projektni vodja**.

3. Izberite **Shrani** in nato zaprite stran.
4. Na zavihku **Sposobnosti** dodajte znanje **Vodenje projektov** in potrdilo **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]