---
title: Novosti v marcu 2022 – Project Operations za primere uporabe z viri/brez zalog
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations marca 2022 za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910926"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v marcu 2022 – Project Operations za primere uporabe z viri/brez zalog

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno delovanje v a Dataverse različica okolja 4.30.0.99
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.25

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

Dnevnice so zdaj podprte v novem in na novo zasnovanem sodobnem delovnem prostoru stroškov. Podjetja, ki uporabljajo dnevnice, lahko to funkcijo omogočijo, da uporabnikom omogočijo enostaven način za oddajo in povračilo dnevnic. Za več informacij glejte [Dnevnice](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Naslednji seznam prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations marca 2022.

| **Preslikava entitete** | **Posodobljena različica** | **Pripombe** |
| --- | --- | --- |
| Integracija projektnih operacij, izvozna entiteta vrstice računa prodajalca projekta msdyn\_ projektvendorinvoicelines | 1.0.0.3 | Preslikave so posodobljene tako, da se uskladijo z entiteto vrstice računa prodajalca v Dataverse. <br>Ne aktivirajte različice preslikave 1.0.0.4. V naslednji mesečni posodobitvi bo pripravljen za uporabo v kombinaciji z različico okolja Finance 10.0.26. |

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili izključen zemljevid tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu zemljevida naletite na težavo, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Čas in strošek | 2388011 | Pokažite zavrnitvene komentarje vlagateljem vnosa časa med odobritvijo v velikem obsegu. |
| Načrtovanje in sledenje projektov | 2495294 | Podrobnosti projekta ni mogoče urejati na **Podrobnosti o nalogi** stran. |
| Zaračunavanje in cene | 2499605 | Mejniki pogodbe, ki so ustvarjeni iz mejnikov ponudbe, so napačno označeni kot samo za branje. |
| Načrtovanje in sledenje projektov | 2506050 | Nabor operacij ostane na čakanju eno uro, če ni sprememb za shranjevanje. Nabor je nato napačno označen kot **Neuspešno**, medtem ko ga je treba dokončati takoj. |
| Zaračunavanje in cene | 2507401 | Privzete pogodbene enote so napačno vnesene v projekte zaradi nepravilnega predpomnjenja. |
| Zaračunavanje in cene | 2541660 | **Potrditev ustvarjanja prodajnega naročila** v dvojnem pisanju mora biti samo za naročila, ki temeljijo na projektu. |
| Zaračunavanje in cene | 2552745 | Davek ni razdeljen med stranke, ki so nastavile pravila za deljeno obračunavanje. |
| Zaračunavanje in cene | 2558859 | Izboljšana sporočila o napakah pri nastavitvi dimenzij cen. |
| Zaračunavanje in cene | 2558933 | **Uvoz iz ocen projekta** ne uspe, ko **msdyn\_ projekt** je dodan kot cena. |
| Zaračunavanje in cene | 2559101 | Brisanje parametrov projekta ni blokirano in povzroča težave. |
| Upravljanje priložnosti | 2570390 | Vtičnik dvojnega pisanja prisili vrsto računa na ponudbe, naročila in priložnosti **Stranka**, tudi če ta vrsta računa ni pravilna. |
| Zaračunavanje in cene | 2586097 | Dejanski dejanski zaračunani stroški se ne razveljavijo, ko je projekt odstranjen iz pogodbene vrstice projekta. |
| Zaračunavanje in cene | 2589619 | Davek na vpisno gradivo se razširi na neobračunano dejansko prodajo in račun. |
| Upravljanje priložnosti | 2594015 | Ponudbe ni mogoče zaključiti kot zmagovalno za stranke, ki so **Net60** plačilni pogoji. |
| Načrtovanje in sledenje projektov | 2595841 | V Project for the Web uporabniki prejmejo sporočilo o napaki o manjkajočih **msdyn\_ dejanski začetek** ko ustvarijo novo zahtevo za vir. |
| Čas in strošek | 2602511 | The **Zavrnjeno s strani** polje za prikaze časovnih vnosov **sistem** namesto imenovanega uporabnika kot zavrnilca. |
| Čas in strošek | 2602528 | Odobritelj projekta lahko odobri čas za projekte, kjer niso navedeni kot odobritelj. |
| Zaračunavanje in cene | 2608550 | Popravek računa je mogoče potrditi tudi, če izvirnik ni sprememb. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vodenje projektov in računovodstvo na Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Obstaja neskladje med financami in projektnimi operacijami v dovoljeni dolžini **ID kategorije** polje. |
| Upravljanje projektov in računovodstvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projektov s fiksno ceno ni mogoče odpraviti, ko **Na račun računov** polje je nastavljeno na **Profit in izguba** in **Izpolnjen odstotek** uporablja se načelo. |
| Upravljanje projektov in računovodstvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nepravilna privzeta skupina prometnega davka je vnesena iz nastavitve projekta v odhodkovne vrstice v integracijskem dnevniku projektnih operacij. |
| Upravljanje projektov in računovodstvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Razsežnosti glave predloga računa projekta ne morete urejati v integrirani razmestitvi s projektnimi operacijami. |
| Upravljanje projektov in računovodstvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Računi med podjetji ne smejo biti integrirani z Dataverse. |
| Upravljanje projektov in računovodstvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Obstaja neusklajenost v valuti stanja strank in valuti poročanja. |
| Upravljanje projektov in računovodstvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektni račun lahko objavite tudi, če je stranka na čakanju za vse račune. |
| Upravljanje projektov in računovodstvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | The **Izbrišite vse vrstice** V predlogih projektnih računov, ki imajo možnost, manjka gumb **Glava** in **vrstice** pogledov. |
| Upravljanje projektov in računovodstvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Ko knjižite račun prodajalca, se pojavi naslednja napaka: »Obračunski datum za račun mora biti v istem obračunskem letu kot povezano kupljeno naročilo. Zaženite postopek ob koncu leta naročilnice ali spremenite datum v tekoče obračunsko leto." |
| Pot in stroški | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Prevzeti stroški za projekt se ne sprostijo po sprostitvi obveznosti potnih zahtevkov. |
| Pot in stroški | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Ko oddate poročilo o stroških, se pojavi naslednja napaka: "Sledenje sklada: Podjetje ne obstaja." |
| Pot in stroški | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Privzeto **ID projekta** se ne vnese v poročila o izdatkih, ko je **Zahtevaj dejavnost za revijo** parameter je izbran na projektu. |
| Pot in stroški | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | The **Poštni stroški** Gumb ne deluje pravilno v projektnih operacijah za scenarije virov/brez zalog. |
| Pot in stroški | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Obstaja težava z **Stopnja na miljo** za poročilo o stroških prevoženih kilometrov, ki vključuje potnike. |
| Pot in stroški | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Stopnje stroškov prevoženih kilometrov za zaposlene niso pravilno sešteti, če sta v uporabi dve različni vrsti vozil **Stopnje kilometrine** kategorijo stroškov. |
| Pot in stroški | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Iskanje za **Projekt** polje v vrstici potnih zahtevkov ne vrne pravilnega seznama projektov. |
| Pot in stroški | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometraža v pregledu** prikazuje opozorilo na poročilih o stroških. |
| Pot in stroški | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Storitev optičnega prepoznavanja znakov (OCR) potrdila ne deluje zaradi težave z URL-jem storitve OCR stroškov. |
| Pot in stroški | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ko **Sposobnost hitrega razvrščanja ponavljajočih se stroškov** je omogočena, se zneski v vrsticah razčlenitve v poročilih o izdatkih spremenijo zneske vsakič, ko se **Razčlenite** stran se odpre. |
| Pot in stroški | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Poročila o stroških ne morete izbrisati, če ima vmesni seznam več kot enega odobritelja. |

## <a name="removed-and-deprecated-features"></a>Odstranjene in zastarele funkcije

The [Odstranjene ali zastarele funkcije v Project Operations](removed-depreciated-features-project.md) članek opisuje funkcije, ki so bile odstranjene ali zastarele Dynamics 365 Project Operations.

- Odstranjena funkcija v izdelku ni več na voljo.
- Zastarela funkcija ni v aktivnem razvoju in bo morda odstranjena v prihodnji posodobitvi.

Obvestilo o prenehanju veljavnosti bo prikazano v [Odstranjene ali zastarele funkcije v Project Operations](removed-depreciated-features-project.md) člen 12 mesecev preden se katera koli funkcija odstrani iz izdelka.

Za prekinitvene spremembe, ki vplivajo samo na čas kompilacije, vendar so binarno združljive s peskovnikom in produkcijskimi okolji, bo čas zastaranja krajši od 12 mesecev. Običajno so te spremembe funkcionalne posodobitve, ki jih je treba izvesti v prevajalnik.
