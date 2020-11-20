---
title: Določanje vrste uvedbe
description: Ta tema vsebuje informacije za pomoč pri izbiri prave vrste uvajanja za projektne postopke v vašem podjetju.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401238"
---
# <a name="determine-your-deployment-type"></a>Določanje vrste uvedbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

> [!IMPORTANT]
> Po nakupu licence določite najboljši model uvajanja v aplikaciji Dynamics 365 Project Operations z uporabo [vodenega postopka namestitve](https://aka.ms/provisionprojectoperations).
> Ko dokončate vodeni postopek namestitve, boste preusmerjeni na pravi portal za upravljanje, da dokončate namestitev. Za dokončanje namestitve glejte podrobnosti o uvajanju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Obstoječe stranke rešitve Dynamics, ki uporabljajo aplikacijo Dynamics 365 Project Service Automation
Aplikacija Project Operations vključuje zmogljivosti, ki so bile na voljo v aplikaciji Project Service Automation. Pot nadgradnje bo tem strankam izdana v 1. valu izdaj za leto 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Obstoječe stranke aplikacije Dynamics 365 Finance, ki uporabljajo Projektno vodenje in računovodstvo 

Obstoječe stranke rešitve Finance, ki uporabljajo funkcionalnost upravljanja projektov in računovodstva lahko nadaljujejo z uporabo rešitve, kakršna je. Glejte razdelek [Aplikacija Project Operations za scenarije z naročili na zalogi/v proizvodnji](#pma).


## <a name="deployment-types"></a>Vrste uvajanja
Aplikacija Project Operations podpira več možnosti uvajanja, ki ustrezajo vašim zahtevam. Ne glede na to, ali ste nov ali obstoječ uporabnik rešitve Dynamics 365, lahko aplikacija Project Operations ustreza vašim zahtevam.

Naš [vprašalnik o uvajanju](https://aka.ms/provisionprojectoperations) vam bo pomagal določiti pravo vrsto uvajanja. Rezultati vas bodo vodili do enega od naslednjih vrst uvajanja:

- [Poenostavljeno uvajanje – posel do izstavitve predračuna](#lite)
- [Project Operations za primere uporabe z viri/brez zalog](#integrated)
- [Project Operations za primere uporabe z naročili na zalogi/v proizvodnji](#pma)

Aplikacija Project Operations podpira primere naročil na zalogi/v proizvodnji in primere z viri/brez zalog v istem okolju prek konfiguracij na ravni pravne osebe. Družba Contoso lahko na primer izkoristi zmogljivosti zalog/proizvodnih naročil v svojem ameriškem proizvodnem obratu (pravna oseba = Contoso Manufacturing United States). Družba Contoso lahko na primer izkoristi zmogljivosti virov/brez zalog v njihovem obratu za servisiranje Contoso Robotics Arms v ZK (pravna oseba = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Poenostavljeno uvajanje – posel do izstavitve predračuna

Poenostavljeno uvajanje vključuje naslednje zmožnosti:

- Prodajni proces za projekte, ki razširja izkušnje aplikacije Dynamics 365 Sales
- Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project
- Večrazsežnostno oblikovanje cen
- Poenoteno upravljanje virov
- Sledenje času
- Osnovni stroški
- Predračun in izstavljanje računov za stranke 

#### <a name="deployment-steps"></a>Koraki uvajanja
Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).

Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](lite-preview-subscription-sign-up.md) in [Omogočanje novega okolja](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations za primere uporabe z viri/brez zalog
Projektni postopki za primere z viri/brez zalog vključujejo naslednje zmožnosti:
 
- Prodajni proces za projekte, ki razširja aplikacijo Dynamics 365 Sales
- Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project
- Večrazsežnostno oblikovanje cen
- Poenoteno upravljanje virov
- Sledenje času
- Osnovni stroški
- Celoten strošek
- Optično branje računov s tehnologijo OCR
- Predračun in izstavljanje računov za stranke 
- Pripoznavanje prihodkov za projekte

#### <a name="deployment-steps"></a>Koraki uvajanja
Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).

Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](resource-sign-up-preview-subscription.md) in [Omogočanje novega okolja](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations za primere uporabe z naročili na zalogi/v proizvodnji

- Načrtovanje projekta z uporabo SČD
- Upravljanje virov
- Sledenje času
- Celotni stroški
- Optično branje računov s tehnologijo OCR
- Celoten postopek izdaje računa
- Pripoznavanje prihodkov
- Proizvodna naročila
- Podpora za materiale

#### <a name="deployment-steps"></a>Koraki uvajanja
Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).

Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) in [Omogočanje novega okolja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

