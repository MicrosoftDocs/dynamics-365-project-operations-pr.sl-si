---
title: Zaposlovanje pogodbenih delavcev in podizvajalskih zmogljivosti pri projektu
description: Ta članek pojasnjuje, kako je mogoče projektne zahteve izpolniti s pogodbenimi delavci ali podizvajalskimi zmogljivostmi v Microsoftu Dynamics 365 Project Operations.
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

Člani generične projektne skupine so lahko zaposleni z zaposlenimi ali pogodbenimi delavci. Pri zaposlovanju projekta s pogodbenimi delavci lahko svoje možnosti zaposlovanja omejite na določene pogodbene delavce, ki so dodeljeni vrsti podizvajalcev. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Poiščite zahteve glede kadrovskih virov s pogodbenimi delavci, ki spadajo v določeno linijo podizvajalcev

Če želite poiskati in zahtevati kadrovske vire s pogodbenimi delavci, ki spadajo v določeno linijo podizvajalcev, sledite tem korakom:

1. Ustvarite generičnega člana projektne skupine, ki se sklicuje na podizvajalsko pogodbo in vrstico podizvajalske pogodbe.
2. Ustvarite zahtevo po sredstvih za tega generičnega člana projektne skupine z uporabo **Ustvari zahtevo** gumb na podmreži članov projektne skupine.
3. Izberite vrstico s člani ekipe in nato izberite **Knjiga** gumb na podmreži. 
4. S tem se odpre tabla razporeda s kontekstom zahteve. Skupaj z drugimi atributi, kot so datumi, vloge in polja organizacijske enote, se filtri tabele razporedov samodejno zapolnijo tudi s polji dobavitelja, podizvajalca in podizvajalske vrstice iz zahteve po sredstvih.
5. Sistem išče vire, ki ustrezajo kriterijem filtra, in jih izpiše. 
6. Izberite enega od filtriranih virov in rezervirajte vir za zahtevo. 
7. Član projektne skupine je ustvarjen in posodobljen s podizvajalci in referencami podizvajalcev. Pojdi do **Ocene projekta** in izberite **Posodobite cene** da vidite posodobljene stroške dodelitve vira. 

> [!NOTE]
> Posodabljanje člana projektne skupine s podizvajalsko pogodbo in referenco podizvajalske vrstice morda ne bo vedno mogoče med rezervacijo, če je vir dodeljen več podizvajalskim vrsticam. Če sistem ne more posodobiti člana projektne skupine s podizvajalsko pogodbo in podizvajalsko vrstico, odprite zapis člana projektne skupine in ročno posodobite ta polja, tako da bo ocena finančnih stroškov natančno odražala stroške podizvajalca.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Poiščite zahteve glede kadrovskih virov pri katerem koli pogodbenem delavcu

Če želite poiskati in zahtevati kadrovske vire s katerim koli pogodbenim delavcem, sledite tem korakom:

1. Ustvarite generičnega člana projektne skupine.
2. Ustvarite zahtevo po sredstvih za tega generičnega člana projektne skupine z uporabo **Ustvari zahtevo** gumb na podmreži članov projektne skupine.
3. Izberite vrstico s člani ekipe in nato izberite **Knjiga** gumb na podmreži. 
4. S tem se odpre tabla razporeda s kontekstom zahteve. Skupaj z drugimi atributi, kot so datumi, vloge in polja organizacijske enote, se filtri tabele razporedov samodejno zapolnijo tudi s polji dobavitelja, podizvajalca in podizvajalske vrstice iz zahteve po sredstvih. Ker zahteva ni imela izpolnjenih vrednosti podizvajalske pogodbe ali vrstice podizvajalske pogodbe, bodo ti atributi v podoknu filtra prazni.
5. Sistem išče vire, ki ustrezajo kriterijem filtra, in jih izpiše.
6. Posodobite **Delavski tip** polje v podoknu filtra za **Pogodbeni delavec** omejiti iskanje na pogodbene delavce. Nadgradnja **Prodajalec** v podoknu s filtri, da izberete prodajalca, da omejite iskanje na prikaz samo pogodbenih delavcev, ki pripadajo določenemu podjetju prodajalca.
7. S seznama izberite pogodbenega delavca in rezervirajte vir za zahtevo.
8. Ustvari se član projektne skupine. Vendar član projektne skupine ni posodobljen z nobeno podizvajalsko pogodbo ali vrstico podizvajalske pogodbe, zato dodelitev virov ne bo ovrednotena z uporabo cen podizvajalske pogodbe. Ročno posodobite člana projektne skupine s podizvajalsko vrstico in pojdite na **Ocene projekta** in izberite **Posodobite cene** da vidite posodobljene stroške dodelitve vira.

> [!NOTE]
> Člani projektne skupine, ki imajo **Delavski tip** kot **Pogodbeni delavec** vendar nimajo reference podizvajalca, so označeni kot **Neveljavno** na **Člani projektne skupine** mreža. Če obstajajo člani projektne skupine s tem statusom, odprite zapis člana projektne skupine in ročno posodobite polja podizvajalske pogodbe in vrstice podizvajalske pogodbe, tako da bo ocena finančnih stroškov natančno odražala stroške podizvajalca na **Ocene** zavihek. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
