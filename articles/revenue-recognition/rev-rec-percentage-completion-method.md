---
title: Projekti ocene prihodkov s fiksno ceno
description: Ta tema vsebuje informacije o prihodkih s fiksno ceno v projektih.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531558"
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