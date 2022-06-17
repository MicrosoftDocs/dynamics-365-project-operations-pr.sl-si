---
title: Posodabljanje atributov vtičnikov z novimi cenovnimi razsežnostmi
description: Ta članek vsebuje informacije o tem, kako posodobiti atribute vtičnika za razsežnosti cen.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920034"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Posodabljanje atributov vtičnikov z novimi cenovnimi razsežnostmi

Ta članek vsebuje informacije o tem, kako posodobiti atribute vtičnika za razsežnosti cen.

> [!NOTE]
> Ta člen se uporablja samo za ponudbe in funkcije pogodbe v Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Zahteve
Preden dokončate korake v tem članku, morate opraviti postopke v naslednjih člankih:

  - [Ustvarjanje polj in entitet po meri](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete ](add-custom-fields-price-setup-transactional-entities.md)
  - [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-custom-fields-pricing-dimensions.md). 
  
Če teh postopkov še niste izvedli, jih dokončajte in se nato vrnite na ta članek.

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