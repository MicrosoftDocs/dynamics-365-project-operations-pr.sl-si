---
title: Posodobitev projekta
description: Ta tema vsebuje informacije o posodabljanju projektov v aplikacij Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897832"
---
# <a name="update-a-project"></a>Posodobitev projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Spodaj je povzetek polj, ki jih je mogoče po projektu posodobiti, in morebitne posledice posodobitev.

## <a name="project-detail-fields"></a>Polja s predvidenimi vrednostmi projekta

- **Ime**: ime projekta.
- **Opis**: pregled projekta.
- **Stranka**: podjetje, ki mu bo projekt dostavljen.
- **Predloga koledarja**: delovni čas projekta. Ko se polje spremeni, se celotni urnik preračuna.
- **Valuta**: valuto za projekt. To polje privzeto temelji na valuti, določeni v pogodbeni enoti. Ko se pogodbena enota posodobi, se posodobi tudi polje.
- **Pogodbena enota**: organizacijska enota, ki predstavlja skupino ali oddelek podjetja, ki je primarno odgovoren za izvedbo prodaje in upravljanje zagotavljanja dela in storitev za stranke. 
- **Vodja projekta**: član projektne skupine, ki je pooblaščen za pregled in odobritev časovnih vnosov in stroškov.

## <a name="estimate-fields"></a>Polja s predvidenimi vrednostmi

- **Predvideni datum začetka**: datum začetka projekta. Ko se to polje posodobi, se bodo vsa opravila v projektu sorazmerno premaknila glede na nov datum začetka.
- **Datum zaključka**: datum zaključka projekta.
- **Obseg dela**: predviden obseg dela. Ko so opravila dodana projektu, tega polja ni več mogoče urejati.
- **Predvideni stroški dela**: predvideni stroški dela za projekt. Ko so stroški dela dodani projektu, tega polja ni več mogoče urejati.
- **Predvideni stroški**: predvideni stroški projekta. Ko so stroški dodani projektu, tega polja ni več mogoče urejati.

## <a name="project-actual-fields"></a>Dejanska polja projekta
- **Dejanski začetek**: datum začetka projekta.
- **Dejanski zaključek**: se posodobi po zaključku projekta.

## <a name="project-status-fields"></a>Polja stanja projekta

- **Splošno stanje projekta**: splošno stanje projekta, ki ga zagotavlja vodja projekta.
- **Komentarji**: komentarji o trenutnem stanju projekta, ki jih zagotovi vodja projekta.

