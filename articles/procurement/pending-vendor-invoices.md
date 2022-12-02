---
title: Nakup materialov, ki niso na zalogi, ali kategorij za nabavo s čakajočim računom dobavitelja
description: V tem članku je pojasnjeno, kako zabeležiti čakajoče račune dobavitelja.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922012"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nakup materialov, ki niso na zalogi, ali kategorij za nabavo s čakajočim računom dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ker podjetje za projekt nabavlja materiale, ki niso na zalogi, ali kategorije za nabavo lahko stroške takoj zabeležimo glede na projekt. 

Na primer, Contoso Robotics US izvaja projekt obnovitve opreme in potrebuje licence za programsko opremo. Te licence dobavlja neodvisni dobavitelj.  Z aplikacijo Dynamics 365 Finance uradnik za obveznosti zabeleži dokument čakajočega računa dobavitelja in neposredno pripiše stroške licence projektu obnove opreme. 

> [!IMPORTANT]
> Preden uporabite funkcijo, opisano v tem članku, preglejte zahtevane konfiguracije in jih uporabite. Za več informacij glejte članka [Omogočanje materialov, ki niso na zalogi, in čakajočih računov dobavitelja](configure-materials-nonstocked.md) in [Uporaba kategorij za nabavo z naročilnicami projektov in računi dobaviteljev na čakanju](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Knjiženje čakajočega računa dobavitelja, povezanega s projektom 

Čakajoče račune dobavitelja lahko zabeležite na strani **Čakajoči računi dobavitelja** (**Obveznosti** > **Računi** > **Čakajoči računi dobavitelja**). Izvedite naslednje korake, če želite knjižiti čakajoči račun dobavitelja, ki je povezan s projektom:

1. V razdelku **Obveznosti** > **Računi** izberite **Novo**. 
1. V polju **Račun za obračun** izberite dobavitelja, v polje **Številka** pa vnesite identifikacijo računa dobavitelja.
1. Na račun dobavitelja dodajte vrstico in v polju **Številka elementa** izberite element, ki ni na zalogi in je bil kupljen pri dobavitelju. Druga možnost je, da v polju **Kategorija za nabavo** izberete kategorijo za nabavo, ki je bila kupljena pri dobavitelju.   
1. Dodajte količino, ki je bila kupljena. Sistem zapolni ceno enote glede na konfiguracijo cene elementa, ki ni na zalogi. 
1. V vrstici preverite skupni znesek in druge zahtevane podrobnosti.
1. V podrobnostih vrstice na zavihku **Projekt** izberite ID projekta, v katerega bo ta element zabeležen.
1. Izbirno: izberite številko dejavnosti in posodobite kategorijo projekta in lastnost vrstice.
1. Knjižite čakajoči račun dobavitelja. Ko je račun knjižen, sistem beleži naslednje informacije:
    
    - znesek stanja dobavitelja,
    - znesek prometnega davka,
    - stroške glede na projekt so zabeleženi na račun za integracijo naročil,
    - Transakcija dejanskih stroškov projekta v storitvi Dataverse.  Ta transakcija se nadalje obdeluje z [dnevnikom integracij za Project Operations](../project-accounting/project-operations-integration-journal.md). Knjiženje tega dnevnika premakne znesek z računa za integracijo naročil na račun stroškov projekta. 
    - Nakupi, ki se naročniku projekta zaračunajo po načinu obračunavanja časa in materiala. Poleg tega se v storitvi Dataverse za nakupe ustvarijo neobračunane prodajne transakcije. Cenik izdelkov v storitvi Dataverse se uporablja za prodajne cene in zneske za neobračunane prodajne transakcije.
