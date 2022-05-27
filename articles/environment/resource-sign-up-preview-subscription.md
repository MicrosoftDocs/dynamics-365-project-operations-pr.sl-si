---
title: Prijava za naročnino na predogledno različico storitve Project Operations za primere uporabe z viri/brez zalog
description: Ta tema ponuja informacije o tem, kako se naročiti in uvesti storitev Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575830"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijava za naročnino na predogledno različico storitve Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_



Ta tema vsebuje informacije o tem, kako se naročiti na preskusno različico in uvesti okolje storitve Project Operations za scenarije, ki temeljijo na virih/nezalogi.

## <a name="prerequisites"></a>Zahteve
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure. Med prvim koriščenjem ponudbe lahko ustvarite najemnika. 
- Za uvedbo finančnega okolja je potrebna veljavna naročnina na Azure, ki se zaračuna za posamezno okolje. Za začetek lahko uporabite obstoječo naročnino svoje organizacije ali [preskusno različico Azure](https://azure.microsoft.com/free/). Okolje CDS bo na voljo za 30-dnevno brezplačno uporabo.

> [!IMPORTANT]
> To nalogo mora opraviti samo ena oseba in sicer skrbnik najemnika v organizaciji. Če niste naročnik te izdaje, počakajte, da se organizacija prijavi in prejmete svoje uporabniške poverilnice.
> 
> Preskusne različice v najemniku so namenjene enkratni uporabi. Preskusno različico lahko namestite samo enkrat. Priporočamo, da za preskusno različico ustvarite novega najemnika.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – preskusna različica za predogled 

Preden začnete, se prepričajte, da ste prijavljeni v brskalnik z uporabnikovim službenim računom v najemniku, kjer želite imeti predogled aplikacije Project Operations.

1. Unovčite prvo kodo v okviru ponudbe **Dynamics 365 Project Operations**, in sicer tukaj [Preskusna različica aplikacije Project Operations](https://aka.ms/try-po).
2. Potrdite svoje naročilo.

  Videli boste, da je bila ponudba za potrditev uspešno izkoriščena.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance predogled preskusne različice

Pojdite v razdelek [Dynamics 365 za preskusno različico storitve Finance](https://aka.ms/trypoche) in ponovite korake iz prejšnjega razdelka s ponudbo, »Prijava za okolje, gostovano v oblaku«.  

## <a name="assign-licenses"></a>Dodeljevanje licenc

> [!IMPORTANT]
> Potrebovali boste skrbniški dostop do portala Microsoft 365 vaše organizacije, če želite dokončati naslednje korake.

1. Pojdi do [Microsoft 365 skrbniško središče](https://portal.office.com/) za dodelitev licenc vašim uporabnikom.

2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.

3. Prepričajte se, da ste izbrali licenco **Dynamics 365 Project Operations**, in izberite možnost **Shrani spremembe**.

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
Ta korak dokončajte šele, ko je predstavitveno okolje storitve Finance uvedeno in ko so predstavitveni podatki pripravljeni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
