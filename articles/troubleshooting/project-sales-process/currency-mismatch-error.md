---
title: Napaka zaradi neujemanja valute
description: Ta članek ponuja informacije o odpravljanju težav v zvezi z napako zaradi neujemanja valute, ki se pojavi, ko shranite določene vrste zapisov.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914744"
---
# <a name="currency-mismatch-error"></a>Napaka zaradi neujemanja valute 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ko shranite projekt, pogodbo, ponudbo, vir, ki ga je mogoče rezervirati, lahko pride do napake **Valuta lastniškega podjetja se ne ujema z valuto pogodbene enote. Če želite nadaljevati, izberite drugo lastniško podjetje ali pogodbeno enoto za projektno pogodbo**. Do tega pride, ker obstaja napaka zaradi neujemanja valute med valuto pogodbene enote za zapis in valuto lastniškega podjetja.


## <a name="resolution"></a>Razrešitev

Če želite odpraviti to težavo, storite naslednje:
- Preverite valuto pogodbene enote za ta zapis. Valuto si lahko ogledate tako, da odprete zapis organizacijske enote in preverite vrednost v zavihku **Splošno** v polju **Valuta**.
- Preverite valuto lastniškega podjetja. Valuto si lahko ogledate tako, da odprete **Povezano** > **Glavne knjige** v zapisu podjetja. Dvokliknite zapis glavne knjige, ki je povezan s podjetjem, in preverite vrednost v zavihku **Splošno** v polju **Računovodska valuta**.

Če se valuta, nastavljena v pogodbeni enoti, in zapis glavne knjige ne ujemata, prilagodite konfiguracijo ali izberite druge vrednosti, ko shranite zapis. Sistem zahteva, da se ti zapisi ujemajo, da zagotovi pravilne tokove izdajanja računov med podjetji. Za več informacij o medpodjetniških konfiguracijah glejte [Ustvarjanje medpodjetnih transakcij](../../project-accounting/create-intercompany-transactions.md).

Če zapis podjetja nima povezanega zapisa glavne knjige, to pomeni, da pri nastavitvi okolja manjka konfiguracija. Konfiguracijo mora popraviti skrbnik sistema. Skrbnik sistema mora odpreti **Konfiguracije za dvojno zapisovanje** ter ustaviti in znova zagnati **Preslikave dvojnega zapisovanje v glavnih knjigah** z začetno sinhronizacijo te preslikave in njenimi predpogoji. Za več informacij si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../../environment/resource-dual-write-maps.md).
