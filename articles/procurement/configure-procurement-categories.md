---
title: Uporabite kategorije javnih naročil z naročili za projekt in čakajočimi računi dobavitelja
description: Ta članek opisuje, kako konfigurirati kategorije javnih naročil, ki jih je mogoče uporabiti z naročili za projekt in čakajočimi računi dobavitelja.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Uporabite kategorije javnih naročil z naročili za projekt in čakajočimi računi dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Strokovnjaki za nabavo lahko ustvarijo in vzdržujejo kataloge artiklov in storitev, ki jih je mogoče uporabiti v projektnih naročilnicah in čakajočih računih dobaviteljev. [Katalogi nabave](/dynamics365/supply-chain/procurement/procurement-catalogs) vam omogoča enostaven način za kategorizacijo nakupov, ne da bi morali konfigurirati in uporabljati izdani katalog izdelkov. Vsako kategorijo nabave je mogoče preslikati v kategorijo projekta za transakcije časa, stroškov ali postavk. Po objavi čakajočega računa dobavitelja, ki uporablja kategorijo nabave, bo sistem ustvaril dejanske podatke o času, stroških ali materialu, projektne transakcije in vnose v podknjigo.

## <a name="minimum-version-requirements"></a>Minimalne zahteve glede različice

Naslednje različice so potrebne za uporabo kategorij javnih naročil s projektnimi naročili za Microsoft Dynamics 365 Project Operations scenariji brez zalog/na virih:

- Projektne operacije Dataverse različica rešitve 4.41.0.45 ali novejša
- Okolje financ in operacij različica 10.0.26 ali novejša

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Zaženite zemljevide dvojnega pisanja za podporo kategorije naročila

Prepričajte se, da je preslikava za **Izvoz entitete msdyn za integracijo projektnih operacij dobavitelja vrstice računa\_ projectvendorinvoicelines** uporablja različico 1.0.0.4 ali novejšo.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogočite funkcijski ključ za kategorije javnih naročil

Sledite tem korakom, da omogočite funkcionalnost za uporabo kategorij javnih naročil z naročili za projekt.

1. V Dynamics 365 Finance odprite **Upravljanje funkcij** delovni prostor.
1. Na seznamu funkcij poiščite **Uporabite kategorije javnih naročil v Project Operations za scenarije, ki temeljijo na virih/brez zaloge** in nato izberite **Omogoči**.

> [!IMPORTANT]
> Kot predpogoj morate omogočiti tudi **Omogoči čakajoče račune dobaviteljev v Project Operations za scenarije, ki temeljijo na virih/nezaloženih** funkcija.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Preslikajte kategorije projektov v hierarhiji kategorij naročil

Sledite tem korakom, da preslikate kategorije projektov v kategorije javnih naročil v **Kategorija nabave** hierarhija:

1. Pojdi do **Nabava in pridobivanje virov \> Kategorije javnih naročil**.
1. Izberite **Uredite hierarhijo kategorij**.
1. Izberite želeno vozlišče hierarhije kategorij in nato na **Dodelite kategorije projektov** povežite vozlišče s kategorijo projekta iz **Čas**, **·**, ali, **Projekt predmeta** kategorijo (to je **Privzeti čas** oz **Privzeti stroški** kategorija).
1. Izberite **Shrani**.
1. Zaprite stran.

> [!NOTE]
> Preslikava kategorije javnega naročila v kategorijo projekta ni obvezna. Če kategorija naročila ni preslikana, bo sistem uporabil vrednost, ki je nastavljena v **Postavka** polje v **Privzete kategorije projektov** razdelek o **Projektne operacije na Dynamics 365 Customer Engagement** zavihek od **Projektno vodenje in računovodski parametri** strani.
