---
title: Beleženje uporabe materiala v projektih in projektnih nalogah
description: Ta tema ponuja informacije o tem, kako beležiti uporabo materiala glede na projekte in opravila projekta.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c739d7fabb96a845eaf139fcc9eab21247b0860
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001581"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Beleženje uporabe materiala v projektih in projektnih nalogah

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Projektna ekipa porabi ali uporabi materiale, ko izvaja opravila projekta. Dnevnik uporabe materiala omogoča zapisovanje uporabe, tako da jo lahko odobri vodja projekta in jo stranki sčasoma zaračuna. 

Če želite zapisati uporabo materialov iz kataloga ali materialov, ki jih ni v katalogu, in to predložiti odobritelju, sledite tem korakom: 

1. V podoknu za krmarjenje izberite možnost **Uporaba materiala** in nato **Novo**.
2. Na strani **Nova uporaba materiala**, vnesite zahtevane podatke o uporabi materiala in izberite možnost **Shrani**.

Naslednja tabela vsebuje informacije o poljih na strani **Dnevnik uporabe materiala**. 

| **Polje** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Opis | Opis določene uporabe materiala. | To polje nima nadaljnjega vpliva. |
| Datum | Datum, ko naj bi se material uporabil. | To polje nima nadaljnjega vpliva. |
| Project | Seznam aktivnih projektov. | Izbira projekta za dnevnik uporabe materiala vpliva na polje **Opravilo** tako, da se prikažejo samo tista opravila, ki so v projektu. |
| Opravilo | Seznam opravil za projekt, vključno z opravili povzetka in listnega vozlišča. | Izbira opravila za dnevnik uporabe materiala vpliva na dejanske stroške materiala in dejansko prodajo materiala za opravilo. Če je to polje prazno, se ustrezni stroški uporabe materiala in prodaja spremljajo in povzemajo samo na ravni projekta. |
| Izbira izdelka | Določite, ali je ta uporaba materiala predvidena za **obstoječ** izdelek (iz kataloga) ali izdelek, **ki ni v katalogu**. | To polje določa vrsto izdelka. |
| Izdelku | ID izdelka iz kataloga izdelkov. Ko izberete ID izdelka, se polje **Izbira izdelka** samodejno posodobi na **obstoječ izdelek**. ID se uporablja za iskanje cen stroškov in prodaje iz cenika. | To polje nima nadaljnjega vpliva. |
| Opis izdelka, ki ni v katalogu | Besedilno polje za zapis imena izdelka. To polje je na voljo le, če izberete **Izdelek, ki ni v katalogu** v polju **Izberite izdelek**.| To polje nima nadaljnjega vpliva. |
| Vir, ki ga je mogoče rezervirati| Vir, ki je za projekt uporabil to gradivo. Privzeta vrednost za to polje je vir vpisanega uporabnika, ki ga je mogoče rezervirati, vendar ga lahko spremenite tako, da bo zapisoval uporabo v imenu drugih članov projektne ekipe. | To polje nima nadaljnjega vpliva. |
| Skupina enot | Privzeta vrednost v tem polju prihaja iz skupine enot, ki je za katalog izdelkov nastavljena kot privzeta. Če želite izbrati drugo skupino enot, lahko to polje posodobite. | To polje nima nadaljnjega vpliva. |
| Enota | Privzeta vrednost v tem polju je privzeta enota izbranega izdelka. Če želite izbrati drugo enoto, lahko to polje posodobite. | Sprememba enote povzroči drugačno privzeto ceno in stroške enote. |
| Količina | Količina izdelka, ki je bila uporabljena pri projektu ali projektnem opravilu. | To polje nima nadaljnjega vpliva. |
| Strošek na enoto | Cena na enoto za izbrani izdelek in kombinacijo enot, kot je določena v veljavnem ceniku z lastnimi cenami. | Cena na enoto je vedno prikazana v valuti cene projekta. Če v ceniku ni stroškov na enoto za kombinacijo izdelka in enote, bodo stroški na enoto privzeto 0,00. |
| Skupna cena | Cena, ki se izračuna kot količina \* cena na enoto.| Cena je vedno prikazana v valuti cene projekta. |


## <a name="submit-material-usage-for-review-and-approval"></a>Predložitev uporabe materiala v pregled in odobritev 
Ko zajamete vso uporabo materiala in ste pripravljeni na odobritev, morate podatke o uporabi predložiti v pregled.

1. Pojdite v **Dnevnik uporabe materiala** in izberite enega ali več vnosov. Ali pa s potrditvenim poljem v glavi izberite vse zapise o uporabi materiala.
2. Izberite **Pošlji**. Sistem obdela izbrane vnose in nato ustvari zahteve za odobritev uporabe materiala.

## <a name="recall-a-material-usage-log"></a>Preklic dnevnika uporabe materiala

Po potrebi lahko prekličete predložen uporabljeni material. Čas, potreben za preklic vnosa uporabe materiala, je odvisen od stopnje odobritve.  Če odobritelj še ni odobril vnosa, se lahko preklic izvede takoj. Če pa je vnos že odobren, se od odobritelja zahteva odobritev preklica in razveljavitev transakcij.

1. Pojdite v možnost **Uporaba materiala** in na seznamu dnevnikov uporabe materiala izberite uporabo materiala, ki jo želite preklicati.
2. Izberite **Prekliči**. Če vnos uporabe materiala še ni odobren, ga sistem takoj prekliče. Če je bil vnos materiala že odobren, se ustvari zahteva za preklic, ki odobritelja obvesti, da želite preklicati uporabo materiala. Odobritelj bo nato potrdil, ali je razveljavitev mogoča, in vnos bo vrnjen.

## <a name="delete-a-material-usage-log"></a>Brisanje dnevnika uporabe materiala

Dnevnike uporabe materiala, ki niso bili poslani, lahko izbrišete. Če želite izbrisati že oddani dnevnik uporabe materiala, ga morate najprej preklicati.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
