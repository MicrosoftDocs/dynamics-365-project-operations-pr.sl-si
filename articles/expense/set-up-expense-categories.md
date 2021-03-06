---
title: Nastavitev kategorij stroškov
description: Ta tema vsebuje informacije o nastavitvi kategorij stroškov in skupnih kategorij za poročila o stroških.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896706"
---
# <a name="set-up-expense-categories"></a>Nastavitev kategorij stroškov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ko zaposleni ustvarijo poročila o stroških, morajo biti vsi zabeleženi stroški povezani s kategorijo stroškov. Kategorije stroškov izhajajo iz skupnih kategorij, ki si jih delijo vse pravne osebe v vaši organizaciji. Če struktura vaše organizacije to omogoča, lahko te kategorije stroškov delite tudi z drugimi področji. Na podlagi strukture vaše organizacije in navodil izvedbene ekipe morate določiti, ali se bodo kategorije, ki se uporabljajo pri upravljanju stroškov, uporabljale samo pri upravljanju stroškov ali jih boste delili z drugimi področji.

> [!NOTE]
> Te kategorije si lahko delita oddelka »Vodenje projekta in računovodstvo« in »Upravljanje stroškov« oz. »Vodenje projekta in računovodstvo« in »Proizvodnja«. Ne moreta pa si jih deliti »Upravljanje stroškov« in »Proizvodnja«.

Pred začetkom postopka namestitve se morate za vsako kategorijo stroškov odločiti o naslednjem:

- Katera kategorija stroška je izbrana? Primeri vključujejo kategorije za lete, hotele ali kilometrino.
- Ali lahko kategorijo stroškov uporabljajo tudi na oddelku »Vodenje projekta in računovodstvo«? Če je odgovor pritrdilen, morate določiti tudi naslednje:

    - Kateri računi stroškov bodo uporabljeni za naslednje stroške?

        - Cena
        - Dodelitev plače
        - Vrednost cene WIP
        - Element stroška
        - Element vrednosti cene WIP
        - Vračunana izguba
        - Vračunana izguba WIP

    - Kateri računi prihodkov bodo uporabljeni za naslednje vire prihodkov?

        - Fakturirani prihodek
        - Vračunana vrednost prihodkov od prodaje
        - Vrednost prodaje WIP
        - Vračunano razmerje med prihodkom in proizvodnjo
        - Proizvodnja WIP
        - Vračunano razmerje med prihodkom in dobičkom
        - Dobiček WIP
        - Vračunano razmerje med prihodkom in naročnino
        - Naročnina WIP

- Katera vrsta stroška je izbrana?
- Kateri je privzeti način plačila za kategorijo stroškov?
- Ali je treba razčleniti stroške v kategoriji stroškov?
- Kateri je glavni privzeti račun za kategorijo stroškov?
- Katera je privzeta davčna skupina za prodajo izdelka za kategorijo stroškov?
- Ali so za kategorijo stroškov dovoljeni dodatni načini plačila? Če je odgovor pritrdilen, kateri so to?
- Ali obstajajo podkategorije v tej kategoriji stroškov? Če obstajajo podkategorije, morate določiti tudi naslednje:

    - Ali je katera od podkategorij izključena iz davčne olajšave?
    - Katera davčna skupina za prodajo izdelka velja za podkategorije?
