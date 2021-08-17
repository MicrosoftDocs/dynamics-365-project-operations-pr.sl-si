---
title: Konfiguracija vodenja računov za interne projekte
description: Ta tema vsebuje informacije o nastavitvah računovodskih postopkov za interne projekte v aplikaciji Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005546"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfiguracija vodenja računov za interne projekte

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Interni projekti podjetjem omogočajo sledenje stroškom, povezanih z dejavnostmi, ki niso obračunane za stranko. Primeri internih projektov so:

- Razvijanje izdelka, kot je mobilna aplikacija, in sledenje stroškom, ki so povezani z razvojem.
- Upravljanje časa in stroškov pred prodajo Ta interni predprodajni projekt je v primeru pridobljene ponudbe mogoče pozneje pretvoriti v projekt, ki ga je mogoče obračunati.

Vsak projekt, ki ni povezan s pogodbo v aplikaciji Dynamics 365 Project Operations, se obravnava kot notranji. Profili stroškov in prihodkov podjetja se ne uporabljajo za določanje računovodskih pravil za projekt. Stroški internega projekta se vedno knjižijo po načelih dobička in izgube. Računi glavne knjige za vknjižbe so opredeljeni na strani **z nastavitvami vnašanja v glavno knjigo**.

- Časovne transakcije so knjižene v breme na računu **Stroški** in v dobro na računu **Dodelitev plače**.
- Stroškovne transakcije so knjižene v breme na računu **Stroški** in v dobro na računu **Protikonto za stroške**.
- Transakcije postavk se knjižijo z obremenitvijo računa **Stroški** in kreditiranjem računa **Stroški – postavka**.

Potem ko so transakcije vknjižene za projekt in če je projekt povezan s projektno pogodbo, sistem stornira vse zbrane transakcije in ustvari nove transakcije, ki jih je mogoče obračunati. Transakcije, ki jih je mogoče obračunati, sledijo računovodskim pravilom, opredeljenim v ustreznem profilu stroškov in prihodkov projekta.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
