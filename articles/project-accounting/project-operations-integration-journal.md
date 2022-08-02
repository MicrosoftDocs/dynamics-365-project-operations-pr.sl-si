---
title: Dnevnik integracij v aplikaciji Project Operations
description: Ta članek nudi informacije o delu z dnevnikom Integration v Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106295"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracij v aplikaciji Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ustvarjanje vnosov časa, stroškov, honorarjev in materiala **Dejansko** transakcije, ki predstavljajo operativni pogled na opravljeno delo glede na projekt. Aplikacija Dynamics 365 Project Operations računovodjam zagotavlja orodje za pregled transakcij in prilagoditev računovodskih atributov. Po zaključku pregleda in prilagoditev se transakcije zabeležijo v podknjigo in glavno knjigo projekta. Računovodja lahko te dejavnosti izvaja z uporabo **Integracija projektnih operacij** dnevnik (**Dynamics 365 Finance** > **Vodenje projektov in računovodstvo** > **Dnevniki** > **Integracija projektnih operacij** dnevnik.

![Potek dnevnika integracij.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Ustvarjanje zapisov v dnevniku integracij za Project Operations

Zapisi v dnevniku integracij za Project Operations so ustvarjeni s periodičnim postopkom **Uvoz iz pripravljalne tabele**. Ta postopek lahko zaženete tako, da obiščete **Dynamics 365 Finance** > **Vodenje projektov in računovodstvo** > **Periodično** > **Integracija projektnih operacij** > **Uvoz iz uprizoritvene tabele**. Proces lahko zaženete interaktivno ali ga po potrebi konfigurirate tako, da se izvaja v ozadju.

Ko se periodični postopek zažene, so najdene vse dejanske vrednosti, ki še niso dodane v dnevnik integracij za Project Operations. Ustvari se vrstica dnevnika za vsako dejansko transakcijo.
Sistem združuje vrstice temeljnic v ločene temeljnice na podlagi vrednosti, izbrane v **Enota obdobja v dnevniku integracije projektnih operacij** polje (**Finance** > **Vodenje projektov in računovodstvo** > **Nastaviti** > **Projektno vodenje in računovodski parametri**, **operacije na Dynamics 365 Customer Engagement** zavihek). Možne vrednosti za to polje vključujejo:

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
    - če **Kategorija transakcije** ni nastavljen v dejanskem projektu, sistem uporabi vrednost v **Privzete kategorije projektov** polje na **Projektne operacije na Dynamics 365 Customer Engagement** zavihek na **Projektno vodenje in računovodski parametri** strani.
  - Polje **Vir** predstavlja vir projekta, povezanega s to transakcijo. Vir se uporablja kot sklic na stranke v predlogah za račune projekta.
  - The **Menjalni tečaj** polje privzeto od **Menjalni tečaj** nastavite v Dynamics 365 Finance. Če nastavitev menjalnega tečaja manjka, periodični postopek **Uvoz iz pripravljanja** ne bo zabeležil zapisa v dnevnik in v dnevnik za izvedbo posla bo dodano sporočilo o napaki.
  - Polje **Lastnost vrstice** predstavlja vrsto obračunavanja v dejanskih vrednostih projekta. Lastnost linije in preslikava vrste zaračunavanja sta definirana na **Projektne operacije na Dynamics 365 Customer Engagement** zavihek na **Projektno vodenje in računovodski parametri** strani.

V vrsticah dnevnika integracij za Project Operations je mogoče posodobiti samo naslednje računovodske atribute:

- **Obračunavanje skupine prometnega davka** in **Obračunavanje skupine davka od prodaje izdelkov**
- **Finančne razsežnosti** (uporaba dejanja **Porazdelitev zneskov**)

Vrstice dnevnika integracije je mogoče izbrisati. Vse neobjavljene vrstice pa bodo znova vstavljene v dnevnik, ko znova zaženete **Uvoz iz uprizoritve** periodični proces.

### <a name="post-the-project-operations-integration-journal"></a>Objavite integracijski dnevnik projektnih operacij

Ko objavite dnevnik integracije, se ustvarijo transakcije podknjige in glavne knjige. Uporabljajo se pri izdajanju računov strankam, pripoznavanju prihodkov in finančnih poročil iz strežnika.

Izbrani dnevnik integracije projektnih operacij je mogoče objaviti z uporabo **Objavi** na strani dnevnika integracije Project Operations. Vse dnevnike je mogoče samodejno objaviti z izvajanjem postopka na **Periodika** > **Integracija projektnih operacij** > **Dnevnik integracije po projektnih operacijah**.

Knjiženje se lahko izvaja interaktivno ali v paketu. Upoštevajte, da bodo vse revije, ki imajo več kot 100 vrstic, samodejno objavljene v paketu. Za boljšo zmogljivost, ko so dnevniki, ki imajo veliko vrstic, objavljeni v paketu, omogočite **Post Project Operations integracijski dnevnik z uporabo več paketnih opravil** funkcija v **Upravljanje funkcij** delovni prostor. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Prenesite vse vrstice z napakami pri knjiženju v nov dnevnik

> [!NOTE]
> Če želite uporabiti to možnost, omogočite **Prenesite vse vrstice z napakami pri knjiženju v nov dnevnik integracije Project Operations** funkcija v **Upravljanje funkcij** delovni prostor.

Med objavljanjem v integracijski dnevnik Project Operations sistem preveri vsako vrstico v dnevniku. Sistem knjiži vse vrstice, ki nimajo napak, in ustvari nov dnevnik za vse vrstice, ki imajo napake pri knjiženju. Če želite pregledati dnevnike, ki imajo vrstice napak pri knjiženju, pojdite na **Vodenje projektov in računovodstvo** > **Dnevniki** > **Dnevnik integracije projektnih operacij** in filtrirajte dnevnike z uporabo **Izvirni dnevnik** polje.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
