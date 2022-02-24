---
title: Dnevnice
description: Ta tema vsebuje informacije o pravilih za dnevnice, ki se uporabljajo pri upravljanju stroškov.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128528"
---
# <a name="per-diems"></a>Dnevnice

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Dnevnica je dodatek, ki se izplača delavcu, ki dela na terenu. V razdelku »Upravljanje stroškov« lahko ustvarite pravila za dnevnice za različne potovalne situacije. Dnevnice lahko temeljijo na letnem času, kraju potovanja ali obojem. Ko ustvarite pravilo za dnevnice, lahko določite, da se izbrani odstotek od dnevnice zadrži, če delavec prejme brezplačne obroke ali storitve. Določite lahko tudi najmanjše in največje število ur, za katera lahko velja dnevnica za potovanje delavca.

## <a name="configuration"></a>Konfiguracija 

1. Če želite dodati lokacije dnevnic, odprite **Nastavi** > **Izračuni in kode** > **Dnevnice**.
2. Za vsako od zgoraj dodanih lokacij izberite vrednost dnevnice in valuto, ki velja med izbranim začetnim ter končnim datumom za hotel, prehrano in druge stroške. Vrednosti dnevnic in valute konfigurirate tako, da odprete **Nastavi** > **Izračuni in kode** > **Dnevnice**.
3. Na strani **Dnevnice** konfigurirajte stopnje za vrednost dnevnic. Stopnje vrednosti dnevnic vam omogočajo, da določite odstotek razdelitve dnevnic za stroške hotela, prehrane in druge stroške. 
4. Če želite znižati odstotek za obrok za zajtrk, kosilo ali večerjo, posodobite polja na strani **Parametri upravljanja stroškov** na zavihku **Dnevnica**. 
    
## <a name="submit-expenses-using-per-diem"></a>Pošiljanje stroškov z možnostjo dnevnic
Če želite poslati stroške z možnostjo dnevnic, uporabite kategorijo stroška **Dnevnica**, ko ustvarite poročilo o stroških. Vnesite **Začetni datum dnevnic**, **Končni datum dnevnic** in **Lokacija dnevnic**. Znesek se izračuna na podlagi vrednosti dnevnic za izbrano lokacijo, znižanje za obrok pa na podlagi stopnje vrednosti dnevnic.
