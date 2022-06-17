---
title: Novosti v februarju 2021 – Project Operations za primere uporabe z viri/brez zalog
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations februarja 2021 za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 38fede1746bcb09700c9c9c5e20653e0c39fea2a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910664"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v februarju 2021 – Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje Dynamics 365 Project Operations komponente in različice:

- Project Operations v okolju Dataverse 4.7.0.95
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.16 

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| **Zaračunavanje in oblikovanje cen** | 2053736 | Podrobnosti vrstice računa so zdaj dostopne prek možnosti **Račun** > **Sorodne informacije**. |
| **Zaračunavanje in oblikovanje cen** | 2122613 | Dejanji **Aktiviranje** in **Deaktiviranje** sta bili odstranjeni iz entitet povezav **Cenik**. |
| **Zaračunavanje in oblikovanje cen** | 2128606 | Odpravljena težava z možnostjo **ullReferenceException** v vtičniku **GetEstimatesForProject**. |
| **Uvajanje in konfiguracija** | 2139346 | Odpravljena težava z uvozom neupravljane rešitve **Dynamics365ProjectOperationsDualWrite**. |
| **Uvajanje in konfiguracija** | 2140569 | V okoljih ekip mora Dataverse ne sme biti nameščena projektna rešitev. |
| **Uvajanje in konfiguracija** | 2086991 | Omejena lokalizacija prilagajanja spletnih virov. |
| **Upravljanje priložnosti** | 2136794 | Prikaz pravilnega sporočila o napaki, ko ne uspe postopek **Potrdi račun** ali **Označi račun kot plačan**. |
| **Upravljanje priložnosti** | 2139330 | Zamenjava projektnega vodje na projektu ne sme ponastaviti lastniško podjetje nazaj na privzeto vrednost. |
| **Upravljanje priložnosti** | 2146376 | Popravljeni znesek davka v dejanskem delu, ki se ne zaračuna, je ustvarjen iz potrditve računa. |
| **Načrtovanje in sledenje projektov** | 2099879 | Uvajanje okolja Dataverse mora ustvariti privzeto kategorijo transakcije s statičnim ID-jem in ne naključno ustvariti ene na okolje. |
| **Načrtovanje in sledenje projektov** | 2128577 | Popravljene uporabniške pravice za Project Service, da se posodobi kategorija transakcije na dodelitvi vira. |
| **Načrtovanje in sledenje projektov** | 2164035 | Odpravljene težave s funkcijo **Kopiraj projekt**. |
| **Časovni vnos** | 2129161 | Uveljavljene so strožje omejitve, da se zagotovi, da uporabniki ne morejo spreminjati in posodabljati časovnega vnosa, ki je bil predložen ali odobren. |
| **Časovni vnos** | 2103572 | Odobritev časa za neprojektne časovne vnose ne sme iskati vloge odobritelja projekta. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vodenje projektov in računovodstvo v Dynamics 365 Finance 

Za več informacij o vodenju in računovodstvu projektov v Dynamics 365 Finance glejte [Kaj je novega januar 2021 – Projektne operacije za scenarije, ki temeljijo na virih/brez zalog](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije Finance in Operations glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Drug način za informiranje o regulativnih posodobitvah je vpis v Lifecycle Services (LCS) in ogled načrtovanih regulativnih posodobitev z orodjem za iskanje težav. Iskanje težav omogoča iskanje po državi, vrsti funkcije in izdaji.


[!INCLUDE[footer-include](../includes/footer-banner.md)]