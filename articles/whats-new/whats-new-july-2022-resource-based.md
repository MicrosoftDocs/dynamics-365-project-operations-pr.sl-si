---
title: Novosti za julij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta julija 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zaloge.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183938"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za julij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse različica okolja 4.44.0.22
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance verzija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje projektne operacije Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljen zemljevid tabel, znova uveljavite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če naletite na težavo, ko zaženete zemljevid, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Uvajanje in konfiguracija | 2761472 | Obdelana je napaka pri namestitvi Project Operations. |
| Zaračunavanje in oblikovanje cen | 2746940 | Ime vrstice podizvajalca mora imeti največ 100 znakov. |
| Zaračunavanje in oblikovanje cen | 2739162 | Stranke morajo imeti možnost videti gumbe na traku v dejanskem mrežnem pogledu. |
| Načrtovanje in sledenje projektov | 2730318 | Posodobljeno preverjanje veljavnosti za nepodprte znake v predmetu projekta. |
| Zaračunavanje in oblikovanje cen | 2705361 | Dejanske vrednosti zaračunane prodaje mejnikov morajo biti vključene v polja za sledenje projekta. |
| Zaračunavanje in oblikovanje cen | 2675880 | Preprečite, da bi bil projekt povezan s pogodbeno vrstico, ki ne temelji na delu. |
| Zaračunavanje in oblikovanje cen | 2664396 | Če je ponudbeni cenik shranjen brez ponudbe, mora obstajati napaka, da ponudba ne sme biti prazna. |
| Zaračunavanje in oblikovanje cen | 2184019 | The **Zaračunavanje na podlagi nalog** Zavihek ne sme biti prikazan za projekte, ki nimajo podporne pogodbe ali ponudbe. |

### <a name="project-management-and-accounting-in-finance"></a>Vodenje projektov in računovodstvo v Financah

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite v Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije so privzeto vklopljene v prihajajoči izdaji

Naslednja tabela navaja funkcije, ki so privzeto vklopljene v različici 10.0.29. Večino funkcij, ki so bile samodejno vklopljene, je mogoče izklopiti v [Upravljanje funkcij](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V prihodnosti bodo nekatere funkcije, ki so bile samodejno vklopljene, morda odstranjene iz upravljanja funkcij in bodo postale obvezne. Ta sprememba zagotavlja, da stranke uporabljajo trenutno funkcionalnost, tako da lahko izboljšave gradijo na trenutni funkcionalnosti, ko so dodane. Funkcije ne bodo nikoli samodejno omogočene v manj kot enem letu, razen če se ugotovi, da so bistvene.

| Ime funkcije | Omogoči datum | Dodana funkcija | Stanje funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogoči prilagoditev transakcije ur glede na spremembo dodelitve pravila financiranja | 16. september 2022 | 7. oktober 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Funkcija razveljavitve predplačilnega računa za naročilo projekta | 16. september 2022 | 6. oktober 2021 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Izbrišite vrstice predlogov računa, ko uporabljate Project Operations za scenarije, ki temeljijo na virih/nezaloženih | 16. september 2022 | 6. oktober 2021 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Prilagodite računovodstvo na transakciji knjiženega projekta | 16. september 2022 | 10. maj 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogoči privzeto nastavitev računovodstva za projekt | 16. september 2022 | 19. februar 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogočanje več podrobnosti pogodbe za projekt | 16. september 2022 | 29. junij 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Naj bodo dnevniki Project Hour samo za branje, če trenutno stanje odobritve ne dovoljuje urejanja | 16. september 2022 | 6. oktober 2021 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogoči sinhronizacijo prodajnih vrstic iz nabavnih vrstic, ko so nabavne vrstice posodobljene in je vklopljen parameter za upravljanje sprememb nakupnega naročila | 16. september 2022 | 7. oktober 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Omogoči projektne operacije na Dynamics 365 Customer Engagement | 16. september 2022 | 29. junij 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |
| Funkcija popravka razveljavitve projektne transakcije | 16. september 2022 | 13. julij 2020 | Privzeto vklopljeno | Upravljanje projektov in računovodstvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcije, ki bodo postale obvezne v prihajajoči izdaji

Naslednja tabela navaja funkcije, ki so obvezne od različice 10.0.29 dalje.

| Ime funkcije | Omogoči datum | Dodana funkcija | Stanje funkcije | Modul |
| --- | --- | --- | --- | --- |
| Izračunajte dodeljeno vrednost na viru financiranja brez zaokroževanja menjalnega tečaja | 16. september 2022 | 14. junij 2020 | Obvezno | Upravljanje projektov in računovodstvo |
| Omogoči knjiženje prilagoditve projekta z istim računom glavne knjige kot prvotna transakcija | 16. september 2022 | 14. junij 2020 | Obvezno | Upravljanje projektov in računovodstvo |
| Podrobnosti o dodeljenem znesku projektne pogodbe | 16. september 2022 | 31. avgusta 2019 | Obvezno | Upravljanje projektov in računovodstvo |
| Omogoči razvrščanje po viru med ustvarjanjem predloga računa za projekt | 16. september 2022 | 31. avgusta 2019 | Obvezno | Upravljanje projektov in računovodstvo |
