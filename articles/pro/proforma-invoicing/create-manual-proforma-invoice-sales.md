---
title: Ustvarjanje ročnega predračuna
description: Ta tema vsebuje informacije o ustvarjanju ročnih predračunov v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084985"
---
# <a name="creating-a-manual-proforma-invoice"></a>Ustvarjanje ročnega predračuna

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko predračune po potrebi ustvarite ročno. Predračun lahko ročno ustvarite iz strani s seznamom **Projektne pogodbe** ali s strani s podrobnostmi **Projektna pogodba**.

##  <a name="project-contracts-list-page"></a>Stran s seznamom projektnih pogodb

Na strani s seznamom **Projektne pogodbe** izberite eno ali več projektnih pogodb in ustvarite račune za vse izbrane zapise.

Sistem preveri, katera od izbranih projektnih pogodb ima nedokončana opravila **Pripravljeno na izdajanje računa** , ki so bila ustvarjena pred današnjim dnem. Iz teh pogodb sistem ustvari osnutke predračunov. Če ima projektna pogodba več strank, je lahko ustvarjen en račun na stranko in več računov na projektno pogodbo.

Vsi ustvarjeni projektni računi so na voljo na strani **Račun** v razdelku **Obračunavanje** območja **Prodaja**.

## <a name="project-contract-details-page"></a>Stran s podrobnostmi o projektni pogodbi

Predračun lahko ustvarite tudi iz strani s podrobnostmi **Projektna pogodba** , ki ustvari račun za določeno projektno pogodbo. Sistem preveri, katera od izbranih projektnih pogodb ima nedokončana opravila **Pripravljeno na izdajanje računa** , ki so bila ustvarjena pred današnjim dnem. Iz teh pogodb sistem ustvari osnutke predračunov na podlagi števila strank v vsaki podrobnosti pogodbe.

Ko je ustvarjen prvi predračun, se odpre stran **Račun**. Če je za to projektno pogodbo ustvarjenih več računov, se odpre stran s seznamom **Računi** , da se prikažejo vsi ustvarjeni računi.
