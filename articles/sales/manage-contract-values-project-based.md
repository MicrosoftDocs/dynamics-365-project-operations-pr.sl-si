---
title: Delo s podrobnostmi pogodbe, ki temeljijo na projektu
description: V tej temi so na voljo informacije o podrobnostih pogodb, ki temeljijo na projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990066"
---
# <a name="work-with-projectbased-contract-lines"></a>Delo s podrobnostmi pogodbe, ki temeljijo na projektu

Podrobnosti pogodbe, ki temelji na projektu, v aplikaciji Dynamics 365 Project Operations so zasnovane, da hranijo dogovore o oceni in obračunavanju za določene komponente dela na projektu v interakciji. Struktura podrobnosti pogodbe, ki temeljijo na projektu, je razširjena za ocene projektov in scenarije obračunavanja z naslednjimi koncepti:

- Način obračunavanja
- Preslikavanje projektov in opravil
- Vključuje razrede transakcij
- Omejitev »Ni dovoljeno preseči«
- Nastavitev možnosti zaračunavanja
- Ocene s podrobnosti vrstice pogodbe
- Stranke podrobnosti pogodbe

Naslednja polja so vključena na zavihku **Splošno** podrobnosti pogodbe, ki temeljijo na projektu. Ta polja pomagajo nastaviti podlago za podrobno, celovito oceno in dogovore za obračunavanje za delo, ki temelji na projektu.

| Polje | Opis | Nadaljnji vpliv |
| --- | --- | --- |
| **Ime** | Ime podrobnosti pogodbe, ki opredeljuje posamezno komponento pogodbe, ki se ocenjuje. Za projektno pogodbo, ustvarjeno iz ponudbe, je ta vrednost kopirana iz pripadajoče vrednosti podrobnosti ponudbe, ki temelji na projektu. | Ta vrednost polja je kopirana v projektno vrstico računa, ki je ustvarjena iz teh podrobnosti pogodbe, ko je ustvarjen račun. |
| **Način obračunavanja** | V projektni pogodbi, ustvarjeni iz ponudbe, je ta vrednost kopirana iz pripadajočega polja podrobnosti ponudbe. To je nabor možnosti, ki predstavlja dva glavna pogodbena modela, ki ju podpira Project Operations:</br>- **Fiksna cena**</br>- **Čas in material** | Na podlagi metode obračunavanja v sklicevanih podrobnostih pogodbe bo dejanska transakcija obdelana. Če imajo podrobnosti pogodbe, sklicevane z dejansko vrednostjo, način obračunavanja časa in materiala, sta ustvarjena zapisa stroška in dejanska vrednost neobračunane prodaje. Če imajo podrobnosti pogodbe, na katere se sklicuje dejanska vrednost, način obračunavanja fiksne cene, je ustvarjena samo dejanska vrednost stroška. |
| **Project** | Uporabite to polje za prepoznavanje projekta, ki bo uporabljen za zagotavljanje dela za to interakcijo. | Vrednost v tem polju je uporabljena v povezavi s poljema **Vključena opravila** in **Vključeni razredi transakcij** za odpravljanje sklica podrobnosti pogodbe v zapisu dejanskih ali ocenjenih podrobnosti. |
| **Vključi čas** | Oznaka označuje, ali so časovne transakcije ali stroški dela v izbranem projektu vključeni v te podrobnosti pogodbe. Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v te podrobnosti pogodbe. Vrednost **Da** označuje, da bodo. | Ta vrednost polja je uporabljena v povezavi s projektom za odpravljanje sklica podrobnosti pogodbe v zapisu dejanskih ali ocenjenih podrobnosti. |
| **Vključi strošek** | Oznaka označuje, ali bodo stroški v izbranem projektu vključeni v te podrobnosti pogodbe. Vrednost **Ne** označuje, da stroški ne bodo vključeni v te podrobnosti pogodbe. Vrednost **Da** označuje, da bodo. | Ta vrednost polja je uporabljena v povezavi s projektom za odpravljanje sklica podrobnosti pogodbe v zapisu dejanskih ali ocenjenih podrobnosti. |
| **Vključi dajatev** | Oznaka označuje, ali bodo dajatve v izbranem projektu vključene v te podrobnosti pogodbe. Vrednost **Ne** označuje, da dajatve ne bodo vključene v te podrobnosti pogodbe. Vrednost **Da** označuje, da bodo. | Ta vrednost polja je uporabljena v povezavi s projektom za odpravljanje sklica podrobnosti pogodbe v zapisu dejanskih ali ocenjenih podrobnosti. |
| **Pogodbeni znesek** | V podrobnostih pogodbe za fiksno ceno je to dogovorjena vrednost, ki bo zaračunana stranki za vse komponente dela, povezane s temi podrobnostmi pogodbe. V podrobnostih pogodbe za čas in material je ta znesek ocenjena vrednost, kaj bo zaračunano stranki za vse komponente dela, povezane s temi podrobnostmi pogodbe. V projektni pogodbi, ki je ustvarjena iz ponudbe, je ta vrednost kopirana iz pripadajočega polja podrobnosti ponudbe. Ko imajo podrobnosti pogodbe, ki temeljijo na projektu, podrobnosti vrstice, je to polje zaklenjeno za urejanje in je povzeto z zneska v podrobnostih vrstice pogodbe. | Ko imajo podrobnosti pogodbe podrobnosti vrstice, je mogoče to vrednost spremeniti s spremembo zneskov v podrobnostih vrstice. V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje zneska pred davkom v rednih mejnikih obračunavanja. |
| **Predvideni davek** | Uporabnik lahko uredi to polje za vnos ocenjenega zneska davka v podrobnosti pogodbe. Ko imajo podrobnosti pogodbe, ki temeljijo na projektu, podrobnosti vrstice, je to polje zaklenjeno za urejanje in je povzeto z zneska davka v podrobnostih vrstice pogodbe. | Ko imajo podrobnosti pogodbe podrobnosti vrstice, je mogoče to vrednost spremeniti s spremembo zneskov davka v podrobnostih vrstice. V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje davka v rednih mejnikih obračunavanja. |
| **Pogodbeni znesek po obdavčitvi** | Znesek podrobnosti pogodbe po obdavčitvi. To polje je samo za branje in je izračunano kot **Pogodbeni znesek + davek**. | V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje rednih mejnikov obračunavanja. |
| **Omejitev »Ni dovoljeno preseči«** | Uporabnik lahko to polje ureja ter je na voljo samo za podrobnosti pogodbe, ki temeljijo na projektu, ki imajo način obračunavanja časa in materiala. | Uporabnik lahko ureja to polje. Ko se dejanska vrednost časa ali stroška sklicuje na te podrobnosti pogodbe za čas in material, je znesek dejanske vrednosti ocenjen glede na omejitev, ki je ni dovoljeno preseči, za te podrobnosti pogodbe po računovodstvu za že porabljenega in potrjenega zneska. |
| **Proračun stranke** | To polje je mogoče urejati in je kopirano iz pripadajočega polja za podrobnosti ponudbe, če je bila pogodba ustvarjena iz ponudbe. | To polje se uporablja samo za informacije in nima pomena v poteku navzdol. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Veljavnostna pravila za možnosti na zavihku »Splošno« podrobnosti pogodbe, ki temelji na projektu

Pravilo: projekt in določen razred transakcije je lahko vključen samo v enem sklopu podrobnosti pogodbe, ki temeljijo na projektu, v pogodbi.

| Pogodba | Podrobnosti pogodbe | Project | Vključi čas | Vključi strošek | Vključi dajatev | Veljavno/neveljavno | Razlog                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | O1      | Da          | Da             | Da         | Neveljavno       | Krši pravilo. Čas, strošek in dajatve za projekt P1 so vključene v obeh sklopih podrobnosti pogodbe, CL1 in CL2.                                                                                       |
| C1       | CL2           | O1      | Da          | Da             | Da         | Neveljavno       | Krši pravilo. Čas, strošek in dajatve za projekt P1 so vključene v obeh sklopih podrobnosti pogodbe, CL1 in CL2.                                                                                       |
| C1       | CL1           | O1      | Da          | No              | Da         | Neveljavno       | Krši pravilo. Čas in dajatve za projekt P1 so vključene v obeh sklopih podrobnosti pogodbe, CL1 in CL2.                                                                                                   |
| C1       | CL2           | O1      | Da          | Da             | Da         | Neveljavno       | Krši pravilo. Čas in dajatve za projekt P1 so vključene v obeh sklopih podrobnosti pogodbe, CL1 in CL2.                                                                                                   |
| C1       | CL1           | O1      | Da          | No              | Da         | Veljavno           | Čas in dajatve za projekt P1 so vključeni v CL1. Stroški za projekt P1 so vključeni v CL2. </br>   Ni prekrivanja v tem, kar je vključeno v vsak sklop podrobnosti pogodbe, zato je veljavno.  |
| C1       | CL2           | O1      | No           | Da             | No          | Veljavno           | Čas in dajatve za projekt P1 so vključeni v CL1. Stroški za projekt P1 so vključeni v CL2. </br>   Ni prekrivanja v tem, kar je vključeno v vsak sklop podrobnosti pogodbe, zato je veljavno.  |
| C1       | CL1           | O1      | Da          | Da             | Da         | Neveljavno       | Krši pravilo. Čas, strošek in dajatve za projekt P1 so vključene v podrobnostih dveh pogodb.                                                                                               |
| CL2      | CL2           | O1      | Da          | Da             | Da         | Neveljavno       | Krši pravilo. Čas, strošek in dajatve za projekt P1 so vključene v podrobnostih dveh pogodb.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]