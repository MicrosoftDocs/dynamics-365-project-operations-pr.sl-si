---
title: Upravljanje več strank v podrobnostih ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o upravljanju več strank pri podrobnostih ponudb, ki temeljijo na projektu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4fa0adc877797d782173f29690b33d38ba7f8dcd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277943"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Upravljanje več strank v podrobnostih ponudb, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Podrobnosti ponudb, ki temeljijo na projektu, podpirajo scenarije, kjer ima vsaka podrobnost ponudbe seznam strank, ki zanj plačujejo. Ta seznam strank pri podrobnostih ponudb, ki temeljijo na projektu, je lahko enak seznamu strank v ponudbi. Seznam strank lahko spremenite tudi tako, da je drugačen. Za ustvarjanje morebitne pogodbe za projekt, ko pridobite ponudbo za projekt, se seznam strank pri podrobnostih ponudb, ki temeljijo na projektu, kopira v ustrezno podrobnost pogodbe, ki temelji na projektu. Stranke v ponudbi, ki temelji na projektu, se kopirajo v pogodbo za projekt.

Ko izstavite račun za morebitno pogodbo za projekt, ima seznam strank pri podrobnosti pogodbe, ki temelji na projektu, prednost pred seznamom v pogodbi za projekt. Seznam strank v pogodbi za projekt se uporablja samo za privzete nastavitve v podrobnostih pogodbe za nov projekt.

Vse stranke ponudbe na zavihku **Stranke** ponudbe za projekt so privzeto nastavljene kot stranke v podrobnostih ponudbe pri katerih koli podrobnostih ponudbe, ki temelji na projektu, ustvarjenih za ponudbo za projekt. Morebitne obstoječe podrobnosti ponudbe, ki temelji na projektu, ne podedujejo novih zapisov strank o ponudbah, ki so bili ustvarjeni pozneje.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Ustvarjanje, posodobitev oz. brisanje zapisa stranke s podrobnostmi ponudbe

Ustvarite, posodobite ali izbrišete lahko stranko s podrobnostmi ponudbe na zavihku **Stranke v podrobnostih ponudbe** na strani **Podrobnosti ponudb, ki temeljijo na projektih**. Ko dodate novo stranko v podrobnost ponudbe, ki temelji na projektu, se stranka doda tudi v celotno ponudbo kot stranka ponudbe, pri čemer je privzeti odstotek razdelitve stroškov za celotno ponudbo 0 %. Odstotek razdelitve stroškov za celotno ponudbo se kopira v nove podrobnosti ponudbe in v morebitno pogodbo za projekt. Vendar se pri izstavljanju računov iz pogodbe uporablja odstotek razdelitve stroškov na ravni podrobnosti ponudbe in ne odstotek razdelitve stroškov na celotni ravni pogodbe. 

Naslednja tabela prikazuje polja pri zapisu stranke podrobnosti ponudbe za podrobnost ponudbe, ki temelji na projektu.

| Polje | LOkacija | Opis in navodila | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **Kupec** | Mreža, ki jo je mogoče urejati, na zavihku **Stranke v podrobnostih ponudbe**, glavni obrazec in obrazec za hitro ustvarjanje za stranko v podrobnostih ponudbe. | Navedeni so vsi aktivni kupci. Po ustvarjanju zapisa je to polje zaklenjeno. Če želite posodobiti polje, izbrišite in znova ustvarite zapis. Če ste zabeležili dejanske vrednosti, zapisa ne morete izbrisati. | Ko na glavnem seznamu kupcev izberete kupca, ki ga želite dodati, se stranka v podrobnostih ponudbe doda tudi kot stranka ponudbe. Ko je ponudba pridobljena, se stranke v podrobnostih ponudbe kopirajo v stranke v podrobnostih pogodbe za projekt. |
| **Odstotek delitve za izstavitev računa** | Mreža, ki jo je mogoče urejati, na zavihku **Stranke v podrobnostih ponudbe**, glavni obrazec in obrazec za hitro ustvarjanje za stranko v podrobnostih ponudbe. | Predstavlja odstotek vsake neobračunane prodajne transakcije, ki bo pripisana tej stranki v podrobnostih ponudbe. | Kopirano med stranke v podrobnostih pogodbe za projekt. |
| **Omejitev »Ni dovoljeno preseči«** | Mreža, ki jo je mogoče urejati, na zavihku **Stranke v podrobnostih ponudbe**, glavni obrazec in obrazec za hitro ustvarjanje za stranko v podrobnostih ponudbe. | Označuje, ali obstaja dogovorjena omejitev ali zgornja meja skupnega zneska, ki bo tej stranki zaračunan za to podrobnost ponudbe. | Kopirano med stranke v podrobnostih pogodbe za projekt, ko je pridobljena ponudba. |
| **Lastniško podjetje** | Mreža, ki jo je mogoče urejati, na zavihku **Stranke v podrobnostih ponudbe**, glavni obrazec in obrazec za hitro ustvarjanje za stranko v podrobnostih ponudbe. | Pravna oseba, pri kateri je ta stranka nastavljena v modulu **Vodenje projektov in računovodstvo**. To polje je samo za branje in je nastavljeno na lastniško podjetje same ponudbe. Seznam strank, ki jih želite dodati v polje **Kupec**, je že filtrirano na seznam od lastniškega podjetja v modulu Project Operations **Vodenje projektov in računovodstvo**. | Lastniško podjetje je enako konceptu pravne osebe. Vsi stroški in prihodki, ki nastanejo pri tem projektu, se zabeležijo v glavni knjigi lastniškega podjetja. |
| **Je zaokroževanje** | Mreža, ki jo je mogoče urejati, na zavihku **Stranke v podrobnostih ponudbe**, glavni obrazec in obrazec za hitro ustvarjanje za stranko v podrobnostih ponudbe. | Označuje, ali je ta stranka privzeta stranka za zaokroževanje za to podrobnost ponudbe, ki temelji na projektu. | Kopirano med stranke v pogodbi za projekt, ko je pridobljena ponudba. |

## <a name="edit-billing-split-percentages"></a>Urejanje odstotkov razdelitve stroškov

Odstotke razdelitve stroškov lahko uredite v vrstici. Ko odstotki razdelitve stroškov ne znašajo skupno 100 %, pride do napake. Ko uredite odstotke razdelitve stroškov, osvežite stran s podrobnostjo ponudbe, da odstranite napako.

Uporabite dejanje enakomerne porazdelitve v podmreži strank za podrobnosti ponudbe, da dodelite odstotke razdelitve stroškov vsem strankam v podrobnostih ponudbe. Če obstaja dejavnik zaokroževanja, bo to dodano stranki za zaokroževanje. Ena od strank v podrobnostih ponudbe je vedno označena kot stranka za zaokroževanje, kar pomeni, da ima zapis stranke v podrobnostih ponudbe zastavico za zaokroževanje nastavljeno na **Da**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]