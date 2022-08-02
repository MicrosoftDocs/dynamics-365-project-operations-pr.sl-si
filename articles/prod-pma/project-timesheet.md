---
title: Mobilna aplikacija Project Timesheet
description: Ta članek vsebuje informacije o Microsoft Dynamics 365 Project Timesheet mobilna aplikacija. Mobilna aplikacija Project Timesheet omogoča uporabnikom, da oddajo časovne liste za projekte in jih odobrijo prek mobilne naprave.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110995"
---
# <a name="project-timesheet-mobile-application"></a>Mobilna aplikacija Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pregled

The Microsoft Dynamics 365 Project Timesheet mobilna aplikacija uporabnikom omogoča oddajo in odobritev časovnic za projekte na svoji mobilni napravi (iPhone ali Android). Ta mobilna aplikacija prikazuje funkcionalnost časovnega lista, ki se nahaja v območju za upravljanje projektov in računovodstvo Dynamics 365 Finance. Pomaga izboljšati produktivnost in učinkovitost uporabnikov ter omogoča pravočasen vnos in odobritev projektnih časovnic.

## <a name="download-and-install-the-mobile-app"></a>Prenos in namestitev mobilne aplikacije

Iz trgovine z aplikacijami si za svojo napravo prenesite in namestite mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet za naprave Android ali iPhone.

## <a name="enable-the-app"></a>Omogočanje aplikacije 

V rešitvi Finance mora biti omogočena mobilna aplikacija Project Timesheet. Če želite omogočiti funkcionalnost, pojdite na **Vodenje projekta in računovodski parametri \> Časovni list** in izberite **Omogočanje parametra za Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Rešite težave s prijavo

**Težava:** Med prijavo v aplikacijo Project Timesheet Mobile uporabniki prejmejo sporočilo o napaki, ki navaja, da "ne morejo dostopati do aplikacije"2bc50526-cdc3-4e36-a970-c284c34cbd6e ' v tem najemniku."

**Težava:** Med prijavo v aplikacijo Project Timesheet Mobile uporabniki prejmejo napako, ki je podobna enemu od naslednjih primerov:

- "AADSTS50020: Uporabniški račun '[uporabniško ime]' od ponudnika identitete 'https://sts.windows.net/ [id aplikacije]' ne obstaja v najemniku '[id najemnika]' in ne more dostopati do aplikacije '[id aplikacije]' v tem najemniku.«
- "Izbrani uporabniški račun ne obstaja v najemniku '[id najemnika]' in ne more dostopati do aplikacije '[id aplikacije]' v tem najemniku."

**Pojasnilo:** Te težave so posledica spremembe, ki je bila izvedena v Azure Active Directory (Azure AD) maja 2022 in je povezano z zunanjimi uporabniki. Ker ta sprememba ni bila narejena za aplikacije za financiranje in poslovanje, lahko vpliva na stranke na kateri koli različici platforme ali aplikacije.

**Popravek:** Vsi zunanji uporabniki morajo biti povabljeni k najemniku prek Azure AD. Za več informacij glejte [Povabi uporabnike z Azure Active Directory B2B sodelovanje](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Prijava v mobilno aplikacijo

1.  Zaženite aplikacijo v mobilni napravi.

2.  Vnesite URL za rešitev Finance.

3.  Ko se prvič prijavite, boste pozvani k vnosu uporabniškega imena in gesla. Vnesite svoje poverilnice.

4. Prijavljeni boste v svoje privzeto podjetje.

## <a name="submit-a-project-timesheet"></a>Pošiljanje časovnega lista projekta

V aplikaciji lahko ustvarite časovni razpored projekta in ga pošljete. Nov časovni list lahko razvijete na podatkih iz prejšnjega časovnega lista, shranjenih vrstic ali projektnih nalog. Če ste imenovani za pooblaščenca, lahko vnesete tudi časovnico za drugega delavca. Če želite ustvariti časovnico kot pooblaščenec, izberite **meni** in nato izberite ime vira.

Stran s časovnim listom bo ustvarila nov časovni list za obdobje časovnega lista, ki temelji na trenutnem datumu. Prikazan bo delovni teden. Če obdobje časovnega lista zajema več tednov, lahko na zavihkih delovnega tedna izberete drug delovni teden.
Če obstaja časovni list za trenutni datum, bo prikazan. Če želite ustvariti nov časovni list v drugem obdobju časovnega lista, izberite gumb **Meni** in nato **Nov časovni list**.

Informacije o projektu lahko vnesete tako, da kliknete dejanje **Dodaj čas** ali **Kopiraj čas iz**. Dejanje **Kopiraj čas iz** kopira podatke o vrstici projekta, ne kopira pa ur. Meni **Kopiraj čas iz** vključuje naslednje možnosti:

- **Kopiraj iz obstoječega časovnega lista** – kopiranje vrstic časovnega lista iz obstoječega časovnega lista.

- **Kopiraj iz priljubljenih** – ustvarjanje novih vrstic časovnega lista z uporabo nastavitev za časovni list, ki ste jih izbrali kot priljubljene.

- **Kopiraj iz naloge** – ustvarjanje novih vrstic časovnega lista iz dodeljenih projektov.

Prikazane informacije o projektu so odvisne od mobilnih parametrov, ki ste jih določili na strani **Vodenje projekta in računovodski parametri**.

V polju **Pravna oseba** izberite pravno osebo, za katero ste izvedli projektno delo. Polje **Pravna oseba** je na voljo samo, če je za vašo pravno osebo omogočena podpora za časovni list med podjetji.

Za časovni list izberite stranko, ki je povezana s projektom. Za prvo izdajo na Android, vnos s strani stranke ni podprt, saj morate najprej izbrati projekt. Če ste najprej izbrali projekt, se polje **Stranka** samodejno izpolni.

V **Projekt** polje izberite projekt, za katerega vnašate čas. Polje **Stranka** se samodejno izpolni.

Iskanje strank in projektov omogoča iskanje med strankami in projekti.

Izberite zahtevane podatke v poljih **Kategorija**, **Dejavnost**, **Lastnost vrstice**, **Skupina prometnega davka** in **Skupina prometnega davka za izdelek**. Ta polja je mogoče preglasiti.

Polje **Lastnost vrstice** bo nastavljeno na privzeto vrednost, ki temelji na vodenju projekta in računovodskih parametrih. Če so projekt/kategorija in parametri kategorije/vira omogočeni, bo vrednost polja **Lastnost vrstice** nastavljena na privzeto vrednost, ki ste jo določili za to preverjanje veljavnosti. Ko parametra projekta/kategorije in kategorije/vira nista omogočena, se **Lastnost vrstice** vrednost bo privzeta glede na **Omogoči privzeto lastnost vrstice** polje na **Projektno vodenje in računovodski parametri** strani. vrednost polja **Lastnost vrstice** je mogoče preglasiti.

Če želite dodati čas, izberite dan. Vnesite število ur, ki ste jih opravili vsak dan.

Če želite dodati komentarje o urah, ki jih vnašate, kliknite **Dodajte komentarje**, nato pa vnesite komentarje za interno občinstvo, stranko občinstvo ali oboje.
Notranje komentarje si lahko ogledajo vodje projektov. Komentarji strank so vključeni v računih.

Če želite vrstico shraniti med priljubljene, potrdite polje in kliknite **Shrani med priljubljene**.

Finančna dimenzija in podpora za priloge v mobilni aplikaciji nista na voljo.

Za izpolnjevanje časovnega list nadaljujte z dodajanjem zahtevanih projektnih vrstic.

Kliknite **Pošlji**, da pošljete časovni list v potek dela za odobritev.

## <a name="review-timesheets"></a>Pregled časovnih listov

Seznam časovnic, ki jih je treba pregledati, je na voljo v meniju. Ta možnost je na voljo le, če ste bili imenovani za odobritelja poteka dela. Podprta sta odobritev glave in vrstic. Odobritev ravni vrstice ponuja možnost označevanja ene ali več vrstic za odobritev. Po pregledu podatkov o časovnem listu kliknite **Odobri**, **Pooblasti** ali **Nazaj** za nadaljevanje poteka dela.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
