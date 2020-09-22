---
title: Ključni pojmi
description: Ta tema vsebuje informacije o ključnih pojmih za upravljanje virov v aplikaciji Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f5f96f65-c191-493a-aef7-df7deb52a9cb
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4a839b828d5e1da1e5a8d8a378197b3d4932e529
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755851"
---
# <a name="key-concepts"></a>Ključni pojmi

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V spodnji tabeli so opredeljeni ključni pojmi, ki so uporabljeni v aplikaciji Dynamics 365 Project Service Automation.

| Pojem                    | Definicija |
|----------------------------|------------|
| Član projektne ekipe        | Član projektne ekipe je lahko v okviru projektne ekipe opredeljen kot poimenovani vir z rezervacijami, poimenovani vir brez rezervacij ali splošni vir. Splošni viri nimajo rezervacij, so lokalni glede na projekt in nimajo omejitev glede zmogljivosti pri posameznih projektih. |
| Splošni vir projekta   | Označba mesta za vir, ki vam omogoča oblikovanje ekipe in zasnovo projektnega načrta, ne da bi poznali poimenovane vire. Projektni koledar se uporablja kot koledar splošnega vira. Splošne vire je mogoče dodati projektni ekipi in dodeliti posameznim opravilom. |
| Rezervirane ure               | Rezervacije ur za vire znotraj posameznega projekta so potrjene, da se zagotovi dokončanje projektnega dela. Rezervirane ure se odštejejo od celotne zmogljivosti vira. Rezervacije je mogoče izvesti le za poimenovane vire, ne pa tudi za splošne vire. |
| Dodeljene ure             | Ure za vir so dodeljene opravilom v projektnem razporedu. Dodelitve je mogoče izvesti tako za poimenovane kot splošne vire. Dodelitve niso odvisne od rezervacij. |
| Zahtevane ure dela             | Zahtevana zmogljivost, ki je poimenovani vir še ni izpolnil. Zahtevane ure dela zadevajo le splošne člane ekipe z generiranimi zahtevanimi pogoji za vire. |
| Povpraševanje                     | Trenutna in pričakovana delovna obremenitev. V storitvi Project Service Automation je povpraševanje prikazano v obliki zahtevanih pogojev za vire ali zahtev za vire. |
| Zahtevani pogoj za vir       | Entiteta, ki zajema zahtevane ure, začetne in končne datume, znanja, geografsko lokacijo in druge dejavnike cen za zahtevane vire. Zahtevani pogoji za vir se generirajo iz članov projektne ekipe ali ustvarijo posamično. |
| Zahteva za vir           | Entiteta, ki se uporablja kot »pisemska ovojnica« za prenos zahtevanega pogoja za vir, ki ga mora izpolniti upravitelj virov. |
| Privzeta vloga vira      | Vloga, pod katero je zabeležen posamezen vir za izračun ciljne uporabe. Predpostavlja se, da ima vir zahtevana znanja za določeno vlogo in ustreza ciljni uporabi za to vlogo. |
| Organizacijska enota vira | Organizacijska enota, h kateri je dodeljen posamezen vir. |
| Krivulja                    | Trajanje opravila, zahtevanega pogoja ali dodelitve, prikazan glede na dnevno razporeditev. Petdnevno opravilo z obsegom 40 ur je mogoče s krivuljo prikazati kot osem ur na dan v petih dneh. |
| Pogled »Uskladitev«        | Pogled, ki prikazuje rezervacije in dodelitve za vsakega člana projektne ekipe. Ta pogled omogoča vodji projekta, da si ogleda morebitna neskladja med rezervacijami in dodelitvami ter sprejme popravljalna dejanja v primeru neskladij. |
| Delovne ure                 | Entiteta, ki se uporablja za določitev zmogljivosti vira ter njegovega delovnega in prostega časa. Ta entiteta se imenuje tudi koledar virov. |
