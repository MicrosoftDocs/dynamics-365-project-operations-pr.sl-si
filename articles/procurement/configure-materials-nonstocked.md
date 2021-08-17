---
title: Konfiguracija materialov, ki niso na zalogi, in čakajočih računov dobavitelja
description: V tej temi je pojasnjeno, kako omogočiti materiale, ki niso na zalogi, in čakajoče račune dobavitelja.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003251"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfiguracija materialov, ki niso na zalogi, in čakajočih računov dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

## <a name="minimum-version-requirement"></a>Zahteva za najmanjšo različico

Uporaba materialov, ki niso na zalogi, in čakajočih računov dobavitelja za aplikacijo Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/nezalogi, zahtevajo naslednje različice:

Rešitve Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 ali novejša različica
- Osnovna rešitev za organiziranje aplikacije z dvojnim zapisovanjem – 2.2.2.23 ali novejša različica

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) ali novejša različica. Za izpolnitev zahtev za najmanjšo različico poskrbite, da posodobite okolje Finance in uporabite vse posodobitve kakovosti.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Zagon preslikav za dvojno zapisovanje za materiale, ki niso na zalogi, in čakajoče račune dobavitelja

V tem razdelku so na voljo informacije o posebnih preslikavah, potrebnih za materiale, ki niso na zalogi, in čakajoče račune dobavitelja. Preverite, ali se zahtevane preslikave, navedene v temi [Omogočanje novega okolja](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps), izvajajo v vašem okolju.

1. Odprite storitev Lifecycle Services (LCS), pomaknite se v svoj projekt LCS in odprite stran **Podrobnosti o okolju**.
2. V razdelku **Informacije o okolju Common Data Service** izberite možnost **Povezava do storitve CDS za aplikacije**. Ko izberete povezavo, boste preusmerjeni na seznam entitet v preslikavah.
3. Prepričajte se, da se izvajajo naslednje preslikave. Če se ne izvajajo, jih zaženite in vključite vse povezane preslikave tabel.

    - CDS je izdal različne izdelke (izdelki)
    - Dobavitelji v2 (msdyn_vendors)
    - Tabela aplikacije Project Operations za ocene materiala (msdyn_estimatelines)
    - Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices)
    - Entiteta za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoicelines)
    - Dejanske vrednosti integracije za Project Operations (msdyn_actuals). Prepričajte se, da se izvaja različica preslikave 1.0.0.14 ali novejša. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Novo različico preslikave lahko aktivirate tako, da izberete možnost **Različica preslikave tabele** in nato shranite izbrano različico.

Če uporabljate standardne predstavitvene podatke, boste morda morali z začetno sinhronizacijo zaustaviti naslednje preslikave entitet in jih znova zagnati:
  - Dnevi plačila CDS V2 (msdyn_paymentdays)
  - Razpored plačil (msdyn_paymentschedules)
  - Plačilni pogoji (msdyn_paymentterms)
  - Skupine dobaviteljev (msdyn_vendorgroups)
  - Enote (uom)

> [!NOTE]
> Začetna sinhronizacija za skupine dobaviteljev in enote morda ne bo uspela za nekaj zapisov v obstoječem naboru predstavitvenih podatkov. Napake lahko prezrete, saj ne preprečijo uporabe predstavitvenih podatkov z aplikacijo Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfiguracija zahtev v storitvi Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktiviranje poteka dela za ustvarjanje računov na podlagi entitete dobavitelja

Osnovna rešitev za organiziranje z dvojnim zapisovanjem zagotavlja [Glavno integracijo dobaviteljev](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Kot predpogoj za to funkcijo je treba podatke dobavitelja ustvariti v entiteti **Kupci**. Aktivirajte postopek predloge poteka dela za ustvarjanje dobaviteljev v tabeli **Kupci**, kot je opisano v članku [Preklop med načrti dobaviteljev](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Nastavitev izdelkov, da bodo ustvarjeni kot dejavni

Materiali, ki niso na zalogi, morajo biti v aplikaciji Finance nastavljeni kot **Izdani izdelki**. Osnovna rešitev za organiziranje z dvojnim zapisovanjem zagotavlja vnaprej pripravljeno [Integracijo izdanih izdelkov v katalog izdelkov storitve Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Privzeto se izdelki iz aplikacije Finance sinhronizirajo v storitev Dataverse v stanju osnutka. Če želite izdelek sinhronizirati v dejavno stanje, tako da ga je mogoče neposredno uporabiti v dokumentih za uporabo materiala ali v čakajočih računov dobavitelja, se pomaknite v razdelek **Sistem** > **Administracija** > **Administracija sistema** > **Sistemske nastavitve** in na zavihku **Prodaja** nastavite možnost **Ustvari izdelke v dejavnem stanju** na **Da**.

## <a name="configure-prerequisites-in-finance"></a>Konfiguracija zahtev v storitvi Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Omogočanje funkcijski ključ za čakajoče račune dobavitelja

Izvedite naslednje korake, da omogočite funkcionalnost dodajanja podrobnosti projekta v vrstice čakajočih računov dobavitelja.

1. V aplikaciji Finance odprite delovni prostor **Upravljanje funkcij**.
2. Na seznamu funkcij poiščite funkcijo **Omogočanje čakajočih računov dobavitelja v aplikaciji Project Operations za scenarije, ki temeljijo na virih/nezalogi** in izberite možnost **Omogoči**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Določanje skupine kategorij in kategorije projektov za elemente

Konfigurirajte najmanj eno skupino kategorij za vrsto transakcije **Element** in najmanj eno kategorijo projekta, ki uporablja to skupino. Za več informacij glejte [Konfiguracija kategorij projekta](../project-accounting/configure-project-categories.md#category-groups).

Preglejte profile stroškov in prihodkov projekta ter konfigurirajte nastavitev knjiženja v glavno knjigo za transakcije postavk. Za več informacij glejte [Konfiguracija vodenja računov za plačljive projekte](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Nastavitev izdelka, ki ni v katalogu

V aplikaciji Project Operations lahko beležite ocene in uporabo materiala za izdelke iz kataloga, ki so konfigurirani v izdanem katalogu izdelkov, in za izdelke, ki niso v katalogu. Za uporabo izdelkov, ki niso v katalogu, je potreben en sam izdan izdelek, ki je v ta namen konfiguriran v aplikaciji Finance. Izvedite naslednje korake za konfiguriranje izdelka, ki ni v katalogu. Te korake izvedite v vsaki pravni osebi, ki uporablja aplikacijo Project Operations za scenarije, ki temeljijo na virih/nezalogi.

1. V aplikaciji Finance se pomaknite v razdelek **Upravljanje podatkov o izdelkih** > **Izdelki** > **Izdani izdelki** in izberite možnost **Novo**.
2. V polju **Vrsta izdelka** izberite možnost **Element**, v polju **Podvrsta izdelka** pa izberite **Izdelek**.
3. Vnesite številko izdelka (NI V KATALOGU) in ime izdelka (izdelek, ki ni v katalogu).
4. Izberite skupino modelov elementov. Prepričajte se, da ima izbrana skupina modelov elementov polje **Pravilnik o zalogi izdelkov na zalogi** nastavljeno na **Neresnično**.
5. Izberite vrednosti v poljih **Skupina elementov**, **Skupina za razsežnost pomnilnika** in **Skupina za razsežnost sledenja**. Uporabite samo možnost **Razsežnost pomnilnika** za **Mesto** in v polju **Razsežnosti sledenja** izberite **Brez**.
6. Izberite vrednosti v poljih **Enota zaloge**, **Enota nakupa** in **Enota prodaje** in shranite spremembe.
7. Na zavihku **Načrt** nastavite privzete nastavitve naročila, na zavihku **Zaloga** pa nastavite privzeto lokacijo in skladišče.
8. V razdelku **Upravljanje projektov in računovodstva** > **Nastavitev** > **Vodenje projektov in računovodski parametri** odprite možnost **Project Operations v storitvi Dynamics 365 Dataverse**. 
9. Na zavihku **Materiali** v polju **Izdelek, ki ni v katalogu** izberite izdelek, ki ste ga ustvarili.
10. V svojem okolju Dataverse na zemljevidu mesta odprite entiteto **Izdelki** in poiščite zapis izdelka, ki ni v katalogu. 
11. Odprite podrobnosti zapisa in nastavite stanje izdelka na **Umaknjeno**. To stanje izdelka preprečuje, da bi kdo nenamerno uporabil ta zapis neposredno v dokumentih za ocene in uporabo materiala.

### <a name="set-up-a-procurement-integration-account"></a>Vzpostavitev računa za integracijo naročil

Račun za integracijo naročil se uporablja kot račun za obračun pri knjiženju čakajočega računa dobavitelja z vrsticami, dodeljenimi projektu.

Ko sistem poknjiži čakajoči račun dobavitelja, se ta račun uporabi za znesek stroškov projekta. Podrobnosti računa dobavitelja se obdelujejo v storitvi Dataverse in ustvari se ustrezna dejanska vrednost projekta. Podatki iz dejanske vrednosti projekta so dodane v dnevnik integracij za Project Operations. Ko poknjižite dnevnik integracij, se znesek izbriše iz računa za integracijo naročil in zabeleži v stroške projekta.

1. Če želite vzpostaviti račun za integracijo naročil, v razdelku **Upravljanje projektov in računovodstva** > **Nastavitev** > **Vodenje projektov in računovodski parametri** odprite možnost **Project Operations v storitvi Dynamics 365 Dataverse**. 
2. Na zavihku **Materiali** v polju **Račun za integracijo naročil** izberite vrednost.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Nastavite privzete kategorije projekta za element

1. V aplikaciji Finance v razdelku **Upravljanje projektov in računovodstva** > **Nastavitev** > **Vodenje projektov in računovodski parametri** odprite možnost **Project Operations v storitvi Dynamics 365 Dataverse**. 
2. Na zavihku **Privzete kategorije projekta** v polju **Element** izberite vrednost. Ta kategorija projekta se uporablja za materialne transakcije, če kategorija projekta ni bila določena v zapisu dejanskih vrednosti projekta.
