---
title: Določanje vrste uvedbe
description: Ta članek vsebuje informacije, ki vam bodo pomagale določiti pravilno vrsto uvajanja operacij projekta za vaše podjetje.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912214"
---
# <a name="determine-your-deployment-type"></a>Določanje vrste uvedbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

> [!IMPORTANT]
> Po nakupu licence začnite lahko tukaj ugotovite najboljši model uvajanja za Dynamics 365 Project Operations z uporabo [vodenega poteka namestitve](https://aka.ms/provisionprojectoperations).
> Ko dokončate vodeni postopek namestitve, boste preusmerjeni na pravi portal za upravljanje, da dokončate namestitev. Za dokončanje namestitve glejte podrobnosti o uvajanju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Obstoječe stranke rešitve Dynamics, ki uporabljajo aplikacijo Dynamics 365 Project Service Automation
Aplikacija Project Operations vključuje zmogljivosti, ki so bile na voljo v aplikaciji Project Service Automation. Pot nadgradnje bo tem strankam izdana v 1. valu izdaj za leto 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Obstoječe stranke Dynamics 365 Finance uporabljajo projektno vodenje in računovodstvo 

Obstoječe stranke rešitve Finance, ki uporabljajo funkcionalnost upravljanja projektov in računovodstva lahko nadaljujejo z uporabo rešitve, kakršna je. Glejte razdelek [Aplikacija Project Operations za scenarije z naročili na zalogi/v proizvodnji](#pma).


## <a name="deployment-regions"></a>Območja uvajanja
Če želite ugotoviti, za katera območja je podprto uvajanje aplikacije Project Operations, glejte [poročilo o geografski razpoložljivosti storitev Dynamics 365 in Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Izberite možnost **Ogled poročila** in odprite razdelek **Dynamics 365 > Operacijske aplikacije > Dynamics 365 Project Operations**, da si ogledate podprte regije.

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
- Izstavljanje predračunov za pregled in urejanje vodje projekta 

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
- Celoten strošek
- Optično branje računov s tehnologijo OCR
- Celoten postopek izdaje računa
- Prepoznavanje prihodkov
- Proizvodna naročila
- Podpora za material na zalogi z inventarjem

#### <a name="deployment-steps"></a>Koraki uvajanja
Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).

Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) in [Omogočanje novega okolja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]