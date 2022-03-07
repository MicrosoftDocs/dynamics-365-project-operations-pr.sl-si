---
title: Novosti v marcu 2021 – Project Operations za primere uporabe z viri/brez zalog
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v marčevski izdaji (2021) aplikacije Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006356"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v marcu 2021 – Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

- Project Operations v okolju Dataverse različice 4.8.0.91 
- Upravljanje projektov in računovodstvo v okolju Dynamics 365 Finance, različica 10.0.16 

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse


| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in cene | 2133873 | Popravljen je prikaz simbola valute za **prodajno ceno na enoto** v mreži **ocen stroškov**. |
| Zaračunavanje in cene | 2174616 | Ko je ponudba pridobljena, je v podrobnostih pogodbe, ki se kopirajo iz ponudbe, sklic na pogodbi prilagojen cenik. |
| Upravljanje priložnosti | 2167475 | Popravljen je znesek davka na popravljenem računu, iz katerega izvira neobračunan dejanski vnos. |
| Upravljanje priložnosti | 2176285 | Zneska davka ni dovoljeno kopirati iz podrobnosti prodajne pogodbe/ponudbe v stroškovne podrobnosti  pogodbe/ponudbe. |
| Upravljanje priložnosti | 2188079 | Pravilo za izstavitev deljenega računa ne sme biti ustvarjeno za pogodbe, ki ne temeljijo na delu. |
| Načrtovanje in sledenje | 2125274 | Atribut **Projekt Dual Write Map** za **preslikavo datuma začetka projekta** je posodobljen iz **msdyn\_taskearlieststart** na **msdyn\_actualstart**. |
| Načrtovanje in sledenje | 2138853 | Funkcija kopiranja projekta je posodobljena za zagotavljanje kopiranja vrstic za oceno stroškov, ki se sklicujejo na opravila, v ciljni projekt. |
| Načrtovanje in sledenje | 2154306 | Odpravljene težave z brisanjem ocen stroškov v aplikaciji Project Operations za scenarije, ki temeljijo na virih. |
| Načrtovanje in sledenje | 2173259 | Funkcija kopiranja projekta je posodobljena, da se v nekaterih primerih ne prikaže sporočilo o napaki **kopiranja WBS**. |
| Čas in strošek | 2148910 | V mreži **časovnih vnosov** je odpravljena težava s stranjo za **urejanje vnosov**. |
| Čas in strošek | 2159798 | Poostren je nadzor za preprečevanje urejanja odobrenih vnosov stroškov. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Pregled upravljanja projektov in računovodstva v storitvi Dynamics 365 Finance

Za več informacij glejte [Novosti v januarju 2021 – Project Operations za primere uporabe z viri/brez zalog](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije Finance and Operations glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Drug način za informiranje o regulativnih posodobitvah je vpis v LCS in ogled načrtovanih regulativnih posodobitev z orodjem za iskanje težav. Iskanje težav omogoča iskanje po državi, vrsti funkcije in izdaji.


[!INCLUDE[footer-include](../includes/footer-banner.md)]