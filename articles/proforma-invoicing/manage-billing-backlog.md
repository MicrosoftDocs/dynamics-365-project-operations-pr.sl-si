---
title: Upravljanje nedokončanih opravil obračunavanja
description: Ta članek vsebuje informacije o tem, kako si ogledati in uporabljati nedokončana opravila obračunavanja v aplikaciji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929398"
---
# <a name="manage-billing-backlog"></a>Upravljanje nedokončanih opravil obračunavanja

**Velja za**: za scenarije v aplikaciji Project Operations, ki temeljijo na virih/nezalogi

Aplikacija Dynamics 365 Project Operations ima namenske poglede za pomoč pri upravljanju nedokončanih opravil obračunavanja. Za upravljanje nedokončanih opravil obračunavanja izberite povezave v območju **Prodaja** pod možnostjo **Obračunavanje**. 

Na voljo so ti pogledi:

- Honorarji in predujmi
- Razpoložljivi honorarji in predujmi
- Mejniki s fiksno ceno
- Nedokončana opravila obračunavanja časa in materiala

## <a name="retainers-and-advances"></a>Honorarji in predujmi

Pogled **Honorarji in predujmi** navaja honorarje in predujme v vseh projektnih pogodbah. Po zaračunanju honorarja ali predujma postane znesek predujma na voljo za uporabo.

## <a name="available-retainers-and-advances"></a>Razpoložljivi honorarji in predujmi

Pogled **Razpoložljivi honorarji in predujmi** navaja vse razpoložljive honorarje in predujme v vseh projektnih pogodbah. Po zaračunanju honorarja ali predujma postane znesek predujma na voljo za uporabo in je dodan na seznam. Ko je znesek honorarja ali predujma v celoti porabljen, se odstrani s seznama.

## <a name="fixed-price-milestones"></a>Mejniki s fiksno ceno

Pogled **Mejniki s fiksno ceno** navaja vse mejnike s fiksno ceno v vseh podrobnostih projektne pogodbe. V tem pogledu lahko enega ali več mejnikov označite kot **Pripravljeno na račun** ali **Ni pripravljeno na račun**. Z označevanjem mejnika kot **Pripravljeno za izdajanje računov** ta postane na voljo za dajanje na osnutke računov.

Ko imajo podrobnosti pogodbe za več strank način obračunavanja fiksne cene, je mejnik ustvarjen za vsako stranko v podrobnostih pogodbe. Mejnik je lahko ustvarjen in nato razdeljen na posamezne zapise mejnikov, specifične za stranko. Ta delitev je interna in v skladu z delitvijo odstotkov obračunavanja, opredeljenega za vsako stranko v podrobnostih pogodbe. V pogledu **Mejniki s fiksno ceno** boste videli posamezne zapise mejnikov, specifičnih za stranko. V tem pogledu je mogoče vsakega od teh zapisov o mejnikih ločeno označiti z možnostjo **Pripravljeno za izdajanje računa**. Ko je eden ali več povezanih razdeljenih mejnikov označenih kot **Pripravljeno na račun**, se stanje glave z **Ni se še začelo** posodobi na **V postopku**. Ko so vsi deli mejnika zaračunani, se stanje glave mejnika posodobi na **Dokončano**.

V tem pogledu je prikazan mejnik na osnutku računa s stanjem obračunavanja **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, je stanje obračunavanja na zapisu posodobljeno na **Račun za stranko je objavljen**. 

> [!NOTE] 
> Te vrednosti stanja ne posodabljajte s kodo po meri. Project Operations ne deluje pravilno, ko so te vrednosti stanja posodobljene s kodo po meri.

## <a name="time-and-material-billing-backlog"></a>Nedokončana opravila obračunavanja časa in materiala

V pogledu **Nedokončana opravila obračunavanja časa in materiala** so navedene vse neobračunane dejanske vrednosti prodaje po vseh projektnih pogodbah v sistemu, ki niso bile zaračunane. V tem pogledu lahko posamezno ali več dejanskih vrednosti neobračunane prodaje označimo kot **Pripravljeno za izdajanje računa** ali **Ni pripravljeno za izdajanje računa**. Če označite dejansko vrednost neobračunane prodaje kot **Pripravljeno za izdajanje računa**, bo na voljo za osnutek računa.

Neobračunanih dejanskih vrednosti prodaje s stanjem **Ni dovoljeno preseči** za **Ni uspelo** ni mogoče označiti kot **Pripravljeno za izdajanje računov**. Če je treba dejanske vrednosti označiti kot **Pripravljeno na račun**, ponastavite stanje za druge potrjene dejanske vrednosti v podrobnostih pogodbe in nato ponovno ocenite stanje **ne sme preseči**.

Če imajo podrobnosti pogodbe za več strank način obračunavanja časa in materiala, je ob odobritvi časa in stroškov ustvarjena ena dejanska vrednost neobračunane prodaje za vsako stranko v podrobnostih pogodbe v skladu z delitvijo odstotkov obračunavanja, opredeljenega za vsako od strank. V pogledu **Nedokončana opravila obračunavanja časa in materiala** boste videli te posamezne neobračunane dejanske vrednosti prodaje, specifične za stranko. V tem pogledu je mogoče vsakega od teh zapisov o dejanskih vrednostih neobračunane prodaje ločeno označiti z možnostjo **Pripravljeno za izdajanje računa**.

V tem pogledu je prikazana dejanska neobračunana prodaja na osnutku računa in ima status **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, se stanje obračunavanja tega zapisa posodobi na **Račun za stranko je knjižen**. 

> [!NOTE] 
> Te vrednosti stanja ne posodabljajte s kodo po meri. Project Operations ne deluje pravilno, ko so te vrednosti stanja posodobljene s kodo po meri.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
