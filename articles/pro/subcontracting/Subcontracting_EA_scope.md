---
title: Oktobrska (2021) izdaja za oddajanje naročil podizvajalcem; zgodnji dostop
description: V tej temi so predstavljene zmogljivosti za oddajanje naročil podizvajalcem v aplikaciji Project Operations, ki so vključene v oktobrsko (2021) izdajo za zgodnji dostop.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383715"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Oktobrska (2021) izdaja za oddajanje naročil podizvajalcem; zgodnji dostop

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V tej temi so predstavljene zmogljivosti za oddajanje naročil podizvajalcem v aplikaciji Dynamics 365 Project Operations, ki so vključene v oktobrsko (2021) izdajo za zgodnji dostop. Nabor funkcij ni pripravljen za produkcijsko okolje ali okolje, ki deluje v živo, zato bodo funkcije vse do izdaje celotnega nabora na voljo le v okviru izdaje za zgodnji dostop. Priporočamo vam, da nabora funkcij za oddajanje naročil podizvajalcem za scenarije v živo, ki temeljijo na proizvodnji, ne uporabljate, dokler pasica za predogledno različico ni odstranjena. 

V nadaljevanju so povzete storitve, ki so trenutno na voljo v okviru oktobrske (2021) izdaje za zgodnji dostop:

1. Vodja projekta sklene podizvajalsko pogodbo z dobaviteljem. Pri podizvajalski pogodbi se privzeto uporabljajo ceniki, ki so priloženi zapisu dobavitelja. Račun dobavitelja ima vrsto odnosa **Prodajalec** ali **Dobavitelj**.

2. Vodja projekta lahko vse nakupe v podizvajalski pogodbi razvrsti kot postavke izdelka. Podizvajalske pogodbe so lahko vezane na čas, stroške ali izdelke. Razred transakcije v vsaki podrobnosti podizvajalske pogodbe določa, čemu ta podrobnost služi.

3. Upravljavec računa dobavitelja in vodja projekta lahko ponovita podizvajalsko pogodbo. Cene v nabavnem ceniku, ki so priložene podizvajalski pogodbi, se lahko prilagodijo.

4. Če je podrobnost podizvajalske pogodbe namenjena za časovni vnos, upravitelj računa dobavitelja na tej točki ali pozneje stike dobavitelja poveže z vsako vrstico podizvajalske pogodbe. Ta povezava posreduje informacije vodji projekta, ki dela na podizvajalski pogodbi. Ko je stik dobavitelja povezan s podrobnostjo podizvajalske pogodbe, sistem iz stika samodejno ustvari vir, ki ga je mogoče rezervirati, če tak vir še ne obstaja.

5. Način obračunavanja na vsaki vrstici podizvajalske pogodbe je lahko **Fiksna cena** ali **Čas in material**. Za podrobnosti podizvajalske pogodbe s fiksno ceno je nastavljen razpored za izdajanje računov, ki temelji na mejnikih.

Preostali koraki poteka poslovnega procesa za oddajanje naročil podizvajalcem, navedeni v pregledu, trenutno niso na voljo. Ko bodo dodane nove funkcije, bo tema posodobljena. 

Na spodnji sliki je predstavljena izdaja za oddajanje del podizvajalcem za zgodnji dostop, vpeta v kontekst celovitega poslovnega procesa.

![Potek procesa podizvajalskih pogodb](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Podrobnosti podizvajalske pogodbe, ki temeljijo na količini, in tiste, ki temeljijo na delu (izdaja za zgodnji dostop)
V oktobrski (2021) izdaji za zgodnji dostop so podprte samo podrobnosti podizvajalske pogodbe, ki temeljijo na količini. To pomeni, da je s pomočjo podrobnosti podizvajalske pogodbe z dobaviteljem mogoče načrtovati čas, stroške ali material, ne pa celotnega dela. To pomeni tudi, da je mogoče količino v podrobnostih podizvajalske pogodbe (enote časa, stroškov ali količino materiala) uporabiti za katerikoli projekt v sistemu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
