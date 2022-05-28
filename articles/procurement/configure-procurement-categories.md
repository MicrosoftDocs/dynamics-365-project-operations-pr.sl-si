---
title: Uporabite kategorije nabave s projektnimi naročili in čakajočimi računi prodajalcev
description: Ta tema opisuje, kako konfigurirati kategorije javnih naročil, ki jih je mogoče uporabiti s projektnimi naročili in čakajočimi računi prodajalcev.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613367"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Uporabite kategorije nabave s projektnimi naročili in čakajočimi računi prodajalcev

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Strokovnjaki za nabavo lahko ustvarijo in vzdržujejo kataloge artiklov in storitev, ki se lahko uporabljajo v projektnih naročilnicah in čakajočih računih prodajalcev. [Katalogi nabav](/dynamics365/supply-chain/procurement/procurement-catalogs) vam omogoča enostaven način za kategorizacijo nakupov, ne da bi vam bilo treba konfigurirati in uporabljati izdani katalog izdelkov. Vsako kategorijo javnih naročil je mogoče preslikati v kategorijo projekta za transakcije časa, stroškov ali artiklov. Ko je knjižen čakajoči račun prodajalca, ki uporablja kategorijo nabave, bo sistem ustvaril dejanske podatke o času, stroških ali materialnih projektih, transakcije projekta in vnose v podknjigi.

## <a name="minimum-version-requirements"></a>Zahteve glede minimalne različice

Naslednje različice so potrebne za uporabo kategorij javnih naročil s projektnimi naročilnicami za Microsoft Dynamics 365 Project Operations scenariji brez zalog/iz virov:

- Projektne operacije Dataverse različica rešitve 4.41.0.45 ali novejša
- Različica okolja Finance in Operations 10.0.26 ali novejša

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Zaženite zemljevide z dvojnim pisanjem za podporo za kategorijo naročil

Prepričajte se, da je preslikava za **Integracija projektnih operacij, izvozna entiteta vrstice računa prodajalca projekta msdyn\_ projektvendorinvoicelines** uporablja različico 1.0.0.4 ali novejšo.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Omogočite funkcijski ključ za kategorije naročil

Sledite tem korakom, da omogočite funkcionalnost za uporabo kategorij nabav s projektnimi naročilnicami.

1. V Dynamics 365 Finance odprite **Upravljanje funkcij** delovni prostor.
1. Na seznamu funkcij poiščite **Uporabite kategorije nabave v projektnih operacijah za scenarije, ki temeljijo na virih/brez zalog** funkcijo in nato izberite **Omogoči**.

> [!IMPORTANT]
> Kot predpogoj morate omogočiti tudi **Omogoči čakajoče račune dobavitelja v projektnih operacijah za scenarije, ki temeljijo na virih/brez zalog** funkcija.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Preslikajte kategorije projektov v hierarhijo kategorij nabave

Sledite tem korakom za preslikavo kategorij projektov v kategorije javnih naročil v **Kategorija nabave** hierarhija:

1. Pojdi do **Nabava in pridobivanje \> Kategorije javnih naročil**.
1. Izberite **Uredite hierarhijo kategorij**.
1. Izberite želeno vozlišče hierarhije kategorij in nato na **Dodeli kategorije projektov** zavihku, povežite vozlišče s kategorijo projekta iz **Čas**, Stroški**, oz **,Projekt predmeta** kategorija (tj **Privzeti čas** oz **Privzeti stroški** kategorija).
1. Izberite **Shrani**.
1. Zaprite stran.

> [!NOTE]
> Preslikavanje kategorije naročil v kategorijo projekta ni obvezno. Če kategorija naročila ni preslikana, bo sistem uporabil vrednost, ki je nastavljena v **Artikel** polje v **Privzete nastavitve kategorije projekta** razdelek o **Project Operations on Dynamics 365 Vključevanje strank** zavihek na **Vodenje projektov in računovodski parametri** stran.
