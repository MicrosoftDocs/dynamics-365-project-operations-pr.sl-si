---
title: Upravljanje dobaviteljev in cenikov nabave v storitvi Project Operations
description: Ta tema vsebuje informacije, ki vam bodo pomagale ustvariti in vzdrževati podatke o dobaviteljih in cenikih nakupov podizvajalskih pogodb.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994161"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Upravljanje dobaviteljev in cenikov nabave v storitvi Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

## <a name="vendors-in-project-operations"></a>Dobavitelji v storitvi Project Operations

Računi dobavitelja imajo vrsto odnosa **Prodajalec** ali **Dobavitelj** v storitvi Microsoft Dynamics 365 Project Operations. Za dobavitelja pri podizvajalski pogodbi lahko izberete samo zapis računa, ki ima eno od teh vrst odnosov.

Z zapisom dobavitelja lahko povežete enega ali več nakupnih cenikov. Vendar bi moral imeti vsak nakupni cenik, ki je povezan z zapisom dobavitelja, različni datum veljavnosti. Storitev Project Operations ne podpira prekrivanja datumov začetka veljavnosti cenikov.

Naslednja polja in koncepti v zapisu dobavitelja se privzeto uporabljajo za katero koli podizvajalsko pogodbo, ki je ustvarjena za dobavitelja:

- Plačilni pogoji
- Stik za plačilo
- Glavni stik

    > [!NOTE]
    > Primarni stik dobavitelja se privzeto uporablja kot upravitelj računa dobavitelja podizvajalske pogodbe.

- Valuta
- Trenutni nabavni cenik

## <a name="purchase-price-lists-in-project-operations"></a>Nabavni cenik v storitvah Project Operations

Cenik, kjer je polje **Kontekst** nastavljeno na **Nakup** velja za nakupni cenik. Nakupne cenike je mogoče opredeliti kot katalog nakupnih cen za čas, stroške in material. Nakupni ceniki so podobni stroškom in prodajnim cenikom v storitvah Project Operations. Naslednji pojmi veljajo za nakupne cenike na enak način kot za stroške in prodajne cenike:

- **Datum veljavnosti** - Nakupni ceniki imajo datum veljavnosti. Datum veljavnosti je na vsakem ceniku predstavljen s polji začetnega in končnega datuma. Čas med začetnim in končnim datumom je obdobje datuma veljavnosti.
- **Valuta** - Valuta v glavi cenika se uporablja kot valuta, v kateri so izražene nakupne cene za delo, kategorije stroškov in izdelke v katalogu.
- **Privzeta časovna enota** - Privzeta časovna enota izraža cene dela pri nakupih. Polje časovne enote v ceniku se uporablja samo za podajanje privzete vrednosti. To vrednost lahko spremenite v posameznih vrsticah za cene vlog.

Nakupni ceniki se lahko priložijo evidencam dobavitelja kot združenja, ki so znana kot ceniki projektov. Ti ceniki se uporabljajo za vnos privzetih cen v vrsticah podizvajalskih pogodb. Kadar je v zapisu dobavitelja priloženih več nakupnih cenikov, se pri podizvajalskih pogodbah, ki so ustvarjene za dobavitelja, privzeto uporabi najnovejši cenik. Samo ceniki, kjer je polje **Kontekst** nastavljeno na **Nakup**, se lahko priložijo zapisom dobavitelja.

### <a name="subcontract-specific-purchase-price-lists"></a>Ceniki, določeni s strani podizvajalca

Ceniki se lahko priložijo podizvajalskim pogodbam kot združenja, ki so znana kot ceniki projektov. Ti ceniki se uporabljajo za vnos privzetih cen v vrsticah podizvajalskih pogodb. Kadar je podizvajalski pogodbi priloženih več cenikov, mora vsak privzeto imeti različen datum veljavnosti. Storitev Project Operations ne podpira prekrivanja datumov začetka veljavnosti cenikov. Samo ceniki, kjer je polje **Kontekst** nastavljeno na **Nakup**, se lahko priložijo zapisom podizvajalskih pogodb.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
