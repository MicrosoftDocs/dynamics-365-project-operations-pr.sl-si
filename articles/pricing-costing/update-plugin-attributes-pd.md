---
title: Posodabljanje atributov vtičnikov z novimi cenovnimi razsežnostmi
description: Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274703"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Posodabljanje atributov vtičnikov z novimi cenovnimi razsežnostmi

Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.

> [!NOTE]
> Ta tema se uporablja samo za funkcije ponudbe in pogodbe v storitvi Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Zahteve
Preden dokončate korake v tej temi, morate izvesti postopke v naslednjih temah:

  - [Ustvarjanje polj in entitet po meri](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete ](add-custom-fields-price-setup-transactional-entities.md)
  - [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-custom-fields-pricing-dimensions.md). 
  
Če teh postopkov še niste izvedli, jih dokončajte in se vrnite na to temo.

## <a name="register-a-plug-in"></a>Registracija vtičnika
Ko se na strani **Vrstica ponudbe** ustvarijo podrobnosti vrstice ponudbe za projektno vrstico ponudbe, sistem ustvari dve vrstici ocene. Ena vrstica je na strani stroškov ocene, druga vrstica pa na strani prodaje. Enako velja za podrobnosti projektne pogodbe.

Ko spremenite količino ali polje na stroškovni strani, se ta sprememba razširi tudi na prodajno stran. To je mogoče, ker vtičniki PreOperation na entitetah s podrobnostmi QuoteLineDetail in ContractLine povežejo določene atribute na strani stroškov s prodajno stranjo transakcije. Če bi radi, da se spremembe vrednosti cenovnih razsežnosti na prodajni strani izvedejo tudi na strani stroškov, je treba po spremembi cenovnih razsežnosti naslednje vtičnike ponovno registrirati.

Spodaj so našteti vtičniki za posodobitev in ponovno registracijo:

- PreOperationContractLineDetailUpdate – **Posodobitev msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate – **Posodobitev msdyn_quotelinetransaction**

Dokončajte naslednje korake za posodobitev in ponovno registracijo vtičnikov.

1. Odprite **PluginRegistrationTool** in se povežite s svojim okoljem Dataverse v storitvi Project Operations.
2. Izberite **Iskanje** in vnesite prvih nekaj črk vtičnika, ki ga želite posodobiti.
3. Ko najdete vtičnik, ga izberite in nato kliknite **Izberi v glavnem obrazcu**.
4. Izberite korak **Posodobitev msdyn_orderlinetransaction**, ga kliknite z desno tipko miške in izberite **Posodobi**.
5. V pogovornem oknu **Posodobitev** kliknite tri pike (**...**) v atributih za filtriranje.
6. Odprlo se bo okno atributov za filtriranje skupaj s seznamom vseh atributov v entiteti in cenovnih razsežnostih. Izberite potrditvena polja za atribute cenovnih razsežnosti.
7. Kliknite **V redu**, da zaprete stran, nato izberite možnost **Posodobi korak**.
8. Ponovite korake od 2 do 7 za drugi vtičnik **PreOperationQuoteLineDetail**. Za ta vtičnik morate posodobiti korak **Posodobitev msdyn_quotelinetransaction**.
9. Zaprite **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]