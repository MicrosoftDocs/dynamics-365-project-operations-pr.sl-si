---
title: Omogočanje novega okolja
description: Ta tema vsebuje informacije o omogočanju novega okolja v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727810"
---
# <a name="provision-a-new-environment"></a>Omogočanje novega okolja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ta tema vsebuje informacije o tem, kako zagotoviti novo okolje Dynamics 365 Project Operations za primere uporabe z viri/brez zalog.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Omogočite avtomatizirano omogočanje uporabe storitve Project Operations v projektu LCS

Uporabite naslednje korake, da omogočite avtomatizirano omogočanje uporabe storitve Project Operations za vaš projekt LCS.

1. Odprite [LCS](https://lcs.dynamics.com/v2) in izberite ploščico **Upravljanje funkcije predogleda**.
2. V seznamu **Funkcija predogleda** izberite **Funkcija Project Operations** in izberite **Omogoči funkcijo predogleda**, da omogočite storitev Project Operations.

> [!NOTE]
> Ta korak se izvede samo enkrat za posamezni projekt LCS.

## <a name="provision-a-project-operations-environment"></a>Omogočanje uporabe okolja Project Operations

1. Odprite novo [predstavitveno okolje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ali [preskusno/produkcijsko okolje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) za uvedbo. 
2. Sprehodite se skozi čarovnika **Omogočanje okolja**. 

> [!IMPORTANT]
> Prepričajte se, da je izbrana različica aplikacije 10.0.13 ali novejša.

3. če želite omogočiti storitev Project Operations odprite možnost **Napredne nastavitve** in izberite **Common Data Service**. 
4. Omogočite **Nastavitev Common Data Service**, tako da izberete **Da** in vnesite podatke v zahtevana polja:

  - Imenu
  - Regija
  - Language
  - Valuta
 
5. V polju **Predloga Common Data Service** izberite **Project Operations** 

6. Izberite vrsto okolja za vašo uvedbo. Preskus na podlagi naročnine vam bo omogočil uvedbo okolja CDS za 30 dni. 

![Nastavitve uvedbe](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Izberite možnost **Strinjam se**, da potrdite pogoje storitve, nato izberite **Končano**, da se vrnete v nastavitve uvajanja.

![Soglasje uvedbe](./media/2DeploymentConsent.png)

7. Izbirno – uporabi predstavitvene podatke v okolju. Pojdite na **Napredne nastavitve**, izberite **Prilagajanje konfiguracije zbirke podatkov SQL** in nastavite **Določi nabor podatkov za zbirko podatkov aplikacije** na **Predstavitev**.

8. Izpolnite preostala zahtevana polja v čarovniku in potrdite uvajanje. Čas za omogočanje okolja za uporabo se razlikuje na podlagi vrste okolja. Omogočanje uporabe lahko traja do šest ur.

  Ko se uvajanje uspešno zaključi, bo okolje prikazano kot **Uvedeno**.

9. Za potrditev, da je bilo okolje uspešno omogočeno za uporabo, izberite **Prijava** in se prijavite v okolje za potrditev.

![Podrobnosti o okoljih v storitvi ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Uporaba posodobitev za okolje Finance

Za storitev Project Operations je zahtevano okolje Finance z različico aplikacije **10.0.13 (10.0.569.20009)** ali novejšo.

Za prejem te različice boste morda morali zagnati posodobitev kakovosti svojega okolja Finance.

1. V LCS na strani **Podrobnosti o okolju** odprite razdelek **Razpoložljive posodobitve** in izberite **Prikaz posodobitev**.

![Prikaz posodobitev](./media/5ViewUpdates.png)

2. Na strani **Binarne posodobitve** izberite **Shrani paket**.

![Shrani paket](./media/6SavePackage.png)

3. Kliknite **Izberi vse** in nato **Shrani paket**.

![Pregled in shranjevanje posodobitev](./media/7ReviewAndSaveUpdates.png)

4. Vnesite ime in opis paketa, nato pa izberite **Shrani**. Ta postopek lahko traja nekaj časa, odvisno od internetne povezave.

![Nalaganje paketa v knjižnico sredstev](./media/8UploadPackageToAssetsLibrary.png)

5. Ko je paket shranjen, izberite možnost **Končano** in shranite ta paket v knjižnico sredstev v vašem projektu LCS.

Shranjevanje in preverjanje veljavnosti paketa lahko traja približno 15 minut.

6. Če želite uporabiti posodobitev, pojdite na stran **Podrobnosti o okolju** v LCS in izberite **Vzdrževanje** > **Uporabi posodobitve**.

![Vzdrževanje okolij](./media/9MaintainEnvironment.png)

7. Na seznamu posodobitev izberite paket, ki ste ga ustvarili, in izberite **Uporabi**.

![Uporabi posodobitve](./media/10ApplyUpdates.png)

Vzdrževanje okolja bo trajalo nekaj časa. Ko bo končano, se bo okolje vrnilo v stanje ob uvedbi.

![Uvedeno okolje](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Vzpostavite povezavo za dvojno zapisovanje 

1. V projektu LCS odprite stran **Podrobnosti o okolju**.
2. V možnosti **Informacije o okolju Common Data Service** izberite **Povezava do CDS-ja za aplikacije**.
3. Ko je povezava vzpostavljena, ponovno izberite **Povezava do CDS-ja za aplikacije**. Preusmerjeni boste na funkcijo dvojnega zapisovanja v storitvi Finance.

![Povezava do CDS](./media/12LinktoCDS.png)

4. Izberite **Uporabi rešitev**, če želite dostopati do entitet, ki bodo preslikane v integraciji.

![Uporaba rešitev](./media/13ApplySolutions.png)

5. Izberite rešitvi **Preslikava entitete za dvojno pisanje Dynamics 365 Finance and Operations** in **Preslikava entitete za dvojno pisanje Dynamics 365 Project Operations** ter izberite **Uporabi**.

![Potrjevanje rešitev](./media/14ConfirmSolutions.png)

Po uporabi rešitev se entitete za dvojno zapisovanje uporabijo v samem okolju.

![Uporaba rešitev](./media/15ApplyingSolutions.png)

Po uporabi entitet se v okolju prikažejo vse razpoložljive preslikave.

![Zemljevidi entitet za dvojno zapisovanje](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Po posodobitvi osvežite podatkovne vnose

1. V storitvi Finance odprite delovni prostor **Upravljanje podatkov**.

![Delovni prostor »Upravljanje podatkov«](./media/16DataManagement.png)

2. Izberite ploščico **Parametri ogrodja**.

![Parametri ogrodja](./media/17FrameworkParameters.png)

3. Na strani **Nastavitve entitete** izberite **Osveži seznam entitet**.

![Osveži seznam entitet](./media/18RefreshEntityList.png)

Osveževanje bo trajalo približno 20 minut. Ko bo končano, boste prejeli obvestilo.

![Potrditev osveževanja](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Posodobitev varnostnih nastavitev v storitvi Project Operations na Dataverse

1. Pojdite na Project Operations v svojem okolju Dataverse. 
2. Pojdite na **Nastavitve** > **Varnost** > **Varnostne vloge**. 
3. Na strani **Varnostne vloge** na seznamu vlog izberite **uporabnik aplikacije dvojnega zapisovanja** in izberite zavihek **Entitete po meri**.  
4. Prepričajte se, da ima vloga dovoljenji **Branje** in **Prilaganje k** za:
      
      - **Vrsta menjalnega tečaja valute**
      - **Kontni načrt**
      - **Poslovni koledar**
      - **Knjiga**

5. Ko je varnostna vloga posodobljena, pojdite na **Nastavitve** > **Varnost** > **Ekipe** in izberite privzeto ekipo v pogledu ekipe **Lastnik lokalnega podjetja**.
6. Izberite **Upravljanje vlog** in se prepričajte, da je varnostna pravica **uporabnik aplikacije dvojnega zapisovanja** uveljavljena za to ekipo.

## <a name="run-project-operations-dual-write-maps"></a>Zagon zemljevidov za dvojno zapisovanje v aplikaciji Project Operations

1. V projektu LCS odprite stran **Podrobnosti o okolju**.
2. V možnosti **Informacije o okolju Common Data Service** izberite **Povezava do CDS-ja za aplikacije**. Ko izberete povezavo, boste preusmerjeni na seznam entitet v preslikavah.
3. Zaženite zemljevide, kot je opisano v naslednji tabeli. Upoštevajte navedeno zaporedje.

| **Preslikava entitete** | **Osveži entiteto** | **Začetna sinhronizacija** | **Glavni za začetno sinhronizacijo** | **Zaženi predhodne zahteve** | **Začetna sinhronizacija predhodnih zahtev** |
| --- | --- | --- | --- | --- | --- |
| **Vloge projektnih virov za vsa podjetja (bookableresourcecategories)** | No | Da | Common Data Service | No | Ni na voljo |
| **Pravne osebe (cdm\_companies)** | No | Da | Aplikacije Finance and Operations | No | Ni na voljo |
| **Knjiga (msdyn_ledgers)** | No | Da | Aplikacije Finance and Operations | Da | Da, aplikacije Finance and Operations |
| **Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)** | No | No | Ni na voljo | Da | No |
| **Podrobnosti pogodbe (salesorderdetails)** | No | No | Ni na voljo | No | No |
| **Integracijska entiteta za odnose projektne transakcije (msdyn\_transactionconnections)** | No | No | Ni na voljo | No | Ni na voljo |
| **Mejniki podrobnosti pogodbe o integraciji storitve Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Ni na voljo | No | Ni na voljo |
| **Integracijska entiteta za ocene stroškov v storitvi Project Operations (msdyn\_estimateslines)** | No | No | Ni na voljo | No | Ni na voljo |
| **Entiteta za izvoz kategorije stroškov projekta pri integraciji storitve Project Operations (msdyn\_expensecategories)** | No | No | Ni na voljo | No | Ni na voljo |
| **Entiteta za izvoz stroškov projekta pri integraciji storitve Project Operations (msdyn\_expenses)** | Da | No | Ni na voljo | No | Ni na voljo |
| **Integracijska entiteta za oceno časa v storitvi Project Operations (msdyn\_resourceassignments)** | Da | No | Ni na voljo | No | Ni na voljo |


4. Če želite osvežiti entiteto, izberite ime zemljevida in nato **Osveži entitete**. 


![Osveži zemljevid](./media/20RefreshMapping.png)

5. Po zaključenem osveževanju izvajajte zemljevid. Preden omogočite naslednji zemljevid, preverite, ali je zemljevid v tabeli v stanju **Se izvaja**. Izvajanje zemljevidov z večjim številom predhodnih zahtev lahko traja nekaj časa.

Za izvajanje zemljevida s predhodnimi zahtevami omogočite preklopno stikalo **Prikaz zemljevidov povezanih entitet**. Če je v tabeli možnost **Predpogoj za začetno sinhronizacijo** nastavljena na **Ne**, preverite, ali je zastavica **Začetna sinhronizacija** nastavljena na **Izklopljeno** na vseh zahtevanih zemljevidih, preden jih zaženete.

![Zagon zemljevida](./media/21RunMap.png)

6. Preverite, ali se izvajajo vsi s projektom povezani zemljevidi.

![Vsi zemljevidi se izvajajo](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Uporaba konfiguracijskih podatkov v storitvi CDS za Project Operations (izbirno)

Če ste predstavitvene podatke uporabili za okolje Finance in jih želite uporabiti v okolju CDS, glejte [Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations](resource-apply-pro-setup-config-data.md).


Vaše okolje Project Operations je zdaj omogočeno in konfigurirano. 
