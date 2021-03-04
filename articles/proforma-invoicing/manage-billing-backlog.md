---
title: Upravljanje nedokončanih opravil obračunavanja
description: Ta tema vsebuje informacije o tem, kako si ogledati in uporabljati nedokončana opravila obračunavanja v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122363"
---
# <a name="manage-the-billing-backlog"></a>Upravljanje nedokončanih opravil obračunavanja

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations ima dva namenska pogleda, ki vam pomagata pri delu in upravljanju nedokončanih opravil obračunavanja. To sta **Mejniki s fiksno ceno** in **Nedokončana opravila obračunavanja časa in materiala** Za izbiro pogleda pojdite v razdelek **Prodaja** v aplikaciji Project Operations in na levi strani za krmarjenje izberite **Obračunavanje**. Tam so shranjene povezave do nedokončanih opravil obračunavanja.

## <a name="fixed-price-milestones"></a>Mejniki s fiksno ceno

V tem pogledu so navedeni vsi mejniki s fiksno ceno vseh podrobnosti projektnih pogodb v sistemu. V tem pogledu lahko posamezne mejnike ali več mejnikov označimo kot **Pripravljeno za izdajanje računa** ali **Ni pripravljeno za izdajanje računa**. Ko označite mejnik z možnostjo **Pripravljeno za izdajanje računa**, postane na voljo za osnutek računa.

Ko imajo podrobnosti pogodb za več strank vzpostavljen način obračunavanja po fiksni ceni, se za vsako stranko v podrobnostih pogodb ustvari en mejnik. Uporabnik ustvari mejnik in ta mejnik se interno razdeli na zapise o posameznih mejnikih za stranke v skladu z razdelitvijo deleža obračuna, ki je določen za vsako stranko v podrobnostih pogodbe. V pogledu **Mejniki s fiksno ceno** boste videli zapise o posameznih mejnikih za stranke. V tem pogledu je mogoče vsakega od teh zapisov o mejnikih ločeno označiti z možnostjo **Pripravljeno za izdajanje računa**. Ko je eden ali več povezanih razdeljenih mejnikov označenih z možnostjo **Pripravljeno za izdajanje računa**, se glava premakne v stanje **V teku** iz **Se še ni začelo**. Ko so fakturirani vsi razdeljeni mejniki, se stanje glave mejnika spremeni v **Dokončano**.

V tem pogledu je prikazan mejnik na osnutku računa s stanjem obračunavanja **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, se stanje obračunavanja tega zapisa posodobi na **Račun je knjižen**. Posodabljanje teh vrednosti stanja s kodami po meri ni priporočljivo. Aplikacija Project Operations ne bo delovala pravilno, če bodo te vrednosti stanja posodobljene s kodami po meri.

## <a name="time-and-material-billing-backlog"></a>Nedokončana opravila obračunavanja časa in materiala

Ta pogled navaja vse dejanske prodajne podatke, ki niso bili fakturirani v vseh projektnih pogodbah v sistemu. V tem pogledu lahko posamezno ali več dejanskih vrednosti neobračunane prodaje označimo kot **Pripravljeno za izdajanje računa** ali **Ni pripravljeno za izdajanje računa**. Če označite dejansko vrednost neobračunane prodaje kot **Pripravljeno za izdajanje računa**, bo na voljo za osnutek računa.

Dejanskih vrednosti neobračunane prodaje, katerih stanje **Ne sme preseči** je **Neuspešno**, ni mogoče označiti kot **Pripravljeno za izdajanje računa**. Če je treba te dejanske vrednosti označiti kot take, ponastavite stanje drugih dejanskih vrednosti v podrobnostih pogodbe in ocenite stanje **Ne sme preseči**.

V primeru podrobnosti pogodb z več strankami, ki imajo vzpostavljen način obračunavanja po času in materialu, se ob odobritvi časa in stroškov za vsako stranko v podrobnostih pogodbe ustvari dejanska vrednost neobračunane prodaje glede na razdeljeni odstotek obračunavanja, ki je določen za vsako stranko v podrobnostih pogodbe. V pogledu **Nedokončana opravila obračunavanja časa in materiala** boste videli te dejanske vrednosti neobračunane prodaje za posamezne stranke. V tem pogledu je mogoče vsakega od teh zapisov o dejanskih vrednostih neobračunane prodaje ločeno označiti z možnostjo **Pripravljeno za izdajanje računa**.

V tem pogledu so prikazane dejanske vrednosti neobračunane prodaje na osnutku računa s **Stanjem obračunavanja** **Račun za stranko je ustvarjen**. Ko je osnutek računa potrjen, se stanje obračunavanja tega zapisa posodobi na **Račun za stranko je knjižen**. Posodabljanje teh vrednosti stanja s kodami po meri, kadar so v tem stanju, ni priporočljivo. Aplikacija Project Operations ne bo delovala pravilno, če bodo te vrednosti stanja posodobljene s kodami po meri.


[!INCLUDE[footer-include](../includes/footer-banner.md)]