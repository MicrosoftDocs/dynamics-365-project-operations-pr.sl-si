---
title: Določanje vrste uvedbe
description: Ta tema vsebuje informacije za pomoč pri izbiri prave vrste uvajanja za projektne postopke v vašem podjetju.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084760"
---
# <a name="determine-your-deployment-type"></a>Določanje vrste uvedbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

> [!IMPORTANT]
> Po nakupu licence določite najboljši model uvajanja v aplikaciji Dynamics 365 Project Operations z uporabo [vodenega postopka namestitve](https://aka.ms/provisionprojectoperations).
> Ko dokončate vodeni postopek namestitve, boste preusmerjeni na pravi portal za upravljanje, da dokončate namestitev. Za dokončanje namestitve glejte podrobnosti o uvajanju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Obstoječe stranke rešitve Dynamics, ki uporabljajo aplikacijo Dynamics 365 Project Service Automation
Aplikacija Project Operations vključuje zmogljivosti, ki so bile na voljo v aplikaciji Project Service Automation. Za te stranke bo v prihodnosti objavljena možnost nadgraditve.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Obstoječe stranke aplikacije Dynamics 365 Finance, ki uporabljajo Projektno vodenje in računovodstvo 

Obstoječe stranke aplikacije Finance, ki uporabljajo projektno upravljanje in računovodske funkcije, lahko to še naprej uporabljajo v dozdajšnji obliki. Glejte razdelek [Aplikacija Project Operations za scenarije z naročili na zalogi/v proizvodnji](#pma).


## <a name="deployment-types"></a>Vrste uvajanja
Aplikacija Project Operations podpira več možnosti uvajanja, ki ustrezajo vašim zahtevam. Ne glede na to, ali ste nov ali obstoječ uporabnik rešitve Dynamics 365, lahko aplikacija Project Operations ustreza vašim zahtevam.

Naš [vprašalnik o uvajanju](https://aka.ms/provisionprojectoperations) vam bo pomagal določiti pravo vrsto uvajanja. Rezultati vas bodo vodili do enega od naslednjih vrst uvajanja:

- [Poenostavljeno uvajanje – posel do izstavitve predračuna](#lite)
- [Project Operations za primere uporabe z viri/brez zalog](#integrated)
- [Project Operations za primere uporabe z naročili na zalogi/v proizvodnji](#pma)

Aplikacija Project Operations podpira primere naročil na zalogi/v proizvodnji in primere z viri/brez zalog v istem okolju prek konfiguracij na ravni pravne osebe. Družba Contoso lahko na primer izkoristi zmogljivosti zalog/proizvodnih naročil v svojem ameriškem proizvodnem obratu (pravna oseba = Contoso Manufacturing United States). Družba Contoso lahko na primer izkoristi zmogljivosti virov/brez zalog v njihovem obratu za servisiranje Contoso Robotics Arms v ZK (pravna oseba = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Poenostavljeno uvajanje – posel do izstavitve predračuna

Poenostavljeno uvajanje vključuje naslednje zmožnosti:

- Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project
- Večrazsežnostno oblikovanje cen
- Poenoteno upravljanje virov
- Sledenje času
- Osnovne stroške
- Predloge računov

#### <a name="deployment-steps"></a>Koraki uvajanja
Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).

Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](lite-preview-subscription-sign-up.md) in [Omogočanje novega okolja](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations za primere uporabe z viri/brez zalog
Projektni postopki za primere z viri/brez zalog vključujejo naslednje zmožnosti:
  
- Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project
- Večrazsežnostno oblikovanje cen
- Poenoteno upravljanje virov
- Sledenje času
- Osnovne stroške
- Celotni stroški
- Optično branje računov s tehnologijo OCR
- Celoten postopek izdaje računa
- Pripoznavanje prihodkov

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

