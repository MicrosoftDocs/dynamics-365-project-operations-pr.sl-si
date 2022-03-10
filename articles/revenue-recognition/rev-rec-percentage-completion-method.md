---
title: Projekti ocene prihodkov s fiksno ceno
description: Ta tema vsebuje informacije o prihodkih s fiksno ceno v projektih.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 451f0403f0111b5ea4de6c91b54eae157830e413d3a21f23bd841a66905e147b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006446"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projekti ocene prihodkov s fiksno ceno 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ko ustvarite podrobnosti pogodbe projekta z naslednjimi atributi v aplikaciji Dynamics 365 Project Operations prek Microsoft Dataverse, sistem samodejno ustvari projekt ocene prihodka s fiksno ceno. Informacije v tem projektu temeljijo na naslednjih dejavnikih:

  - Način obračunavanja po fiksni ceni.
  - Povezani projekt.
  - Vsaj en mejnik, opredeljen v zavihku **Razpored izdajanja računov** na strani **Podrobnosti pogodbe projekta**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Pregled projektov ocen prihodkov s fiksno ceno
Če želite pregledati projekte ocen prihodkov s fiksnimi cenami, izvedite naslednje korake:

1. V okolju Dynamics 365 Finance odprite **Upravljanje projektov in računovodstvo** > **Projekti** > **Projekti ocene prihodkov s fiksno ceno**.
2. Izberite projekt, ki si ga želite ogledati, in dvokliknite možnost **ID ocene projekta**, da odprete zapis in pregledate podrobnosti projekta.
3. Razširite zavihek **Projekt**. Projekt se vam bo prikazal v mreži **Izbrani projekti**. Sistem ga uporablja kot privzeti projekt, saj je povezan s podrobnostmi pogodbe projekta. 
4. Če želite spremeniti povezavo, izberite dodatne projekte in jih dodajte v mrežo **Izbrani projekti**. Če je v tej mreži izbranih več projektov, se odstotek dokončanosti projekta in ocene prihodkov izračunajo skupaj za vse izbrane projekte.

  Stroške projekta, profil prihodka, predlogo stroškov in kodo obdobja lahko nastavite ročno. Če jih ne nastavite ročno, se med prvim izračunom ocene projekta uporabijo privzete vrednosti s pomočjo pravil, konfiguriranih za stroške projekta in profile prihodkov.



[!INCLUDE[footer-include](../includes/footer-banner.md)]