---
title: Dodajanje naročnine na Azure projektu LCS
description: Ta tema vsebuje informacije o povezovanju naročnine Azure s projektom LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880558"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodajanje naročnine na Azure projektu LCS

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Okolja, ki se jih gosti v oblaku, je treba uvesti z obstoječo naročnino na Azure. Ta tema pojasnjuje, kako lahko povežete obstoječo naročnino na Azure s projektom LCS. 

## <a name="grant-admin-consent"></a>Podelitev soglasja skrbnika

1. V projektu LCS v razdelku **Okolja** izberite **Nastavitve Microsoft Azure**.

![Nastavitve Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na strani **Nastavitve projekta** na zavihku **Povezovalniki Azure** izberite **Pooblasti**. To omogoča uvedbo okolij v ta projekt.

![Povezovalniki Azure](./media/2AzureConnectors.png)

3. Znova izberite **Pooblasti**, da zagotovite soglasje skrbnika.

![Podelitev soglasja skrbnika](./media/3GrantAdminConsent.png)

4. Sprejmite zahtevo za dovoljenja.

![Sprejmite zahtevo za dovoljenja](./media/4AcceptPermissionRequest.png)

Pooblastitev je zdaj končana. 

![Pooblastitev je bila uspešna](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Omogočite dostop do storitev za uvajanje Dynamics za naročnino Azure

1. Odprite [Obračunavanje Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) in izberite naročnino. Storitve za uvajanje Dynamics morajo imeti dostop do te naročnine, da lahko uvajajo okolja.

![Podrobnosti o naročnini Azure](./media/6AzureSubscription.png)

2. V podoknu za krmarjenje izberite **Nadzor dostopa (IAM)** in nato izberite **Dodaj dodelitev vloge**.
3. Pri drsniku na desni strani izberite **Vloga sodelujočega** ter na podanem seznamu poiščite in izberite **Storitve za uvajanje Dynamics**. 
4. Izberite **Shrani**.

![Dostop do naročnine](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Dodajanje povezovalnika naročnine na projekt LCS

1. V projektu LCS na strani z **nastavitvami Microsoft Azure** izberite **Dodaj**, da dodate nov povezovalnik.
2. Vnesite ID naročnine na Azure. ID naročnine na Azure lahko najdete v [portalu Azure](https://ms.portal.azure.com/), pod možnostjo **Nastavitve** v spodnjem levem kotu zaslona.
3. V polju **Konfiguriraj za uporabo storitve Azure Resource Manager** izberite **Da**.
4. Prepričajte se, da se domena najemnika AAD za naročnino AAD ujema z naročnino na Azure, ki jo uporabljate in je lastnik domene, in izberite **Naprej**.
5. Na zaslonu **Nastavitev Microsoft Azure** izberite **Naprej**, da potrdite izbiro. Če se na tem zaslonu prikaže napaka, se vrnite v razdelek [Omogočite dostop do storitev za uvajanje Dynamics za naročnino Azure](#provide) v tej temi in se prepričajte, da ste opravili vse korake.
6. Prenesite potrdilo o upravljanju Azure v lokalno mapo v računalniku. Prosite skrbnika naročnine za Azure, da potrdilo naloži na portal za upravljanje Azure tako, da izbere naročnino in odpre razdelek **Nastavitve** > **Potrdila o upravljanju**. To potrdilo omogoča LCS, da v vašem imenu komunicira z Azure. Ta korak lahko preskočite, če ima vaš uporabnik dostop do naročnine.
7. Izberite **Naprej**.
8. Izberite regijo Azure, v kateri želite uvesti to možnost, in izberite podatkovno središče, ki je blizu mesta, kjer nameravate uporabljati ta sistem.
9.  Izberite **Poveži**.

Uspešno ste povezali naročnino na Azure. Zdaj lahko uvedete okolja Dynamics 365 Finance, ki se jih gosti v oblaku.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
