---
title: Novosti za julij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji aplikacije Microsoft Dynamics 365 Project Operations julija 2022 za scenarije, ki temeljijo na virih/nezalogi.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403972"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za julij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.44.0.22. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Uvajanje in konfiguracija | 2761472 | Obdelana je napaka pri namestitvi aplikacije Project Operations. |
| Zaračunavanje in oblikovanje cen | 2746940 | Ime podrobnosti podizvajalske pogodbe podizvajalca ima lahko največ 100 znakov. |
| Zaračunavanje in oblikovanje cen | 2739162 | Stranke morajo videti gumbe na traku v dejanskem mrežnem pogledu. |
| Načrtovanje in sledenje projektov | 2730318 | Posodobljeno preverjanje veljavnosti za nepodprte znake v predmetu projekta. |
| Zaračunavanje in oblikovanje cen | 2705361 | Dejanske vrednosti zaračunane prodaje mejnikov morajo biti vključene v polja za sledenje projekta. |
| Zaračunavanje in oblikovanje cen | 2675880 | Preprečite, da bi bil projekt povezan s podrobnostmi pogodbe, ki ne temeljijo na delu. |
| Zaračunavanje in oblikovanje cen | 2664396 | Če je cenik ponudbe shranjen brez ponudbe, je prišlo do napake, ki navaja, da ponudba ne sme biti prazna. |
| Zaračunavanje in oblikovanje cen | 2184019 | Zavihek **Zaračunavanje na podlagi opravil** ne sme biti prikazan za projekte, ki nimajo podporne pogodbe ali ponudbe. |
| Čas in strošek | 2754459 | Ko je ponavljajoči se tok za oblak za razporejanje neaktiven, se prikaže pasico in obide asinhrono obdelavo. |
| Zaračunavanje in oblikovanje cen | 2724391 | Ko pravilu za razdeljeno obračunavanje projektne pogodbe manjka vrednost stranke, se pojavi napačna izjema. |
| Zaračunavanje in oblikovanje cen | 2708638 | Zapis ni bil najden med iskanjem po mreži v razdelkih »Uporaba materiala« in »Odobritve za uporabo materiala«.|
| Zaračunavanje in oblikovanje cen | 2686977 | Preprečite preverjanje veljavnosti za vrstico računa med ustvarjanjem računa. |
| Zaračunavanje in oblikovanje cen | 2683032 | Kopiranje plačljivih vlog in kategorij ne presega 5000 zapisov.|
| Zaračunavanje in oblikovanje cen | 2673363 | Odstotek porabe stroškov pri projektu je poškodovan, ko za projekt obstajajo ocene truda in stroškov ter dejanske vrednosti. |

### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije so privzeto vklopljene v prihajajoči izdaji

Naslednja tabela navaja funkcije, ki so privzeto vklopljene v različici 10.0.29. Večino funkcij, ki so bile samodejno vklopljene, je mogoče izklopiti v razdelku [Upravljanje funkcij](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V prihodnosti bodo nekatere funkcije, ki so bile samodejno vklopljene, morda odstranjene iz razdelka »Upravljanje funkcij« in bodo postale obvezne. Ta sprememba strankam zagotavlja uporabo trenutnih funkcionalnosti, da lahko izboljšave, ko so dodane gradijo na trenutni funkcionalnosti. Funkcije ne bodo nikoli samodejno omogočene v manj kot enem letu, razen če se ugotovi, da so bistvene.

| Ime funkcije | Datum omogočanja | Funkcija je dodana | Stanje funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogočanje prilagoditev transakcije ur glede na spremembo dodelitve pravil financiranja | 16. september 2022 | 7. oktober 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Funkcija razveljavitve predračuna za naročilnico projekta | 16. september 2022 | 6. oktober 2021 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Brisanje vrstice predloga računa pri uporabi aplikacije Project Operations za primere, ki temeljijo na virih/nezalogi | 16. september 2022 | 6. oktober 2021 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Prilagoditev računovodstva na transakciji knjiženega projekta | 16. september 2022 | 10. maj 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogočanje privzete nastavitve računovodstva za projekt | 16. september 2022 | 19. februar 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogočanje več podrobnosti pogodbe za projekt | 16. september 2022 | 29. junij 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Dnevniki ur projekta bodo samo za branje, če trenutno stanje odobritve ne dovoljuje urejanja | 16. september 2022 | 6. oktober 2021 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogoči sinhronizacijo prodajnih vrstic iz nabavnih vrstic, ko so nabavne vrstice posodobljene in je vklopljen parameter za upravljanje sprememb naročilnice | 16. september 2022 | 7. oktober 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogočanje aplikacije Project Operations v storitvi Dynamics 365 Customer Engagement | 16. september 2022 | 29. junij 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Funkcija popravka razveljavitve transakcije projekta | 16. september 2022 | 13. julij 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcije, ki bodo postale obvezne v prihajajoči izdaji

Naslednja tabela navaja funkcije, ki so obvezne od različice 10.0.29 dalje.

| Ime funkcije | Datum omogočanja | Funkcija je dodana | Stanje funkcije | Modul |
| --- | --- | --- | --- | --- |
| Izračun dodeljene vrednosti na viru financiranja brez zaokroževanja menjalnega tečaja | 16. september 2022 | 14. junij 2020 | Obvezno | Upravljanje projektov in računovodstvo |
| Omogočanje knjiženja prilagoditve projekta z istim računom glavne knjige kot prvotna transakcija | 16. september 2022 | 14. junij 2020 | Obvezno | Upravljanje projektov in računovodstvo |
| Podrobnosti o dodeljenem znesku projektne pogodbe | 16. september 2022 | 31. avgusta 2019 | Obvezno | Upravljanje projektov in računovodstvo |
| Omogočanje razvrščanja po viru med ustvarjanjem predloga računa za projekt | 16. september 2022 | 31. avgusta 2019 | Obvezno | Upravljanje projektov in računovodstvo |
