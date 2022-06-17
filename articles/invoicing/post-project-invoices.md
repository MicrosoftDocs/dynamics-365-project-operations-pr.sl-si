---
title: Pregled postopka izdajanja računa
description: Ta članek ponuja pregled postopka izdajanja računov v projektnih operacijah za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923116"
---
# <a name="invoicing-process-overview"></a>Pregled postopka izdajanja računa

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Aplikacija Project Operations za primere uporabe z viri/brez zalog ponuja obsežne zmogljivosti, prilagojene potrebam vodje projekta in referenta za terjatve/projektnega računovodje. Pri postopku izdajanja računov vodja projekta upravlja nedokončana opravila obračunavanja v projektu, referent za terjatve/projektni računovodja pa ustvari skladen in točen račun za stranko.

![Diagram poteka izdajanja računa.](./media/invoicing-flow.png)

Podrobnosti projektne pogodbe določajo način obračunavanja za povezane projektne transakcije. Ko vodja projekta odobri časovne in stroškovne transakcije, sistem zabeleži transakcije v **Dejanski podatki o projektu** subjekt in podatke pošlje na **Vodenje projektov in računovodstvo** modul v Dynamics 365 Finance. Projektni računovodja nato pregleda in objavi zapise v [dnevniku integracij za aplikacijo Project Operations](../project-accounting/project-operations-integration-journal.md). V tem dnevniku so pomembne računovodske podrobnosti za opravljeno delo v projektu, kot so obračun, skupina prometnega davka, skupina prometnega davka za artikel obračuna in finančne razsežnosti.

Vodja projekta lahko pregleda neobračunane prodajne transakcije z metodo obračunavanja časa in materiala v možnosti [Nedokončana opravila obračunavanja časa in materiala](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) in obračunavanja po fiksni ceni v možnosti [Mejniki s fiksno ceno](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ti pogledi vam omogočajo, da filtrirate in izberete transakcije, ki jih je treba vključiti v naslednji cikel obračunavanja, in jih nato označite kot **Pripravljeno za izdajanje računov**.

Lahko [ročno ustvarite predračun](../proforma-invoicing/create-manual-proforma-invoice.md) ali uporabite [periodični postopek](../proforma-invoicing/configure-automated-invoice-creation.md). Vodja projekta lahko po potrebi [prilagodi osnutek predračuna](../proforma-invoicing/manage-proforma-invoice.md) in ga nato potrdi.

Potrjeni predračun se pošlje v modul **Upravljanje projektov in računovodstvo** v storitvi Finance. Projektni računovodja oblikuje in posodobi predlog za račun projekta, nato pa objavi in natisne dokument. Objavljeni projektni računi se evidentirajo v glavni knjigi ter podknjigah za stranke in projekte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]