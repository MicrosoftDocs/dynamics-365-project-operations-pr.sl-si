---
title: Mobilna aplikacija za upravljanje stroškov
description: Ta članek vsebuje informacije o mobilnem delovnem prostoru za upravljanje stroškov.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ba7ccae04fbb02252e3ceb01f123ce1e85375b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930246"
---
# <a name="mobile-expense-app"></a>Mobilna aplikacija za upravljanje stroškov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ta članek vsebuje informacije o **Upravljanje odhodkov** mobilni delovni prostor. Ta delovni prostor omogoča uporabnikom, da zajamejo in naložijo potrdilo, da ga lahko pozneje priložijo poročilu o stroških. Uporabniki lahko tudi hitro ustvarijo vrstico stroškov z uporabo priloženega potrdila ter ustvarijo in upravljajo svoja poročila o stroških. Poleg tega lahko odobritelji uporabljajo mobilni delovni prostor **Upravljanje stroškov**, da si ogledajo poročila o stroških, ki so jim dodeljena, in jih odobrijo ali zavrnejo.

Ta mobilni delovni prostor je namenjen uporabi z mobilno aplikacijo Dynamics 365 Unified Ops.

Številne organizacije zahtevajo, da se kopija potrdila priloži poročilu o stroških, povezanih s potovanjem ali poslovanjem, ki ga zaposleni predloži v povračilo. Mobilni delovni prostor **Upravljanje stroškov** uporabnikom omogoča hitro ustvarjanje novih vrstic stroškov na mobilni napravi po lastni izbiri z uporabo priložene fotografije potrdila. Druga možnost je, da uporabniki fotografijo potrdila zajamejo in nato pozneje priložijo poročilu o stroških. Zaposleni lahko tudi ustvarijo in upravljajo svoja poročila o stroških ter jih nato z uporabo mobilne naprave predložijo v odobritev in povračilo.

Natančneje, mobilni delovni prostor **Upravljanje stroškov** uporabnikom omogoča izvajanje teh opravil:

- Snemanje fotografije potrdila. Nalaganje fotografije potrdila in pozneje priložitev k poročilu o stroških.
- Nalaganje datoteke kot zajeto potrdilo. Nato lahko to datoteko pozneje priložite k poročilu o stroških.
- Ustvarjanje nove vrstice stroška z uporabo priloženega potrdila. Nato lahko postavko vrstice pozneje dodate v poročilo o stroških ter ga predložite v odobritev in povračilo.

Uporabite lahko tudi te funkcije:

- Ustvarjanje novega poročila o stroških.
- Prilaganje transakcij kreditne kartice in drugih prej ustvarjenih stroškov v poročilo o stroških.
- Ustvarjanje novih stroškov za poročilo o stroških.
- Prilaganje potrdila kateremu koli strošku za poročilo o stroških, bodisi s fotografiranjem potrdila ali nalaganjem datoteke kot zajeto potrdilo.
- Odvisno od politike podjetja glede stroškov dodajte seznam gostov strošku.
- Odvisno od politike podjetja glede stroškov razčlenite stroške.
- Predložite poročilo o stroških v odobritev in povračilo.
- Odobrite ali zavrnite poročila o stroških, za katere ste dodeljeni odobritelj.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Predpogoji, če uporabljate Dynamics 365 Finance

Če je bila za vašo organizacijo uvedena rešitev Finance, mora skrbnik sistema objaviti mobilni delovni prostor **Upravljanje stroškov**. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Prenos in namestitev mobilne aplikacije Dynamics 365 Unified Ops
Prenos in namestitev mobilne aplikacije Dynamics 365 Unified Ops:

- [Za telefone s sistemom Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Za naprave iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijavite se v mobilno aplikacijo
1. Zaženite aplikacijo v mobilni napravi.
2. Vnesite URL za Dynamics 365.
4. Ko se prvič prijavite, boste pozvani k vnosu uporabniškega imena in gesla. Vnesite svoje poverilnice.
5. Po prijavi se prikažejo razpoložljivi delovni prostori za vaše podjetje. Če skrbnik sistema pozneje objavi nov delovni prostor, boste morali osvežiti seznam mobilnih delovnih prostorov.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zajemite račun s pomočjo mobilnega delovnega prostora za upravljanje stroškov

1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. Izberite **Zajem potrdila**.
3. Izberite **Fotografiraj** ali **Izbira slike**.
4. Sledite enemu od teh postopkov:

    - Če ste izbrali **Fotografiraj**, sledite tem korakom:

        1. Odprla se bo kamera v vaši mobilni napravi, da boste lahko fotografirali potrdilo. 
        2. Ko končate s fotografiranjem, izberite **V redu**, da sprejmete fotografijo.
        3. Izbirno: Vnesite ime fotografije in vnesite morebitne opombe.

    - Če ste izbrali **Izbira slike**, sledite tem korakom:

        1. Izberite sliko s seznama.
        2. Izbirno: Vnesite ime slike in vnesite morebitne opombe.

5. Izberite **Dokončano**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Hitro vnesite strošek s pomočjo mobilnega delovnega prostora za upravljanje stroškov

1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. Izberite **Hiter vnos stroška**.
3. Izberite kategorijo stroška. Videli boste seznam kategorij stroškov, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če vaše kategorije ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po kategoriji stroškov ali preklopite na iskanje po vrsti stroška.
4. Vnesite datum transakcije stroška.
5. Izbirno: Vpišite trgovca za strošek.
6. Vnesite znesek stroška.
7. Izberite valuto stroška. Videli boste seznam kod valut, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 400 valut, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če vaše valute ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po valuti ali preklopite na iskanje po imenu.
8. Izberite **Fotografiraj** ali **Izbira slike**.
9. Sledite enemu od teh postopkov:

    - Če ste izbrali **Fotografiraj**, se bo odprla kamera v vaši mobilni napravi, da boste lahko fotografirali potrdilo. Ko končate s fotografiranjem, izberite **V redu**, da sprejmete fotografijo.
    - Če ste izbrali **Izbira slike**, izberite sliko na seznamu.

10. Izberite **Dokončano**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Odobrite poročilo o stroških z uporabo mobilnega delovnega prostora za upravljanje stroškov

1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. **Odobritve stroškov** prikazuje število poročil o stroških, ki so vam dodeljena v odobritev. Številka se posodobi približno vsakih 30 minut. Izberite **Odobritve stroškov**.

    Prikazan je seznam poročil o stroških, ki so vam dodeljena v odobritev.

3. Izberite poročilo o stroških, da si zanj ogledate podrobnosti o stroških.
4. Izberite strošek, da si zanj ogledate podrobnosti. Informacije, ki so prikazane za strošek, vključujejo podrobnosti o potrdilu, gostu in razčlenitvi.
5. Nazaj na strani **Poročilo o stroških** izberite odobritev ali zavrnitev poročila o stroških.
6. Vnesite morebitne opombe za dejanje odobritve.
7. Izberite **Dokončano**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Ustvarite novo poročilo o stroških in ga oddajte v odobritev z uporabo mobilnega delovnega prostora za upravljanje stroškov

1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. Izberite **Vnos stroška**.
3. Izberite **Novo poročilo** ali izberite obstoječe poročilo o stroških na seznamu.
4. Za nova poročila o stroških vnesite namen in morebitne dodatne informacije, ki so na voljo. Te informacije se razlikujejo, odvisno od načina, kako je za vaše podjetje konfigurirano upravljanje stroškov.
5. Izberite **Dokončano**.
6. Če želite poročilu o stroških dodati obstoječe stroške, na primer transakcije s kreditnimi karticami, izberite **Priloži**.
7. Na seznamu izberite enega ali več stroškov.
8. Izberite **Dokončano**.
9. Če želite poročilu o stroških dodati nove stroške, izberite **Nov strošek**.
10. Izberite kategorijo za strošek. Videli boste seznam kategorij stroškov, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če vaše kategorije ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po kategoriji stroškov ali preklopite na iskanje po vrsti stroška.
11. Izbirno: Vpišite trgovca za strošek.
12. Vnesite datum transakcije stroška.
13. Vnesite znesek stroška.
14. Izberite valuto stroška. Videli boste seznam kod valut, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 400 valut, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če vaše valute ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po valuti ali preklopite na iskanje po imenu.
15. Izberite **Dokončano**.
16. Če želite strošku dodati več podrobnosti, izberite **Dodaj več podrobnosti**. Polja, ki so na voljo, so odvisna od konfiguracije upravljanja stroškov za vaše podjetje.
17. Če je s politiko podjetja zahtevano potrdilo za strošek, izberite **Potrdila**, nato pa sledite tem korakom:

    1. Izberite **Zajemi potrdilo** ali **Priloži potrdilo**.
    2. Sledite enemu od teh postopkov:

        - Če ste izbrali **Zajemi potrdilo**, sledite tem korakom:

            1. Izberite **Fotografiraj** ali **Izbira slike**.
            2. Sledite enemu od teh postopkov:

                - Če ste izbrali **Fotografiraj**, sledite tem korakom:

                    1. Odprla se bo kamera v vaši mobilni napravi, da boste lahko fotografirali potrdilo. Ko končate s fotografiranjem, izberite **V redu**, da sprejmete fotografijo.
                    2. Izbirno: Vnesite ime fotografije in vnesite morebitne opombe.

                - Če ste izbrali **Izbira slike**, sledite tem korakom:

                    1. Izberite sliko s seznama.
                    2. Izbirno: Vnesite ime slike in vnesite morebitne opombe.

            3. Izberite **Dokončano**.

        - Če ste izbrali **Priloži potrdilo**, sledite tem korakom:

            1. Izberite eno ali več slik na seznamu.
            2. Izberite **Dokončano**.

    3. Izberite gumb **Nazaj** za vrnitev na podrobnosti o stroških.

18. Če so s politiko podjetja zahtevani gosti za strošek, izberite **Gosti**, nato pa sledite tem korakom:

    1. Izberite **Gost**, **Prejšnji gostje** ali **Sodelavci**.
    2. Sledite enemu od teh postopkov:

        - Če ste izbrali **Gost**, sledite tem korakom:

            1. Vnesite ime gosta.
            2. Izbirno: vnesite organizacijo in/ali državo gosta.
            3. Izbirno: vnesite naziv gosta.
            4. Izberite **Dokončano**.

        - Če ste izbrali **Prejšnji gostje**, sledite tem korakom:

            1. Na seznamu izberite enega ali več prejšnjih gostov. Prikaže se seznam prejšnjih gostov, ki ste jih dodali v prejšnja poročila o stroških, ki so naloženi v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če vaš prejšnji gost ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po imenu ali preklopite na iskanje po organizaciji, državi ali nazivu.
            2. Izberite **Dokončano**.

        - Če ste izbrali **Sodelavci**, sledite tem korakom:

            1. Na seznamu izberite enega ali več sodelavcev. Videli boste seznam sodelavcev, ki so naloženi v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če sodelavca ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po imenu ali preklopite na iskanje po podjetju ali nazivu.
            2. Izberite **Dokončano**.

    3. Izberite gumb **Nazaj** za vrnitev na podrobnosti o stroških.

19. Če je s politiko podjetja zahtevana razčlenitev stroška, izberite **Razčleni**, nato pa sledite tem korakom:

    1. Izberite prvi datum za razčlenitev.
    2. Izberite **Dodaj razčlenitev**.
    3. Izberite podkategorijo za razčlenitev stroška. Videli boste seznam podkategorij stroškov, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Če vaše podkategorije ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iskanje po imenu podkategorije stroškov.
    4. Vnesite znesek transakcije za razčlenitev.
    5. Uredite datum transakcije, če je potrebno.
    6. Izberite **Dokončano**.
    7. Ponavljajte prejšnje korake, dokler ne dokončate dodajanja vseh razčlenitev za izbrani datum.
    8. Za dodatne dni lahko izberete **Kopiraj na naslednji dan**, da kopirate razčlenitve na naslednji dan. Lahko pa izberete datum za razčlenitev in nato dodate razčlenitve, kot ste storili za prvi datum.
    9. Ko končate z razčlenitvijo stroškov, izberite gumb **Nazaj** za vrnitev na podrobnosti o stroških.

20. Izberite gumb **Nazaj** za vrnitev na stran **Poročilo o stroških**.
21. Ponavljajte prejšnje korake, dokler ne končate z dodajanjem vseh stroškov.
22. Izberite **Pošlji**.
23. Vnesite morebitne opombe za odobritelja.
24. Izberite **Dokončano**.

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Zakaj mobilna aplikacija Expense privzeto ne vnese plačilnega sredstva?

Organizacije lahko prilagodijo **Privzeto plačilno sredstvo** nastavitev za vsako kategorijo stroškov, ko je ustvarjena. Poleg tega lahko, ko nastavite plačilna sredstva, nastavite **Privzeto plačilno sredstvo** polje do **Samo uvoz**.

Kdaj **Samo uvoz** je omogočeno za plačilno sredstvo, plačilno sredstvo ni privzeto vneseno. V kategorijah stroškov, kjer je to plačilno sredstvo nastavljeno, bo prazno. To vedenje je skladno tako v spletni izkušnji kot v mobilni izkušnji.
    
Kdaj **Samo uvoz** ni omogočena za plačilno sredstvo, je nastavljena vrednost privzeto vpisana za kategorije odhodkov, kjer je to plačilno sredstvo nastavljeno. Vendar pa je znana težava, pri kateri privzeta vrednost ni vnesena v mobilno aplikacijo Expense. Če želite odpraviti to težavo, ročno izberite plačilno sredstvo, preden shranite poročilo o stroških. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Zakaj ne morem dodati ali urediti finančnih razsežnosti v mobilni aplikaciji Expense?

Vnos dimenzij in distribucij ni podprt. Če želite premagati to omejitev, lahko ta polja privzeto nastavite v mobilni aplikaciji, tako da nastavite privzete finančne razsežnosti na projekt ali zaposlenega.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Zakaj včasih vidim napako pri sinhronizaciji v mobilni aplikaciji Expense?

Če vrstice stroškov ne izpolnjujejo zahtev pravilnika in uporabnik predloži poročilo o stroških, ne da bi obravnaval opozorilo pravilnika, se mobilni podatki ne sinhronizirajo s strežnikom in pride do napake pri sinhronizaciji. Vsa poročila o stroških, ki so poslana po tem, ko pride do napake pri sinhronizaciji, bodo ostala v neuspešnem stanju in povzročila več napak pri sinhronizaciji. Edini način za odpravo te situacije je, da ročno izbrišete obvestila o sinhronizaciji. To težavo smo odpravili tako, da smo ustavili predložitev poročil o stroških, ko opozorila pravilnika niso bila obravnavana, da bi se izognili napakam pri sinhronizaciji.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Zakaj se validacija projekta in kategorije v mobilni aplikaciji Expense ne odraža pravilno?

Ta potrditev trenutno ni podprta. Vendar pa bo podpora morda dodana v prihodnosti. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Katere vrste dokumentov so podprte v mobilni aplikaciji Expense?

Mobilna aplikacija Expense podpira samo slike. Trenutno ne podpira datotek PDF ali drugih dokumentov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
