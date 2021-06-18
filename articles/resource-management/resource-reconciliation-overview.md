---
title: Pregled uskladitve virov
description: Ta tema podaja informacije, ki vam bodo pomagale zagotoviti, da so rezervacije virov in dodelitve za projekte poravnane.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: be171063c21318f517a37f3088e3f577fd4b6715
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000861"
---
# <a name="resource-reconciliation-overview"></a>Pregled uskladitve virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Pri članih ekipe so rezervacije in dodelitve ohlapno povezane. Z drugimi besedami, viri imajo lahko dodelitve in so brez rezervacij ali pa imajo rezervacije in so brez dodelitev. V idealnem primeru so rezervacije in dodelitve usklajene, tako da imajo viri določeno zmogljivost za izvajanje dodelitev opravila. Vendar pa lahko rezervacije temeljijo na razpoložljivosti, časi opravil pa se lahko spremenijo, ko se projekt nadaljuje. Zato ohlapno povezovanje rezervacij in dodelitev zagotavlja prilagodljivost.

Zavihek **Uskladitev** na strani **Projekti** omogoča vodjam projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektne ekipe.

Zavihek **Uskladitev** prikaže rezervacije in dodelitve vse do ravni dodelitve posameznega opravila za vsakega člana ekipe. Ure so prikazane v celicah, ki predstavljajo različna obdobja, tako mesece kot posamezne dni. Zavihek prikazuje tudi skupno neto vsoto za projekt, skupaj s stolpcem **Skupaj**.

Zavihek **Uskladitev** za vsak vir izračuna razliko med rezervacijami člana ekipe in skupno vrednostjo dodelitev opravil tega člana ekipe. V idealnem primeru je ta razlika 0 (nič). Z drugimi besedami, med rezervacijami in dodelitvami ne bi smelo biti razlike. Razlike so obarvane in osenčene, da opozorijo na dva pogoja:

- **Primanjkljaj rezervacij** – do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij. Ker zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to stanje tako, da razširi rezervacije vira za kritje primanjkljaja.
- **Odvečne rezervacije** – do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom. Ta pogoj je morda sprejemljiv v primerih, ko je bil vir rezerviran za projekt, preden je prišlo do dodelitve opravila. Toda v drugih primerih, kjer se ne načrtuje dodelitev vira opravilom, mora projektni vodja razmisliti o preklicu rezervacij vira. Na ta način se lahko zmogljivost uporabi za drug projekt.

Ko si ogledujete čas na višji ravni, kot je dnevna raven (npr. na ravni meseca), se v nekaterih primerih za vir lahko prikaže neto razlika nič (z drugimi besedami, rezervacije so enake dodelitvam). Če pa pogledate čas na tedenski ravni, boste morda videli, da obstajajo dodelitve z nič urami in rezervacije s 40 urami v prvem tednu ter dodelitve s 40 urami in rezervacije z nič urami v drugem tednu meseca. Na splošno so rezervacije in dodelitve usklajene, vendar se razlikujejo od enega tedna do drugega.

Ko prikažete čas na višjih ravneh, imajo celice na zavihku **Usklajevanje** kazalnik, ki vas obvesti, da obstajajo razlike na nižjih ravneh. Z dvojnim tapom ali dvojnim klikom v celici lahko povečate prikaz in si ogledate razliko. Nato lahko izberete in pridržite (ali kliknete z desno tipko miške), da pomanjšate prikaz. Če izberete vir in nato uporabite kontrolnik **Naslednja razlika** v orodni vrstici mreže, se lahko pomaknete na naslednjo razliko med rezervacijami in dodelitvami za ta vir. Nato lahko za vrnitev uporabite kontrolnik **Prejšnja razlika**. Prav tako lahko v meniju **Nastavitve** izklopite kazalnik razlike in delovanje krmarjenja.

Če imate dodelitve opravil za vir, a nimate rezervacij, izberite primanjkljaj rezervacij na zavihku **Usklajevanje** strani **Projekti** in nato izberite **Podaljšaj rezervacijo**. Prikaže se pogovorno okno **Podaljšaj rezervacijo** in prikaže rezervacijo, ki je potrebna za odpravo primanjkljaja vira. Pogovorno okno prikazuje tudi obstoječe rezervacije vira za vse projekte ali druge entitete, ki jih je mogoče razporediti. Če izberete **V redu**, da ustvarite rezervacijo za vir, lahko ne glede na razpoložljivost tega vira ustvarite prekomerno rezervacijo.

Rezervacije, ki so ustvarjene z dejanjem **Podaljšaj rezervacijo**, so povezane s primarno zahtevo za projekt. Ko je razširitev sprožena, ni mogoče določiti posebne zahteve, ki mora biti razširjena, ker je lahko vir povezan z več kot eno zahtevo za projekt.

Vodja projekta ali upravitelj virov lahko nato s ploščo razporeda reši vse primere, kjer ima vir preveliko število rezervacij glede na svojo zmogljivost.


[!INCLUDE[footer-include](../includes/footer-banner.md)]