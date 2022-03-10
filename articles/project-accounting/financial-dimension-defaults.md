---
title: Privzete vrednosti finančnih razsežnosti
description: V tej temi so na voljo informacije o tem, kako nastaviti privzete vrednosti finančne razsežnosti.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922958"
---
# <a name="financial-dimension-defaults"></a>Privzete vrednosti finančnih razsežnosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations uporablja ogrodje [Finančne razsežnosti](/dynamics365/finance/general-ledger/financial-dimensions) v storitvi Dynamics 365 Finance za podajanje dodatnih vpogledov na transakcije podknjige in glavne knjige projekta.

Privzete finančne razsežnosti je mogoče nastaviti na stranko, vir financiranja projekta, mejnik, vrstico projektne pogodbe ali projekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Določanje privzetih finančnih razsežnosti za stranko

Privzete razsežnosti stranke so določene v storitvi Finance. Dokončajte naslednje korake za nastavitev privzetih vrednosti razsežnosti.

1. Pojdite na **Terjatve** > **Stranke** > **Vse stranke**.
2. Na strani **Stranke** na zavihku **Finančne razsežnosti** nastavite vrednost finančne razsežnosti za določeno stranko.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Določanje privzetih finančnih razsežnosti za projektne pogodbe

Projektne pogodbe so ustvarjene in vzdrževane v storitvi Common Data Service (CDS). Računovodski atributi za projektne pogodbe so nastavljeni v modulu **Upravljanje projektov in računovodstvo** v storitvi Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Nastavitev finančnih razsežnosti za vir financiranja projekta

1. Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Projektne pogodbe**.
2. Izberite zapis, ki ga želite posodobiti, in na zavihku **Projektna pogodba** izberite **Prikaži privzeto računovodstvo**.
3. Razširite **Povezane informacije** in izberite zavihek **Viri financiranja**.
4. Nastavite privzete vrednosti finančne razsežnosti. Upoštevajte, da so privzete vrednosti finančne razsežnosti iz računa stranke.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Nastavitev finančnih razsežnosti za podrobnosti pogodbe projekta

1. Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Projektne pogodbe**.
2. Izberite zapis, ki ga želite posodobiti, in na zavihku **Projektna pogodba** izberite **Prikaži privzeto računovodstvo**.
3. Razširite **Povezane informacije** in izberite zavihek **Podrobnosti pogodbe**.
4. Nastavite privzete vrednosti finančne razsežnosti. Privzete vrednosti finančne razsežnosti so veljavne in se lahko uporabljajo samo s podrobnostmi pogodbe fiksne cene (mejnik).

Te privzete vrednosti se uporabljajo na povezanih transakcijah za kupca in vrsticah računov projekta.

## <a name="define-default-financial-dimensions-for-projects"></a>Določanje privzetih finančnih razsežnosti za projekte

Projekti so ustvarjeni in vzdrževani v storitvi CDS. Računovodski atributi za projekte so nastavljeni v modulu **Upravljanje projektov in računovodstvo** v storitvi Finance.

1. Odprite **Vodenje projekta in računovodstvo** > **Projekti** > **Vsi projekti**.
2. Izberite zapis, ki ga želite posodobiti, in na zavihku **Projekt** izberite **Prikaži privzeto računovodstvo**.
3. Razširite **Povezane informacije** in izberite zavihek **Nastavitev**.
4. Nastavite privzete vrednosti finančne razsežnosti. Upoštevajte, da so privzete vrednosti finančne razsežnosti iz računa stranke. Če je projekt povezan s podrobnostmi pogodbe z več strankami za pogodbo projekta, se uporabi primarna stranka za nastavitev finančnih razsežnosti na privzete.

Privzete finančne razsežnosti projekta se uporabljajo za nastavitev privzetih vrednosti vrstice dnevnika za čas, stroške in brezplačne transakcije v možnosti **Dnevnik integracij za Project Operations** ter na povezanih projektnih vrsticah računa.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Uporabite finančne razsežnosti za vnose časa projekta
Če želite uporabiti finančne razsežnosti za vnose časa projekta, upoštevajte, da privzeta vrednost dimenzije temelji na naslednjem vrstnem redu:

1. Vir
2. Projekt
3. Vir financiranja

Na primer, če je privzeta dimenzija podana v viru, bo uporabljena nad privzeto, ki je podana v projektu. Podobno bo privzeta dimenzija projekta uporabljena nad privzeto, ki je določena v viru financiranja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
