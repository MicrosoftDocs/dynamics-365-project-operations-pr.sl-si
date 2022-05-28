---
title: Varnostni model
description: Ta tema vsebuje informacije o varnostnem modelu v aplikaciji Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 8ba220097589655381ac1da5d4d926605c3ae672
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585766"
---
# <a name="security-model"></a>Varnostni model

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_



Microsoft Dynamics 365 Project Operations vsebuje edinstven varnostni model, ki omogoča delovanje poslovnega varnostnega modela, ki sodeluje s skupinami v Microsoft Office. 


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

| Vloga           | Opis                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Uporabnik projekta   | Sodelujoči uporabnik projekta, ki lahko ustvari lastne projekte in si ogleda vse projekte, ki so v skupni rabi z njimi. | Uporabnik   |
| Sistem projekta | Vloga, uporabljena za kontekst aplikacije. Stranke ne bi smele uporabljati te sistemske vloge.                                    | Globalno |

## <a name="security-enforcement"></a>Izvajanje varnosti
Dejanja, ki se izvajajo na ravni projekta, se izvajajo v kontekstu prijavljenega uporabnika. To pomeni, da mora uporabnik za ustvarjanje, odpiranje ali brisanje projekta imeti na voljo dostop do CDS. Dostop do CDS je mogoče odobriti prek katerega koli razpoložljivega mehanizma v platformi. Uporabnik z večjim obsegom lahko na primer dostopa do projekta, če je bilo izvedeno izrecno dejanje za skupno rabo projekta, ki uporabniku omogoča dostop.

Pomembno je, da se to upošteva pri ustvarjanju projektov v Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Sodelovanje sodobnih skupin s Project Operations
Project for the Web in Project Operations podpirata sodobne skupine za sodelovanje. Uporabniki, ki so dodani v projekt prek skupine, lahko urejajo projektni načrt.

Project for the Web samodejno doda uporabnike v skupino po njihovi dodelitvi.

Skupine omogočajo skupno uporabo dovoljenj za projekt in podporne artefakte. Naslednji diagram prikazuje dogodke in spremembe stanja, do katerih pride med postopkom dodelitve skupine.

Project Operations ne ustvari skupine z implicitnim dejanjem, ampak samo z dejanskim pritiskom na Skupine.

Iskanje članov skupine v pogovornem oknu **Upravljanje skupine** je omejeno na tiste, ki so nastavljeni kot del varnostne skupine okolja. Za več informacij glejte [Nadzor uporabniškega dostopa do okolij: varnostne skupine in licence](/power-platform/admin/control-user-access).

![Način skupine.](./media/groupsmode.png)

1. Projekt je plod in last uporabnika, ki ga je ustvaril.
2. Lastnik projekta je posodobljen v skladu z ekipo.
3. Ekipa lastnika se preslika v navedeno ali ustvarjeno Skupino Office.
4. Prvotni lastnik projekta je dodan v Skupino Office.

## <a name="deployment-recommendation"></a>Priporočilo za uvajanje
Z razvojem modela za sodelovanje v skupini Office bo dodana funkcionalnost, ki bo sčasoma zagotavljala podrobnejši nadzor. Stranke, ki danes uvajajo storitev Project Operations, spodbujamo, da se osredotočijo na tradicionalni varnostni model Microsoft Dynamics 365.

Za več informacij glejte [Varnost v Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Projektno delovanje in Microsoft Dynamics 365 Finančna varnost
Storitev Project Operations vključuje naslednje vloge:

- Vodja projektov
- Projektni računovodja

Za več informacij o varnosti v storitvi Finance glejte [Varnost na podlagi vlog](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]