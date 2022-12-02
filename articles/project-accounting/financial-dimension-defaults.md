---
title: Privzete vrednosti finančnih razsežnosti
description: V tem članku so na voljo informacije o tem, kako nastaviti privzete vrednosti finančne razsežnosti.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9e0d739ac1b7681e2e77ec651daf3da8316ff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931074"
---
# <a name="financial-dimension-defaults"></a>Privzete vrednosti finančnih razsežnosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_



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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
