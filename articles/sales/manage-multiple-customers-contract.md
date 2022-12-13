---
title: Upravljajte več strank na podlagi projektnih pogodb
description: Ta članek ponuja informacije o tem, kako upravljati več strank na podlagi pogodbe, ki temelji na projektu.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1aae178830d7b671c33295ca6d2910ee4be2f8dd
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825399"
---
# <a name="manage-multiple-customers-on-project-based-contracts"></a>Upravljajte več strank na podlagi projektnih pogodb

Ta članek vsebuje informacije o upravljanju več strank v projektni pogodbi. Projektno pogodbo lahko uporabite, kadar je za financiranje posla potreben pogodbeni sporazum za več strank. Na zavihku **Povzetek** na strani **Projektna pogodba** so vključene informacije o primarni stranki za posel. Druge stranke, ki prav tako sodelujejo pri poslu, lahko dodate v zavihku **Stranke**.

Vse stranke pogodbe na zavihku **Stranke** v projektni pogodbi, so privzeto stranke podrobnosti pogodbe v vseh novih podrobnostih pogodb, ki temeljijo na projektu in so ustvarjene za projektno pogodbo. Vse obstoječe podrobnosti pogodbe, ki temeljijo na projektu, ne podedujejo pozneje ustvarjenih novih zapisov o pogodbenih strankah.

Stranke pogodbe in stranke podrobnosti pogodbe lahko pred sklenitvijo pogodbe kadar koli dodate, posodobite ali izbrišete. Stranka v projektni pogodbi mora biti opredeljena kot stranka v lastniški družbi ali pravni osebi na strani **Stranke**. Pravne osebe so opredeljene v modulu **Upravljanje projektov in računovodstvo** storitve Dynamics 365 Project Operations in so na voljo kot podjetja v modulih **Projektna prodaja** in **Dostava** v storitvi Project Operations.

## <a name="primary-customers"></a>Primarne stranke

Potencialna stranka z zavihka **Povzetek** v projektni pogodbi je primarna stranka pogodbe. Primarne stranke ne morete posodobiti s seznama strank pogodbe. Če boste poskusili izbrisati primarno stranko s seznama strank po pogodbi, se bo pojavila napaka, da zapisa primarne stranke v pogodbi ni mogoče izbrisati. Namesto tega raje spremenite stranko v polju **Potencialna stranka** z zavihka **Povzetek** v projektni pogodbi. Ko boste posodobili to polje, se bo na novo izbrana stranka dodala kot nova pogodbena stranka z zastavico **Primarno** nastavljeno na **Da**. Prejšnja primarna stranka je še vedno stranka po pogodbi, vendar ni več primarna stranka.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Ustvarjanje, posodobitev ali brisanje zapisa stranke pogodbe

Stranko pogodbe lahko ustvarite, posodobite ali izbrišete na zavihku **Pogodbene stranke** na strani **Pogodba**. V zapis o pogodbeni stranki na projektni pogodbi so vključena naslednja polja.

| **Polje** | **Mesto** | **Opis** | 
| --- | --- | --- | 
| Račun | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | Navedeni so vsi aktivni kupci. Po ustvarjanju zapisa je to polje zaklenjeno. Če želite posodobiti zapis, ga morate najprej izbrisati in nato ponovno ustvariti. Če ste zabeležili kakršne koli dejanske vrednosti ali če je zapis stranke pogodbe primarna stranka, zapisa ne morete izbrisati. Ko se ustvarijo podrobnosti pogodbe, se stranke pogodbe kopirajo kot stranke podrobnosti pogodbe. |
| Odstotek delitve za izstavitev računa | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | Predstavlja odstotek vsake neobračunane prodajne transakcije, ki je pripisan stranki pogodbe. Ko so ustvarjene nove podrobnosti projektnih pogodb, se odstotek razdelitve obračunavanja kopira v vse na novo ustvarjene podrobnosti pogodb in v stranke podrobnosti projektnih pogodb. |
| Ime stika za plačilo | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | To besedilno polje je namenjeno za opredelitev kontaktne osebe računa za stranko. Uporabljena je privzeta vrednost iz povezanega zapisa kupca. Ime stika je kopirano v polje **Ime stika za plačilo** na računu, ki je ustvarjen za to stranko. |
| Ime plačnika | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | Uporabite to polje, da opredelite kontaktno osebo računa za stranko. Uporabljena je privzeta vrednost iz povezanega zapisa kupca. Ime je kopirano v polje **Ime stika za plačilo** na računu, ki je ustvarjen za to stranko. |
| Plačilni pogoji | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | Uporabljena je privzeta vrednost iz povezanega zapisa kupca. Pogoji so kopirani v polje **Ime stika za plačilo** na računu, ki je ustvarjen za to stranko. |
| Lastniško podjetje | Mrežo lahko urejate na zavihku **Pogodbene stranke projekta**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko projekta. | Pravna oseba, v katero je uvrščena stranka v modulu **Upravljanje projektov in računovodstvo**. To polje je samo za branje in je nastavljeno na podjetje, ki je lastnik projektne pogodbe.</br>Seznam strank, ki jih želite dodati v polje **Kupec**, je že filtrirano na seznam od lastniškega podjetja v modulu Project Operations **Vodenje projektov in računovodstvo**. Lastniško podjetje je enakovredno pravni osebi v modulu **Upravljanje projektov in računovodstvo** znotraj storitve Project Operations. Vsi stroški in prihodki, ki zapadejo iz projekta, so upoštevani v glavni knjigi lastniškega podjetja. |
| Je zaokroževanje | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | Označuje, ali je stranka privzeta stranka zaokroževanja za ta posel. Na projektni pogodbi je lahko samo ena stranka za zaokroževanje. Ko se stroški in neobračunana prodaja razdelijo po količini in privedejo do zaokrožene razlike, se ta razlika uporabi za dejansko vrednost, ki se preslika v to stranko. |
| Omejitev »Ni dovoljeno preseči« | Mrežo lahko urejate na zavihku **Pogodbene stranke**, na glavni strani in na strani za hitro ustvarjanje za pogodbeno stranko. | Označuje, ali obstaja dogovorjena omejitev ali zgornja meja skupnega zneska, ki bo stranki zaračunan za interakcijo. Omejitev »Ni dovoljeno preseči«, nastavljena na ravni pogodbene stranke, je ocenjena na podlagi neobračunane dejanske vrednosti prodaje, ki se sklicuje na to pogodbeno stranko. |

## <a name="edit-billing-split-percentages"></a>Urejanje odstotkov razdelitve stroškov

Odstotke razdelitve stroškov lahko urejate v mreži. Ko odstotki razdelitve stroškov ne znašajo 100 odstotkov, se pojavi napaka. Ko uredite odstotke razdelitve stroškov, osvežite stran **Projektna pogodba**, da odstranite obvestilo o napaki odstranite.

V podmreži stranke projektne pogodbe lahko izberete tudi možnost **Enakomerna razporeditev**. Razdelitev obračunavanja je enakomerno razporejena med vsemi strankami projektne pogodbe. Če obstaja dejavnik zaokroževanja, se doda stranki zaokroževanja. Ena od pogodbenih strank ima zastavico **Zaokroževanje** vedno nastavljeno na **Da**. To je stranka zaokroževanja. Običajno je stranka zaokroževanja tudi glavna pogodbena stranka, vendar ni vedno tako.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
