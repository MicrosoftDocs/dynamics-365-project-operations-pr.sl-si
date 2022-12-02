---
title: Ustvari račune dobavitelja
description: Ta članek opisuje koncept računov dobavitelja in pojasnjuje, kako jih ustvarite v aplikaciji Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475485"
---
# <a name="create-vendor-invoices"></a>Ustvari račune dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Če želite uporabljati funkcionalnost, opisano v tem članku, morate v delovnem prostoru **Upravljanje funkcije** omogočiti funkcijo **Omogočanje obdelave dejanskih vrednosti podizvajalskih pogodb z aplikacijo Project Operations za scenarije, ki temeljijo na virih**.

Izdajanje računov dobaviteljem v aplikaciji Microsoft Dynamics 365 Project Operations se lahko uporablja za zapisovanje stroškov dobav storitev in/ali materialov za projekt, ki ga dokončajo dobavitelji.

Kadar so storitve in/ali materiali oddani v podizvajanje dobavitelju, podizvajalska pogodba predstavlja pogodbeni dogovor s tem dobaviteljem. Ko dobavitelj opravlja storitve ali ko so materiali prejeti in uporabljeni za opravila projekta, se stroški zapišejo za projekt. Dobavitelj nato občasno pošilja račune. Ti računi so preverjeni in usklajeni s stroški, ki so zabeleženi za projekt. Po končanem postopku preverjanja je račun dobavitelja potrjen in sproščen v plačilo.

## <a name="scenarios-for-use"></a>Uporabni scenariji

Račune dobaviteljev v aplikaciji Project Operations lahko uporabite za podporo dveh različnih scenarijev:

- Stranke uporabljajo vse izkušnje podizvajalske pogodbe.
- Stranke ne uporabljajo vseh izkušenj podizvajalske pogodbe, ampak želijo imeti enoten pogled na stroške projektov v aplikaciji Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Stranke uporabljajo vse izkušnje podizvajalske pogodbe

Izkušnje računov dobavitelja ponujajo način za preverjanje časovnih vnosov, porabe materiala in vnosov stroškov, ki se nanašajo na podizvajalske komponente, in njihovo ujemanje z vrsticami računa dobavitelja. Ta proces je mogoče uporabiti za preverjanje točnosti vrstic računa dobavitelja. Ko je postopek preverjanja končan in je račun dobavitelja potrjen, sistem razveljavi dejanske vrednosti, ki so bile zapisane v odobrenih dnevnikih časa, stroškov in porabe materiala, nato pa ustvari nove dejanske stroške z vrsticami računa dobavitelja.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Stranke ne uporabljajo vseh izkušenj podizvajalske pogodbe, ampak želijo imeti enoten pogled na stroške projektov v aplikaciji Project Operations

Če sledite procesu podizvajalske pogodbe v sistemu drugega ponudnika, lahko beležite stroške iz tega sistema v aplikaciji Project Operations tako, da ustvarite račune dobavitelja, ki se ne sklicujejo na podizvajalske pogodbe. Na ta način imajo lahko vaše vodje projekta en poenoten pogled na vse stroške na določenem projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Ustvarjanje računov dobaviteljev v aplikaciji Project Operations

Računi dobavitelja so v aplikaciji Dynamics 365 Finance ustvarjeni z modulom **Obveznosti**. Računov dobaviteljev ne morete ustvariti neposredno v okolju Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Nastavitev preverjanja veljavnosti računov dobavitelja

Če je račun dobavitelja namenjen podizvajalcu v okolju Dataverse, morate omogočiti parameter **Potrebno je ročno preverjanje vodje projekta**. Nastavitev možnosti določa, ali naj se račun dobavitelja samodejno potrdi v okolju Dataverse ali zahteva ročno potrditev. Glava vsakega računa dobavitelja projekta vključuje možnost z istim imenom. Možnost v glavi vseh računov dobavitelja projekta je privzeto nastavljena na vrednost, ki ste jo nastavili tukaj. Vendar pa lahko po potrebi posodobite vrednost v glavi posameznih računov dobavitelja.

Če je možnost nastavljena na **Da**, ima račun dobavitelja, ki je ustvarjen v aplikaciji Finance in sinhroniziran v okolje Dataverse, stanje **Osnutek**. Vodja projekta mora nato preveriti veljavnost računa in ga potrditi, preden je obdelan in knjižen v določenem projektu in računih glavne knjige v aplikaciji Finance.

Če je možnost nastavljena na **Ne**, se račun dobavitelja samodejno potrdi. Nadaljnja dejanja niso potrebna.

Če želite nastaviti preverjanje veljavnosti računov dobavitelja, sledite tem korakom.

1. V aplikaciji Finance odprite razdelek **Vodenje projektov in računovodstvo** \> **Nastavitev** \> **Vodenje projekta in računovodski parametri**.
1. V zavihku **Finance** za možnost **Potrebno je ročno preverjanje vodje projekta** na vrednost **Da**, če pravilnik podjetja zahteva preverjanje veljavnosti računov podizvajalskih dobaviteljev. Če v okolju Dataverse preverjanje vodje projekta ni potrebno, pustite možnost nastavljeno na **Ne**. Nastavitev bo privzeto uporabljena na strani **Čakajoči račun dobavitelja**.

> [!NOTE]
> Račune dobaviteljev, ki so ustvarjeni za podizvajalce v okolju Dataverse, je mogoče pravilno obdelati le, če je možnost **Potrebno je ročno preverjanje vodje projekta** nastavljena na vrednost **Da**. Dejanske vrednosti časa, materiala in stroškov, ki jih ustvarijo podizvajalci, lahko vodja projekta ročno poveže z vrsticami računa dobavitelja samo, če je ta možnost nastavljena na **Da**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Nastavitev računa integracije nabave za račune dobaviteljev

Ko je račun dobavitelja objavljen v aplikaciji Finance za Project Operations – integrirano okolje (brez zaloge), so finančni podatki objavljeni na računu integracije nabave. Sistem v okolju Dataverse za knjižen račun ustvari dejanske vrednosti. Te dejanske vrednosti so objavljene v aplikaciji Finance z dnevnikom integracije projektov. Knjiženje dnevnika integracije projektov knjiži dejansko ceno in razveljavi račun integracije nabave.

Če želite nastaviti račun integracije nabave za račune dobaviteljev, sledite tem korakom.

1. V aplikaciji Finance odprite razdelek **Vodenje projektov in računovodstvo** \> **Nastavitev** \> **Vodenje projekta in računovodski parametri**.
1. V zavihku **Project Operations za Dynamics 365 customer engagement** izberite razdelek **Materiali** \> **Račun integracije nabave**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Ustvarjanje in knjiženje računov podizvajalskih dobaviteljev

Ko uradnik za obveznosti prejme račun od podizvajalca, se v aplikaciji Finance ustvari nov račun.

1. V aplikaciji Finance odprite razdelek **Obveznosti** \> **Računi** \> **Čakajoči računi dobavitelja**.
1. V **Podoknu dejanj** izberite možnost **Novo**, da ustvarite račun dobavitelja.
1. V glavi računa v polju **Račun za obračun** izberite možnost **Podizvajalec**.
1. Izberite datum računa.
1. V zavihku **Glava** za možnost **Potrebno je ročno preverjanje vodje projekta** izberite vrednost **Da**. Privzeta nastavitev te možnosti izvira s strani **Parametri vodenja projekta in računovodstva**. Lahko pa se spremeni na ravni računa dobavitelja.
1. V zavihku za hitri dostop **Vrstica računa** izberite možnost **Dodaj vrstico**, da ustvarite vrstico računa dobavitelja.
1. Izberite kategorijo nabave, ki je bila ustvarjena za podrobnosti podizvajalske pogodbe, in vnesite ceno na enoto, mersko enoto in količino.
1. V razdelku vrstic računa dobavitelja v zavihku **Projekt** izberite projekt, za katerega podizvajalec deli račun podizvajalca.
1. Izberite kategorijo projekta. Lahko je katere koli vrste: **Element**, **Strošek**, **Materiali** ali **Ure**.
1. Izberite vlogo samo, če je izbrana kategorija projekta vrste **Ura**.
1. Izberite možnost **Knjiži**, če želite knjižiti račun dobavitelja.

Lahko tudi ustvarite račun dobavitelja v razdelku **Obveznosti** \> **Računi** \> **Odprti računi dobavitelja**, kjer izberete možnost **Novo**.

Ko je račun dobavitelja knjižen, je na voljo v okolju Dataverse, da lahko vodja projekta preveri veljavnost in ga obdela.

## <a name="vendor-invoice-processing-in-dataverse"></a>Obdelava računa dobavitelja v okolju Dataverse

V računu dobavitelja, ki je ustvarjen v okolju Dataverse, nekatere vrednosti polj izvirajo iz računa dobavitelja, ki je evidentiran v razdelku Finance. Druge vrednosti so privzete vrednosti, ki izhajajo iz podizvajalske pogodbe.

Naslednja polja in povezani zapisi bodo kopirani iz podizvajalske pogodbe v glavo računa dobavitelja:

- Valuta
- Pogodbena enota
- Plačilni pogoji

V vrsticah računa dobavitelja aplikacija Project Operations uporablja naslednje vrednosti polj za vnos privzete podizvajalske pogodbe in sklica podrobnosti podizvajalske pogodbe:

- Razred transakcije
- Vloga
- Kategorija transakcije
- Polja izdelka
- Projekt
- opravilo,

> [!NOTE]
> Nespremenljive cene podrobnosti podizvajalskih pogodb niso podprte v aplikaciji Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
