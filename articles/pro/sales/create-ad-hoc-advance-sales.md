---
title: Ustvarite ad hoc predujem za projektno pogodbo
description: V tem članku so na voljo informacije o ustvarjanju predujma za pogodbo, kot je potrebno.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824882"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Ustvarite ad hoc predujem za projektno pogodbo

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Microsoft Dynamics 365 Project Operations podpira scenarije za izstavljanje računov, ki vključujejo predplačila in predujme. Postopek za uporabo možnosti **Predujmi** v storitvi **Project Operations** je podoben pogodbam **Honorar**. 

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
