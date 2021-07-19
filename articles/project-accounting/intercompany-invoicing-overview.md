---
title: Pregled izstavljanja računov med podjetji
description: Ta tema vsebuje informacije in primere o medpodjetnem izdajanju računov za projekte.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369396"
---
# <a name="intercompany-invoicing-overview"></a>Pregled izstavljanja računov med podjetji

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Vaša organizacija ima lahko več oddelkov, podružnic in drugih pravnih subjektov, ki si za projekte izmenjujejo izdelke in storitve. Pravna oseba, ki zagotavlja storitev ali izdelek, se imenuje *posojilna pravna oseba*. Pravna oseba, ki sprejme storitev ali izdelek, se imenuje *izposojevalna pravna oseba*.

Naslednja ilustracija prikazuje tipičen scenarij, ko si dve pravni entiteti, Contoso Robotics USA (izposojevalna pravna entiteta) in Contoso Robotics UK (posojilna pravna oseba) delita sredstva za izvedbo projekta za stranko Adventure works. V tem primeru je podjetje Contoso Robotics USA po pogodbi dolžno dostaviti delo podjetju Adventure Works.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]