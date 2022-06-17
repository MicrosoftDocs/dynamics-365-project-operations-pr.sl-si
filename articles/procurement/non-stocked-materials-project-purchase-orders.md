---
title: Naročanje materialov, ki niso na zalogi, za projekt, ki uporablja naročilnice za projekte
description: V tem članku je razloženo, kako lahko naročite materiale brez zalog za projekt z naročili projekta.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929832"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Naročite kategorije nabave ali materiale brez zalog za projekt z uporabo projektnih naročil

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Nabavni oddelek v vaši organizaciji bi lahko uporabil [naročilnice](/dynamics365/supply-chain/procurement/purchase-order-overview) za sledenje naročil blaga in storitev. Projektu je mogoče pripisati naročila za nabavne kategorije ali materiale, ki niso na zalogi. Zaračunavanje teh naročilnic beleži stroške projekta.

## <a name="prerequisites"></a>Zahteve
Upoštevajte naslednje korake, da omogočite funkcijo naročilnic projektov.

1. V Dynamics 365 Finance pojdite na **Upravljanje funkcij** delovni prostor.
2. Na seznamu funkcij poiščite in izberite funkcijo **Omogoči naročilnice projektov v aplikaciji Project Operations za scenarije, ki temeljijo na virih/nezalogi**.
3. Izberite **Omogoči**.
4. Konfigurirajte materiale, ki niso na zalogi, in račune dobaviteljev v čakanju, kot je opisano v razdelku [Konfiguracija materialov, ki niso na zalogi, in računov dobaviteljev v čakanju](configure-materials-nonstocked.md).
5. Konfigurirajte kategorije naročil, kot je opisano v [Uporabite kategorije nabave s projektnimi naročilnicami in čakajočimi računi prodajalcev](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Ustvarite naročilnico projekta s seznama naročilnic projektov

1. V razdelku za finance odprite možnost **Upravljanje projektov in vodenje računov** > **Projekti** > **Vsi projekti** in izberite projekt.
2. V podoknu za dejanja v zavihku **Upravljanje** v skupini **Novo** izberite **Opravilo elementa** > **Naročilnica**.
3. Na strani **Ustvarite naročilnico** izberite dobavitelja, pri katerem želite oddati naročilo, vnesite ustrezne druge podatke in nato izberite možnost **V redu**.
4. Na strani **Naročilnica** v mreži **Vrstice naročilnic** izberite **Dodaj vrstico**.
5. Vnesite številko artikla ali kategorijo nabave, količino, enoto, ceno na enoto in druge ustrezne informacije.

    > [!NOTE]
    > S projektnimi naročilnicami se lahko uporabljajo samo kategorije nabav, artikli, ki niso na zalogi, in storitve. Založeni artikli niso podprti.

6. Po potrebi nadaljujte z dodajanjem artiklov ali kategorij nabave in potrdite naročilo.

    Potrdilo o blagu in storitvah lahko zabeležite tako, da ustvarite in objavite potrdilo o izdelku.

    > [!NOTE]
    > Potrdila o izdelkih se ne beležijo v dejanskih vrednosti projekta v storitvi Microsoft Dataverse in ne vplivajo na analitično evidenco projekta.

    Potem ko dobavitelj pošlje račun za izdelke in storitve na naročilnici, lahko dobavni oddelek ustvari račun za naročilnico tako, da v podoknu za dejanja odpre možnost **Račun** > **Ustvari** > **Račun**. Za več informacij o čakajočih računih dobaviteljev glejte razdelek [Nakup materialov, ki niso na zalogi, z uporabo čakajočega računa dobavitelja](pending-vendor-invoices.md).
