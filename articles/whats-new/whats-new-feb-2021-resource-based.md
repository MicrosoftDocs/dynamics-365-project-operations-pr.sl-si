---
title: Novosti v februarju 2021 – Project Operations za primere uporabe z viri/brez zalog
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v februarski izdaji (2021) aplikacije Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029642"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v februarju 2021 – Project Operations za primere uporabe z viri/brez zalog

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

- Project Operations v okolju Dataverse 4.7.0.95
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.16 

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

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektov in računovodstvo v okoljih aplikacij Dynamics 365 Finance 

Za več informacij o upravljanju projektov in računovodstva v storitvi Dynamics 365 Finance, glejte [Novosti v januarju 2021 – Project Operations za primere uporabe z viri/brez zalog](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regulativne posodobitve

Za informacije o regulativnih posodobitvah za aplikacije za finance in postopke glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Drug način za informiranje o regulativnih posodobitvah je vpis v Lifecycle Services (LCS) in ogled načrtovanih regulativnih posodobitev z orodjem za iskanje težav. Iskanje težav omogoča iskanje po državi, vrsti funkcije in izdaji.


[!INCLUDE[footer-include](../includes/footer-banner.md)]