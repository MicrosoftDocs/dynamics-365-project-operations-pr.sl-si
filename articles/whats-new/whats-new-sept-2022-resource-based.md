---
title: Novosti za september 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: V tem članku so informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta septembra 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zaloge.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634826"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za september 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse različica okolja 4.46.0.60
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance verzija 10.0.29

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

| Območje funkcij | Ime funkcije | Več informacij |
| --- | --- | --- |
| Upravljanje priložnosti | **Revizija in aktivacija ponudb**<br>Project Operations prinaša popolno podporo prodajnemu procesu. Projektne ponudbe je mogoče aktivirati, da predstavljajo stanje, v katerem je ponudba samo za branje in je v pregledu. Aktivirane ponudbe je mogoče spremeniti, da se ustvarijo nove ponudbe, ki imajo povečano številko revizije. Aktivirane projektne ponudbe ali revizije ponudb je mogoče zapreti kot zmagovalne ali izgubljene. | [Aktiviranje in popravljanje projektne ponudbe](/dynamics365/project-operations/sales/activation-and-revision) |
| Zaračunavanje in oblikovanje cen | **Neplačila cene glede na časovni pas**<br>Project Operations je uvedel koncept agnostičnega datuma glede na časovni pas za vse dejanske podatke projekta. Novo polje, **Datum transakcije**, je zdaj na voljo v vrsticah dnevnika in dejanskih podatkih in bo uporabljen za shranjevanje datuma, ko je prišlo do transakcije, vendar brez pretvorbe tega datuma v koordinirani univerzalni čas. Ta datum bo uporabljen za nadaljnje postopke, kot sta neplačilo cene in ustvarjanje računov. | <p>[Določite stopnje stroškov za ocene in dejanske vrednosti na podlagi projekta](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Določite prodajne cene za ocene in dejanske vrednosti na podlagi projekta](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Zaračunavanje in oblikovanje cen | **Preglasitve cen z datumom veljavnosti v Project Operations**<br>Preglasitve cen z datumom veljavnosti omogočajo preglasitev ali spremembo določenih cen v ceniku. | [Preglasitve cen z datumom veljavnosti](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Podizvajanje | **Usklajevanje računov podizvajalcev in dobaviteljev**<br>Ta funkcija strankam omogoča ustvarjanje podizvajalskih pogodb za nakup časa virov, kategorij stroškov in materialov, ki se uporabljajo za projektno delo. Prav tako strankam omogoča, da v aplikacijah za finance in poslovanje zabeležijo račune dobaviteljev, ki bodo vodjem projektov na voljo v Dataverse za preverjanje. | <p>[Upravljanje s podizvajalci](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Ustvari račune dobavitelja](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Čas in strošek | **Globalni odobritelj**<br>Ta funkcija omogoča neodvisnega prodajalca programske opreme (ISV) in centralizirano odobritev, ne glede na projekt ali status člana ekipe v projektu. | [Varnost in odobritve](/dynamics365/project-operations/approvals/approvals-security) |
| Upravljanje stroškov | **Možnost knjiženja obveznosti za stroške v valuti prodajalca**<br>Ta funkcija omogoča objavo poročil o stroških v valuti prodajalca za način gotovinskega plačila. | [Možnost knjiženja obveznosti za stroške v valuti prodajalca](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Nabava projekta | **Plačajte, ko plačate plačila prodajalca**<br>Ta funkcija omogoča uporabo funkcije Plačaj ob plačilu (PWP) v okoljih Project Operations brez zaloge. Omogoča blokiranje/zadrževanje plačil prodajalca na podlagi pogojev hrambe, dokler plačilo ni prejeto od stranke. | [Plačajte, ko plačate plačila prodajalca](/dynamics365/project-operations/procurement/pay-when-paid) |
| Nabava projekta | **Zahtevki za nakup projekta**<br>Ta funkcija uporabnikom omogoča ustvarjanje naročilnic, povezanih s projektom, v pravnih osebah, kjer je omogočena integracija projektnih operacij na Dynamics 365 Customer Engagement. Naročila za projekt se lahko uporabijo za evidentiranje nabave materiala, ki ni na zalogi, za projekt s strani osebne službe nabave. Projektna naročila ne bodo sinhronizirana z Dataverse. Vendar pa lahko uporabite navidezno entiteto, da prikažete vrstice naročilnice za Project Dataverse za informacije vodje projekta. Stroški računa dobavitelja, povezani s projektom, so integrirani z entiteto Project Actuals v Dataverse. Stroški projekta se evidentirajo v podknjigi projekta z uporabo dnevnika integracije projektnih operacij. | |
|Načrtovanje in sledenje projektov|**Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja** </br> </br>API za urejanje obrisa dodelitve virov omogoča razvijalcem, da programsko določijo trud osebe, ki je dodelila nalogo, v katerem koli podprtem časovnem obdobju za bolj natančno načrtovanje truda v časovnih fazah.|[Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Naslednja tabela prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations septembra 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| -------------- | ------------------- | ------------|
| Dejanske vrednosti integracije za Project Operations (msdyn_actuals) | 1.0.0.15 | Ta zemljevid podpira obdelavo dejanskih podatkov podizvajalcev s projektnimi operacijami za scenarije, ki temeljijo na virih. |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Ta zemljevid podpira obdelavo dejanskih podatkov podizvajalcev s projektnimi operacijami za scenarije, ki temeljijo na virih. |
| Entiteta za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ta zemljevid podpira obdelavo dejanskih podatkov podizvajalcev s projektnimi operacijami za scenarije, ki temeljijo na virih. |

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje projektne operacije Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljen zemljevid tabel, znova uveljavite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če naletite na težavo, ko zaženete zemljevid, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2754422 | Ocene materiala in stroškov se ne prenesejo v Finance, ko so projekti kopirani Dataverse. |
| Čas in strošek | 2787409 | Neveljavni odobritelj lahko odobri vnos časa, ki ni projekt. |
| Upravljanje priložnosti | 2788907 | Posodobljeno sporočilo o napaki pri preverjanju edinstvenosti za vrstice naročila, ki vključujejo zastavice. |
| Čas in strošek | 2842253 | Obravnava ničelne izjeme za odobritev časa. |
| Zaračunavanje in oblikovanje cen | 2844181 | Neuspešno pridobivanje ID-ja korelacije blokira ustvarjanje računa. |
| Zaračunavanje in oblikovanje cen | 2876628 | QLD, CLD – Ocena razrešitve cenika bi morala uporabljati podedovana polja datumskega obsega cenika. |
| Podizvajanje | 2893222 | Če za linijo podizvajalca ni določena nobena vloga, bi moralo biti mogoče to linijo izbrati pri članu skupine za katero koli vlogo. |

### <a name="project-management-and-accounting-in-finance"></a>Vodenje projektov in računovodstvo v Financah

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite v Microsoft Dynamics Storitve življenjskega cikla in si oglejte [Članek KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije so privzeto vklopljene v prihajajoči izdaji

Naslednja tabela navaja funkcije, ki so privzeto vklopljene v različici 10.0.30. Večino funkcij, ki so bile samodejno vklopljene, je mogoče izklopiti v [Upravljanje funkcij](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V prihodnosti bodo nekatere funkcije, ki so bile samodejno vklopljene, morda odstranjene iz upravljanja funkcij in bodo postale obvezne. Ta sprememba zagotavlja, da stranke uporabljajo trenutno funkcionalnost, tako da lahko izboljšave gradijo na trenutni funkcionalnosti, ko so dodane. Funkcije ne bodo nikoli samodejno omogočene v manj kot enem letu, razen če se ugotovi, da so bistvene.

| Ime funkcije | Omogoči datum | Dodana funkcija | Stanje funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogoči asinhrono operacijo, ko mora uporabnik preklopiti med sinhronizacijo in asinhrono operacijo | 21. oktober 2022 | 9. april 2021 | Privzeto vklopljeno | Upravljanje stroškov |
| Zahtevana je ocena stroškovne politike za prejemke | 21. oktober 2022 | 20. december 2021 | Privzeto vklopljeno | Upravljanje stroškov |
| Pogled seznama poročil o stroških, ki so jih ustvarili delegirani delavci | 21. oktober 2022 | 19. februar 2020 | Privzeto vklopljeno | Upravljanje stroškov |
| Izračun skupne kilometrine po proračunsko leto | 21. oktober 2022 | 10. maj 2022 | Privzeto vklopljeno | Upravljanje stroškov |
