---
title: Pregled uskladitve virov
description: Ta tema vsebuje informacije o zagotavljanju, da so rezervacije virov in dodelitve projektom poravnane.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084698"
---
# <a name="resource-reconciliation-overview"></a>Pregled uskladitve virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Pri članih ekipe so rezervacije in dodelitve ohlapno povezane. Z drugimi besedami, viri imajo lahko dodelitve brez rezervacij ali pa rezervacije brez dodelitev. V idealnem primeru so rezervacije in dodelitve usklajene, tako da imajo viri določeno zmogljivost za izvajanje dodelitev opravila. Vendar pa lahko rezervacije temeljijo na razpoložljivosti, časi opravil pa se lahko spremenijo, ko se projekt nadaljuje. Zato ohlapno povezovanje rezervacij in dodelitev zagotavlja prilagodljivost.

Zavihek **Uskladitev** v obrazcu **Projekt** omogoča vodjem projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektne ekipe.

Zavihek **Uskladitev** prikaže tudi rezervacije in dodelitve vse do ravni dodelitve posameznega opravila za vsakega člana ekipe. Ure so prikazane v celicah, ki predstavljajo časovna obdobja od mesecev do dni.

Zavihek prikazuje tudi skupno neto vsoto za projekt, skupaj s stolpcem **Skupaj**.

Zavihek za vsak vir izračuna razliko med rezervacijami člana ekipe in skupno vrednostjo dodelitev opravil člana ekipe. V idealnem primeru je ta razlika 0 (nič). Z drugimi besedami, med rezervacijami in dodelitvami ne bi smelo biti razlike. Razlike so obarvane in osenčene, da opozorijo na dva pogoja:

- **Primanjkljaj rezervacij** – do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij. Ker ta zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to stanje tako, da razširi rezervacije vira za kritje primanjkljaja.
- **Odvečne rezervacije** – do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom. Ta pogoj je morda sprejemljiv v primerih, ko je bil vir rezerviran za projekt, preden je prišlo do dodelitve opravila. V drugih primerih pa vir morda ni načrtovan za dodelitev opravilom. V takem primeru bi moral upravitelj projekta razmisliti o preklicu rezervacij vira, da se lahko zmogljivost uporabi za drug projekt.

Ko si ogledujete čas na višji ravni, kot je dnevna raven (npr. na ravni meseca), se v nekaterih primerih za vir lahko prikaže neto razlika nič (z drugimi besedami, rezervacije = dodelitve). Če pa pogledate čas na tedenski ravni, boste morda videli, da obstajajo dodelitve z nič urami in rezervacije s 40 urami v prvem tednu ter dodelitve s 40 urami in rezervacije z nič urami v drugem tednu meseca. Na splošno so rezervacije in dodelitve usklajene, vendar se razlikujejo od enega tedna do drugega.

Ko prikažete čas na višjih ravneh, imajo celice na zavihku **Usklajevanje** kazalnik, ki vas obvesti, da obstajajo razlike na nižjih ravneh. Z dvojnim klikom v celici lahko povečate prikaz in si ogledate razliko. Nato lahko kliknete z desno tipko miške, da pomanjšate prikaz. Če izberete vir in nato uporabite kontrolnik **Naslednja razlika** v orodni vrstici mreže, se lahko pomaknete na naslednjo razliko med rezervacijami in dodelitvami za ta vir. Nato lahko za vrnitev uporabite kontrolnik **Prejšnja razlika**. Prav tako lahko v meniju **Nastavitve** izklopite kazalnik razlike in delovanje krmarjenja.


Če imate dodelitve opravil za vir, a nimate rezervacij, na strani **Projekti** na zavihku **Usklajevanje** izberite primanjkljaj rezervacij in nato **Podaljšaj rezervacijo**. Prikaže se pogovorno **Podaljšaj rezervacijo** in prikaže rezervacijo, ki je potrebna za odpravo primanjkljaja vira. Prikazuje tudi obstoječe rezervacije vira za vse projekte ali druge entitete, ki jih je mogoče razporediti. Če izberete **V redu** , da ustvarite rezervacijo za vir, lahko ne glede na razpoložljivost tega vira ustvarite prekomerno rezervacijo.

Vodja projekta ali upravitelj virov lahko nato s ploščo razporeda reši vse primere, kjer ima vir preveliko število rezervacij glede na svojo zmogljivost.

