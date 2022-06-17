---
title: Dnevnik integracij v aplikaciji Project Operations
description: Ta članek vsebuje informacije o delu z revijo Integration v Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: befb1756ad77708805f3cbb06168b93e44296df0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923898"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracij v aplikaciji Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Vnosi časa in stroškov ustvarijo **Dejanske** transakcije, ki predstavljajo operativni pogled na delo, opravljenega v zvezi s projektom. Aplikacija Dynamics 365 Project Operations računovodjam zagotavlja orodje za pregled transakcij in prilagoditev računovodskih atributov. Po zaključku pregleda in prilagoditev se transakcije zabeležijo v podknjigo in glavno knjigo projekta. Računovodja lahko te dejavnosti izvaja z uporabo **Integracija projektnih operacij** dnevnik (**Dynamics 365 Finance** > **Vodenje projektov in računovodstvo** > **Časopisi** > **Integracija projektnih operacij** dnevnik.

![Potek dnevnika integracij.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Ustvarjanje zapisov v dnevniku integracij za Project Operations

Zapisi v dnevniku integracij za Project Operations so ustvarjeni s periodičnim postopkom **Uvoz iz pripravljalne tabele**. Ta postopek lahko zaženete tako, da obiščete **Dynamics 365 Finance** > **Vodenje projektov in računovodstvo** > **Periodično** > **Integracija projektnih operacij** > **Uvoz iz uprizoritvene tabele**. Proces lahko zaženete interaktivno ali ga po potrebi konfigurirate tako, da se izvaja v ozadju.

Ko se periodični postopek zažene, so najdene vse dejanske vrednosti, ki še niso dodane v dnevnik integracij za Project Operations. Ustvari se vrstica dnevnika za vsako dejansko transakcijo.
Sistem razvrsti vrstice dnevnika v ločene dnevnike na podlagi vrednosti, izbrane v **Enota obdobja v reviji Project Operations Integration** polje (**finance** > **Vodenje projektov in računovodstvo** > **Nastaviti** > **Vodenje projektov in računovodski parametri**, **projekta na Dynamics 365 Customer Engagement** zavihek). Možne vrednosti za to polje vključujejo:

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
    - Če **Kategorija transakcije** ni nastavljena v projektu Dejanski, sistem uporablja vrednost v **Privzete nastavitve kategorije projekta** polje na **Operacije projekta na Dynamics 365 Customer Engagement** zavihek na **Vodenje projektov in računovodski parametri** stran.
  - Polje **Vir** predstavlja vir projekta, povezanega s to transakcijo. Vir se uporablja kot sklic na stranke v predlogah za račune projekta.
  - The **Menjalni tečaj** polje privzeto od **Menjalni tečaj** nastavljeno v Dynamics 365 Finance. Če nastavitev menjalnega tečaja manjka, periodični postopek **Uvoz iz pripravljanja** ne bo zabeležil zapisa v dnevnik in v dnevnik za izvedbo posla bo dodano sporočilo o napaki.
  - Polje **Lastnost vrstice** predstavlja vrsto obračunavanja v dejanskih vrednostih projekta. Lastnost vrstice in preslikava vrste obračunavanja sta definirana na **Operacije projekta na Dynamics 365 Customer Engagement** zavihek na **Vodenje projektov in računovodski parametri** stran.

V vrsticah dnevnika integracij za Project Operations je mogoče posodobiti samo naslednje računovodske atribute:

- **Obračunavanje skupine prometnega davka** in **Obračunavanje skupine davka od prodaje izdelkov**
- **Finančne razsežnosti** (uporaba dejanja **Porazdelitev zneskov**)

Vrstice dnevnika integracij je mogoče izbrisati, vendar bodo vse neobjavljene vrstice znova vstavljene v dnevnik po ponovnem zagonu periodičnega postopka **Uvoz iz pripravljanja**.

Ko objavite dnevnik integracije, se ustvarijo transakcije podknjige in glavne knjige. Uporabljajo se pri izdajanju računov strankam, pripoznavanju prihodkov in finančnih poročil iz strežnika.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
