---
title: Upravljanje več strank v projektnih pogodbah – poenostavljeno
description: Ta tema vsebuje informacije o upravljanju več strank v projektnih pogodbah.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 015e407b1b9e464edec1e57ce6b5132f21f5ae6d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593080"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Upravljanje več strank v projektnih pogodbah – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Projektne pogodbe v aplikaciji Dynamics 365 Project Operations podpirajo scenarij, kjer pogodbeni dogovor vključuje več strank, ki financirajo posel. Na strani **Projektna pogodba** zavihek **Povzetek** vključuje polje **Stranka**. To polje določa primarno stranko posla. Druge stranke za posel lahko nastavite na strani **Projektna pogodba** na zavihku **Stranke**.

Vse stranke pogodbe, ki so na seznamu projektne pogodbe, so privzeto stranke podrobnosti pogodbe v vseh novih podrobnostih pogodb, ki temeljijo na projektu in so ustvarjene za projektno pogodbo. Obstoječe podrobnosti pogodbe, ki temeljijo na projektu, ne podedujejo novih strank pogodbe, ko nastajajo novi zapisi.

Podrobnosti pogodbe, ki temeljijo na izdelkih, so samodejno povezane s primarno stranko.

Stranke pogodbe in stranke podrobnosti pogodbe lahko pred sklenitvijo pogodbe kadar koli dodate, posodobite ali izbrišete.

## <a name="primary-customer"></a>Primarna stranka

Stranka, navedena na zavihku **Povzetek** v projektni pogodbi kot možna stranka je primarna stranka pogodbe. Ko poskusite izbrisati primarno stranko s seznama strank v pogodbi, boste prejeli sporočilo o napaki, da zapisa primarne stranke v pogodbi ni mogoče izbrisati.

Primarne stranke ni mogoče posodobiti s seznama strank pogodbe. Namesto tega spremenite možno stranko na zavihku **Povzetek** v pogodbi. Ko je to polje na strani **Povzetek pogodbe** posodobljeno, je nova stranka dodana kot nova stranka pogodbe z nastavljeno zastavico na **Primarno**. Prejšnja primarna stranka bo še vedno stranka v pogodbi.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Ustvarjanje, posodobitev ali brisanje zapisa stranke pogodbe

Stranko pogodbe lahko ustvarite, posodobite ali izbrišete z zavihka **Stranke** na strani **Projektna pogodba**. Polja v naslednji tabeli so v zapisu stranke pogodbe o projektni pogodbi in jih je treba upoštevati, ko delate s pogodbo.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **Kupec** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | Navedeni so vsi aktivni kupci. Po ustvarjanju zapisa je to polje zaklenjeno. Če želite posodobiti račun, izbrišite zapis in ga znova ustvarite. Če ste zabeležili kakršne koli dejanske vrednosti ali če je zapis stranke pogodbe primarna stranka, zapisa ne morete izbrisati. | Stranke pogodbe se kopirajo kot stranke podrobnosti pogodbe, ko se ustvarijo podrobnosti pogodbe. |
| **Odstotek delitve za izstavitev računa** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | Predstavlja odstotek vsake neobračunane prodajne transakcije, ki je pripisan tej stranki pogodbe. | Kopirano v nove podrobnosti pogodbe in stranke podrobnosti projektne pogodbe za nove podrobnosti projektne pogodbe. |
| **Ime stika za plačilo** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | To je besedilno polje in ga je treba uporabiti za identifikacijo stika za izstavljanje računa za to stranko. To polje sledi privzetim nastavitvam povezanega zapisa kupca. | Kopirano v polje **Ime stika za plačilo** na računu, ki je ustvarjen za to stranko. |
| **Ime plačnika** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za stranko pogodbe | To je besedilno polje in ga je treba uporabiti za identifikacijo stika za izstavljanje računa za to stranko. To polje sledi privzetim nastavitvam povezanega zapisa kupca. | Kopirano v polje **Ime stika za plačilo** na računu, ki je ustvarjen za to stranko. |
| **Plačilni pogoji** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | Ta vrednost sledi privzetim nastavitvam povezanega zapisa kupca. | Kopirano v polje **Ime stika za plačilo** na računu, ki je ustvarjen za to stranko. |
| **Je zaokroževanje** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | Označuje, ali je ta stranka privzeta stranka za zaokroževanje za ta posel. Na projektni pogodbi je lahko samo ena stranka za zaokroževanje. | Ko se stroški in neobračunana prodaja na količini možne stranke razdelijo na zaokroženo razliko, se ta razlika uporabi za dejansko vrednost, ki se preslikav to stranko. |
| **Omejitev »Ni dovoljeno preseči«** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za stranko pogodbe | Označuje, ali obstaja dogovorjena omejitev ali zgornja meja skupnega zneska, ki bo stranki zaračunan za to interakcijo. | **Omejitev »Ni dovoljeno preseči«** nastavljen na ravni stranke pogodbe bo ocenjen na **neobračunani dejanski vrednosti prodaje**, ki se sklicuje na to stranko pogodbe. |

## <a name="edit-billing-split-percentages"></a>Urejanje odstotkov razdelitve stroškov

Odstotke razdelitve stroškov lahko urejate z izkušnjo urejanja mreže v vrstici. Ko odstotki razdelitve stroškov ne znašajo 100 odstotkov, se prikaže napaka. Ko uredite odstotke razdelitve stroškov, osvežite stran, da obvestilo o napaki opustite.

Lahko tudi izberete možnost **Enakomerna razporeditev** na podmreži **Stranke pogodbe**, da enakomerno dodelite razdelitve stroškov vsem strankam pogodbe. Če obstaja dejavnik zaokroževanja, se doda stranki za zaokroževanje. Ena od strank pogodbe je vedno označena kot stranka za **zaokroževanje**, kar pomeni, da je v zapisu stranke pogodbe nastavljena zastavica **Da**. Običajno je to primarna stranka pogodbe, vendar jo je mogoče tudi spremeniti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]