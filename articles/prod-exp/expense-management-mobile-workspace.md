---
title: Mobilni delovni prostor za upravljanje stroškov
description: Ta tema vsebuje informacije o mobilnem delovnem prostoru »Upravljanje stroškov«. Ta delovni prostor omogoča uporabnikom, da zajamejo in naložijo potrdilo, da ga lahko pozneje priložijo poročilu o stroških. Uporabniki lahko tudi hitro ustvarijo vrstico stroškov z uporabo priloženega potrdila ter ustvarijo in upravljajo svoja poročila o stroških.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc19297131937949fe6f7eed00ee66fb5e3bff13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950499"
---
# <a name="expense-management-mobile-workspace"></a>Mobilni delovni prostor za upravljanje stroškov

Ta tema vsebuje informacije o mobilnem delovnem prostoru **Upravljanje stroškov**. Ta delovni prostor omogoča uporabnikom, da zajamejo in naložijo potrdilo, da ga lahko pozneje priložijo poročilu o stroških. Uporabniki lahko tudi hitro ustvarijo vrstico stroškov z uporabo priloženega potrdila ter ustvarijo in upravljajo svoja poročila o stroških. Poleg tega lahko odobritelji uporabljajo mobilni delovni prostor **Upravljanje stroškov**, da si ogledajo poročila o stroških, ki so jim dodeljena, in jih odobrijo ali zavrnejo.


Ta mobilni delovni prostor je namenjen uporabi z mobilno aplikacijo Dynamics 365 Unified Ops.


## <a name="overview"></a>Pregled

Številne organizacije zahtevajo, da se kopija potrdila priloži poročilu o stroških, povezanih s potovanjem ali poslovanjem, ki ga zaposleni predloži v povračilo. Mobilni delovni prostor **Upravljanje stroškov** uporabnikom omogoča hitro ustvarjanje novih vrstic stroškov na mobilni napravi po lastni izbiri z uporabo priložene fotografije potrdila. Druga možnost je, da uporabniki fotografijo potrdila zajamejo in nato pozneje priložijo poročilu o stroških. Zaposleni lahko tudi ustvarijo in upravljajo svoja poročila o stroških ter jih nato z uporabo mobilne naprave predložijo v odobritev in povračilo.


Natančneje, mobilni delovni prostor **Upravljanje stroškov** uporabnikom omogoča izvajanje teh opravil:

- Fotografirajte račun in ga naložite v Dynamics 365 Finance. To fotografijo lahko pozneje priložite k poročilu o stroških.
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

## <a name="prerequisites"></a>Zahteve
Predpogoji se razlikujejo glede na različico, ki je uvedena za organizacijo.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Predpogoji, če uporabljate Dynamics 365 Finance 
Če je bila za vašo organizacijo uvedena rešitev Finance, mora skrbnik sistema objaviti mobilni delovni prostor **Upravljanje stroškov**. Za navodila glejte [Objava mobilnih delovnih prostorov](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Predpogoji, če uporabljate različico 1611 s posodobitvijo platforme na 3 ali novejšo
Če je bila za vašo organizacijo uvedena različica 1611 s posodobitvijo platforme na 3 ali novejšo, mora sistemski skrbnik izpolniti naslednje predpogoje. 

<table>
<thead>
<tr class="header">
<th>Predpogoj</th>
<th>Vloga</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uvedba hitrega popravka KB 4019015.</td>
<td>Skrbnik sistema</td>
<td>KB 4019015 je posodobitev X ++ ali hitri popravek za metapodatke, ki vsebuje mobilni delovni prostor za <strong>Upravljanje stroškov</strong>. Za uvedbo hitrega popravka KB 4019015 v sistem mora skrbnik sistema upoštevati naslednje korake.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Prenos hitrega popravka za metapodatke iz portala Lifecycle Services (LCS) storitve Microsoft Dynamics</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Namestitev hitrega popravka za metapodatke</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Ustvarjanje paketa za uvajanje</a> z modeloma <strong>ApplicationSuite</strong> in <strong>ExpenseMobile</strong>, ki ga nato naložite na portal LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Uporaba paketa za uvajanje</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Objava mobilnega delovnega prostora <strong>Upravljanje stroškov</strong>.</td>
<td>Skrbnik sistema</td>
<td>Glejte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Objava mobilnega delovnega prostora</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Prenos in namestitev mobilne aplikacije Dynamics 365 for Operations
Prenos in namestitev mobilne aplikacije Dynamics 365 Unified Ops:

- [Za telefone s sistemom Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Za naprave iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijavite se v mobilno aplikacijo
1. Zaženite aplikacijo v mobilni napravi.
2. Vnesite URL za Dynamics 365.
4. Ko se prvič prijavite, boste pozvani k vnosu uporabniškega imena in gesla. Vnesite svoje poverilnice.
5. Po prijavi se prikažejo razpoložljivi delovni prostori za vaše podjetje. Če skrbnik sistema pozneje objavi nov delovni prostor, boste morali osvežiti seznam mobilnih delovnih prostorov.


[![Povlecite za osvežitev](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zajemite račun s pomočjo mobilnega delovnega prostora za upravljanje stroškov

1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. Izberite **Zajem potrdila**.
3. Izberite **Fotografiraj** ali **Izbira slike**.
4. Sledite enemu od teh postopkov:

    - Če ste izbrali **Fotografiraj**, sledite tem korakom:

        1. Odprla se bo kamera v vaši mobilni napravi, da boste lahko fotografirali potrdilo. Ko končate s fotografiranjem, izberite **V redu**, da sprejmete fotografijo.
        2. Izbirno: Vnesite ime fotografije in vnesite morebitne opombe.

    - Če ste izbrali **Izbira slike**, sledite tem korakom:

        1. Izberite sliko s seznama.
        2. Izbirno: Vnesite ime slike in vnesite morebitne opombe.

5. Izberite **Dokončano**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Hitro vnesite strošek s pomočjo mobilnega delovnega prostora za upravljanje stroškov
1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. Izberite **Hiter vnos stroška**.
3. Izberite kategorijo za strošek. Videli boste seznam kategorij stroškov, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če vaše kategorije ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po kategoriji stroškov ali preklopite na iskanje po vrsti stroška.
4. Vnesite datum transakcije stroška.
5. Izbirno: Vpišite trgovca za strošek.
6. Vnesite znesek stroška.
7. Izberite valuto stroška. Videli boste seznam kod valut, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 400 valut, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če vaše valute ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po valuti ali preklopite na iskanje po imenu.
8. Izberite **Fotografiraj** ali **Izbira slike**.
9. Sledite enemu od teh postopkov:

    - Če ste izbrali **Fotografiraj**, se bo odprla kamera v vaši mobilni napravi, da boste lahko fotografirali potrdilo. Ko končate s fotografiranjem, izberite **V redu**, da sprejmete fotografijo.
    - Če ste izbrali **Izbira slike**, izberite sliko na seznamu.

10. Izberite **Dokončano**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Odobrite poročilo o stroških z uporabo mobilnega delovnega prostora za upravljanje stroškov (če uporabljate posodobitev iz julija 2017)
1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. **Odobritve stroškov** prikazuje število poročil o stroških, ki so vam dodeljena v odobritev. Številka se posodobi približno vsakih 30 minut. Izberite **Odobritve stroškov**.

    Prikazan je seznam poročil o stroških, ki so vam dodeljena v odobritev.
    
3. Izberite poročilo o stroških, da si zanj ogledate podrobnosti o stroških.
4. Izberite strošek, da si zanj ogledate podrobnosti. Informacije, ki so prikazane za strošek, vključujejo podrobnosti o potrdilu, gostu in razčlenitvi.
5. Nazaj na strani **Poročilo o stroških** izberite odobritev ali zavrnitev poročila o stroških.
6. Vnesite morebitne opombe za dejanje odobritve.
7. Izberite **Dokončano**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Ustvarite novo poročilo o stroških in ga predložite v odobritev z uporabo mobilnega delovnega prostora za upravljanje stroškov (če uporabljate posodobitev iz julija 2017)
1. V mobilni napravi odprite delovni prostor **Upravljanje stroškov**.
2. Izberite **Vnos stroška**.
3. Izberite **Novo poročilo** ali izberite obstoječe poročilo o stroških na seznamu.
4. Za nova poročila o stroških vnesite namen in morebitne dodatne informacije, ki so na voljo. Te informacije se razlikujejo, odvisno od načina, kako je za vaše podjetje konfigurirano upravljanje stroškov.
5. Izberite **Dokončano**.
6. Če želite poročilu o stroških dodati obstoječe stroške, na primer transakcije s kreditnimi karticami, izberite **Priloži**.
7. Na seznamu izberite enega ali več stroškov.
8. Izberite **Dokončano**.
9. Če želite poročilu o stroških dodati nove stroške, izberite **Nov strošek**.
10. Izberite kategorijo za strošek. Videli boste seznam kategorij stroškov, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če vaše kategorije ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po kategoriji stroškov ali preklopite na iskanje po vrsti stroška.
11. Izbirno: Vpišite trgovca za strošek.
12. Vnesite datum transakcije stroška.
13. Vnesite znesek stroška.
14. Izberite valuto stroška. Videli boste seznam kod valut, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 400 valut, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če vaše valute ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po valuti ali preklopite na iskanje po imenu.
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

            3.  Izberite **Dokončano**.

        - Če ste izbrali **Priloži potrdilo**, sledite tem korakom:

            1.  Izberite eno ali več slik na seznamu.
            2.  Izberite **Dokončano**.

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

            1. Na seznamu izberite enega ali več prejšnjih gostov. Prikaže se seznam prejšnjih gostov, ki ste jih dodali v prejšnja poročila o stroških, ki so naloženi v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če vaš prejšnji gost ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po imenu ali preklopite na iskanje po organizaciji, državi ali nazivu.
            2. Izberite **Dokončano**.

        - Če ste izbrali **Sodelavci**, sledite tem korakom:

            1. Na seznamu izberite enega ali več sodelavcev. Videli boste seznam sodelavcev, ki so naloženi v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če sodelavca ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iščite po imenu ali preklopite na iskanje po podjetju ali nazivu.
            2. Izberite **Dokončano**.

    3. Izberite gumb **Nazaj** za vrnitev na podrobnosti o stroških.

19. Če je s politiko podjetja zahtevana razčlenitev stroška, izberite **Razčleni**, nato pa sledite tem korakom:

    1. Izberite prvi datum za razčlenitev.
    2. Izberite **Dodaj razčlenitev**.
    3. Izberite podkategorijo za razčlenitev stroška. Videli boste seznam podkategorij stroškov, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Za več informacij naj razvijalci preberejo razdelek [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Če vaše podkategorije ni na seznamu, izberite **Iskanje**, da izvedete spletno iskanje. Iskanje po imenu podkategorije stroškov.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]