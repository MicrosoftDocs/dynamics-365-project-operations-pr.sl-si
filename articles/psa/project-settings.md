---
title: Nastavitve projekta
description: Ta tema vsebuje informacije o nastavitvah upravljanja projektov.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 075cbdd30c4986e514e4d357a08ef99cf3eb101f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601314"
---
# <a name="project-settings"></a>Nastavitve projekta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Za dostop do funkcij za načrtovanje projekta uporabite spodnje nastavitve.

## <a name="work-template"></a>Predloga za delo

Če želite ustvariti razpored projekta, ustvarite predlogo koledarja za projekt, ki določa število delovnih ur na dan in vse dneve, ko je podjetje zaprto. Če želite ustvariti predlogo koledarja za projekt, povežite delovno predlogo s poljem **Predloga koledarja** za projekt. Za ustvarjanje delovne predloge sledite spodnjim korakom.

1. V PSA v podoknu za krmarjenje na levi kliknite **Viri**. 
2. Na strani seznama **Viri** odprite zapis uporabnika in nato izberite **Prikaži delovne ure**.

  > [!NOTE]
  > Preverite, ali dovolite pojavna okna na strani brskalnika. Tako lahko vidite delovne ure, nastavljene za vir.
  
3. Na zavihku **Mesečni pogled** kliknite **Nastavi**. Prikaže se seznam treh možnosti: 

  - Nov tedenski urnik
  - Urnik dela za en dan
  - Prosti čas

> ![Nastavitev možnosti.](media/project-13.png)

4. Izberite **Nov tedenski urnik** in nato nastavite možnosti za ta razpored virov. Nastavite lahko ponavljajoči se tedenski razpored, dnevne in urne parametre, čas, ko je podjetje zaprto, in še več.
5. Nastavite datumski obseg, izberite **Shrani** in nato kliknite **Zapri**. 
6. Vrnite se na stran seznama **Viri** in izberite vir, za katerega ste nastavili delovne ure. 
7. Izberite **Nastavi koledar kot**, da nastavite delovno predlogo. 
8. V pogovornem oknu **Delovna predloga** vnesite ime delovne predloge in izberite **Uporabi**. 

Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.

## <a name="resource-roles"></a>Vloge virov

Izraz *vloga vira* se nanaša na nabor znanja, sposobnosti in potrdil, ki jih mora imeti oseba, da lahko izvaja določeno skupino opravil v okviru projekta. PSA vam omogoča zaračunati in obračunati čas vira na podlagi vloge, s katero je vir povezan. Vsaka organizacija mora nastaviti te vloge v podoknu za krmarjenje na levi strani menija **Project Service**.

Vsaka organizacija mora nastaviti te vloge na strani **Kategorije dejavnih virov**. Če želite odpreti to stran, v podoknu za krmarjenje na levi izberite **Vloge virov**.

## <a name="price-lists"></a>Ceniki

S ceniki lahko nastavite lastne in prodajne cene za vloge virov, kategorije stroškov, izdelke in druge elemente v organizaciji. Preden nastavite finančne ocene za delo, ki mora biti opravljeno pri projektu, ustvarite osnovni cenik z lastnimi in prodajnimi cenami. V razdelku s parametri nastavite tudi privzeti cenik z lastnimi in prodajnimi cenami, ki velja za vse projekte, ustvarjene v organizaciji. Na strani **Dejavni projektni parametri** preverite, ali ste nastavili privzeti cenik z lastnimi in prodajnimi cenami.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
