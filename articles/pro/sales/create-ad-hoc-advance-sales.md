---
title: Ustvarjanje namenskega predplačila za pogodbo – poenostavljena različica
description: V tej temi so na voljo informacije o ustvarjanju predujma za pogodbo, kot je potrebno.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181382"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Ustvarjanje namenskega predplačila za pogodbo – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Microsoft Dynamics 365 Project Operations podpira scenarije izstavljanja računov, ki vključujejo predplačila in predujme. Postopek za uporabo možnosti **Predujmi** v storitvi **Project Operations** je podoben pogodbam **Honorar**. 

Izpolnite naslednje korake, da stranki izdate račun za predujem.

1. Pojdite na stran **Projektna pogodba** in nato izberite zavihek **Predujmi in honorarji**.
2. V podmreži, ki navaja vse prej zabeležene predujme in predplačila, izberite **+ Nov honorar za projektno pogodbo**. 

    Odpre se obrazec **Hitro ustvarjanje** za beleženje predplačila ali predujma.
    
3. Spodnja tabela navaja polja za beleženje predujma in vidike, ki jih je treba upoštevati ob ustvarjanju novih:

    | Polje | Opis | Nadaljnji vpliv |
    | --- | --- | --- |
    | **Stranka projektne pogodbe** | To polje označuje, kateri stranki v pogodbi bo zaračunano za ta predujem. | Če imate v pogodbi več strank in želite vsaki od njih izdati račun za določen znesek honorarja ali predujma, ustvarite predujem za vsako stranko posebej. |
    | **Opis** | Opis namena ali časa predujma za lažje prepoznavanje tega predujma. | Ta opis je prikazan v vrstici računa za ta predujem. |
    | **Znesek** | Znesek za predplačilo ali predujem. | Ta znesek je prikazan v vrstici računa za ta predujem. |
    | **Datum računa** | Datum, ko je ta predujem zaračunan stranki. | To je datum za avtomatizirani postopek ustvarjanja računov, da se ustvari vrstica računa za ta predujem. |
    | **Stanje računa** | To je nastavitev možnosti, ki označuje, ali je predujem dodan v osnutek računa za to stranko. Možne vrednosti so:</br>- **Ni pripravljeno za izdajanje računov**</br>- **Pripravljeno za izdajanje računov** | Ko je predujem ali predplačilo označeno kot **Pripravljeno za izdajanje računov**, je dodano kot čas vrstice v osnutku računa. Samo v celoti zaračunan predujem je mogoče uporabiti za uskladitev glede na projektne stroške za naslednje obdobje računa. |

4. Izberite **Shrani in zapri** v pogovornem oknu za hitro ustvarjanje, da zabeležite predujem ali predplačilo.
