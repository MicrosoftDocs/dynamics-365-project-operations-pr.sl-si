---
title: Deaktivacija cenikov
description: Ta tema pojasnjuje, kako deaktivirati ali odstraniti neuporabljene ali stare cenike.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001356"
---
# <a name="deactivate-price-lists"></a>Deaktivacija cenikov 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Če želite odstraniti stare ali neuporabljene cenike iz storitve Dynamics 365 Project Operations, morate opraviti dva koraka. 

1. Odstranite ali izbrišite cenik z določenih strani.
2. Deaktivirajte ali izbrišite cenik iz aktivnih cenikov na strani **Ceniki**.

>[!IMPORTANT]
> Za popolno odstranitev cenika morate opraviti oba koraka. Izvedba izključno 2. koraka, torej neposrednega brisanja ali deaktiviranja cenika iz pogleda »Aktivni ceniki«, ni dovolj. Povezavo tega cenika morate izbrisati tudi iz vseh krajev, omenjenih v 1. koraku.

## <a name="delete-the-price-list-from-specific-pages"></a>Izbrišite cenik z določenih strani
1. Če želite izbrisati cenik iz aplikacije Project Operations, pojdite na naslednje strani:  

      - Stran **Projektni parametri** > zavihek **Ceniki**
      - Stran **Organizacijska enota** > mreža **Ceniki**
      - stran **Kupec** > mreža **Ceniki projekta**
      - Stran **Projektne ponudbe** > mreža **Ceniki projektov**: to velja za vse aktivne projektne ponudbe.
      - Stran **Projektne pogodbe** > mreža **Ceniki projektov**: to velja za vse aktivne projektne pogodbe.

 2. Za vsako stran morate izbrati cenik, ki ga želite izbrisati, in nato izbrati **Izbriši**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Brisanje ali deaktivacija cenika iz aktivnih cenikov na strani »Ceniki«
 
1. Če želite izbrisati cenik iz aktivnih cenikov, pojdite v **Prodaja** > **Stranke** > **Ceniki**. 
2. Izberite cenike, ki jih želite izbrisati, in izberite **Izbriši**. Če se cenik sklicuje na katero koli obstoječo transakcijo, ga ne boste mogli izbrisati. Če se to zgodi, lahko deaktivirate cenik, tako da se ne prikaže v nobenem pogledu. 
3. Če želite deaktivirati cenik, znova izberite cenik in nato **Deaktiviraj**.   
