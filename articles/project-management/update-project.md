---
title: Ustvarjanje in posodabljanje projekta
description: Ta članek vsebuje informacije o posodabljanju projektov v aplikacij Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911110"
---
# <a name="create-and-update-a-project"></a>Ustvarjanje in posodabljanje projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Sledi povzetek polj, ki jih je mogoče posodobiti v projektu, potem ko je bil ustvarjen. To vključuje tudi vse posledice, ki bi lahko sledile in temeljijo na teh posodobitvah.

## <a name="project-detail-fields"></a>Polja s predvidenimi vrednostmi projekta

- **Ime**: ime projekta.
- **Opis**: pregled projekta.
- **Stranka**: podjetje, ki mu bo projekt dostavljen.
- **Predloga koledarja**: delovni čas projekta. Ko se polje spremeni, se celotni urnik preračuna.
- **Valuta**: valuto za projekt. Privzeta vrednost za to polje temelji na valuti, ki je definirana v pogodbeni enoti. Ko se pogodbena enota posodobi, se posodobi tudi polje.
- **Pogodbena enota**: organizacijska enota, ki predstavlja skupino ali oddelek podjetja, ki je primarno odgovoren za izvedbo prodaje in upravljanje zagotavljanja dela in storitev za stranke.  Če organizacijska enota vodje projekta ni definirana, se to polje povrne na vrednost, definirano v parametrih projekta.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
