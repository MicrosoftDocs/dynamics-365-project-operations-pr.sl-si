---
title: Kupite materiale brez zalog ali kategorije nabave z uporabo čakajočega računa prodajalca
description: V tej temi je pojasnjeno, kako zabeležiti čakajoče račune dobavitelja.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612677"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Kupite materiale brez zalog ali kategorije nabave z uporabo čakajočega računa prodajalca

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ker podjetje za projekt nabavlja materiale brez zalog ali kategorije nabave, se stroški lahko takoj evidentirajo v okviru projekta. 

Na primer, Contoso Robotics US izvaja projekt obnovitve opreme in potrebuje licence za programsko opremo. Te licence dobavlja neodvisni dobavitelj.  Z uporabo Dynamics 365 Finance referent obračuna obveznosti zabeleži dokument o računu prodajalca in stroške licence pripiše neposredno projektu obnove opreme. 

> [!IMPORTANT]
> Preden uporabite funkcijo, opisano v tej temi, preglejte zahtevane konfiguracije in jih uporabite. Za več informacij glejte [Omogoči materiale brez zalog in čakajoče račune prodajalcev](configure-materials-nonstocked.md) in [Uporabite kategorije nabave s projektnimi naročili in čakajočimi računi prodajalcev](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Knjiženje čakajočega računa dobavitelja, povezanega s projektom 

Čakajoče račune dobavitelja lahko zabeležite na strani **Čakajoči računi dobavitelja** (**Obveznosti** > **Računi** > **Čakajoči računi dobavitelja**). Izvedite naslednje korake, če želite knjižiti čakajoči račun dobavitelja, ki je povezan s projektom:

1. Pojdi do **Plačljive obveznosti** > **Računi** in izberite **Novo**. 
1. V **Račun za račun** izberite ponudnika in nato v polju **Številka** vnesite identifikacijo računa prodajalca.
1. Dodajte vrstico na račun prodajalca in nato v **Številka artikla** v polju izberite izdelek, ki ni na zalogi, ki je bil kupljen pri prodajalcu. Druga možnost je v **Kategorija nabave** v polju izberite kategorijo nabave, ki je bila kupljena pri prodajalcu.   
1. Dodajte kupljeno količino. Sistem izpolni ceno na enoto na podlagi konfiguracije cene artikla brez zaloge. 
1. V vrstici preverite skupni znesek in druge zahtevane podrobnosti.
1. V podrobnostih vrstice, na **Projekt** zavihku izberite ID projekta, v katerega bo ta element zabeležen.
1. Izbirno: izberite številko dejavnosti in posodobite kategorijo projekta in lastnost vrstice.
1. Objavite čakajoči račun prodajalca. Ko je račun knjižen, sistem zabeleži naslednje podatke:
    
    - znesek stanja dobavitelja,
    - znesek prometnega davka,
    - stroške glede na projekt so zabeleženi na račun za integracijo naročil,
    - Transakcija dejanskih stroškov projekta v storitvi Dataverse.  Ta transakcija se nadalje obdeluje z [dnevnikom integracij za Project Operations](../project-accounting/project-operations-integration-journal.md). Knjiženje tega dnevnika premakne znesek z računa za integracijo naročil na račun stroškov projekta. 
    - Nakupi, ki se naročniku projekta zaračunajo po načinu obračunavanja časa in materiala. Poleg tega se v storitvi Dataverse za nakupe ustvarijo neobračunane prodajne transakcije. Cenik izdelkov v storitvi Dataverse se uporablja za prodajne cene in zneske za neobračunane prodajne transakcije.
