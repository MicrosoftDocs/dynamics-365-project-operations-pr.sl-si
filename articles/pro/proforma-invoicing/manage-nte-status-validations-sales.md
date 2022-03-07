---
title: Upravljanje stanja in veljavnosti »Ni dovoljeno preseči«
description: Ta tema vsebuje informacije o preverjanjih veljavnosti »Ni dovoljeno preseči« izvedenih v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274054"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Upravljanje stanja in veljavnosti »Ni dovoljeno preseči« 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

## <a name="not-to-exceed-on-approvals"></a>»Ni dovoljeno preseči« za odobritve

Ko je oddan vnos časa ali stroškov, se ustvari zapis odobritve. Če je odobritev plačljiva in se ujema s podrobnosti pogodbe za čas in material, sistem opravi preverjanje veljavnosti »Ni dovoljeno preseči« na naslednjih ravneh:

  - Preverjanje omejitve, nastavljene za stranko v vrstici projektne pogodbe
  - Preverjanje omejitve, nastavljene v podrobnosti pogodbe
  - Preverjanje omejitve, nastavljene za stranko
  - Preverjanje omejitve, nastavljene v pogodbi

Preverjanja na vsaki ravni vključujejo zagotovitev, da znesek vrednosti prodaje na tej odobritvi ne bo kršil omejitve »Ni dovoljeno preseči« na tej ravni, potem ko se upošteva že zabeleženi znesek nedokončanih opravil obračunavanja in do danes zaračunani znesek na tej ravni.

Če preverjanje uspe, je stanje preverjanja veljavnosti odobritve **Uspelo**.

Če preverjanje ne uspe, je stanje preverjanja veljavnosti odobritve **Neuspelo**. Podrobnosti preverjanja veljavnosti »Ni dovoljeno preseči« uporabnika obvestijo, na kateri ravni preverjanje ni uspelo.

Kadar se oddani vnos časa ali stroškov šteje za neplačljivega, je stanje preverjanja veljavnosti »Ni dovoljeno preseči« nastavljeno na **Ni na voljo**, podrobnostmi preverjanja veljavnosti pa na **Ni na voljo**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>»Ni dovoljeno preseči« za neobračunane dejanske vrednosti prodaje

Ko je vnos časa ali stroškov odobren, se ustvarijo zapisi dejanskih vrednosti stroškov in neobračunane dejanske prodaje. Če je ustvarjena neobračunana dejanska vrednost prodaje plačljiva in se ujema s podrobnosti pogodbe za čas in material, aplikacija izvede preverjanje veljavnosti »Ni dovoljeno preseči« na naslednjih ravneh:

  - Preverjanje omejitve, nastavljene za stranko vrstice projektne pogodbe
  - Preverjanje omejitve, nastavljene v podrobnosti pogodbe
  - Preverjanje omejitve, nastavljene za stranko
  - Preverjanje omejitve, nastavljene v pogodbi

Preverjanja na vsaki ravni zagotavljajo, da znesek vrednosti prodaje na dejanskih podatkih ne bo kršil omejitve »Ni dovoljeno preseči« na tej ravni, potem ko se upošteva že zabeleženi znesek nedokončanih opravil obračunavanja in do danes zaračunani znesek na tej ravni.

Če preverjanje uspe, je stanje »Ni dovoljeno preseči« neobračunane dejanske prodaje **Potrjeno**.

Če preverjanje ne uspe, je stanje »Ni dovoljeno preseči« neobračunane dejanske prodaje **Neuspelo**. Podrobnosti preverjanja veljavnosti uporabnika obvestijo, na kateri ravni preverjanje ni uspelo.

Če se neobračunana dejanska vrednost prodaje obravnava kot neplačljivo ali brezplačno in če na nobeni od štirih ravni ni omejitve »Ni dovoljeno preseči« ali če je dejanska vrednost, ki se ustvarja, za stroške, honorar, enoto vira ali prodajo znotraj organizacije, morata biti polja **Stanje »Ni dovoljeno preseči«** in **Podrobnosti preverjanja veljavnosti »Ni dovoljeno preseči«** nastavljena na **Ni na voljo**.

## <a name="reset-the-not-to-exceed-status"></a>Ponastavitev stanja »Ni dovoljeno preseči«

Opravite lahko množično ponastavitev stanja »Ni dovoljeno preseči«. To vodjam projektov omogoča, da preverjanje veljavnosti »Ni dovoljeno preseči« prednostno obravnava določeno delo, čas ali stroške pred drugimi, ki so že potrjeni iz razpoložljivega zneska »Ni dovoljeno preseči«.

Ko je pri neobračunanih dejanskih vrednostih prodaje po ponastavitvi stanja »Ni dovoljeno preseči«, se potrjeni znesek zmanjša. Vodja projekta lahko izbere drugo delo, čas ali stroške, ki prej niso prestali preverjanja veljavnosti »Ni dovoljeno preseči«, ter jih znova oceni. Z zmanjšanjem potrjenega zneska bodo dejanske vrednosti zdaj prestale preverjanje veljavnosti. To vodji projekta za to obdobje zagotovi večji vpliv in nadzor nad fakturiranimi transakcijami.

Če želite ponastaviti stanje »Ni dovoljeno preseči« izberite eno ali več dejanskih vrednosti v pogledu **Nedokončana opravila obračunavanja časa in materiala** ali **Dejanske vrednosti** in nato izberite **Ponastavi stanje »Ni dovoljeno preseči«**.

Stanje »Ni dovoljeno preseči« je ponastavljeno na **Ni ocenjeno** na vseh pomembnih izbranih dejanskih vrednostih. Dejanske vrednosti, ki imajo ponastavljeno stanje »Ni dovoljeno preseči«, so neobračunane dejanske vrednosti prodaje, ki še niso fakturirane, niso na osnutku računa in so označene kot plačljive. Ostale izbrane dejanske vrednosti so prezrte.

## <a name="reevaluate-not-to-exceed-status"></a>Ponovno ocenjevanje stanja »Ni dovoljeno preseči«

Opravite lahko množično ponovno ocenjevanje stanja »Ni dovoljeno preseči«. Ponovno ocenjevanje stanja »Ni dovoljeno preseči« je uporabna v teh primerih:

  - Prišlo je do ponovnih pogajanj s stranko o omejitvah »Ni dovoljeno preseči«, zato je treba dejanske vrednosti ponovno oceniti.
  - Vodja projekta želi dodatno omejiti izdajanje računov za nedokončana opravila obračunavanja za prodajo tako, da daje prednost eni vrsti dela pred drugo.

Če želite ponovno oceniti stanje »Ni dovoljeno preseči« izberite eno ali več dejanskih vrednosti v pogledu **Nedokončana opravila obračunavanja časa in materiala** ali **Dejanske vrednosti** in nato izberite **Ponovno ocenjevanje stanja »Ni dovoljeno preseči«**.

Vse pomembne izbrane dejanske vrednosti z omejitvijo »Ni dovoljeno preseči« bodo ocenjene glede na nastavitev omejitve »Ni dovoljeno preseči«. Dejanske vrednosti, ki so pomembne za ponovno ocenjevanje stanja »Ni dovoljeno preseči«, so neobračunane dejanske vrednosti prodaje, ki niso fakturirane, niso na osnutku računa in so označene kot plačljive. Druge izbrane dejanske vrednosti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]