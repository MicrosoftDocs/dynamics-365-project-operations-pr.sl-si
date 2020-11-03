---
title: Pošiljanje zahteve za vir
description: Ta tema vsebuje informacije o pošiljanju zahteve za vir projekta.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084849"
---
# <a name="submitting-a-resource-request"></a>Pošiljanje zahteve za vir

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ustvarjen zahtevani pogoj za vir lahko pošljete kot zahtevo za vir. Zahteva se nato pošlje upravitelju virov v izpolnitev.

1. V aplikaciji Project Service Automation (PSA) na strani **Projekti** kliknite zavihek **Skupina** , če si želite ogledati seznam virov, ki jih je mogoče rezervirati. 
2. Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato kliknite **Pošlji zahtevo**.

![Pošiljanje zahteve za vir](media/RM-how-to-18.png)

Status zahteve splošnega člana ekipe se bo spremenil v **Poslano**.

Ko upravitelj virov izpolni zahtevo, bo imenovani vir nadomestil splošni vir, v primeru da upravitelj virov izpolni zahtevo z rezervacijo imenovanega vira. V nasprotnem primeru bo splošni vir ostal v ekipi in se bo stanje zahteve spremenilo v **Potreben pregled** , če je upravitelj virov predlagal imenovani vir.
