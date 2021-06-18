---
title: Prijava za naročnino na predogledno različico storitve Project Operations za primere uporabe z viri/brez zalog
description: Ta tema ponuja informacije o tem, kako se naročiti in uvesti storitev Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000456"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijava za naročnino na predogledno različico storitve Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ta tema razlaga, kako se naročite na predogled/ponudbo za partnerje in uvedete okolje Project Operations za primere uporabe z viri/brez zalog.

## <a name="prerequisites"></a>Zahteve

- Prejeli boste e-poštno sporočilo z vabilom k sodelovanju v predogledu. Predogled lahko zahtevate na [spletnem mestu storitve Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure.
- Za uvedbo finančnega okolja je potrebna veljavna naročnina na Azure, ki se zaračuna za posamezno okolje. Za začetek lahko uporabite obstoječo naročnino svoje organizacije ali [preskusno različico Azure](https://azure.microsoft.com/en-us/free/). Okolje CDS bo na voljo za 30-dnevno brezplačno uporabo.

## <a name="subscribe"></a>Naročite se

Ko bo vaša [zahteva za predogled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) odobrena, boste od Microsofta po elektronski pošti prejeli tri ponudbe. Te ponudbe omogočajo uvedbo predogleda Project Operations:

- Dynamics 365 Project Operations (CRM) – predogled preskusne različice
- Office 365 Project Operations – poskusna različica
- Dynamics 365 Finance – preskus predogleda

> [!IMPORTANT]
> To nalogo mora opraviti samo ena oseba in sicer skrbnik najemnika v organizaciji. Če niste naročnik te izdaje, počakajte, da se organizacija prijavi in prejmete svoje uporabniške poverilnice.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – predogled preskusne različice 

Preden začnete, se prepričajte, da ste prijavljeni v brskalnik z uporabnikovim službenim računom v najemniku, kjer želite imeti predogled aplikacije Project Operations.

1. Unovčite prvo promocijsko kodo **Dynamics 365 Project Operations (CRM) – predogled preskusne različice**, tako da jo prilepite v URL brskalnika.

![Prevzem ponudbe](./media/16RedeemFirstOfferNew.png)

2. Potrdite svoje naročilo.

![Potrdite naročilo](./media/17ConfirmOrderNew.png)

Videli boste, da je bila ponudba za potrditev uspešno izkoriščena.

![Potrditev](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – poskusna različica

Ponovite enake korake kot pri kodi prve ponudbe. Ne pozabite dodati kode druge ponudbe z istim uporabniškim računom, ki je bil uporabljen za kodo prve ponudbe.

### <a name="dynamics-365-finance-preview-trial"></a>Preskus predogleda storitve Dynamics 365 Finance

Ponovite iste korake z zadnjo ponudbo iz e-poštnega sporočila z dobrodošlico.

## <a name="assign-licenses"></a>Dodeljevanje licenc

> [!IMPORTANT]
> Potrebovali boste skrbniški dostop do portala Microsoft 365 vaše organizacije, če želite dokončati naslednje korake.

1. Odprite [skrbniško središče za Microsoft 365](https://portal.office.com/), da dodelite licence svojim uporabnikom.

![Začetna stran skrbniškega središča](./media/14AdminPortal.png)

2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.

![Dodeljevanje licenc](./media/15AssignLicenses.png)

3. Preverite, ali sta bili izbrani licenci **Predogledna različica Dynamics 365 Project Operations (CRM)** in **Office 365 Project Operations – Predogled** in izberite **Shrani spremembe**.

> [!NOTE]
> Preskusne ponudbe storitve Finance ni treba dodeliti uporabniku.

## <a name="start-a-new-project-in-lcs"></a>Začetek novega projekta LCS

Ustvarite nov projekt LCS, kot je opisano v temi [Začnite nov projekt v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodajanje naročnine na Azure projektu LCS

Za dokončanje te naloge sledite korakom v temi [Dodajanje naročnine na Azure projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Uvedba predstavitvenega okolja Finance s storitvijo Project Operations za primere uporabe z viri/brez zalog

Sledite navodilom v temi [Zagotovitev novega okolja](resource-provision-new-environment.md), da dokončate uvajanje. Za predogled uporabite vrsto uvajanja za [predstavitveno okolje](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment). 

## <a name="install-cds-setup-and-configuration-data"></a>Namestitev podatkov za nastavitev in konfiguracijo CDS

Namestite podatke za nastavitev in konfiguracijo CDS, kot je opisano v temi [Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service](resource-apply-pro-setup-config-data.md).
Ta korak dokončajte šele, ko bo predstavitveno okolje Finance uvedeno in bodo predstavitveni podatki v FO-ju pripravljeni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]