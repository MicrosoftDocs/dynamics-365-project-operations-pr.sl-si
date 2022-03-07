---
title: Upravljanje več strank v podrobnostih pogodb, ki temeljijo na projektih – poenostavljeno
description: Ta tema zagotavlja informacije o upravljanju več strank v podrobnostih pogodb, ki temeljijo na projektu.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a7e29b1a92a5fefcf4812931383d03e5f81a27001f0e6525bb4eeb8dc93b18b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001811"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Upravljanje več strank v podrobnostih pogodb, ki temeljijo na projektih – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podrobnosti pogodb, ki temeljijo na projektu, lahko vključujejo seznam strank, ki so odgovorne za plačilo. Ta seznam strank v podrobnosti pogodbe, ki temelji na projektu, je lahko enak seznamu strank v pogodbi, vendar to ni zahtevano. Ko je projektna ponudba pridobljena in se ustvari projektna pogodba, se seznam strank v vrstici ponudbe kopira v ustrezne podrobnosti pogodbe. Stranke v ponudbi so kopirane v pogodbo.

Ko je projektna pogodba zaračunana, ima seznam strank v podrobnosti pogodbe, ki temelji na projektu, prednost pred seznamom strank v pogodbi. Seznam strank v projektni pogodbi se uporablja samo za privzete nove podrobnosti pogodbe.

Vse stranke pogodbe na zavihku **Stranke** v projektni pogodbi, so privzeto stranke podrobnosti pogodbe v vseh novih podrobnostih pogodb, ki so ustvarjene za projektno pogodbo. Vse obstoječe podrobnosti pogodbe ne bodo podedovale novih zapisov strank pogodbe, ki so ustvarjeni po njih.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Ustvarjanje, posodobitev ali brisanje zapisa stranke podrobnosti pogodbe

Stranko podrobnosti pogodbe lahko ustvarite, posodobite ali izbrišete na zavihku »Stranke podrobnosti pogodbe« na strani »Podrobnosti pogodbe, ki temelji na projektu«. Ko se v podrobnosti pogodbe, ki temelji na projektu, doda nova stranka, je ta dodana tudi v splošno pogodbo kot stranka pogodbe s privzetim odstotkom razdelitve stroškov nič odstotkov. Odstotek razdelitve stroškov splošne pogodbe se kopira v nove podrobnosti pogodbe in v morebitno projektno pogodbo. Pri izdajanju računov iz pogodbe pa se uporablja odstotek razdelitve stroškov na ravni podrobnosti pogodbe in ne odstotek razdelitve stroškov na ravni splošne pogodbe.

Spodaj so polja na zapisu stranke podrobnosti **pogodbe** v podrobnosti pogodbe, ki temelji na projektu, ki jih je treba upoštevati pri delu:

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| **Kupec** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | Vsi aktivni računi. Po ustvarjanju zapisa je to polje zaklenjeno. Če želite posodobiti polje, izbrišite zapis in ustvarite nov zapis. Če ste zabeležili kakršne koli dejanske vrednosti, zapisa ni mogoče izbrisati. Vendar lahko odstotek razdelitve stroškov za ta račun označite kot nič. Ko je zapis označen kot nič, to vpliva na morebitne dejanske stroške in prihodke, ki so pripisani ali razdeljeni tej stranki. | Ko na glavnem seznamu kupcev izberete kupca, ki ga želite dodati in shraniti, se stranka podrobnosti pogodbe doda kot stranka pogodbe. Stranke podrobnosti pogodbe se uporabljajo, ko se ustvarjajo računi. |
| **Odstotek delitve za izstavitev računa** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | To polje predstavlja odstotek vsake neobračunane prodajne transakcije, ki bo pripisana tej stranki podrobnosti pogodbe. | Stranke podrobnosti pogodbe in odstotki razdelitve stroškov se uporabljajo, ko se po odobritvi ustvarijo dejanske vrednosti in ko se ustvari račun. |
| **Omejitev »Ni dovoljeno preseči«** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za pogodbeno stranko. | Označuje, ali obstaja dogovorjena omejitev ali zgornja meja skupnega zneska, ki bo tej stranki zaračunan za te podrobnosti pogodbe. | Omejitev »Ni dovoljeno preseči« za stranko podrobnosti pogodbe se uporablja, ko se ustvarijo dejanske vrednosti in računi. |
| **Je zaokroževanje** | Mrežo lahko urejate na zavihku **Projektna pogodba** in obrazcema **Glavno** in **Hitro ustvarjanje** za stranko podrobnosti pogodbe. | To polje označuje, ali je ta stranka privzeta stranka za zaokroževanje za te podrobnosti pogodbe, ki temeljijo na projektu. | Ko ustvarite dejansko vrednost glede na odstotek razdelitve stroškov, lahko pride do nekaterih razlik v zaokroževanju. Tej stranki se v tem primeru pripišejo razlike v zaokroževanju. |

## <a name="edit-billing-split-percentages"></a>Urejanje odstotkov razdelitve stroškov

Odstotke razdelitve stroškov lahko urejate v mreži. Ko odstotki razdelitve stroškov ne znašajo 100 odstotkov, se prikaže napaka. Ko uredite odstotke razdelitve stroškov, osvežite stran, da obvestilo o napaki odstranite.

V podmreži stranke podrobnosti pogodbe lahko izberete možnost **Enakomerna razporeditev**. To dejanje enakomerno dodeli razdelitve stroškov vsem strankam podrobnosti pogodbe. Če obstaja dejavnik zaokroževanja, se doda stranki za zaokroževanje. Ena stranka podrobnosti pogodbe je vedno označena kot stranka za **Zaokroževanje** z nastavljeno zastavico **Zaokroževanje** na **Da**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]