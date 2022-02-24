---
title: Pregled izstavljanja računov med podjetji
description: Ta tema vsebuje informacije in primere o medpodjetnem izdajanju računov za projekte.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595555"
---
# <a name="intercompany-invoicing-overview"></a>Pregled izstavljanja računov med podjetji

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Vaša organizacija ima lahko več oddelkov, podružnic in drugih pravnih subjektov, ki si za projekte izmenjujejo izdelke in storitve. Pravna oseba, ki zagotavlja storitev ali izdelek, se imenuje *posojilna pravna oseba*. Pravna oseba, ki sprejme storitev ali izdelek, se imenuje *izposojevalna pravna oseba*.

Naslednja slika prikazuje tipičen scenarij, kjer si dve pravni osebi, Contoso Robotics USA (izposojevalna pravna oseba) in Contoso Robotics UK (posojilna pravna oseba), delita sredstva za izvedbo projekta za stranko Adventure works. V tem scenariju je podjetje Contoso Robotics USA po pogodbi dolžno opraviti storitev za Adventure Works.

![Izstavljanje računov med podjetji](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations uporablja spodaj prikazani potek za obdelavo medpodjetnih transakcij:

1. Viri posojilne pravne entitete beležijo medpodjetne transakcije s časom ali stroški, tako da knjižijo čas in stroške za projekte v izposojevalni pravni entiteti.
2. Čas in stroški so zabeleženi v posojilnem podjetju po ceniku izposojevalnega podjetja.
3. Medpodjetne neobračunane prodajne transakcije so zabeležene v posojilnem podjetju po ceniku izposojevalnega podjetja.
4. Neobračunani prihodki so zabeleženi v izposojevalnem podjetju po prodajnem ceniku projektne pogodbe. Stranki se lahko zaračuna, ko se zabeležijo neobračunani prihodki. Stranki ni treba čakati, da se zaključi obdelava izdajanja računov med podjetji.
5. Medpodjetni računi za stranke se periodično ustvarjajo v posojilnem podjetju. Računi se ustvarjajo ročno ali z uporabo periodičnega avtomatiziranega procesa. Ustvariti je mogoče poseben račun za vsako izposojevalno pravno osebo ali ločene račune po projektih.
6. Ko je račun za medpodjetno stranko knjižen v posojilni pravni osebi, se v izposojevalni pravni osebi ustvari čakajoč račun za dobavitelja. Stroški na čakajočem računu za dobavitelja bodo zabeleženi v podknjigi projekta ob knjiženju računa.

Naslednji diagram prikazuje medpodjetno izdajanje računov, saj se nanaša na računovodske dogodke in pričakovana knjiženja v glavno knjigo.

![Medpodjetni potek](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Dodatni viri

- [Konfiguriranje izstavljanja računov med podjetji](configure-intercompany-invoicing.md)
- [Beleženje medpodjetnih transakcij](create-intercompany-transactions.md)
- [Ustvarjanje računov medpodjetnih strank in prodajalcev](create-intercompany-customer-vendor-invoices.md)
