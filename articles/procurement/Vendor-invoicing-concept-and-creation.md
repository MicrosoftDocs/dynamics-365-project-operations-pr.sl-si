---
title: Ustvarite račune dobavitelja
description: Ta članek opisuje koncept računov dobavitelja in pojasnjuje, kako jih ustvarite v Microsoftu Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Ustvarite račune dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Če želite uporabljati funkcionalnost, opisano v tem članku, morate omogočiti **Omogočite obdelavo dejanskih podizvajalskih pogodb s projektnimi operacijami za scenarije, ki temeljijo na virih** funkcija v **Upravljanje funkcij** delovni prostor.

Fakturiranje dobavitelja v Microsoftu Dynamics 365 Project Operations se lahko uporablja za beleženje stroškov dobav storitev in/ali materialov na projektu, ki ga dokončajo prodajalci.

Kadar so storitve in/ali materiali oddani v podizvajanje prodajalcu, podizvajalska pogodba predstavlja pogodbeni dogovor s tem prodajalcem. Ko prodajalec opravlja storitve ali ko materiale prejme in uporabi pri projektnih nalogah, se stroški evidentirajo na projektu. Prodajalec nato periodično pošilja račune. Ti računi so preverjeni in usklajeni s stroški, ki so zabeleženi na projektu. Po končanem postopku preverjanja je račun dobavitelja potrjen in sproščen v plačilo.

## <a name="scenarios-for-use"></a>Scenariji za uporabo

Račune dobaviteljev v Project Operations je mogoče uporabiti za podporo dveh različnih scenarijev:

- Stranke uporabljajo vse izkušnje podizvajalcev.
- Stranke ne uporabljajo vseh podizvajalskih izkušenj, ampak želijo imeti enoten pogled na stroške projektov v projektnih operacijah.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Stranke uporabljajo vse izkušnje podizvajalcev

Izkušnje z računi dobavitelja ponujajo način za preverjanje časovnih vnosov, porabe materiala in vnosov stroškov, ki se nanašajo na podizvajalske komponente, in njihovo ujemanje z vrsticami računa dobavitelja. Ta postopek je mogoče uporabiti za preverjanje točnosti vrstic računa dobavitelja. Ko je postopek preverjanja končan in je račun dobavitelja potrjen, sistem razveljavi dejanske vrednosti, ki so bile zabeležene v odobrenih dnevnikih časa, stroškov in porabe materiala, nato pa ustvari nove dejanske stroške z uporabo vrstic računa dobavitelja.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Stranke ne uporabljajo vseh podizvajalskih izkušenj, ampak želijo imeti enoten pogled na stroške projektov v projektnih operacijah

Če sledite postopku podizvajanja v sistemu tretje osebe, lahko beležite stroške iz tega sistema tretje osebe v Project Operations tako, da ustvarite račune dobavitelja, ki se ne sklicujejo na podizvajalske pogodbe. Na ta način imajo lahko vaši vodje projektov enoten, poenoten pogled na vse stroške na določenem projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Ustvarite račune dobavitelja v Project Operations

Računi dobavitelja se ustvarijo v Dynamics 365 Finance, z uporabo **Obveznosti** modul. Računov dobaviteljev ne morete ustvariti neposredno v Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Nastavite preverjanje računov dobavitelja

Če je račun prodajalca namenjen podizvajalcu v Dataverse, morate omogočiti **Zahtevano je ročno preverjanje pri PM** parameter. Nastavitev opcije določa, ali naj se račun dobavitelja samodejno potrdi Dataverse, ali zahteva ročno potrditev. Glava vsakega računa prodajalca projekta vključuje možnost z istim imenom. Privzeto je možnost v glavi vseh računov dobavitelja projekta nastavljena na vrednost, ki ste jo nastavili tukaj. Vendar pa lahko po potrebi posodobite vrednost v glavi posameznih računov dobavitelja.

Če je možnost nastavljena na **ja**, račun dobavitelja, ki se ustvari v Financah in sinhronizira z njim Dataverse ima **Osnutek** stanje. Račun mora nato potrditi in potrditi vodja projekta ter potrditi, preden je obdelan in objavljen na določenem projektu in kontih glavne knjige v Financah.

Če je možnost nastavljena na **št**, se račun dobavitelja samodejno potrdi. Nadaljnji ukrepi niso potrebni.

Če želite nastaviti preverjanje računov dobavitelja, sledite tem korakom.

1. V Financah pojdite na **Vodenje projektov in računovodstvo** \> **Nastaviti** \> **Projektno vodenje in računovodski parametri**.
1. Na **Finančna** zavihek, nastavite **Zahtevano je ročno preverjanje pri PM** možnost za **ja** če politika podjetja zahteva preverjanje računov prodajalcev podizvajalcev. Če preverjanje s strani vodje projekta ni potrebno v Dataverse, pustite nabor možnosti za **št**. Privzeto bo nastavitev uporabljena na **Čakajoč račun prodajalca** strani.

> [!NOTE]
> Računi dobaviteljev, ki so ustvarjeni za podizvajalce v Dataverse je mogoče pravilno obdelati le, če **Zahtevano je ročno preverjanje pri PM** možnost je nastavljena na **ja**. Dejanske stroške časa, materiala in stroškov, ki jih ustvarijo podizvajalci, lahko vodja projekta ročno poveže z vrsticami računa dobavitelja samo, če je ta možnost nastavljena na **ja**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Nastavite integracijski račun nabave za račune dobaviteljev

Ko je račun dobavitelja objavljen v Finance for Project Operations – integrirano okolje (brez zaloge), so finančni podatki objavljeni na računu integracije nabave. Sistem generira dejanske podatke Dataverse za izstavljeni račun. Ta dejstva so objavljena v Financah z uporabo Dnevnika integracije projektov. Knjiženje dnevnika integracije projekta knjiži dejanski strošek in stornira račun integracije nabave.

Če želite nastaviti integracijski račun nabave za račune dobaviteljev, sledite tem korakom.

1. V Financah pojdite na **Vodenje projektov in računovodstvo** \> **Nastaviti** \> **Projektno vodenje in računovodski parametri**.
1. Na **Projektne operacije za vključevanje strank Dynamics 365** zavihek izberite **Materiali** \> **Račun integracije nabave**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Ustvarite in knjižite račune podizvajalcev

Ko računovodstvo prejme račun od podizvajalca, se v Financah ustvari nov račun.

1. V Financah pojdite na **Obveznosti do dobaviteljev** \> **Računi** \> **Čakajoči računi dobavitelja**.
1. Na **Podokno dejanj**, izberite **Novo** za ustvarjanje računa dobavitelja.
1. V glavi računa v **račun račun** polje izberite **Podizvajalec**.
1. Izberite datum računa.
1. Na **Glava** zavihek, nastavite **Zahtevano je ročno preverjanje pri PM** možnost za **ja**. Privzeta nastavitev te možnosti izvira iz **Projektno vodenje in računovodski parametri** strani. Lahko pa se spremeni na ravni računa dobavitelja.
1. Na **Vrstica računa** FastTab, izberite **Dodaj vrstico** ustvarite vrstico računa dobavitelja.
1. Izberite kategorijo nabave, ki je bila ustvarjena za podizvajalske postavke, in vnesite ceno na enoto, mersko enoto in količino.
1. V razdelku vrstic računa dobavitelja na **Projekt** izberite projekt, za katerega podizvajalec deli račun podizvajalca.
1. Izberite kategorijo projekta. Lahko je katere koli vrste **Postavka**, **·**, **·**, oz **Ure**.
1. Izberite vlogo samo, če je izbrana kategorija projekta **ura** vrsta.
1. Izberite **Objavi** za knjiženje računa dobavitelja.

Druga možnost je, da ustvarite račun prodajalca tako, da obiščete **Obveznosti** \> **Računi** \> **Odprti računi dobavitelja** in izbiranje **Novo**.

Ko je račun dobavitelja objavljen, postane na voljo v Dataverse za preverjanje in obdelavo vodje projekta.

## <a name="vendor-invoice-processing-in-dataverse"></a>Obdelava računov dobaviteljev v Dataverse

V računu dobavitelja, ki je ustvarjen v Dataverse, nekatere vrednosti polj izvirajo iz računa dobavitelja, ki je evidentiran v Financah. Druge vrednosti so privzete vrednosti, ki izhajajo iz podizvajalske pogodbe.

Naslednja polja in povezani zapisi bodo kopirani iz podizvajalske pogodbe v glavo računa dobavitelja:

- Valuta
- Pogodbena enota
- Plačilni pogoji

V vrsticah računa dobavitelja Project Operations uporablja naslednje vrednosti polj za vnos privzete podizvajalske pogodbe in reference vrstice podizvajalske pogodbe:

- Razred transakcije
- Vloga
- Kategorija transakcije
- Polja izdelkov
- Projekt
- opravilo,

> [!NOTE]
> Podizvajalske vrstice s fiksno ceno niso podprte v Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
