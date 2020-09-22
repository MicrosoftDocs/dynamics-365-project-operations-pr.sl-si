---
title: Pošiljanje zahteve za vir
description: Ta tema vsebuje informacije o pošiljanju zahteve za vir projekta.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755841"
---
# <a name="submit-a-resource-request"></a>Pošiljanje zahteve za vir

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ustvarjen zahtevani pogoj za vir lahko pošljete kot zahtevo za vir. Zahteva se nato pošlje upravitelju virov v izpolnitev.

1. V aplikaciji Project Service Automation (PSA) na strani **Projekti** kliknite zavihek **Skupina**, če si želite ogledati seznam virov, ki jih je mogoče rezervirati. 
2. Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato kliknite **Pošlji zahtevo**.

![Pošiljanje zahteve za vir](media/RM-how-to-18.png)

Status zahteve splošnega člana ekipe se bo spremenil v **Poslano**.

Ko upravitelj virov izpolni zahtevo, bo imenovani vir nadomestil splošni vir, v primeru da upravitelj virov izpolni zahtevo z rezervacijo imenovanega vira. V nasprotnem primeru bo splošni vir ostal v ekipi in se bo stanje zahteve spremenilo v **Potreben pregled**, če je upravitelj virov predlagal imenovani vir.
