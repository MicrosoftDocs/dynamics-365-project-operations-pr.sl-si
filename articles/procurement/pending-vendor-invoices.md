---
title: Nakup materialov, ki niso na zalogi, s čakajočim računom dobavitelja
description: V tej temi je pojasnjeno, kako zabeležiti čakajoče račune dobavitelja.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880686"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Nakup materialov, ki niso na zalogi, s čakajočim računom dobavitelja

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ker podjetje za projekt nabavlja materiale, ki niso na zalogi, lahko stroške takoj zabeležimo glede na projekt. 

Podjetje Contoso Robotics US na primer izvaja projekt obnove opreme in potrebuje licence za programsko opremo. Te licence dobavlja neodvisni dobavitelj.  Z aplikacijo Dynamics 365 Finance uradnik za obveznosti zabeleži dokument čakajočega računa dobavitelja in neposredno pripiše stroške licence projektu obnove opreme. 

> [!IMPORTANT]
> Preden uporabite funkcijo, opisano v tej temi, preglejte zahtevane konfiguracije in jih uporabite. Za več informacij glejte [Omogočanje materialov, ki niso na zalogi, in čakajočih računov dobavitelja](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Knjiženje čakajočega računa dobavitelja, povezanega s projektom 

Čakajoče račune dobavitelja lahko zabeležite na strani **Čakajoči računi dobavitelja** (**Obveznosti** > **Računi** > **Čakajoči računi dobavitelja**). Izvedite naslednje korake, če želite knjižiti čakajoči račun dobavitelja, ki je povezan s projektom:

1. V razdelku **Obveznosti** > **Računi** izberite **Novo**. 
2. V polju **Račun za obračun** izberite dobavitelja, v polje **Številka** pa vnesite identifikacijo računa dobavitelja.
3. Na račun dobavitelja dodajte vrstico in v polju **Številka elementa** izberite element, ki ni na zalogi, kupljen pri dobavitelju. 

    > [!NOTE]
    > Vrstic računa dobavitelja, ki temeljijo na kategoriji nabave, ni mogoče zabeležiti glede na projekt. 
    
5. Dodajte količino kupljenega. Sistem bo zapolnil ceno enote glede na konfiguracijo cene elementa, ki ni na zalogi. 
6. V vrstici preverite skupni znesek in druge zahtevane podrobnosti.
7. V podrobnostih vrstice na zavihku **Projekt** izberite ID projekta, v katerega bo ta element zabeležen.
8. Po želji izberite številko dejavnosti in posodobite kategorijo projekta in lastnost vrstice.
9. Knjižite čakajoči račun dobavitelja. Ko je račun knjižen, sistem zabeleži:
    
    - znesek stanja dobavitelja,
    - znesek prometnega davka,
    - stroške glede na projekt so zabeleženi na račun za integracijo naročil,
    - dejansko transakcijo projekta v storitvi Dataverse. Ta transakcija se nadalje obdeluje z [dnevnikom integracij za Project Operations](../project-accounting/project-operations-integration-journal.md). Knjiženje tega dnevnika premakne znesek z računa za integracijo naročil na račun stroškov projekta.
