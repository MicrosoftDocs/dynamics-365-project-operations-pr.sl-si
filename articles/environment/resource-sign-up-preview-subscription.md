---
title: Prijava za naročnino na predogledno različico storitve Project Operations za primere uporabe z viri/brez zalog
description: Ta tema ponuja informacije o tem, kako se naročiti in uvesti storitev Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949082"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijava za naročnino na predogledno različico storitve Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema razlaga, kako se naročite na predogled/ponudbo za partnerje in uvedete okolje Project Operations za primere uporabe z viri/brez zalog.

## <a name="prerequisites"></a>Zahteve

- Prejeli boste e-poštno sporočilo z vabilom k sodelovanju v predogledu. Predogled lahko zahtevate na [spletnem mestu storitve Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure.
- Za uvedbo finančnega okolja je potrebna veljavna naročnina na Azure, ki se zaračuna za posamezno okolje. Za začetek lahko uporabite obstoječo naročnino svoje organizacije ali [preskusno različico Azure](https://azure.microsoft.com/en-us/free/). Okolje CDS bo na voljo za 30-dnevno brezplačno uporabo.

## <a name="subscribe"></a>Naročite se

Ko bo vaša [zahteva za predogled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) odobrena, boste od Microsofta po elektronski pošti prejeli dve ponudbi. Te ponudbe omogočajo uvedbo predogleda Project Operations:

- Dynamics 365 Project Operations – preskus predogleda
- Preskus predogleda storitve Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> To nalogo mora opraviti samo ena oseba in sicer skrbnik najemnika v organizaciji. Če niste naročnik te izdaje, počakajte, da se organizacija prijavi in prejmete svoje uporabniške poverilnice.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – preskus predogleda

1. Prevzemite prvo ponudbo, **preskus storitve Dynamics 365 Project Operations**, z URL-jem, navedenim v e-poštnem sporočilu z dobrodošlico.

![Prva ponudba](./media/1FirstOffer.png)

2. Preverite, ali ste prijavljeni kot uporabnik, ki pripada organizaciji, ki se bo naročila na storitev.
3. Nadaljujte z unovčenjem ponudbe. 
4. Izberite **Da, možnost dodaj v moj račun**.

![Prevzem ponudbe](./media/2RedeemFirstOffer.png)

![Potrditev ponudbe](./media/3ConfirmFirstOffer.png)

![Ponudba prevzeta](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Preskus predogleda storitve Dynamics 365 Finance

Ponovite iste korake z drugo ponudbo iz e-poštnega sporočila z dobrodošlico.

## <a name="assign-licenses"></a>Dodeljevanje licenc

> [!IMPORTANT]
> Potrebovali boste skrbniški dostop do portala Office 365 vaše organizacije, če želite dokončati naslednje korake.

1. Odprite [skrbniško središče za Microsoft 365](https://portal.office.com/), da dodelite licence svojim uporabnikom.

![Skrbniški portal za Office](./media/5OfficeAdminPortal.png)

2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.

![Dodeljevanje licenc](./media/6AssignLicenses.png)

3. Preverite, ali je bila izbrana licenca Project Operations, in izberite **Shrani spremembe**. 

> [!NOTE]
> Preskusne ponudbe storitve Finance ni treba dodeliti uporabniku.

## <a name="start-a-new-project-in-lcs"></a>Začetek novega projekta LCS

Ustvarite nov projekt LCS, kot je opisano v temi [Začnite nov projekt v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodajanje naročnine na Azure projektu LCS

Za dokončanje te naloge sledite korakom v temi [Dodajanje naročnine na Azure projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Uvedba predstavitvenega okolja Finance s storitvijo Project Operations za primere uporabe z viri/brez zalog

Sledite navodilom v temi [Zagotovitev novega okolja](resource-provision-new-environment.md), da dokončate uvajanje. Za predogled uporabite vrsto uvajanja za [predstavitveno okolje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).

## <a name="install-cds-setup-and-configuration-data"></a>Namestitev podatkov za nastavitev in konfiguracijo CDS

Namestite podatke za nastavitev in konfiguracijo CDS, kot je opisano v temi [Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service](resource-apply-pro-setup-config-data.md).

