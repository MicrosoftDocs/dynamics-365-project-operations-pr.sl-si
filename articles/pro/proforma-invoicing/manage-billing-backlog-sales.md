---
title: Upravljanje nedokončanih opravil obračunavanja v projektu
description: Ta tema vsebuje informacije o različnih pogledih, ki so na voljo za upravljanje nedokončanih opravil obračunavanja na projektih.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988311"
---
# <a name="manage-project-billing-backlog"></a>Upravljanje nedokončanih opravil obračunavanja v projektu 

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations ima namenske poglede za pomoč pri upravljanju nedokončanih opravil obračunavanja. Za upravljanje nedokončanih opravil obračunavanja izberite povezave v območju **Prodaja** pod možnostjo **Obračunavanje**. 

Na voljo so ti pogledi:

- Honorarji in predujmi
- Razpoložljivi honorarji in predujmi
- Mejniki s fiksno ceno
- Nedokončana opravila obračunavanja izdelkov
- Nedokončana opravila obračunavanja časa in materiala

## <a name="retainers-and-advances"></a>Honorarji in predujmi

V pogledu **Honorarji in predujmi** so navedeni vsi honorarji in predujmi po vseh projektnih pogodbah v sistemu. Po zaračunanju honorarja ali predujma postane znesek predujma na voljo za uporabo.

## <a name="available-retainers-and-advances"></a>Razpoložljivi honorarji in predujmi

V pogledu **Razpoložljivi honorarji in predujmi** so navedeni vsi razpoložljivi honorarji in predujmi po vseh projektnih pogodbah v sistemu. Po zaračunanju honorarja ali predujma postane znesek predujma na voljo za uporabo in je dodan na seznam. Ko je znesek honorarja ali predujma povsem porabljen, je odstranjen s seznama.

## <a name="fixed-price-milestones"></a>Mejniki s fiksno ceno

V pogledu **Mejniki s fiksno ceno** so navedeni mejniki s fiksno ceno po vseh podrobnostih projektne pogodbe v sistemu. V tem pogledu lahko posamezne mejnike ali več mejnikov označimo kot **Pripravljeno za izdajanje računa** ali **Ni pripravljeno za izdajanje računa**. Z označevanjem mejnika kot **Pripravljeno za izdajanje računov** ta postane na voljo za dajanje na osnutke računov.

Ko imajo podrobnosti pogodbe za več strank način obračunavanja fiksne cene, je mejnik ustvarjen za vsako stranko v podrobnostih pogodbe. Mejnik je lahko ustvarjen in nato razdeljen na posamezne zapise mejnikov, specifične za stranko. Ta delitev je interna in v skladu z delitvijo odstotkov obračunavanja, opredeljenega za vsako stranko v podrobnostih pogodbe. V pogledu **Mejniki s fiksno ceno** boste videli posamezne zapise mejnikov, specifičnih za stranko. V tem pogledu je mogoče vsakega od teh zapisov o mejnikih ločeno označiti z možnostjo **Pripravljeno za izdajanje računa**. Ko je eden ali več povezanih delitev mejnikov označenih kot **Pripravljeno za izdajanje računov**, je stanje glave posodobljeno na **V teku** s **Ni se začelo**. Ko so vse delitve mejnika zaračunane, je stanje mejnika glave posodobljeno na **Dokončano**.

V tem pogledu je prikazan mejnik na osnutku računa s stanjem obračunavanja **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, je stanje obračunavanja na zapisu posodobljeno na **Račun za stranko je objavljen**. Te vrednosti stanja ne posodobite s kodo po meri. Project Operations ne deluje pravilno, ko so te vrednosti stanja posodobljene s kodo po meri.

## <a name="product-billing-backlog"></a>Nedokončana opravila obračunavanja izdelkov

V pogledu **Nedokončana opravila obračunavanja izdelkov** so navedene vse podrobnosti pogodbe, ki temeljijo na izdelkih, po vseh projektnih pogodbah v sistemu. V tem pogledu lahko posamezne podrobnosti pogodbe, ki temeljijo na izdelkih, ali več podrobnosti pogodbe, ki temeljijo na izdelkih, označimo kot **Pripravljeno za izdajanje računa** ali **Ni pripravljeno za izdajanje računa**. Z označevanjem podrobnosti pogodbe, ki temeljijo na izdelkih, kot **Pripravljeno za izdajanje računov** ta postane na voljo za dajanje na osnutke računov.

Podrobnosti pogodbe, ki temeljijo na izdelkih, ki so na osnutku računa, so prikazane v tem pogledu s stanjem obračunavanja **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, se stanje obračunavanja tega zapisa posodobi na **Račun za stranko je knjižen**. Te vrednosti stanja ne posodobite s kodo po meri. Project Operations ne deluje pravilno, ko so te vrednosti stanja posodobljene s kodo po meri.

## <a name="time-and-material-billing-backlog"></a>Nedokončana opravila obračunavanja časa in materiala

V pogledu **Nedokončana opravila obračunavanja časa in materiala** so navedene vse neobračunane dejanske vrednosti prodaje po vseh projektnih pogodbah v sistemu, ki niso bile zaračunane. V tem pogledu lahko posamezno ali več dejanskih vrednosti neobračunane prodaje označimo kot **Pripravljeno za izdajanje računa** ali **Ni pripravljeno za izdajanje računa**. Če označite dejansko vrednost neobračunane prodaje kot **Pripravljeno za izdajanje računa**, bo na voljo za osnutek računa.

Neobračunanih dejanskih vrednosti prodaje s stanjem **Ni dovoljeno preseči** za **Ni uspelo** ni mogoče označiti kot **Pripravljeno za izdajanje računov**. Če morajo biti dejanske vrednosti označene kot **Pripravljeno za izdajanje računov**, ponastavite stanje drugih dejanskih vrednosti na podrobnostih pogodbe, ki so potrjene. In nato znova ocenite stanje **Ni dovoljeno preseči**.

Če imajo podrobnosti pogodbe za več strank način obračunavanja časa in materiala, je ob odobritvi časa in stroškov ustvarjena ena dejanska vrednost neobračunane prodaje za vsako stranko v podrobnostih pogodbe v skladu z delitvijo odstotkov obračunavanja, opredeljenega za vsako od strank. V pogledu **Nedokončana opravila obračunavanja časa in materiala** boste videli te posamezne neobračunane dejanske vrednosti prodaje, specifične za stranko. V tem pogledu je mogoče vsakega od teh zapisov o dejanskih vrednostih neobračunane prodaje ločeno označiti z možnostjo **Pripravljeno za izdajanje računa**.

Dejanska vrednost neobračunane prodaje, ki je na osnutku računa, je prikazana v tem pogledu s stanjem obračunavanja **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, se stanje obračunavanja tega zapisa posodobi na **Račun za stranko je knjižen**. Te vrednosti stanja ne posodobite s kodo po meri. Project Operations ne deluje pravilno, ko so te vrednosti stanja posodobljene s kodo po meri.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
