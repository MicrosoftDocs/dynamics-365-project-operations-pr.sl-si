---
title: Naročilnice za projekt
description: V tem članku so opisane različne metode, s katerimi lahko ustvarite naročilnice za projekt. Uporabljena metoda je odvisna od namena naročilnice in od tega, kdaj se kupljeni artikli uporabijo in zaračunajo za projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289209"
---
# <a name="purchase-orders-for-a-project"></a>Naročilnice za projekt

[!include [banner](../includes/banner.md)]

V tem članku so opisane različne metode, s katerimi lahko ustvarite naročilnice za projekt. Uporabljena metoda je odvisna od namena naročilnice in od tega, kdaj se kupljeni artikli uporabijo in zaračunajo za projekt.

### <a name="methods-for-creating-a-purchase-order"></a>Metode za ustvarjanje naročilnice

Za ustvarjanje naročilnice v območju »Vodenje projektov in računovodstvo« lahko uporabite eno od spodnjih metod. Namen naročilnice določa, kdaj je naročilnica uporabljena in kdaj se zaračunajo artikli za projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Način</th>
<th>Namen</th>
<th>Poraba izdelkov</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ustvarite naročilnico neposredno iz projekta.</td>
<td>To metodo uporabite za nakup artiklov od zunanjega dobavitelja za uporabo v projektu. Naročilnico lahko ustvarite na dva načina:
<ul>
<li>V samem projektu. V tem primeru je projekt že opredeljen za naročilnico.</li>
<li>Tako da poiščete in odprete naročilnico projekta. Za izdelavo naročilnice morate izbrati dobavitelja in projekt, za katerega jo želite ustvariti.</li>
</ul></td>
<td>Izdelki se porabijo, ko se posodobi račun dobavitelja.</td>
</tr>
<tr class="even">
<td>Ustvarite naročilnico iz prodajnega naloga.</td>
<td>To metodo uporabite za nakup artiklov, ko ustvarite prodajni nalog iz projekta.</td>
<td>Izdelki se porabijo, ko je stranki zaračunan prodajni nalog.</td>
</tr>
<tr class="odd">
<td>Ustvarite naročilnico iz zahteve za izdelek.</td>
<td>To metodo uporabite za nakup artiklov, ko ustvarite zahtevo za artikel iz projekta.</td>
<td>Izdelki se porabijo s posodobitvijo odpremnice za zahtevo za izdelek.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Ko posodobite račun dobavitelja ali odpremnico, morate posodobiti tudi odpremnico v zahtevi za artikel.

Za več informacij glejte [Prejemanje izdelkov, ki so navedeni v naročilu, v okviru zahteve po izdelku](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]