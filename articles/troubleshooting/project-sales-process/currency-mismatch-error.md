---
title: Napaka neusklajenosti valute
description: Ta tema ponuja informacije o odpravljanju težav o napaki pri neujemanja valute, ki se pojavi, ko shranite določene vrste zapisov.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903795"
---
# <a name="currency-mismatch-error"></a>Napaka neusklajenosti valute 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ko shranite projekt, pogodbo, ponudbo ali vir, ki ga je mogoče rezervirati, se lahko prikaže napaka, **Valuta lastniškega podjetja se ne ujema z valuto pogodbene enote. Za nadaljevanje izberite drugo lastniško podjetje ali pogodbeno enoto**. To je zato, ker obstaja valutna neusklajenost med valuto pogodbene enote za zapis in valuto lastniškega podjetja.


## <a name="resolution"></a>Razrešitev

Če želite odpraviti to težavo, naredite naslednje:
- Preverite valuto pogodbene enote za ta zapis. Valuto si lahko ogledate tako, da odprete zapis organizacijske enote in preverite vrednost na **General** zavihek v **valuta** polje.
- Preverite valuto lastniškega podjetja. Valuto si lahko ogledate tako, da obiščete **Povezano** > **Glavne knjige** v evidenci podjetja. Dvokliknite zapis glavne knjige, ki je povezan s podjetjem, in preverite vrednost na **General** zavihek v **Računovodska valuta** polje.

Če se valuta, nastavljena v pogodbeni enoti, in zapis knjige ne ujemata, prilagodite konfiguracijo ali izberite različne vrednosti, ko shranite zapis. Sistem zahteva, da se ti zapisi ujemajo, da zagotovi pravilne tokove izdajanja računov med podjetji. Za več informacij o konfiguracijah med podjetji glejte [Ustvarite transakcije med podjetji](../../project-accounting/create-intercompany-transactions.md).

Če zapis podjetja nima povezanega zapisa glavne knjige, to pomeni, da pri nastavljanju okolja manjka konfiguracija. Konfiguracijo mora popraviti skrbnik sistema. Skrbnik sistema mora iti na **Konfiguracije dvojnega pisanja** in ustavite in znova zaženite **Zemljevid z dvojnim zapisom Ledgers** z začetno sinhronizacijo tega zemljevida in to predpogoji. Za več informacij si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../../environment/resource-dual-write-maps.md).
