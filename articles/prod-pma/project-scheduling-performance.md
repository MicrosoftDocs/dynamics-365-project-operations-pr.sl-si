---
title: Učinkovitost razporejanja projektnih virov
description: Ta tema vsebuje informacije o tem, kako izboljšati učinkovitost razporejanja virov za veliko število projektov.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007301"
---
# <a name="project-resource-scheduling-performance"></a>Učinkovitost razporejanja projektnih virov

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Težave z učinkovitostjo, povezane z razporejanjem virov, se lahko pojavijo, ko število projektov postane večje od tisoč. Za izboljšanje učinkovitosti razporejanja virov je na voljo funkcija, ki uporabnikom omogoča, da skrajšajo čas, potreben za zagon obrazca o razpoložljivosti virov. Odpravlja namreč postopek sinhronizacije za zbiranje zmogljivosti vira in uporablja tabelo **ResProjectResource** za hitrejše iskanje virov. Upoštevajte, da se tabela **ResRollup** ne bo več uporabljala.

> [!IMPORTANT]
> Če obstaja odvisnost bodisi od postopka sinhronizacije za zbiranje zmogljivosti vira bodisi od tabele **ResProjectResource**, ne uporabljajte te funkcije.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Omogočanje funkcije za izboljšanje učinkovitosti razporejanja virov
Če želite omogočiti funkcijo za izboljšanje učinkovitosti razporejanja virov, upoštevajte ta navodila.

1. Izberite **Upravljanje funkcij** > **Vse** in na seznamu funkcij poiščite **Omogoči funkcijo za izboljšanje učinkovitosti razporejanja projektnih virov**.
2. Izberite **Omogoči zdaj**.

> [!NOTE]
> Če funkcije ne najdete na seznamu, izberite **Preveri, ali so na voljo posodobitve**, da osvežite seznam.

3. Osvežite brskalnik in izberite **Vodenje projektov in računovodstvo** > **Redno** > **Projektni viri** > **Sinhroniziraj zmogljivosti vira v koledarjih v vseh podjetjih**.
4. Nastavite **Odstrani obstoječe zapise o zmogljivosti** na **Da**, da odstranite prejšnje podatke. Če želite ustvariti postopne podatke, možnost nastavite na **Ne**.
5. V polju **Koda obdobij** izberite obdobje, v katerem naj se ustvarijo podatki. Če izberete kodo obdobij, začetnega in končnega datuma ni treba določiti.
6. Če pustite polje **Koda obdobij** prazno, izberite določene začetne in končne datume za ustvarjanje podatkov.
7. Izberite **V redu**.

 > [!NOTE]
 > S tem se bo tabela **ResCalendarCapacity** izpolnila s splošnimi podatki za vsa podjetja v vašem okolju, zato je treba paketno opravilo izvesti samo pri eni pravni osebi. Podatki pri tem paketnem opravilu so potrebni za izračun zmogljivosti vira prek povezanega koledarja.

8. Izberite **Vodenje projektov in računovodstvo** > **Redno** > **Projektni viri** > **Izpolni projektne vire za vsa podjetja** in nato izberite **V redu**. To je skript za nadgradnjo podatkov, in sicer za splošne podatke v tabelah **ResProjectResource**, **ResCalendarDateTimeRange** in **ResEffectiveDateTimeRange**. Vrednosti za polje **PSAPRojSchedRole.RootActivity** se tudi posodobijo. Če se to ne zažene, boste prejeli opozorilo, ko boste poskušali izvesti postopke razporejanja virov.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Izklop funkcije za izboljšanje učinkovitosti razporejanja virov

1. Izberite **Upravljanje funkcij** > **Vse** in poiščite **Omogoči funkcijo za izboljšanje učinkovitosti razporejanja projektnih virov**.
2. Izberite funkcijo in nato izberite **Onemogoči**.
3. Osvežite brskalnik.
4. Izberite **Vodenje projektov in računovodstvo** > **Redno** > **Sinhronizacija zmogljivosti** > **Sinhronizacija zbiranj zmogljivosti vira**.
5. Na strani **Sinhronizacija zbiranj zmogljivosti vira** nastavite **Odstrani obstoječe zapise o zmogljivosti** na **Da**, da odstranite prejšnje podatke. Če želite ustvariti postopne podatke, možnost nastavite na **Ne**.
6. V polju **Koda obdobij** izberite obdobje, v katerem naj se ustvarijo podatki. Če izberete kodo obdobij, začetnega in končnega datuma ni treba določiti.
7. Če pustite polje **Koda obdobij** prazno, izberite določene začetne in končne datume za ustvarjanje podatkov.
8. Izberite **V redu**.

> [!NOTE]
> S tem se bo tabela **ResRollup** izpolnila s splošnimi podatki za vsa podjetja v vašem okolju, zato je treba paketno opravilo izvesti samo pri eni pravni osebi. To paketno opravilo je potrebno za vse poglede za **razpoložljivost virov**. Če se to paketno opravilo ne zažene, bodo podatki **ResRollup** bodo ustvarjeni sproti, kar lahko traja nekaj časa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]