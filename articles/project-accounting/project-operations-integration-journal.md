---
title: Dnevnik integracij v aplikaciji Project Operations
description: Ta tema vsebuje informacije o delu z dnevnikom integracij v aplikaciji Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c5cc3254c52750b35be2c66137b6c57bbd9acbfbc89dedc6559059a89c8e2393
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987951"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracij v aplikaciji Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Vnosi časa in stroškov ustvarijo **Dejanske** transakcije, ki predstavljajo operativni pogled na delo, opravljenega v zvezi s projektom. Aplikacija Dynamics 365 Project Operations računovodjam zagotavlja orodje za pregled transakcij in prilagoditev računovodskih atributov. Po zaključku pregleda in prilagoditev se transakcije zabeležijo v podknjigo in glavno knjigo projekta. Računovodja lahko te dejavnosti izvaja s pomočjo dnevnika **Integracija za Project Operations** (**Dynamics 365 Finance** > **Upravljanje projektov in računovodstvo** > **Dnevniki** >  Dnevnik **integracij za Project Operations**.

![Potek dnevnika integracij.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Ustvarjanje zapisov v dnevniku integracij za Project Operations

Zapisi v dnevniku integracij za Project Operations so ustvarjeni s periodičnim postopkom **Uvoz iz pripravljalne tabele**. Ta postopek lahko zaženete tako, da odprete **Dynamics 365 Finance** > **Upravljanje projektov in računovodstvo** > **Periodično** > **Integracija za Project Operations** > **Uvoz iz pripravljalne tabele**. Proces lahko zaženete interaktivno ali ga po potrebi konfigurirate tako, da se izvaja v ozadju.

Ko se periodični postopek zažene, so najdene vse dejanske vrednosti, ki še niso dodane v dnevnik integracij za Project Operations. Ustvari se vrstica dnevnika za vsako dejansko transakcijo.
Sistem vrstice dnevnika razvrsti v ločene dnevnike glede na vrednost, izbrano v polju **Enota obdobja v dnevniku integracij za Project Operations** (**Finance** > **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Parametri upravljanja projektov in računovodstvo**, zavihek **Project Operations v storitvi Dynamics 365 Customer Engagement**). Možne vrednosti za to polje vključujejo:

  - **Dnevi**: dejanske vrednosti so razvrščene po datumu transakcije. Za vsak dan se ustvari ločen dnevnik.
  - **Meseci**: dejanske vrednosti so razvrščene po koledarskem mesecu. Za vsak mesec se ustvari ločen dnevnik.
  - **Leta**: dejanske vrednosti so razvrščene po koledarskem letu. Za vsako leto se ustvari ločen dnevnik.
  - **Vse**: vse dejanske transakcije so vključene v isti dnevnik integracij. Če dnevnik ni na voljo, ko se izvaja periodični postopek, na primer če je dnevnik v postopku beleženja transakcij, se ustvari nov dnevnik.

Vrstice dnevnika so ustvarjene na podlagi dejanskih vrednosti projekta. Na spodnjem seznamu so navedena nekatera pomembna privzeta pravila in pravila pretvarjanja:

  - Vsaka dejanska transakcija projekta ima vrstico v dnevniku integracij Project Operations. Stroškovne in neračunane prodajne transakcije za čas in vrsto obračunavanja materiala so prikazane v ločenih vrsticah.
  - Polje **Datum** predstavlja datum transakcije. Polje **Datum knjiženja** predstavlja datum, ko je transakcija zabeležena v knjigo. Če je datum knjiženja v [zaključenem obdobju financ](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) in je parameter **Samodejna nastavitev datuma knjiženja na odprto obdobje knjige** nastavljen na zavihek **Finance** strani **Parametri upravljanja projektov in računovodstvo**, bo sistem prilagodil datum knjiženja transakcije na prvi datum v naslednjem odprtem obdobju knjige.
  - Polje **Kupon** prikazuje številko kupona za vsako dejansko transakcijo. Zaporedje številk kuponov je določeno na zavihku **Zaporedja števil** na strani **Parametri upravljanja projektov in računovodstvo**. Vsaki vrstici je dodeljena nova številka. Ko je kupon zabeležen, si lahko pod možnostjo **Povezani kuponi** na strani **Transakcija s kuponi** ogledate, kako so stroškovne in neračunane prodajne transakcije povezane.
  - Polje **Kategorija** predstavlja projektno transakcijo in sledi privzetim nastavitvam glede na kategorijo transakcije za povezane dejanske vrednosti projekta.
    - Če je v dejanski vrednosti projekta nastavljena **Kategorija transakcije** in obstaja povezana **Kategorija projekta** v dani pravni osebi, kategorija sledi privzetim nastavitvam te kategorije projekta.
    - Če **Kategorija transakcije** v dejanski vrednosti projekta ni nastavljena, sistem uporablja vrednost v polju **Privzete kategorije projekta** na zavihku **Project Operations v storitvi Dynamics 365 Customer Engagement** na strani **Parametri upravljanja projektov in računovodstvo**.
  - Polje **Vir** predstavlja vir projekta, povezanega s to transakcijo. Vir se uporablja kot sklic na stranke v predlogah za račune projekta.
  - Polje **Menjalni tečaj** sledi privzetim navodilom možnosti **Menjalni tečaj valute**, nastavljene v aplikaciji Dynamics 365 Finance. Če nastavitev menjalnega tečaja manjka, periodični postopek **Uvoz iz pripravljanja** ne bo zabeležil zapisa v dnevnik in v dnevnik za izvedbo posla bo dodano sporočilo o napaki.
  - Polje **Lastnost vrstice** predstavlja vrsto obračunavanja v dejanskih vrednostih projekta. Preslikavi lastnosti vrstice in vrste obračunavanja sta določeni na zavihku **Project Operations v aplikaciji Dynamics 365 Customer Engagement** na strani **Parametri upravljanja projektov in računovodstvo**.

V vrsticah dnevnika integracij za Project Operations je mogoče posodobiti samo naslednje računovodske atribute:

- **Obračunavanje skupine prometnega davka** in **Obračunavanje skupine davka od prodaje izdelkov**
- **Finančne razsežnosti** (uporaba dejanja **Porazdelitev zneskov**)

Vrstice dnevnika integracij je mogoče izbrisati, vendar bodo vse neobjavljene vrstice znova vstavljene v dnevnik po ponovnem zagonu periodičnega postopka **Uvoz iz pripravljanja**.

Ko objavite dnevnik integracije, se ustvarijo transakcije podknjige in glavne knjige. Uporabljajo se pri izdajanju računov strankam, pripoznavanju prihodkov in finančnih poročil iz strežnika.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
