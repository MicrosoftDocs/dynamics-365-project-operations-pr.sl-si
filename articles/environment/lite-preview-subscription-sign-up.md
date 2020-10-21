---
title: Prijava za naročnino predogleda
description: Ta tema vsebuje informacije o tem, kako se lahko naročite in uvedete poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949079"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Prijavite se na naročnino predogleda za poenostavljeno uvedbo – od posla do izstavitve predračuna

Ta tema pojasnjuje, kako se lahko naročite na ponudbo partnerja za predogled in nastavite poenostavljeno uvedbo storitve Dynamics 365 Project Operations – od posla do izstavitve predračuna.

> [!NOTE]
> Ta postopek se bo spremenil v prihodnjih izdajah storitve Project Operations.

## <a name="prerequisites"></a>Zahteve

- Prejeli boste e-poštno sporočilo z vabilom k sodelovanju v predogledu. Predogled lahko zahtevate na [spletnem mestu storitve Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure.
- Uporabnik, ki uvede predogled, bo potreboval telefonsko številko in veljavno kreditno kartico. Ob prijavi šest mesecev ne bo stroškov za kartico. Po šestih mesecih morate naročnino preklicati. 
- Preglejte vse pogoje in določila.

## <a name="subscribe"></a>Naročite se

Ko prejmete odobritev [zahteve za predogled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), boste od Microsofta po elektronski pošti prejeli dve ponudbi. Te ponudbe omogočajo uvedbo predogleda Project Operations:

- Preskus predogleda Dynamics 365 Customer Service – koda za enkratno uporabo
- Dynamics 365 Project Operations – preskus predogleda

### <a name="dynamics-365-customer-service-paid-offer"></a>Plačljiva ponudba Dynamics 365 Customer Service

1. Prek okna brskalnika InPrivate/brez beleženja zgodovine unovčite prvo kodo ponudbe za Dynamics 365 Customer Service. Če se želite prijaviti na storitev Customer Service, boste potrebovali:

- telefonsko številko,
- kreditno kartico. Ko se prijavite, šest mesecev ne bo stroškov za kartico. Po šestih mesecih morate naročnino preklicati.
- Preglejte vse pogoje in določila.

2. Navedite svoje podatke za stik.

![Podatki za stik](./media/1ContactInformation.png)

3. Navedite podatke o novem najemniku.

![Ustvarjanje ID-ja uporabnika](./media/2CreateUserID.png)

4. Preverite svojo identiteto, shranite svoj novi ID uporabnika in izberite **Nastavi**.

![Shranjevanje podatkov](./media/3SaveInfo.png)

5. Opravite postopek prijave kreditne kartice ter preglejte vse pogoje in določila. 

![Opravljanje postopka za kreditno kartico](./media/4CompleteCreditCard.png)

![Dokončanje nakupa s kreditno kartico](./media/5CreditCardCheckout.png)

![Shranjevanje naročila](./media/6SaveOrder.png)

![Potrditev kreditne kartice](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Preklic ponudbe za podjetja Dynamics 365 Customer Service

Ponudba za podjetja Dynamics 365 Customer Service je šest mesecev na voljo brezplačno. Ponudba se bo po koncu šestmesečnega obdobja obnovila pri polni ceni. Če želite preklic opraviti pred datumom podaljšanja, upoštevajte naslednja navodila. 

> [!NOTE]
> Ko dokončate te korake, ne boste mogli več uporabljati okolja predogledne različice za javnost Project Operations.

1. Odprite [skrbniški portal](https://admin.microsoft.com/) in pod možnostjo **Obračunavanje** izberite **Vaši izdelki**.

![Skrbniški portal, stran z vašimi izdelki](./media/8AdminPortal.png)

2. Izberite možnost **Ponudba za podjetja Dynamics 365 Customer Service**.

![Preklic naročnine](./media/9CancelSubscription.png)

3. Izberite **Nastavitve** > **Dejanja** > **Prekliči naročnino**.
4. V obrazcu **Preklic naročnine** vnesite podatke v zahtevana polja.
5. Izberite **Prekliči** > **Naročnina.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – preskus predogleda

1. Prevzemite drugo ponudbo, preskus storitve Dynamics 365 Project Operations, z URL-jem, navedenim v e-poštnem sporočilu z dobrodošlico.

![Prevzem ponudbe 2](./media/10RedeemOffer2.png)

2. Preverite, ali ste prijavljeni kot uporabnik, ki pripada isti organizaciji, povezani z naročnino, uporabljeno s prvo kodo ponudbe, in nato nadaljujte s prevzemom ponudbe. 
3. Izberite **Da, možnost dodaj v moj račun**.

![Dodajanje v račun](./media/11AddToAccount.png)

![Zaslon »Preskusite zdaj«](./media/12TryNow.png)

![Podrobnosti naročila](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Dodeljevanje licenc

> [!IMPORTANT]
> Potrebovali boste skrbniški dostop do portala Office 365 vaše organizacije, če želite dokončati naslednje korake.

1. Odprite [skrbniško središče za Microsoft 365](https://portal.office.com/), da dodelite licence svojim uporabnikom.

![Začetna stran skrbniškega središča](./media/14AdminPortal.png)

2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.

![Dodeljevanje licenc](./media/15AssignLicenses.png)

3. Preverite, ali sta izbrani licenci **Customer Service Enterprise** in **Project Operations** ter izberite **Shrani spremembe**.

## <a name="create-a-new-cds-environment"></a>Ustvarjanje novega okolja CDS

Zagotovite si novo okolje za uvajanje CDS Project Operations tako, da upoštevate navodila v temi [Model za uvajanje CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Namestitev predstavitvenih podatkov za nastavitev in konfiguracijo CDS

Namestite konfiguracijo CDS in nastavite predstavitvene podatke ob upoštevanju navodil v temi [Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo](lite-apply-demo-setup-config-data.md).
