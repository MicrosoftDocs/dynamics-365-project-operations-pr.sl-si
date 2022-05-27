---
title: Zaposlovanje pogodbenih delavcev in podizvajalskih zmogljivosti pri projektu
description: Ta tema pojasnjuje, kako je mogoče zapolniti zahteve projekta s pogodbenimi delavci ali podizvajalci v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574662"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Zaposlovanje pogodbenih delavcev in podizvajalskih zmogljivosti pri projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Generični člani projektne skupine so lahko zaposleni z zaposlenimi ali pogodbenimi delavci. Ko zaposlujete projekt s pogodbenimi delavci, lahko omejite svoje kadrovske možnosti na določene pogodbene delavce, ki so dodeljeni podizvajalski vrstici. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Poiščite potrebe po kadrovskih virih s pogodbenimi delavci, ki spadajo v določeno podizvajalsko linijo

Za iskanje in potrebe po kadrovskih virih pri pogodbenih delavcih, ki pripadajo določeni vrsti podizvajalcev, sledite tem korakom:

1. Ustvarite generičnega člana projektne skupine, ki se sklicuje na vrstico podizvajalcev in podizvajalcev.
2. Ustvarite zahtevo po virih za tega generičnega člana projektne skupine z uporabo **Ustvarite zahtevo** gumb na podmreži članov projektne skupine.
3. Izberite vrstico za člane ekipe in nato izberite **knjiga** gumb na podmreži. 
4. To odpre tablo razporeda s kontekstom zahtev. Poleg drugih atributov, kot so polja datumov, vloge in organizacijske enote, se filtri plošče razporeda samodejno izpolnijo tudi s polji vrstice dobavitelj, podizvajalec in podizvajalec iz zahteve po virih.
5. Sistem poišče vire, ki ustrezajo kriterijem filtra, in jih navede. 
6. Izberite enega od filtriranih virov in rezervirajte vir za zahtevo. 
7. Član projektne skupine je ustvarjen in posodobljen s referencami podizvajalskih in podizvajalskih vrstic. Pojdi do **Ocene projekta** in izberite **Posodobite cene** da si ogledate posodobljene stroške dodelitve vira. 

> [!NOTE]
> Posodobitev člana projektne skupine s podizvajalcem in referenco vrstice podizvajalcev morda ni vedno mogoča med rezervacijo, če je vir dodeljen več podizvajalskim vrsticam. Če sistem ne more posodobiti člana projektne skupine z vrstico podizvajalcev in podizvajalcev, odprite zapis članov projektne skupine in ročno posodobite ta polja, tako da ocena finančnih stroškov natančno odraža stroške podizvajalca.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Poiščite in poiščite potrebe po kadrovskih virih s katerim koli pogodbenim delavcem

Če želite pri katerem koli pogodbenem delavcu poiskati zahteve po kadrovskih virih, sledite tem korakom:

1. Ustvarite generičnega člana projektne skupine.
2. Ustvarite zahtevo po virih za tega generičnega člana projektne skupine z uporabo **Ustvarite zahtevo** gumb na podmreži članov projektne skupine.
3. Izberite vrstico za člane ekipe in nato izberite **knjiga** gumb na podmreži. 
4. To odpre tablo razporeda s kontekstom zahtev. Poleg drugih atributov, kot so polja datumov, vloge in organizacijske enote, se filtri plošče razporeda samodejno izpolnijo tudi s polji vrstice dobavitelj, podizvajalec in podizvajalec iz zahteve po virih. Ker zahteva ni imela izpolnjenih vrednosti vrstice podizvajalcev ali podizvajalcev, bodo ti atributi v podoknu filtra prazni.
5. Sistem poišče vire, ki ustrezajo kriterijem filtra, in jih navede.
6. Posodobite **Vrsta delavca** polje na podoknu filtra do **Pogodbeni delavec** omejiti iskanje na pogodbene delavce. Nadgradnja **Prodajalec** v podoknu s filtrom, da izberete prodajalca, da omejite iskanje na prikaz samo pogodbenih delavcev, ki pripadajo določenemu podjetju prodajalca.
7. S seznama izberite pogodbenega delavca in rezervirajte vir za zahtevo.
8. Ustvarjen je član projektne skupine. Vendar pa član projektne skupine ni posodobljen z nobeno vrstico podizvajalcev ali podizvajalcev, zato se dodelitev sredstev ne bo stala z uporabo podizvajalskih cen. Ročno posodobite člana projektne skupine s podizvajalsko vrstico in pojdite na **Ocene projekta** in izberite **Posodobite cene** da si ogledate posodobljene stroške dodelitve vira.

> [!NOTE]
> Člani projektne skupine, ki imajo **Vrsta delavca** kot **Pogodbeni delavec** vendar nimajo reference podizvajalca, so označene kot **Neveljavno** na **Člani projektne ekipe** mreža. Če obstajajo člani projektne skupine s tem statusom, odprite zapis članov projektne skupine in ročno posodobite polja vrstice podizvajalcev in podizvajalcev, tako da ocena finančnih stroškov natančno odraža stroške podizvajalca na **Ocene** zavihek. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
