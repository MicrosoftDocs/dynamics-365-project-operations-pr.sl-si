---
title: Nastavitev virov projekta
description: Ta članek vsebuje informacije o nastavitvi virov projekta ali pošiljanju zahtev za vire projekta.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933788"
---
# <a name="set-up-project-resources"></a>Nastavitev virov projekta

[!include [banner](../includes/banner.md)]

Nastaviti morate koledar in ga povezati z zaposlenim ali delavcem. Koledar se uporablja za načrtovanje projekta in delovnega časa virov, ki so rezervirani za projekt. Med nastavitvijo koledarja lahko projektni vodje opravijo izravnavo virov kot del optimizacije virov. Na podlagi razporeda koledarja je mogoče uvesti omejitve za vire. Koledar lahko nastavite na strani **Koledarji**.

Ko nastavljate delavca kot vir projekta, lahko izbirate med delavci, ki delajo v podjetju, za katero nastavljate vire. Lahko pa izberete delavce iz drugih podjetij v organizaciji. Ti delavci so znani kot medpodjetniški viri.

Z naslednjimi postopki je pojasnjeno, kako nastavite delavca kot vir projekta v vašem podjetju in kako nastavite medpodjetniški vir projekta.

## <a name="set-up-a-worker-as-a-project-resource"></a>Nastavitev delavca kot vir projekta

1. Na strani **Delavci** na seznamu **Delavci** izberite delavca, ki ga dodajate kot vir projekta, in odprite zapis delavca.
2. V podoknu za dejanja izberite **Projekt** &gt; **Nastavitev** &gt; **Nastavitev projekta**.
3. Izberite koledar in nato zaprite stran.

Določite lahko tudi privzete projekte za vire kot vrsto preddodelitve. Preddodelitve je mogoče uporabiti, ko upravitelj virov ali projektni vodja vnaprej ve, na katerih projektih bo delal vir. Preddodelitve lahko temeljijo tudi na zahtevi sponzorja ali stranke projekta. Za preddodelitev projekta na strani **Dodelitve projektov** na zavihku **Projekti** v seznamu **Preostali projekti** izberite primeren projekt.

## <a name="set-up-an-intercompany-resource"></a>Nastavitev medpodjetniškega vira

Ko nastavite delavca kot medpodjetniški vir, morate izvesti nastavitev v podjetju posojevalcu in podjetju izposojevalcu.

### <a name="in-the-lending-company"></a>V podjetju posojevalcu

1. V storitvi Finance potrdite, da je izbrano podjetje posojevalec in nato izvedite postopke v prejšnjem razdelku »Nastavitev delavca kot vir projekta«.
2. Na strani **Medpodjetniško računovodstvo** izberite možnost **Novo**.
3. V polju **ID pravne osebe** izberite podjetje posojevalca. Izpolnite preostala polja, kot je primerno, in nato izberite **Shrani**.
4. Na strani **Cena prenosa** izberite možnost **Novo**.
5. V polju **Pravna oseba izposojevalka** izberite ustrezno podjetje.
6. Da bi podjetju izposojevalcu posodili samo vir, ki ste ga ustvarili na začetku tega razdelka, v polju **Vir** izberite ime vira, ki ste ga ustvarili. Da bi dali vse vire v podjetju posojevalcu na voljo podjetju izposojevalcu, pustite polje **Vir** prazno.
7. Na strani **Vodenje projektov in računovodski parametri** na zavihku **Medpodjetniško** nastavite možnost **Omogoči medpodjetniško razporejanje virov in časovne liste** na **Da**.

### <a name="in-the-borrowing-company"></a>V podjetju izposojevalcu

- Na strani **Seznam virov** v iskalni filter vnesite ime vira, ki ste ga ustvarili za podjetje posojevalca, da preverite, ali je ime vključeno na seznam virov za podjetje izposojevalca.

## <a name="request-project-resources"></a>Zahteva za vire projekta
Funkcionalnost za razporejanje virov projekta samo upraviteljem virov omogoča razporejanje zaposlenih virov angažmajem ali projektom. Če želite omogočiti to funkcionalnost, dokončajte naslednja opravila ali potrdite, da so bila dokončana:

- Nastavite zaporedja številk.
- Nastavite poteke dela vodenja projektov in računovodstva.
- Omogočite poteke dela zahtev za vire.

Ko so prejšnja opravila dokončana, lahko izvedete naslednja opravila, kot je potrebno:

- Ustvarite zahtevo za vir iz začasno rezerviranega zaposlenega vira.
- Spremljajte zahteve za vire.
- Izpolnite zahteve za vire.
- Zahtevajte zaposleni vir iz SČD.
- Rezervirajte vire za projekt, ne da bi morali zahtevati zaposleni vir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]