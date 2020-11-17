---
title: Preoblikovana poročila o stroških
description: Ta tema vsebuje informacije o preoblikovani in na novo zamišljeni izkušnji za vnos poročila o stroških v storitvi Microsoft Dynamics 365 Finance. Nova izkušnja poenostavi postopek izpolnitve poročil o stroških in skrajša potreben čas.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ec8737d848ae5ad25219a43c68306d19b1c1fbce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084799"
---
# <a name="redesigned-expense-reports"></a>Preoblikovana poročila o stroških
[!include[banner](../includes/banner.md)]

Vnos poročila o stroških je bil preoblikovan v želji po poenostavitvi postopka izpolnitve poročil o stroških in skrajšanja potrebnega časa. Tukaj so naštete glavne komponente nove izkušnje vnašanja stroškov:

- Nov delovni prostor za upravljanje stroškov, ki vam omogoča dostop do stroškov vašega pooblaščenca.
- Nova izkušnja z ujemanjem potrdil za boljši prikaz potrdil na ravni glave in poenostavitev postopka prilaganja potrdil na vrstice stroškov.
- Nova mreža samo za branje, ki omogoča ogled številnih dodatnih vrstic stroškov in dodatnih stolpcev s podatki. Zdaj lahko vidite vse razčlenjene in razdeljene vrstice skupaj s pripadajočimi nadrejenimi stroški.
- Poenostavljeno podokno za urejanje stroškov.
- Preoblikovana sporočila za napake, opozorila in pravilnike za zagotavljanje pravega konteksta in lažjega razumevanja ter odpravljanja težav. Microsoft je odstranil številna sporočila, ki so se pojavila, preden so uporabniki imeli priložnost dokončati svoje naloge in odpraviti težave, kot je sporočilo o nepopolnem razčlenjevanju.
- Nova stran, ki določa, katera polja zahteva vaša organizacija, katera polja so izbirna in katerih polj ne smete zajemati. Vpeljava te strani pomaga zmanjšati število polj, ki jih morajo uporabniki nastaviti.
- Prenovljen videz poročil o stroških, ki ne daje pustega računovodskega vtisa.

Če želite vklopiti novo izkušnjo, uporabite delovni prostor **Upravljanje funkcij** za vklop funkcije **Prenovljena poročila o stroških**. Ob vklopu funkcije se zgodijo naslednja dejanja:

- Obstoječi delovni prostor upravljanja stroškov se nadomesti z novim delovnim prostorom.
- Dodana je nova postavka menija za vidljivost polja stroška.
- Ne odstrani se nobenih obstoječih postavk menija za poročila o stroških (obstoječa stran) ali polj za poročila o stroških.
- Poteki dela in morebitne odobritve vas še vedno vodijo na obstoječo stran s poročili o stroških.

## <a name="getting-started-video-for-new-users"></a>Uvodni videoposnetek za nove uporabnike

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Videoposnetek (prikazan zgoraj) [izkušnje upravljanja s stroški v aplikaciji Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) je vključen na seznam predvajanja v aplikaciji [Finance and Operations ](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) , ki je na voljo na portalu YouTube.

## <a name="new-features"></a>Nove funkcije

| Nova funkcija | Opis |
|---|----|
| Vidljivost polja za strošek | Nova stran za nastavitve omogoča, da določite, katera polja je treba onemogočiti za posamezno organizacijo, katera polja naj bodo zahtevana in katera so priporočljiva. |
| Zahtevana polja | Nova preprosta konfiguracija omogoča, da nastavite zahtevana polja, ne da bi morali uporabljati okvir pravilnika. |
| Izbirna polja | Dodana je še ena stran za izbirna polja. Tako se zaposleni ne bodo počutili, kot da bi morali določiti polja, vendar pa so ta še vedno lahko dostopna. |
| Dodajanje nepovezanih potrdil | Možnost dodajanja nepovezanih potrdil v poročilo o stroških izboljša vidljivost v delovnem prostoru in poročilu o stroških. |
| Izboljšano sporočanje | Boljši vpogled v vrstice stroškov, ki vsebujejo opozorila ali napake. |
| Zmanjšanje števila sporočil v vrstici za sporočila| Število sporočil dnevnika podatkov je zmanjšano, še posebej v več primerih podvajanja sporočil. |
| Združevanje pogostih dejanj | Vmesnik je poenostavljen z dodatkom novega gumba za večino pogostih dejanj na ravni vrstice in dodatkom gumba s tropičjem (...) za glavo in druga manj pogosta dejanja. |
| Nov delovni prostor za večjo vidljivost | Nov delovni prostor združuje funkcije in povezave, ki uporabnikom omogočajo premik na različna območja. |
| Dodajanje obstoječih stroškov in potrdil med ustvarjanjem stroškov | Ko ustvarjate poročila o stroških, lahko dodate vse oz. izbrane stroške in potrdila. |
| Kalkulator menjalnega tečaja | Dodan je kalkulator menjalnega tečaja, ki omogoča izračun menjalnega tečaja za večvalutne gotovinske transakcije. |
| Shranjevanje in dodajanje novih vrstic stroškov | Pri vnosu novih stroškov sta na voljo gumba za možnosti **Shrani** in **Novo** za pomoč pri hitrem vnosu vrstic stroškov. |
| Boljši vpogled v razdeljene in razčlenjene vrstice | Razčlenjene in razdeljene vrstice so za dodatno vidljivost dodane neposredno na seznam stroškov, kar vam pomaga opaziti morebitne napake v pravilniku ali druge napake. |
| Prikaz potrdil med razčlenjevanjem | Med razčlenjevanjem je mogoč prikaz potrdil. |

Začetna izdaja je osredotočena na primere vnosa stroškov. Vsak pregled poročila o stroških ali primer odobritve bo še naprej uporabljal obstoječo stran za vnos stroškov.

Naslednje funkcije so prisotne na obstoječi strani, na novi pa še ne. Te funkcije bodo znova vključene v prihajajočih različicah:

- Odobritve
- Odobritve obveznosti in zmožnost urejanja računovodstva
- Več vstopnih točk
- Integracija zahtev za pot
- Podatkovna entiteta za vidljivost polja stroškov
- Vnos dnevnic
- Potek dela na ravni vrstice
- Začasna podpora odobritelja
- Napredno razčlenjevanje