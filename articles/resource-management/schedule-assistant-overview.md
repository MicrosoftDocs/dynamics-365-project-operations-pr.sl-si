---
title: Pregled pomočnika za razporejanje
description: Ta tema vsebuje informacije o uporabljanju pomočnika za razporejanje pri rezervaciji virov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125648"
---
# <a name="schedule-assistant-overview"></a>Pregled pomočnika za razporejanje

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Pomočnik za razporejanje se uporablja za rezerviranje virov na podlagi zahtev, ki jih določi vodja projekta. Pomočnik za razporejanje se pri iskanju vira opira na parametre, navedene v zahtevi za vir. Pomočnik za razporejanje priporoča vire, ki ustrezajo relevantnim zahtevam, kot so časovni okvirji ali potrebna znanja.

Ko so določeni ustrezni viri, lahko vodja virov ali projekta rezervira vir za opravilo.

## <a name="prerequisites"></a>Zahteve

Pomočnik za razporejanje je del rešitve Universal Resource Scheduling. Ta rešitev je vključena in nameščena v storitev Dynamics 365 Project Operations, Dynamics 365 Field Service in Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Usklajevanje zahtev z viri

Ustvarjena zahteva za vir temelji na podrobnostih, kot so:

-   Značilnosti
-   Vloge
-   Poslovne enote
-   Nastavitve virov
-   Krivulja obsega dela
-   Časovni pas

Pomočnik za razporejanje uporabi te podrobnosti za filtriranje virov.

## <a name="launch-the-schedule-assistant"></a>Zagon pomočnika za razporejanje

Pomočnika za razporejanje je mogoče zagnati na dva načina. Če uporabljate hibridni način, lahko v mreži članov ekipe izberete katerega koli člana ekipe z neizpolnjeno zahtevo za vir in kliknete **Rezerviraj**. Če uporabljate osrednji način, bo vir poiskala in izbrala rešitev Resource Manager.

## <a name="schedule-assistant-filters"></a>Filtri pomočnika za razporejanje

Po zagonu pomočnika za razporejanje se podrobnosti iz zahteve za vir prikažejo kot filtrirane vrednosti v levem podoknu. Rešitev Resource Manager ali vodja projektov lahko natančno prilagodi rezultate tako, da prilagodi filtre, ki ustrezajo potrebam po razporejanju.

Podokno filtra prikazuje z delom povezane možnosti, kot so:

-   Začetek in konec dela
-   Značilnosti
-   Vloge
-   Organizacijske enote
-   Podjetje, ki zagotavlja vire
-   Vrste virov
-   Prednostni viri
