---
title: Pregled postopka izdajanja računa
description: V tej temi je na voljo pregled postopka izdajanja računov v aplikaciji Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089304"
---
# <a name="invoicing-process-overview"></a>Pregled postopka izdajanja računa

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Aplikacija Project Operations za primere uporabe z viri/brez zalog ponuja obsežne zmogljivosti, prilagojene potrebam vodje projekta in referenta za terjatve/projektnega računovodje. Pri postopku izdajanja računov vodja projekta upravlja nedokončana opravila obračunavanja v projektu, referent za terjatve/projektni računovodja pa ustvari skladen in točen račun za stranko.

![Diagram poteka izdajanja računa](./media/invoicing-flow.png)

Podrobnosti projektne pogodbe določajo način obračunavanja za povezane projektne transakcije. Ko vodja projekta odobri časovne in stroškovne transakcije, sistem zabeleži transakcije v entiteto **Opravljena dela projekta** in pošlje podatke v modul **Upravljanje projektov in računovodstvo** v storitvi Dynamics 365 Finance. Projektni računovodja nato pregleda in objavi zapise v [dnevniku integracij za aplikacijo Project Operations](../project-accounting/project-operations-integration-journal.md). V tem dnevniku so pomembne računovodske podrobnosti za opravljeno delo v projektu, kot so obračun, skupina prometnega davka, skupina prometnega davka za artikel obračuna in finančne razsežnosti.

Vodja projekta lahko pregleda neobračunane prodajne transakcije z metodo obračunavanja časa in materiala v možnosti [Nedokončana opravila obračunavanja časa in materiala](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) in obračunavanja po fiksni ceni v možnosti [Mejniki s fiksno ceno](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ti pogledi vam omogočajo, da filtrirate in izberete transakcije, ki jih je treba vključiti v naslednji cikel obračunavanja, in jih nato označite kot **Pripravljeno za izdajanje računov**.

Lahko [ročno ustvarite predračun](../proforma-invoicing/create-manual-proforma-invoice.md) ali uporabite [periodični postopek](../proforma-invoicing/configure-automated-invoice-creation.md). Vodja projekta lahko po potrebi [prilagodi osnutek predračuna](../proforma-invoicing/manage-proforma-invoice.md) in ga nato potrdi.

Potrjeni predračun se pošlje v modul **Upravljanje projektov in računovodstvo** v storitvi Finance. Projektni računovodja oblikuje in posodobi predlog za račun projekta, nato pa objavi in natisne dokument. Objavljeni projektni računi se evidentirajo v glavni knjigi ter podknjigah za stranke in projekte.