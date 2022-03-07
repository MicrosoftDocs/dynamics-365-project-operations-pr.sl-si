---
title: Integracija računa dobavitelja
description: Ta tema vsebuje informacije o integraciji računa dobavitelja v aplikaciji Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986511"
---
# <a name="vendor-invoice-integration"></a>Integracija računa dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Projektna naročila iz rešitve Dynamics 365 Project Operations lahko beležite tako, da odprete razdelek **Obveznosti** > **Računi** > **Čakajoči računi prodajalcev** in uporabite dokument čakajočega računa dobavitelja. Za več informacij preberite razdelek [Nakup materialov, ki niso na zalogi, z uporabo čakajočih računov dobavitelja](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Preden uporabite funkcijo, opisano v tej temi, preglejte zahtevane konfiguracije in jih uporabite. Za več informacij glejte [Omogočanje materialov, ki niso na zalogi, in čakajočih računov dobavitelja](../procurement/configure-materials-nonstocked.md).

V aplikaciji Project Operations so računi dobavitelja, povezani s projektom, knjiženi s posebnimi pravili knjiženja:

- Projektni stroški (vključno z nevračljivim davkom) niso takoj knjiženi na račun stroškov projekta v glavni knjigi. Namesto tega so stroški knjiženi na **Račun za integracijo naročil**. Ta račun je konfiguriran v razdelku **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Vodenje projektov in računovodski parametri** na zavihku **Project Operations v aplikaciji Dynamics 365 Customer Engagement**.
- Z dvojnim zapisovanjem se podrobnosti računa dobavitelja sinhronizirajo s storitvijo Microsoft Dataverse z uporabo naslednjih preslikav tabel:

     - **Izvozna entiteta računa dobavitelja projekta za integracijo v Project Operations(msdyn_projectvendorinvoices)**: ta preslikava tabele sinhronizira informacije iz glave računa dobavitelja. S storitvijo Dataverse so sinhronizirani samo računi dobaviteljev z vsaj eno vrstico, ki vsebuje ID projekta.
     - **Izvozna entiteta vrstice računa dobavitelja projekta za integracijo v Project Operations(msdyn_projectvendorinvoicelines)**: ta preslikava tabele sinhronizira informacije iz vrstice računa dobavitelja. S storitvijo Dataverse so sinhronizirane samo vrstice, ki vsebujejo ID projekta.

     > [!NOTE]
     > Podrobnosti o računu dobavitelja v storitvi Dataverse ni mogoče urejati.

Pomožna poslovna knjiga za davke, dobavitelje in druga finančna knjiženja so v aplikaciji Dynamics 365 Finance zabeležena, kot je ustrezno v času knjiženja računa dobavitelja.

![Integracija računa dobavitelja.](media/DW7VendorInvoice.png)

Ko so zapisi v storitvi Dataverse zapisani v entiteti **Račun dobavitelja**, se začne avtomatiziran postopek odobritve zapisov. Po potrebi lahko v storitvi Dataverse stanje avtomatiziranega postopka odobritve preverite tako, da odprete razdelek **Napredne nastavitve** > **Sistem** > **Sistemska opravila**. Po končani odobritvi sistem v entiteti **Dejanske vrednosti** ustvari zapise razreda materialne transakcije.

Dejanske vrednosti, povezane z materiali, so nato obdelane s preslikavo tabele za dvojno zapisovanje **Dejanske vrednosti integracije za Project Operations (msdyn_actuals)**. Za več informacij si preberite razdelek [Ocene in dejanske vrednosti projekta](resource-dual-write-estimates-actuals.md).

Periodični postopek **Uvoz iz pripravljalne tabele** ustvari vrstice dnevnika, povezane z računom dobavitelja, v dnevniku integracij za Project Operations. Protikonto privzeto velja za račun za integracijo naročil. Ko je dnevnik integracije knjiženja objavljen, je za transakcijo računa dobavitelja počiščen saldo konta, znesek stroškov iz vrstice pa je premeščen na račun stroškov projekta. Prav tako so ustvarjene transakcije pomožne poslovne knjige za namene izdajanja računov in prepoznavanja prihodkov.
