---
title: Zaposlovanje pogodbenih delavcev in podizvajalskih zmogljivosti pri projektu
description: V tem članku je pojasnjeno, kako je mogoče projektne zahteve izpolniti s pogodbenimi delavci ali podizvajalci v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522456"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Zaposlovanje pogodbenih delavcev in podizvajalskih zmogljivosti pri projektu

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Splošni člani projektne ekipe so lahko zapolnjeni z zaposlenimi ali pogodbenimi delavci. Pri zaposlovanju pogodbenih delavcev za projekt lahko svoje možnosti zaposlovanja omejite na določene pogodbene delavce, ki so dodeljeni podrobnostim podizvajalske pogodbe. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Poiščite zahteve glede zaposlovanja s pogodbenimi delavci, ki spadajo v določene podrobnosti podizvajalske pogodbe

Če želite poiskati in zapolniti zahteve glede zaposlovanja s pogodbenimi delavci, ki spadajo v določene podrobnosti podizvajalske pogodbe, sledite naslednjim korakom:

1. Ustvarite splošnega člana projektne ekipe, ki se sklicuje na podizvajalsko pogodbo in podrobnosti podizvajalske pogodbe.
2. Ustvarite zahtevo vira za tega splošnega člana projektne ekipe tako, da uporabite gumb **Ustvarjanje zahteve** na podmreži članov projektne ekipe.
3. Izberite vrstico s člani ekipe in nato izberite gumb **Rezervacija** na podmreži. 
4. S tem se odpre tabela za načrtovanje s kontekstom zahteve. Filtri tabele za načrtovanje se skupaj z drugimi atributi, kot so datumi, vloge in polja organizacijske enote, samodejno zapolnijo tudi s polji dobavitelja, podizvajalca in podrobnostmi podizvajalske pogodbe iz zahteve za vir.
5. Sistem išče vire, ki ustrezajo kriterijem filtra, in jih navede. 
6. Izberite enega od filtriranih virov in rezervirajte vir za zahtevo. 
7. Član projektne ekipe je ustvarjen in posodobljen s podizvajalsko pogodbo in sklici podrobnosti podizvajalske pogodbe. Odprite **Ocene projekta** in izberite možnost **Posodobitev cene**, da si ogledate posodobljene stroške dodelitve vira. 

> [!NOTE]
> Posodabljanje člana projektne ekipe s podizvajalsko pogodbo in sklicem podrobnosti podizvajalske pogodbe morda ne bo vedno mogoče med rezervacijo, če je vir dodeljen več podrobnostim podizvajalske pogodbe. Če sistem ne more posodobiti člana projektne ekipa s podizvajalsko pogodbo in podrobnostmi podizvajalske pogodbe, odprite zapis člana projektne ekipe in ročno posodobite ta polja tako, da bo ocena finančnih stroškov natančno odražala stroške podizvajalca.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Iskanje in zapolnitev zahteve virov s katerim koli pogodbenim delavcem

Če želite poiskati in zapolniti zahteve virov s katerim koli pogodbenim delavcem, sledite naslednjim korakom:

1. Ustvarite splošnega člana projektne ekipe.
2. Ustvarite zahtevo vira za tega splošnega člana projektne ekipe tako, da uporabite gumb **Ustvarjanje zahteve** na podmreži članov projektne ekipe.
3. Izberite vrstico s člani ekipe in nato izberite gumb **Rezervacija** na podmreži. 
4. S tem se odpre tabela za načrtovanje s kontekstom zahteve. Filtri tabele za načrtovanje se skupaj z drugimi atributi, kot so datumi, vloge in polja organizacijske enote, samodejno zapolnijo tudi s polji dobavitelja, podizvajalca in podrobnostmi podizvajalske pogodbe iz zahteve za vir. Ker zahteva ni imela izpolnjenih vrednosti podizvajalske pogodbe ali podrobnosti podizvajalske pogodbe, bodo ti atributi v podoknu s filtri prazni.
5. Sistem išče vire, ki ustrezajo kriterijem filtra, in jih navede.
6. Posodobite polje **Vrsta delavca** v podoknu s filtri na **Pogodbeni delavec**, da omejite iskanje na pogodbene delavce. Posodobite polje **Dobavitelj** v podoknu s filtri, da izberete dobavitelja in omejite iskanje na prikaz samo pogodbenih delavcev, ki pripadajo določenemu podjetju dobavitelja.
7. S seznama izberite pogodbenega delavca in rezervirajte vir za zahtevo.
8. Splošni član projektne ekipe je ustvarjen. Vendar član projektne ekipe ni posodobljen z nobeno podizvajalsko pogodbo ali podrobnostmi podizvajalske pogodbe, zato dodelitev virov ne bo ovrednotena s cenami podizvajalske pogodbe. Ročno posodobite člana projektne ekipe s podrobnostmi podizvajalske pogodbe in odprite **Ocene projekta** ter izberite možnost **Posodobitev cene**, da si ogledate posodobljene stroške dodelitve vira.

> [!NOTE]
> Člani projektne ekipe, ki imajo možnost **Vrsta delavca** nastavljeno kot **Pogodbeni delavec**, vendar nimajo sklica na podizvajalsko pogodbo, so v mreži **Člani projektne ekipe** označeni kot **Neveljavno**. Če obstajajo člani projektne ekipe s tem stanjem, odprite zapis člana projektne ekipe in ročno posodobite polja podizvajalske pogodbe in podrobnosti podizvajalske pogodbe tako, da bo ocena finančnih stroškov natančno odražala stroške podizvajalca v zavihku **Ocene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
