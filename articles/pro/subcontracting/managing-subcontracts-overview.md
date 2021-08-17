---
title: Upravljanje podizvajalskih pogodb v aplikaciji Project Operations
description: Ta članek prikazuje pregled postopka upravljanja celovite podizvajalske pogodbe v storitvi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994251"
---
# <a name="subcontract-management-in-project-operations"></a>Upravljanje podizvajalskih pogodb v aplikaciji Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podizvajalske pogodbe v storitvi Microsoft Dynamics 365 Project Operations podpirajo naslednji potek poslovnega procesa.

![Potek procesa podizvajalskih pogodb](../media/SubcontractingProcessFlow.png)

Postopek podizvajalskih pogodb je opisan po korakih.

1. Vodja projekta sklene podizvajalsko pogodbo z dobaviteljem. Pri podizvajalski pogodbi se privzeto uporabljajo ceniki, ki so priloženi zapisu dobavitelja. Račun dobavitelja ima vrsto odnosa **Prodajalec** ali **Dobavitelj**.
2. Vodja projekta lahko vse nakupe v podizvajalski pogodbi razvrsti kot postavke izdelka. Podizvajalske pogodbe so lahko vezane na čas, stroške ali izdelke. Razred transakcij, ki je izbran v vsaki vrstici podizvajalske pogodbe, določa, čemu ta vrstica služi.
3. Upravljavec računa dobavitelja in vodja projekta lahko ponovita podizvajalsko pogodbo. Cene v nabavnem ceniku, ki so priložene podizvajalski pogodbi, se lahko prilagodijo.
4. Če je podizvajalska pogodba za časovni vnos, upravitelj računa dobavitelja na tej točki ali pozneje v postopku poveže stike z vsako vrstico podizvajalske pogodbe. Ta povezava posreduje informacije vodji projekta, ki dela na podizvajalski pogodbi. Ko je stik povezan z vrstico podizvajalca, sistem samodejno ustvari vir, ki ga je mogoče rezervirati, če vir za rezervacijo še ne obstaja.
5. Način obračunavanja na vsaki vrstici podizvajalske pogodbe je lahko **Fiksna cena** ali **Čas in material**. Za vrstice podizvajalske pogodbe s fiksno ceno lahko nastavite razpored za izdajanje računov, ki temelji na mejnikih.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
