---
title: Uporaba kategorij za nabavo z naročilnicami projektov in računi dobaviteljev na čakanju
description: Ta članek opisuje, kako konfigurirati kategorije za nabavo, ki jih je mogoče uporabiti z naročilnicami projektov in računi dobaviteljev na čakanju.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028630"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Uporaba kategorij za nabavo z naročilnicami projektov in računi dobaviteljev na čakanju

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Strokovnjaki za nabavo lahko ustvarijo in vzdržujejo kataloge izdelkov in storitev, ki jih je mogoče uporabiti v naročilnicah projektov in računih dobaviteljev na čakanju. [Katalogi za nabavo](/dynamics365/supply-chain/procurement/procurement-catalogs) vam omogočajo enostaven način za kategorizacijo nakupov, ne da bi vam bilo treba konfigurirati in uporabljati objavljeni katalog izdelkov. Vsako kategorijo za nabavo je mogoče preslikati v kategorijo projekta za čas, stroške ali transakcije postavk. Po objavi računa dobavitelja na čakanju, ki uporablja kategorijo za nabavo, bo sistem ustvaril dejanske vrednosti o času, stroških ali materialu, projektne transakcije in vnose v podknjige.

## <a name="minimum-version-requirements"></a>Zahteve za najmanjšo različico

Naslednje različice so potrebne za uporabo kategorij za nabavo z naročilnicami projektov za scenarije brez zalog/na podlagi virov Microsoft Dynamics 365 Project Operations:

- Project Operations Dataverse, različica rešitve 4.41.0.45 ali novejša
- Okolje za finance in postopke, različica 10.0.26 ali novejša

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Zagon preslikav za dvojno zapisovanje za podporo kategorije za nabavo

Prepričajte se, da preslikava za **izvozno entiteto vrstice računa dobavitelja projekta za integracijo v Project Operations msdyn\_projectvendorinvoicelines** uporablja različico 1.0.0.4 ali novejšo.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogočanje funkcijskega ključa za kategorije za nabavo

Sledite tem korakom, da omogočite funkcijo za uporabo kategorij za nabavo z naročilnicami projektov.

1. V aplikaciji Dynamics 365 Finance odprite delovni prostor **Upravljanje funkcij**.
1. Na seznamu funkcij poiščite funkcijo **Uporaba kategorij za nabavo v aplikaciji Project Operations za scenarije, ki temeljijo na virih/nezalogi** in izberite možnost **Omogoči**.

> [!IMPORTANT]
> Kot predpogoj morate omogočiti tudi funkcijo **Omogočanje računov dobavitelja na čakanju v aplikaciji Project Operations za scenarije, ki temeljijo na virih/nezalogi**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Preslikava kategorij projekta v hierarhijo kategorij za nabavo

Sledite tem korakom, da preslikate kategorije projektov v kategorije za nabavo v hierarhiji **Kategorija za nabavo**:

1. Odprite možnost **Nabava in iskanje dobaviteljev \> Kategorije za nabavo**.
1. Izberite možnost **Urejanje hierarhije kategorije**.
1. Izberite želeno vozlišče hierarhije kategorije in nato v zavihku **Dodelitev kategorij projekta** povežite vozlišče s kategorijo projekta iz kategorije **Čas**, **Stroški** ali **Element projekta** (to je kategorija **Privzeti čas** ali **Privzeti stroški**).
1. Izberite **Shrani**.
1. Zaprite stran.

> [!NOTE]
> Preslikava kategorije za nabavo v kategorijo projekta ni obvezna. Če kategorija za nabavo ni preslikana, bo sistem uporabil vrednost, ki je nastavljena v polju **Element** v razdelku **Privzete kategorije projekta** na zavihku **Project Operations v storitvi Dynamics 365 Customer engagement** na strani **Parametri upravljanja projektov in računovodstvo**.
