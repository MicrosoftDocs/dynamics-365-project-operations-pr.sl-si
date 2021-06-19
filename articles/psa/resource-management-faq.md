---
title: Pogosta vprašanja in odgovori o upravljanju virov
description: Ta tema vsebuje odgovore na pogosta vprašanja o upravljanju virov.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008781"
---
# <a name="resource-management-faq"></a>Pogosta vprašanja in odgovori o upravljanju virov

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Kakšna je razlika med članom ekipe in zahtevanim pogojem za vir?

Član projektne ekipe je lahko dodeljen k opravilom, rezerviran ali prevečkrat rezerviran ter nastavljen kot odobritelj. Zahtevani pogoj za vir lahko obstaja tudi brez člana projektne ekipe v obliki osnutka o povpraševanju. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Kakšna je razlika med predlaganimi in začasno rezerviranimi urami?

Predlagane ure in začasno rezervirane ure se razlikujejo po vidljivosti. Predlagane ure so vidne le upraviteljem virov in vodji projekta, ki je sprožil zahtevo prek zahteve za vir. Začasno rezervirane ure so vidne vsem, ki imajo dostop do plošče razporeda.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Kako lahko vidim začasno rezervirane ure za vire znotraj ekipe?

Začasne rezervacije je mogoče opraviti ob rezervaciji zahtevanega pogoja za vir. Viri, ki so začasno rezervirani v projektni ekipi, se nato prikažejo kot člani ekipe z začasno rezerviranimi urami. Prikažejo se tudi na plošči razporeda.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kako spremenim zahtevane ure ter začetne in končne datume za vir (splošen ali poimenovan), ki sem ga rezerviral/a?

Po opravljeni rezervaciji virov izberite **Upravljanje rezervacij**, če želite izvesti kakršne koli spremembe.

## <a name="what-resources-types-does-project-service-automation-support"></a>Katere vrste virov podpira Project Service Automation?

V aplikaciji Dynamics 365 Project Service Automation sta podprti le vrsti virov **Uporabnik** in **Stik**. Druge vrste virov (na primer **Oprema** in **Skupina**) sicer lahko ustvarite, vendar zanje ni podprt noben celovit primer uporabe.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Kakšna je razlika med dodelitvijo in rezervacijo?

Dodelitve označujejo dodeljevanje virov k projektnim opravilom v projektnem razporedu. Viri so lahko resnični ali splošni. Rezervacije so potrjene ali začasne dodelitve virov določenemu projektu. Potrjene rezervacije porabijo zmogljivost vira. Načeloma bi se morale rezervacije in dodelitve za resnične vire skladati, saj se ne razlikujejo. Vendar PSA ne vsiljuje tega pravila. V pogledu »Usklajevanje« se vodji projekta prikažejo mesta, kjer se rezervacije in dodelitve vira ne skladajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]