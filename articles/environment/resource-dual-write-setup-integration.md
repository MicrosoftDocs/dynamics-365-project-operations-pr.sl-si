---
title: Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov
description: Ta tema vsebuje informacije o nastavitvi in konfiguracij preslikav za dvojno zapisovanje za Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586916"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za entitete nastavitev in konfiguracije.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektne pogodbe, podrobnosti pogodbe in projekti

Projektne pogodbe, pogodbene vrstice in projekti se ustvarjajo v Dataverse in sinhronizirano z aplikacijami Finance in Operations za dodatno računovodstvo. Zapise v teh entitetah je mogoče ustvariti in izbrisati samo v storitvi Dataverse. Vendar pa je mogoče tem zapisom v aplikacijah Finance in Operations dodati računovodske atribute, kot so privzete vrednosti skupine davka na promet in finančne razsežnosti.

  ![Koncepti integracije projektne pogodbe.](./media/1ProjectContract.jpg)

Sledijo se potencialne stranke, priložnosti in ponudbe prodajne dejavnosti Dataverse in ne sinhronizirajte z aplikacijami Finance in Operations, ker s to dejavnostjo ni povezano računovodstvo na nižji stopnji.

Funkcionalnost pogodbe o projektu v Dataverse ustvari zapis projektne pogodbe v aplikacijah Finance in Operations z uporabo **Glave projektne pogodbe (prodajna naročila)** namizni zemljevid. Če shranite projektno pogodbo v storitvi Dataverse, prav tako začnete ustvarjati zapis entitete stranke projektne pogodbe. Ta zapis je sinhroniziran z aplikacijami Finance in Operations z uporabo **Vir financiranja projekta (msdyn\_ projektne pogodbe o deljenem obračunu)** namizni zemljevid. Ta preslikava prav tako sinhronizira tudi dodajanja, posodobitve in brisanja strank projektne pogodbe. Razdeljeni odstotki obračunavanja med naročniki projektne pogodbe se obvladujejo samo v Dataverse in ni sinhroniziran z aplikacijami Finance in Operations.

Po sestavi projektne pogodbe v Dataverse, lahko projektni računovodja posodobi računovodske atribute za to projektno pogodbo v aplikacijah Finance in Operations, tako da odpre **Vodenje projektov in računovodstvo** > **Projektne pogodbe** > **Nastaviti** > **Pokaži privzeto računovodstvo**. Računovodja lahko pregleda operativne atribute pogodbe o projektu, kot sta zahtevani datum dobave in znesek pogodbe, tako da izbere ID pogodbe o projektu v aplikacijah Finance in Operations, ki odpre povezani zapis projektne pogodbe v Dataverse.

Entiteta projekta je sinhronizirana z aplikacijami Finance in Operations z uporabo **Projekti V2 (msdyn\_ projekti)** namizni zemljevid. Računovodja projekta lahko izvede ta dejanja:

  - Preglejte projekte v aplikacijah Finance in Operations, tako da odprete **Vodenje projektov in računovodstvo** > **Vsi projekti**. 
  - Posodobite računovodske atribute za projekt v aplikacijah Finance in Operations, tako da odprete **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Nastaviti** > **Pokaži privzeto računovodstvo**.  
  - Preglejte operativne atribute projekta, kot so predvideni začetni in končni datumi, tako da izberete ID projekta v aplikacijah Finance in Operations, ki odpre povezani zapis projekta v Dataverse.

Projekt je povezan s projektno pogodbo prek entitete **Podrobnosti projektne pogodbe**.

Projektne pogodbene vrstice v Dataverse ustvari pravilo za obračun projektne pogodbe v aplikacijah Finance in Operations z uporabo **Pogodbene vrstice projekta (podrobnosti o prodajnem naročilu)** namizni zemljevid. Metoda obračunavanja definira vrsto pravila za obračun pogodbe o projektu v aplikacijah Finance in Operations:

  - Podrobnosti projektne pogodbe z načinom obračunavanja časa in materiala ustvarjajo vrsto pravila za obračunavanje časa in materiala.
  - Podrobnosti pogodbe z načinom obračunavanja »Fiksna cena« ustvarijo pravilo mejnika obračunavanja.

Projektne pogodbe lahko računovodja projekta pregleda v aplikacijah Finance in Operations, tako da obiščete **Vodenje projektov in računovodstvo** > **Projektne pogodbe** > **Nastaviti** > **Pokaži privzeto računovodstvo**, in pregled podrobnosti o **Pogodbene vrstice** zavihek. Računovodja lahko na tem zavihku nastavi tudi privzete finančne razsežnosti za pogodbene vrstice načina obračunavanja s fiksno ceno.

## <a name="billing-milestones"></a>Mejniki obračunavanja

Podrobnosti projektne pogodbe, ki uporabljajo način obračunavanja »Fiksna cena«, se fakturirajo prek mejnikov obračunavanja. Mejniki zaračunavanja se sinhronizirajo s projektiranjem transakcij na računu v aplikacijah Finance in Operations z uporabo **Mejniki pogodbene linije za integracijo projektnih operacij (msdyn\_ pogodbena linija razpored vrednosti)** namizni zemljevid.

  ![Integracija mejnikov obračunavanja.](./media/2Milestones.jpg)

Računovodja lahko pregleda transakcije na računu in prilagodi atribute računovodstva za te transakcije tako, da se pomakne v razdelek **Pregled upravljanja projektov in računovodstva** > **Projektne pogodbe** > **Vzdrževanje** > **Transakcije za kupca** ali **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Vzdrževanje** > **Transakcije za kupca**.

Ko prvič ustvarite mejnik obračunavanja za določeno podrobnost projektne pogodbe, sistem samodejno ustvari projekt s predvidenimi prihodki s fiksno ceno za projekt, povezan s to podrobnostjo pogodbe. Projekte s predvidenimi prihodki s fiksno ceno je mogoče pregledati v razdelku **Upravljanje projektov in računovodstvo** > **Projekti s predvidenimi prihodki s fiksno ceno**.

### <a name="project-tasks"></a>Projektna opravila

Projektne naloge se sinhronizirajo z aplikacijami Finance in Operations prek **Projektne naloge (msdyn\_ projektna opravila)** zemljevid tabele samo za referenčne namene. Ustvarjanje, posodabljanje in brisanje operacij ni podprto v aplikacijah Finance in Operations.

  ![Integracija opravil projekta.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Viri projekta

The **Vloge projektnih virov** entiteta se sinhronizira z aplikacijami Finance in Operations z uporabo **Vloge projektnih virov za vsa podjetja (kategorije virov, ki jih je mogoče rezervirati)** zemljevid tabele samo za referenčne namene. Ker vloge virov v Dataverse niso specifični za podjetje, sistem samodejno ustvari ustrezne zapise o vlogah virov, specifičnih za podjetje, v aplikacijah Finance in Operations za vse pravne osebe, vključene v obseg integracije z dvojnim pisanjem.

![Integracija vlog virov.](./media/5Resources.jpg)

Projektni viri v projektnih operacijah se vzdržujejo v Dataverse in niso sinhronizirani z aplikacijami Finance in Operations.

### <a name="transaction-categories"></a>Kategorije transakcij

Kategorije transakcij se vzdržujejo v Dataverse in sinhronizirano z aplikacijami Finance in Operations z uporabo **Kategorije projektnih transakcij (msdyn\_ kategorije transakcij)** namizni zemljevid. Po sinhronizaciji zapisa kategorije transakcij sistem samodejno ustvari štiri zapise skupnih kategorij. Vsak zapis ustreza vrsti transakcije v aplikacijah Finance in Operations in jih povezuje z zapisom kategorije transakcije.

![Integracija kategorije transakcij.](./media/4TransactionCategories.jpg)

Uporaba kategorij transakcij za ocene in dejanske vrednosti zahteva, da računovodja projekta ali sistemski skrbnik ustvari ustrezne kategorije projektov v vsaki pravni osebi. Za več informacij glejte [Konfiguracija kategorij projekta](../project-accounting/configure-project-categories.md).
