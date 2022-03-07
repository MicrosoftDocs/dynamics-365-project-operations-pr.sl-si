---
title: Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti
description: Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988806"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Če ne uporabljate funkcij za oblikovanje ponudb in sklepanje pogodb v rešitvi Project Service Automation (PSA), lahko to temo preskočite.

Predpostavljamo, da ste izvedli postopke v temah [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md), [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md) in [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-pricing-dimensions.md). Če teh postopkov še niste izvedli, se vrnite nazaj in jih dokončajte, preden se vrnete na to temo.

Ko ste ustvarili vrstico ponudbe na strani **Vrstica ponudbe** za vrstico ponudbe projekta, bo sistem v ozadju ustvaril dve vrstici ocen – eno za stroškovno stran ocene in eno za prodajno stran. Enako velja za podrobnosti projektne pogodbe.

Ko spremenite količino ali polje na stroškovni strani, se ta sprememba razširi na prodajno stran. To omogočajo spodnji vtičniki, ki jih je treba ponovno registrirati po spremembi cenovnih razsežnosti.

- PreOperationContractLineDetailUpdate – Posodobitve **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – Posodobitve **msdyn_quotelinetransaction**.

Naslednji koraki vam bodo pomagali pri postopku registracije vtičnikov.

1. Odprite orodje **PluginRegistrationTool** in se povežite s spletnim primerkom.
2. Kliknite **Iskanje** in poiščite vtičnik, ki ga želite posodobiti.

 ![Posnetek zaslona drevesa za iskanje.](media/PRT-1.png)

3. Ko najdete vtičnik, ga izberite in nato kliknite **Izberi v glavnem obrazcu**.

4. Izberite korak vtičnika, ki ga želite posodobiti, ga kliknite z desno tipko miške in nato izberite **Posodobi**.

 ![Posnetek zaslona vtičnika, ki ga želite posodobiti.](media/PRT-2.png)
 
5. V oknu za posodobitev kliknite tri pike (**...**) v atributih za filtriranje.

 ![Posnetek zaslona informacij o konfiguraciji možnosti »Posodobi obstoječi korak«.](media/PRT-3.png)
 
6. Izberite potrditvena polja z atributom za določanje cen.

 ![Posnetek zaslona, ki prikazuje izbiro potrditvenega polja atributov za določanje cen.](media/PRT-4.png)

7. Kliknite **V redu**, da zaprete stran, nato izberite možnost **Posodobi korak**.

 ![Posnetek zaslona, ki prikazuje gumb »Posodobi korak«.](media/PRT-5.png)
 
8. Ponovite ta postopek še za drugi vtičnik **PreOperationQuoteLineDetail – Posodobitev msdyn_quotelinetransaction**.

9. Zaprite orodje za registracijo vtičnika.



[!INCLUDE[footer-include](../includes/footer-banner.md)]