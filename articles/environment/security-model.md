---
title: Varnostni model
description: Ta tema vsebuje informacije o varnostnem modelu v storitvi Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896751"
---
# <a name="security-model"></a>Varnostni model

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Microsoft Dynamics 365 Project Operations vsebuje edinstven varnostni model, ki zagotavlja poslovni varnostni model na podlagi vlog in sodeluje s storitvijo Microsoft Office Skupine. 


## <a name="security-roles"></a>Varnostne vloge
Prednostne zmogljivosti Project Operations vključujejo naslednje vloge:

| Vloga                          | Opis                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Upravitelj prakse              | Podpira poročanje med projekti.                                                                                                            | Poslovna enota              |
| Odobritelj projekta              | Odobri čas in stroške projekta.                                                                                                                              | Poslovna enota |
| Skrbnik plačevanja pri projektu | Ustvari predlog računa.                                                                                                                                                 | Poslovna enota |
| Vodja projektov               | Ustvari projektni načrt in pošlje zahteve za vire.                                                                                                                              | Poslovna enota |
| Projektni vir              | Člani ekipe, ki jih je mogoče rezervirati, in čas poročanja.                                                                                                          | Poslovna enota|
| Upravitelj virov              | Vse funkcije za upravljanje virov, kot je izpolnjevanje zahtev za vire in rezervacije, so ločene v podporo hibridne konfiguracije za vodjo projektov + upravitelja virov in enotne, centralizirane vloge upravitelja virov. | Poslovna enota |


Microsoft Project za splet vključuje naslednje vloge:
| Vloga                          | Opis                                                                                                          | Scope |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Uporabnik projekta | Sodelujoči uporabnik projekta, ki lahko ustvari lastne projekte in si ogleda vse projekte, ki so v skupni rabi z njimi.| Uporabnik|
| Sistem projekta | Vloga, uporabljena za kontekst aplikacije. Stranke ne bi smele uporabljati te sistemske vloge. | Globalno|

## <a name="security-enforcement"></a>Izvajanje varnosti
Dejanja, ki se izvajajo na ravni projekta, se izvajajo v kontekstu prijavljenega uporabnika. To pomeni, da mora uporabnik za ustvarjanje, odpiranje ali brisanje projekta imeti na voljo dostop do CDS. Dostop do CDS je mogoče odobriti prek katerega koli razpoložljivega mehanizma v platformi. Uporabnik z večjim obsegom lahko na primer dostopa do projekta, če je bilo izvedeno izrecno dejanje za skupno rabo projekta, ki uporabniku omogoča dostop.

Pomembno je, da se to upošteva pri ustvarjanju projektov v Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Sodelovanje sodobnih skupin s Project Operations
Project for the Web in Project Operations podpirata sodobne skupine za sodelovanje. Uporabniki, ki so dodani v projekt prek skupine, lahko urejajo projektni načrt.

Project for the Web samodejno doda uporabnike v skupino po njihovi dodelitvi.

Skupine omogočajo skupno uporabo dovoljenj za projekt in podporne artefakte. Naslednji diagram prikazuje dogodke in spremembe stanja, do katerih pride med postopkom dodelitve skupine.

Project Operations ne ustvari skupine z implicitnim dejanjem, ampak samo z dejanskim pritiskom na Skupine.

Iskanje članov skupine v pogovornem oknu **Upravljanje skupine** je omejeno na tiste, ki so nastavljeni kot del varnostne skupine okolja. Za več informacij glejte [Nadzor uporabniškega dostopa do okolij: varnostne skupine in licence](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. Projekt je plod in last uporabnika, ki ga je ustvaril.
2. Lastnik projekta je posodobljen v skladu z ekipo.
3. Ekipa lastnika se preslika v navedeno ali ustvarjeno Skupino Office.
4. Prvotni lastnik projekta je dodan v Skupino Office.

## <a name="deployment-recommendation"></a>Priporočilo za uvajanje
Z razvojem modela za sodelovanje v skupini Office bo dodana funkcionalnost, ki bo sčasoma zagotavljala podrobnejši nadzor. Stranke, ki danes uvajajo storitev Project Operations, spodbujamo, da se osredotočijo na tradicionalni varnostni model Microsoft Dynamics 365.

Za več informacij glejte [Varnost v Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Varnost v storitvah Project Operations in Microsoft Dynamics 365 Finance
Storitev Project Operations vključuje naslednje vloge:

- Vodja projektov
- Projektni računovodja

Za več informacij o varnosti v storitvi Finance glejte [Varnost na podlagi vlog](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


