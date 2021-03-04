---
title: Vrstice ponudb, ki temeljijo na izdelkih
description: V tej temi so na voljo informacije o vrsticah ponudb, ki temeljijo na izdelkih.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151273"
---
# <a name="product-based-quote-lines"></a>Vrstice ponudb, ki temeljijo na izdelkih

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


V aplikaciji Dynamics 365 Project Service Automation lahko ustvarite vrstice ponudb, ki temeljijo na izdelku. Vrstice ponudb, ki temeljijo na izdelkih, so lahko vrstice izdelkov, ki niso v katalogu, ali pa artikli iz kataloga izdelkov.

## <a name="product-catalog"></a>Katalog izdelkov

Izdelki v katalogu izdelkov Dynamics 365 imajo privzeto enoto in skupino enot. Če ima več izdelkov enak nabor atributov, lahko ustvarite družino izdelkov, ki ima prav tako te atribute. Vsi izdelki v eni družini izdelkov podedujejo isti nabor atributov.

Podjetje na primer prodaja naročniške licence za različno programsko opremo. Vsa naročniška programska oprema ima ta dva atributa:

- Število uporabnikov 
- Trajanje naročnine (v mesecih)

Takšno vrsto kataloga najlažje upravljate tako, da ustvarite družino izdelkov, ki se imenuje **Naročniška programska oprema** in ima atributa **Število uporabnikov** in **Trajanje naročnine**. Nato lahko dodate posamezne izdelke, na primer **Dynamics 365 Sales** ali **Dynamics 365 Field Service** v družino izdelkov **Naročniška programska oprema**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Dodajanje elementov kataloga izdelkov v projektno ponudbo

Strani projektne ponudbe in projektne pogodbe imajo razdelke za dve vrsti vrstic: vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih. Pri vrsticah, ki temeljijo na izdelku, se Dynamics 365 uporablja za dodajanje elementov iz kataloga izdelkov v ponudbo. Spustni seznam v vrstici ponudbe ali vrstici projekte pogodbe vključuje vse izdelke in enote na ceniku izdelkov, ki je priložen ponudbi ali projektni pogodbi. Dodajate lahko tudi izdelke, ki niso del cenika izdelkov v ponudbi.

Poleg tega lahko izberete izdelke iz drugih cenikov ali pa neposredno iz kataloga izdelkov. Ko izberete izdelke neposredno iz kataloga izdelkov, se za prikaz prodajne cene izdelka uporabi privzeti cenik tega izdelka. Če privzeti cenovni seznam ni nastavljen, je cena nastavljena na 0 (nič).

Če vrstica ponudbe temelji na katalogu izdelkov, lahko prodajno ceno preglasite neposredno v vrstici ponudbe. Upoštevajte, da ima vrstica ponudbe v programu Dynamics 365 polje **Oblikovanje cen**. Na voljo sta dve vrednosti:

- Preglasi oblikovanje cene  
- Uporabi privzeto

Če nastavite to polje na **Preglasi oblikovanje cene**, Dynamics 365 ne nastavi privzete cene. Ceno za izdelek morate vnesti v vrstici ponudbe. Če nastavite to polje na **Uporabi privzeto**, Dynamics 365 uporabi privzeto prodajno ceno in zaklene polje, da prepreči urejanje.

Ko namestite PSA, se privzete prodajne cene vnesejo v vrstice v ponudbi, ki temeljijo na izdelkih. Polje **Oblikovanje cen** je nato nastavljeno na **Preglasi oblikovanje cene**, tako da lahko uredite privzeto ceno v vrsticah ponudbe.

> ![Nastavitev preglasitve oblikovanja cen](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Količniki za količino za izdelke

PSA uporablja količnike za količino, ki podpirajo prodajo naročniških izdelkov. Pri naročniških izdelkih je količina v vrstici ponudbe ali projektne pogodbe izražena kot število mesecev uporabe.

Običajno je cena naročniške programske opreme shranjena v katalogu kot cena na uporabnika na mesec. Vendar pa lahko namesto tega uporabite druge opise časa. Med prodajnim postopkom je cena v vrstici ponudbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent za IT. Vsak posel ima različno število uporabnikov in različno število naročniških mesecev. Količina, ki se uporablja za izračun zneska vrstice ponudbe, je produkt števila uporabnikov in števila mesecev naročnine.

Za podporo tej vrsti prodaje je PSA uvedla koncept količnikov za količino. Količniki za količino temeljijo na atributih izdelka v aplikaciji Dynamics 365. Ko konfigurirate določene lastnosti za izdelek, vam PSA omogoči označevanje podmnožice teh lastnosti ali vseh lastnosti kot količnikov za količino.

PSA preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom. Ko je izdelek, za katerega so konfigurirani količniki za količino, dodan v vrstico ponudbe, polje **Količina** v vrstici ponudbe postane polje samo za branje. Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, PSA izračuna količino vrstice ponudbe.

Dynamics 365 ima lahko na primer te lastnosti: 

- **Št. uporabnikov** – število uporabnikov. 
- **Št. mesecev** – število mesecev naročnine.
- **Inventarna številka izdelka** 

Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov. 

> ![Označevanje lastnosti »Št. uporabnikov« in »Št. mesecev« kot količnikov za količino](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]