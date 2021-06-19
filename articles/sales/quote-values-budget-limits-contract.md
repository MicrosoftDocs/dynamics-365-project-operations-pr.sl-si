---
title: Nastavitve projektnih ponudb
description: Ta tema vsebuje informacije glede podatkov in nastavitev, ki veljajo za projektne ponudbe in vplivajo nanje.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9181fc1f6a4820662cb145abab55072e9743bbaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011346"
---
# <a name="header-details-for-project-based-quotes"></a>Podrobnosti glave za ponudbe, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


V tem članku so pojasnjene informacije, ki veljajo za projektno ponudbo. To vključuje nastavitve, ki vplivajo na vse podrobnosti ponudb, in informacije o ponudbi, ki so povzete za vse vrstične postavke za uporabo KPI-jev projektne ponudbe.

V naslednji tabeli so navedena polja povzetkov podatkov v projektni ponudbi, ki so edinstvena za aplikacijo Dynamics 365 Project Operations ali imajo nekaj pomembnih razlik v vedenju v primerjavi s ponudbami v storitvi Dynamics 365 Sales.

| **Polje** | **Mesto** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Vnesi | Zavihek »Povzetek« (skrito) | To polje z naborom možnosti ima naslednje možnosti:</br>- temelji na delu (na voljo samo, če je nameščena storitev Project Operations)</br>- temelji na elementu (na voljo samo, če sta nameščeni storitvi Project Operations in Sales)</br>- temelji na vzdrževanju storitev (na voljo, ko je nameščena storitev Dynamics 365 Field Service) | Ko uporabljate aplikacijo Project Operations, je vrednost tega polja samodejno nastavljena na **Temelji na delu**. To razvrsti ponudbo med projektne ponudbe. Ponudba mora temeljiti na projektu, da lahko omogoča vse razširitve in funkcije, specifične za projekt. |
| Lastniško podjetje | Povzetek | Pravna oseba, ki bo odgovorna za stroške in prihodke, ki nastanejo iz tega projekta ali projektov, povezanih s to ponudbo. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. | Lastniško podjetje je enako konceptu pravne osebe v modulu **Vodenje projektov in računovodstvo** storitve Project Operations. Vsi stroški in prihodki, ki nastanejo pri tem projektu, se zabeležijo v glavni knjigi lastniškega podjetja. |
| Možna stranka | Zavihek »Povzetek« | Sklic na zapis strankinega podjetja ali kupca. Veljavna stranka za sklicevanje na projektni ponudbi mora biti nastavljena kot stranka v lastniškem podjetju na ponudbi. Lastniško podjetje je prikazuje seznam pravnih oseb, te pa so nastavljene v modulu **Vodenje projektov in računovodstvo** storitve Project Operations. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. | Valuta na projektni ponudbi je privzeto nastavljena glede na valuto stranke. Vendar pa tega ni mogoče spremeniti, preden shranite ponudbo. |
| Vodja za upravljanje kupcev | Zavihek »Povzetek« | Ime upravitelja kupcev za ta posel. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. | Upravitelj kupcev je odgovoren za upravljanje odnosa s stranko do zaključka tega projekta. Na podlagi zapisa vira, ki ga je mogoče rezervirati in je povezan z upraviteljem kupcev, je privzeto nastavljena pogodbena enota na projektni ponudbi.|
| Pogodbena enota | Zavihek »Povzetek« | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s to ponudbo. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto in ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, nastalih med izvajanjem projekta. |
| Cenik izdelkov | Zavihek »Povzetek« | To je cenik, ki se uporablja za privzeto nastavitev cen v podrobnostih ponudbe, ki temeljijo na izdelkih. Seznam možnosti za to polje prikazuje seznam cenikov, kjer se valuta cenika ujema z valuto na ponudbi. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. To polje pri priložnosti je privzeto nastavljeno iz zapisa kupca, vendar ga je mogoče spremeniti. | Ko je ponudba pridobljena, je ta vrednost polja kopirana v projektno pogodbo. |
| Valuta | Zavihek »Povzetek« | To označuje valuto, ki bo uporabljena za poročanje o vrednosti tega posla. To je tudi valuta, v kateri bo stranki fakturiran, če bo posel pridobil. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. To polje pri priložnosti je privzeto nastavljeno iz zapisa kupca, vendar ga lahko uporabnik spremeni.  | Ko je ponudba shranjena, tega polja ni več mogoče urejati. To se uporablja za privzeto nastavitev cenikov izdelkov in projektov na ponudbi. Valuta na ponudbi se uporablja za ujemanje valute na ceniku. |
| Omejitev »Ni dovoljeno preseči« | Zavihek »Povzetek« | To pomeni dogovorjeno zgornjo mejo končne vrednosti, s katero se stranka strinja za ta posel. | Ta zgornja meja se oceni med izvajanjem ter velja za vse vrstične postavke in projekte, povezane s tem poslom. |
| Zahtevani datum dostave | Zavihek »Povzetek« | V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja pri priložnosti. | Ta datum se uporablja kot končni datum za ustvarjanje razporedov za izdajanje računov. |

Spodaj so zavihki in KPI-ji, ki so na voljo v projektni ponudbi, ki so na voljo le v storitvi Project Operations ali pa imajo nekatere pomembne spremembe v delovanju, po katerih se ločijo od ponudb v storitvi Sales:

| **Polje** | **Mesto** | **Opis** |
| --- | --- | --- |
| Analiza dobičkonosnosti | Zavihek na ponudbi | Zavihek prikazuje naslednje metrike:</br>- skupno vrednost stroškov, ki se zaračunajo</br></br>- skupno vrednost stroškov, ki se ne zaračunajo</br>- skupni prihodek</br>- skupni prihodek (osnova)</br>- stopnjo bruto dobička</br>- prilagojeno stopnjo bruto dobička|
| Primerjava s pričakovanji stranke | Zavihek na ponudbi | Ta zavihek prikazuje naslednje metrike:</br>- predviden datum zaključka</br>- zahtevani zaključek</br>- proračun stranke</br>- ponudbena vrednost |
| Analiza ponudbe | Zavihek na ponudbi | Ta zavihek povzema naslednje glavne KPI-je za projektno ponudbo</br>- primerjava s pričakovanji strank glede proračuna in razporeda</br>- stopnjo bruto dobička</br>- prilagojeno stopnjo bruto dobička |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
