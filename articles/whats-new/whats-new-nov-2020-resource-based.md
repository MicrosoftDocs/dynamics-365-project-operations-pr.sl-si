---
title: Novosti v novembru 2020 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v novembrski izdaji (2020) aplikacije Project Operations za scenarije, ki temeljijo na virih/nezalogi.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b76ebbff1cc2720e699334601d425879f2d20770
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600394"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v novembru 2020 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

- Project Operations v okolju CDS, različica 4.4.0.70
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Posodobitve aplikacije Project Operations za scenarije, ki temeljijo na virih/nezalogi

### <a name="project-operations-on-cds"></a>Project Operations v CDS-ju

| Območje funkcij                 | Številka sklica | Posodobitev kakovosti                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Upravljanje priložnosti       | 2036993          | Vrstica ocene in podrobnosti pogodbe za dodelitev vira se posodobijo na zmagovalnih ponudbah, ko je vrsta vrstice ponudbe **Vsa opravila**.                                                 |
| Zaračunavanje in cene          | 2070392          | Podrobnosti projektne pogodbe na računu se povečajo, ko je izbrana možnost **Osvežitev transakcij računa**.                                                                         |
| Načrtovanje projekta             | 2043336          | Zapisa člana projektne ekipe ni mogoče izbrisati.                                                                                                                                  |
| Načrtovanje projekta             | 2046013          | Neskladno delovanje za stolpce oznak »Ocene« med nalaganjem v primerjavi s spremembo vrste časovne razporejenosti.                                                                                   |
| Načrtovanje projekta             | 2046647          | Začetni in končni čas se izklopita za eno uro, ko člani projektne ekipe ustvarijo zahteve za vir.                                                                      |
| Načrtovanje projekta             | 2053879          | (Glede na prihajajočo uvedbo CDS-ja) »PublishUnassignedAssignments« prekine poskus shranjevanja opravila, ko je napaka »Vrednost, poslana za ConditionOperator« prazna.                       |
| Načrtovanje projekta             | 2055501          | Če pustite polje **Začetni datum projekta** prazno, povzročite napako v razporedu.                                                                                                      |
| Načrtovanje projekta             | 2066817          | Splošnega vira ni mogoče ustvariti z izbirnikom oseb na zavihku **Opravila**.                                                                                                   |
| Načrtovanje projekta             | 2067034          | Gumb **Ogled podrobnosti** ni na voljo na strani **Podrobnosti opravila**.                                                                                                       |
| Upravljanje virov          | 2046667          | Splošni člani ekipe se ne izbrišejo niti po tem, ko so izpolnjeni vsi viri.                                                                                                    |
| Vnos časa in hitrih stroškov | 2047499          | Gumb **Novo** na strani »Vnos časa« odpre stran **Nov e-poštni podpis**.                                                                                               |
| Vnos časa in hitrih stroškov | 2059859          | Pri ustvarjanju vnosa stroškov se odpre nepričakovano pojavno okno.                                                                                                                         |
| Drugo                        | 2044181          | (Odstranjevanje naročilnice) ko poskušate odstraniti osnovni rešitvi storitve »msdyn_ProjectServiceCore_Patch« in »msdyn Project«, pride do napake »Zapis ni na voljo«.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vodenje projektov in računovodstvo v Dynamics 365 Finance

| Območje funkcij        | Številka sklica | Posodobitev kakovosti                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prepoznavanje prihodkov | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Celotni odstotek ocene projekta je napačen, če pogodba uporablja tujo valuto in odstotek napredka dela za celotno metodo.                     |
| Pripoznavanje prihodkov | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Ocen ni mogoče objaviti s postopkom končnih odstotkov **Dejanski stroški**.                                                                                                    |
| Pripoznavanje prihodkov | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Odstranjevanje ne uspe zaradi napake pri neravnovesju kupona, če se valuta podjetja in valuta transakcije razlikujeta.                                              |
| Upravljanje stroškov  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Za uporabnike brez skrbniških pravic se vrednosti iskanja za stolpce vrstic za stroške, na primer **ID projekta** in **Kategorija stroška**, ne prikazujejo pravilno v okviru podatkovnega povezovalnika. |
| Upravljanje stroškov  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Privzeta lastnost vrstice ni prikazana za kategorije stroškov.                                                                                                         |
| Upravljanje stroškov  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integracija stroškov mora vključevati lastnost vrstice iz poročila o stroških.                                                                                             |
| Zaračunavanje           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Predlog za račune za projekte ni mogoče objaviti zaradi sporočila o napaki, v katerem piše, da kombinacija za FD ni bila potrjena.                                                    |
| Zaračunavanje           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Transakcij iz strani s podrobnosti o **računih** si ni mogoče ogledati.                                                                                                              |
| Zaračunavanje           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Vrstice predlog za račune je mogoče izbrisati.                                                                                                                                  |
| Vodenje računov projekta  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Elementi menija **Napoved** niso vidni na strani s seznamom **Projekti**.                                                                                                   |
| Vodenje računov projekta  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Razdelka **Izjava o projektu**   > **Transakcije in napoved** ni mogoče odpreti.                                                                                                       |
| Vodenje računov projekta  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | Možnost **Prilagajanje računovodstva** ni omogočena za fakturirane projektne transakcije.                                                                                                  |
| Vodenje računov projekta  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Podrobnosti o vodenju računov niso vključene v tabelo **ProjCDSActualsImport**, ko je objavljen dnevnik **Integracija**.                                                  |
| Vodenje računov projekta  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Vnos napovedi projekta se podvoji, ko odstranite dodelitev vira in jo nato znova dodate.                                                                            |
| Vodenje računov projekta  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Če izberete povezavo za ID projekta, ne odprete URL-ja globoke povezave za CDS.                                                                                                         |
| Vodenje računov projekta  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Začetnega datuma za opravilo v CDS-ju ni mogoče posodobiti.                                                                                                                           |
| Vodenje računov projekta  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Če omogočite funkcijo, možnost več pogodbenih vrstic ni mogoča brez integracije CDS-ja.                                                                                   |

### <a name="regulatory-updates"></a>Regulativne posodobitve
Za informacije o regulativnih posodobitvah za aplikacije Finance in Operations glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prav tako se lahko prijavite v storitev LCS in si ogledate načrtovane regulativne posodobitve z orodjem za iskanje težav. Iskanje težav omogoča iskanje po državi, vrsti funkcije in izdaji.


[!INCLUDE[footer-include](../includes/footer-banner.md)]