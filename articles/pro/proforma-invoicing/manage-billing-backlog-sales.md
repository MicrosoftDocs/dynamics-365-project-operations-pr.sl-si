---
title: Upravljanje nedokončanih opravil obračunavanja – poenostavljena različica
description: V tej temi so na voljo informacije o različnih pogledih, ki so na voljo za uporabo ob upravljanju nedokončanih opravil obračunavanja.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176991"
---
# <a name="manage-the-billing-backlog---lite"></a>Upravljanje nedokončanih opravil obračunavanja – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Dynamics 365 Project Operations ima namenske poglede za pomoč pri upravljanju nedokončanih opravil obračunavanja. Za upravljanje nedokončanih opravil obračunavanja izberite povezave v območju **Prodaja** pod možnostjo **Obračunavanje**. 

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
