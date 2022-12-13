---
title: Prilagoditve projekta
description: Ta članek vsebuje informacije o prilagoditvah projekta.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788376"
---
# <a name="project-adjustments"></a>Prilagoditve projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

## <a name="adjustments-overview"></a>Pregled prilagoditev

Microsoft Dynamics 365 Project Operations lahko konfigurirate tako, da lahko uporabniki spreminjajo objavljene transakcije. Projektne transakcije lahko prilagodite posamično ali pa izberete več transakcij hkrati na seznamu vseh projektnih transakcij. Prilagoditve projekta se na primer uporabljajo za množično posodabljanje plačljivega statusa, ponovni izračun stroškov po spremembi konfiguracije ali posodobitev virov financiranja.

Uporabniki lahko dostopajo do funkcionalnosti prilagajanja projekta na več načinov:

- Z uporabo strani **Prilagodi transakcije**, do katere lahko dostopate iz  **Upravljanja projektov in računovodstva** \> **Nastavitev**.
- Z uporabo gumba **Prilagoditev** na strani **Objavljene transakcije projekta**, do katere lahko dostopate z  **Upravljanje projektov in računovodstvo** \> **Transakcije**.
- Z uporabo gumba **Prilagoditev** na strani **Objavljene transakcije projekta** v kontekstu projekta. Do te strani lahko dostopate iz **Upravljanje projektov in računovodstvo** \> **Vsi projekti**.

Če želite omogočiti prilagoditve, morate omogočiti enega ali več statusov transakcije iz **Upravljanje projektov in računovodstvo** \> **Upravljanje projektov in računovodski parametri** na **Zavihek Splošno** pod razdelkom **Dovoli prilagoditev stanja transakcije**. Primeri statusov transakcij vključujejo knjižene transakcije, fakturirane transakcije ali izločene transakcije. Vsako stanje transakcije, ki je nastavljeno na **Ne** bo imelo transakcije v tem statusu, ki ne bodo prikazane v postopku prilagajanja kot možnosti izbire za prilagoditev.

Konfiguracijska možnost z imenom **Vedno ustvari transakcijo prilagoditve** je trenutno na voljo v upravljanju projektov in računovodskih parametrih. To možnost lahko onemogočite, če želite posodobiti izvirno transakcijo, namesto da ustvarite nove transakcije med prilagajanjem v podnaboru scenarijev. Napovedano je bilo, da bo ta parameter opuščen do 1. marca 2023. Po 1. marcu 2023 se bo sistem vedno obnašal, kot da je možnost omogočena.

## <a name="adjustments-process-flow"></a>Potek postopka prilagoditev

Naslednji koraki prikazujejo tipičen tok za prilagoditve obdelave.

1. Odprite stran **Prilagoditve projekta** .
2. Izberite **Izberite** za iskanje transakcij, ki izpolnjujejo pričakovana merila za prilagoditev.
3. Na seznamu transakcij izberite vse transakcije ali podmnožico transakcij za prilagoditev.
4. Izberite **Prilagodi** in spremenite atribute v vrstici. Če so bile vrednosti med vnosom transakcije določene ročno, lahko izberete vnos privzetih sistemskih vrednosti.
5. Vrne se seznam transakcij in v stolpcu **Prilagoditev v teku** se prikaže kljukica, ki označuje, kje so bile narejene spremembe. Vse prilagoditve, ki imajo čakajoče spremembe, so prikazane v spodnji polovici strani. Tam lahko izvedete dodatne podrobne spremembe poleg tega, kar je bilo prikazano na prejšnji strani.
6. Izberite **Knjiži** za knjiženje transakcij popravkov.

Glede na konfiguracijo se za prilagoditev običajno ustvarijo nove transakcije.

- Polje **Status računa** izvirne transakcije je nastavljeno na **Prilagojeno**.
- Za razveljavitev prvotne transakcije se ustvari razveljavitvena transakcija, polje **Status** je nastavljeno na **Prilagojeno**.
- Ustvari se nova transakcija s spremembami, ki so bile narejene med postopkom prilagajanja.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Izbira več objavljenih projektnih transakcij hkrati za prilagoditve in dobropise

Nova funkcija, ki je bila predstavljena v izdaji 10.0.30, omogoča izbiro več transakcij za prilagoditev hkrati na strani **Objavljene transakcije projekta** .

Preden lahko uporabite to funkcijo, mora biti omogočena v vašem sistemu. Skrbniki lahko uporabijo  **delovni prostor za upravljanje funkcij**, da preverijo stanje funkcije in jo omogočijo, če je potrebna. V delovnem prostoru **Feature management** poiščite in izberite **Večkratna izbira objavljenih projektnih transakcij za prilagoditve in dobropise**, in nato izberite **Omogoči zdaj**.

Ta funkcija omogoča naslednje ključne funkcije:

- Do njega lahko dostopate s strani objavljene transakcije znotraj projekta z uporabo obstoječega gumba **Prilagoditev** .
- Omogoča nadzor izbire več vrstic na strani **Objavljene transakcije projekta** . Filtre lahko uporabite na strani s seznamom in izberete svoje zapise, preden začnete s prilagajanjem.
- Onemogoči gumb **Prilagoditev**, če posamezne transakcije ni mogoče prilagoditi ali če izberete kombinacijo dobropisov in dnevnikov skupaj namesto posamezno.
- Zaradi dodanega kontrolnika za izbiro več vrstic povezava **Committed cost** na traku ni več onemogočena, če je izbranih več vrstic.
- Doda naslednje opozorilno sporočilo: »Izbrali ste več kot (izbrano število) zapisov za prilagoditev. Nadaljevanje tega dejanja lahko traja nekaj časa. Ali ste prepričani, da želite nadaljevati s tem dejanjem?"

Ta funkcija tudi odstrani 2. korak iz poteka procesa, ki je bil opisan prej v tem članku. Zato bodo vse transakcije, ki so bile izbrane, preden je bila odprta stran **Prilagodi transakcije**, vključene na seznam transakcij za prilagoditev. Za iskanje vam ni treba uporabiti gumba **Izberi** .

> [!NOTE] 
> Tudi če je ta funkcija onemogočena, lahko še vedno izberete več zapisov za prilagoditev. Vendar pa bo *ostal izbran* samo en zapis in pogovorno okno **Izberi transakcije** se bo prikazalo takoj, ko izberete odprte prilagoditve.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Statusi transakcij prilagoditev, ki jih je mogoče omogočiti ali onemogočiti za prilagoditve

Naslednje statuse lahko omogočite ali onemogočite na zavihku **Splošno** strani **Upravljanje projekta in računovodski parametri** :

- Objavljeno
- Predloge računov
- Fakturirano
- Predvideno
- Odpravljeno
- Začetno stanje (ura)

## <a name="adjustment-parameters"></a>Prilagoditveni parametri

Ti parametri so navedeni na strani  **Upravljanje projekta in računovodski parametri** na  **zavihku Splošno** pod **Adjustment** skupina in bo spremenila vedenje za način obdelave prilagoditev. 

| Ime parametra | Description |
|----------------|-------------
| Vedno ustvarite prilagoditveno transakcijo | Če je ta parameter omogočen, bo postopek prilagajanja vedno ustvaril novo razveljavitev transakcije in novo prilagojeno transakcijo, ko pride do finančnega vpliva ali vpliva na poročanje. Če je parameter onemogočen, bo postopek prilagoditve posodobil izvirno transakcijo, namesto da bi ustvaril razveljavitev in novo transakcijo za scenarij, kot je posodobitev besedila transakcije. |
| Polje za samodejno posodabljanje | Če je ta parameter omogočen, bo sistem preračunal lastno ceno in prodajno ceno. |
| Uporabite datum prilagoditve kot nov projekt | Ta parameter se uporablja za premikanje transakcij v prihodnji proračunsko obodbje, preden je sistem podpiral to funkcijo. Ne priporočamo, da ga uporabljate, ker spremeni poslovni datum transakcije in bo v prihodnji izdaji opuščen. |
| Dovoli zaprte dejavnosti | Običajno transakcij ni mogoče ustvariti za zaprte dejavnosti. Če je ta parameter omogočen, je to vedenje preglaseno. Zato je mogoče ustvariti prilagoditve za zaprte dejavnosti. |
