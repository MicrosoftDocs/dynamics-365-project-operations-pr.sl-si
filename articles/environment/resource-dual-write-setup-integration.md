---
title: Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov
description: Ta članek vsebuje informacije o nastavljanju in konfiguriranju zemljevidov dvojnega pisanja Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029172"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek ponuja informacije o integraciji dvojnega pisanja Project Operations za nastavitve in konfiguracijske entitete.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektne pogodbe, podrobnosti pogodbe in projekti

Projektne pogodbe, pogodbene linije in projekti so ustvarjeni v Dataverse in sinhroniziran z aplikacijami za finance in poslovanje za dodatno računovodstvo. Zapise v teh entitetah je mogoče ustvariti in izbrisati samo v storitvi Dataverse. Vendar je mogoče tem zapisom v aplikacijah za finance in poslovanje dodati računovodske atribute, kot so privzete vrednosti skupine prometnega davka in finančne razsežnosti.

  ![Koncepti integracije projektne pogodbe.](./media/1ProjectContract.jpg)

Sledijo se prodajne aktivnosti, priložnosti in ponudbe Dataverse in ne sinhronizirajte z aplikacijami za finance in poslovanje, ker s to dejavnostjo ni povezano računovodstvo na nižji stopnji.

Funkcionalnost projektne pogodbe v Dataverse ustvari zapis pogodbe o projektu v aplikacijah za finance in operacije z uporabo **Glave projektnih pogodb (prodajna naročila)** namizni zemljevid. Če shranite projektno pogodbo v storitvi Dataverse, prav tako začnete ustvarjati zapis entitete stranke projektne pogodbe. Ta zapis je sinhroniziran z aplikacijami za finance in poslovanje z uporabo **Vir financiranja projekta (msdyn\_ projectcontractssplitbillingrules)** namizni zemljevid. Ta preslikava prav tako sinhronizira tudi dodajanja, posodobitve in brisanja strank projektne pogodbe. Razdeljene obračunske odstotke med projektnimi pogodbenimi strankami obvladujemo samo v Dataverse in ni sinhroniziran z aplikacijami za finance in poslovanje.

Po sklenitvi projektne pogodbe v Dataverse, lahko računovodja projekta posodobi računovodske atribute za to projektno pogodbo v aplikacijah za finance in operacije tako, da obišče **Vodenje projektov in računovodstvo** > **Projektne pogodbe** > **Nastaviti** > **Prikaži privzeto računovodstvo**. Računovodja lahko pregleda operativne atribute projektne pogodbe, kot sta zahtevani datum dobave in znesek pogodbe, tako da izbere ID projektne pogodbe v aplikacijah za finance in operacije, ki odpre povezani zapis pogodbe o projektu v Dataverse.

Entiteta projekta je sinhronizirana z aplikacijami za finance in poslovanje z uporabo **Projekti V2 (msdyn\_ projekti)** namizni zemljevid. Računovodja projekta lahko izvede ta dejanja:

  - Preglejte projekte v aplikacijah za finance in poslovanje tako, da obiščete **Vodenje projektov in računovodstvo** > **Vsi projekti**. 
  - Posodobite računovodske atribute za projekt v aplikacijah za finance in operacije tako, da obiščete **Vodenje projektov in računovodstvo** > **Vsi projekti** > **Nastaviti** > **Prikaži privzeto računovodstvo**.  
  - Preglejte operativne atribute projekta, kot sta predvideni začetni in končni datum, tako da izberete ID projekta v aplikacijah za finance in operacije, ki odpre povezani zapis projekta v Dataverse.

Projekt je povezan s projektno pogodbo prek entitete **Podrobnosti projektne pogodbe**.

Projektne pogodbe vrstice v Dataverse ustvari pravilo za obračunavanje projektne pogodbe v aplikacijah za finance in operacije z uporabo **Projektne pogodbene vrstice (podrobnosti o prodajnem nalogu)** namizni zemljevid. Metoda zaračunavanja določa vrsto pravila za zaračunavanje projektne pogodbe v aplikacijah za finance in operacije:

  - Podrobnosti projektne pogodbe z načinom obračunavanja časa in materiala ustvarjajo vrsto pravila za obračunavanje časa in materiala.
  - Podrobnosti pogodbe z načinom obračunavanja »Fiksna cena« ustvarijo pravilo mejnika obračunavanja.

Projektne pogodbene vrstice lahko pregleda računovodja projekta v aplikacijah za finance in poslovanje tako, da obišče **Vodenje projektov in računovodstvo** > **Projektne pogodbe** > **Nastaviti** > **Prikaži privzeto računovodstvo**, in pregledovanje podrobnosti na **Pogodbene vrstice** zavihek. Računovodja lahko na tem zavihku nastavi tudi privzete finančne razsežnosti za pogodbene vrstice metode zaračunavanja po fiksni ceni.

## <a name="billing-milestones"></a>Mejniki obračunavanja

Podrobnosti projektne pogodbe, ki uporabljajo način obračunavanja »Fiksna cena«, se fakturirajo prek mejnikov obračunavanja. Mejniki zaračunavanja so sinhronizirani za projiciranje transakcij na računu v aplikacijah za finance in poslovanje z uporabo **Mejniki pogodbene vrstice integracije projektnih operacij (msdyn\_ contractlinescheduleofvalues)** namizni zemljevid.

  ![Integracija mejnikov obračunavanja.](./media/2Milestones.jpg)

Računovodja lahko pregleda transakcije na računu in prilagodi atribute računovodstva za te transakcije tako, da se pomakne v razdelek **Pregled upravljanja projektov in računovodstva** > **Projektne pogodbe** > **Vzdrževanje** > **Transakcije za kupca** ali **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Vzdrževanje** > **Transakcije za kupca**.

Ko prvič ustvarite mejnik obračunavanja za določeno podrobnost projektne pogodbe, sistem samodejno ustvari projekt s predvidenimi prihodki s fiksno ceno za projekt, povezan s to podrobnostjo pogodbe. Projekte s predvidenimi prihodki s fiksno ceno je mogoče pregledati v razdelku **Upravljanje projektov in računovodstvo** > **Projekti s predvidenimi prihodki s fiksno ceno**.

### <a name="project-tasks"></a>Projektna opravila

Projektne naloge so sinhronizirane z aplikacijami za finance in poslovanje prek **Projektne naloge (msdyn\_ projektne naloge)** tabelni zemljevid samo za referenčne namene. Ustvarjanje, posodabljanje in brisanje operacij ni podprto v aplikacijah za finance in operacije.

  ![Integracija opravil projekta.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Viri projekta

The **Vloge projektnih virov** subjekt je sinhroniziran z aplikacijami za finance in poslovanje z uporabo **Vloge projektnih virov za vsa podjetja (bookableresourcecategories)** tabelni zemljevid samo za referenčne namene. Ker vloge virov v Dataverse niso specifične za podjetje, sistem samodejno ustvari ustrezne zapise vlog virov, specifične za podjetje, v aplikacijah za finance in operacije samodejno za vse pravne osebe, vključene v obseg integracije z dvojnim pisanjem.

![Integracija vlog virov.](./media/5Resources.jpg)

Projektni viri v projektnih operacijah se vzdržujejo v Dataverse in niso sinhronizirani z aplikacijami za finance in poslovanje.

### <a name="transaction-categories"></a>Kategorije transakcij

Kategorije transakcij se vzdržujejo v Dataverse in sinhroniziran z aplikacijami za finance in poslovanje z uporabo **Kategorije projektnih transakcij (msdyn\_ kategorije transakcij)** namizni zemljevid. Po sinhronizaciji zapisa kategorije transakcij sistem samodejno ustvari štiri zapise skupnih kategorij. Vsak zapis ustreza vrsti transakcije v aplikacijah za finance in operacije ter jih povezuje z zapisom kategorije transakcije.

![Integracija kategorije transakcij.](./media/4TransactionCategories.jpg)

Uporaba kategorij transakcij za ocene in dejanske vrednosti zahteva, da računovodja projekta ali sistemski skrbnik ustvari ustrezne kategorije projektov v vsaki pravni osebi. Za več informacij glejte [Konfiguracija kategorij projekta](../project-accounting/configure-project-categories.md).
