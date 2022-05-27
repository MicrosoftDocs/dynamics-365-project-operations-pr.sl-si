---
title: Rezervacije virov in njihova povezava z dodelitvami opravil
description: V tej temi so na voljo informacije o upravljanju poimenovanih virov, rezervacij virov in dodelitev opravil ter o tem, kako so povezani med sabo.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 953d7ca1995eae823fd29d0a9e85ff6a2a2eb59b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575508"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Rezervacije virov in njihova povezava z dodelitvami opravil

[!include [banner](../includes/psa-now-project-operations.md)]

Poimenovane vire je za projektno ekipo in dodeljena projektna opravila mogoče rezervirati na dva načina:

- Vir je mogoče neposredno rezervirati za projekt in ga nato dodeliti projektnim opravilom.
- Opravila je mogoče dodeliti splošnemu viru, ki se nato uporabi za iskanje splošnega vira in njegovo zamenjavo s poimenovanim virom. 

V obeh primerih se pri rezervaciji vira uporabi zmogljivost vira.

Vodja projekta, ki načrtuje projekt, je lastnik načrta projekta in razporeda. Z uporabo splošnega vira za dodelitev in nato ustvarjanjem zahteve za vir iz splošnega vira lahko vodja projekta rezervira vire za projekt z obrisi, določenimi v načrtu projekta. Rezervira lahko vire za projekt in jih nato dodeli opravilom, vendar pa obrisov rezervacij nikakor ne more uskladiti z obrisi opravil. Rezervacije ne vplivajo na urnik projekta.

Razmislite o zapletenem projektu z več prekrivajočimi se opravili, kjer mora več virov iste vrste delati hkrati. Če je viru dodan obris, ki se razlikuje od obrisa skupnih dodelitev vira, je opravila težko spremeniti tako, da bi ustrezala obrisu rezervacij za njihova ločena opravila in njihovim izvirnim obrisom.

V spodnjem primeru skupni obseg dela, ki ga zahteva isti vir in je sestavljen iz nabora štirih opravil, znaša 62 ur v obdobju dveh tednov in zanj obstaja poseben obris. Če je vir »Bob« rezerviran za 62 ur v istih dveh tednih, vendar z drugim obrisom, so zahteva in rezervacije usklajene.

| **Obrisi opravil**    | **Skupno število ur** | Pon 6/4 | Tor 6/5 | Sre 6/6 | Čet 6/7 | Pet 6/8 | Sob 6/9 | Ned 6/10 | Pon 6/11 | Tor 6/12 | Sre 6/13 | Čet 6/14 | Pet 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Opravilo 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Opravilo 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Opravilo 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Opravilo 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Vsote**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bobova razpoložljivost
| **Rezervacija vira** | **Skupno število ur** | Pon 6/4 | Tor 6/5 | Sre 6/6 | Čet 6/7 | Pet 6/8 | Sob 6/9 | Ned 6/10 | Pon 6/11 | Tor 6/12 | Sre 6/13 | Čet 6/14 | Pet 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Vendar pa ne obstaja sistematični način dodeljevanja obrisa rezerviranih ur opravilom za vsak dan posebej. Če je vodja projekta pripravljen spremeniti načrt projekta in se seznaniti z razpoložljivostjo vira, bo moral odstraniti dodelitev in pregledati vsa opravila, da se bodo ujemala z obrisi rezervacij.

V primeru, kjer je organizacija opravilo načrtovanja projekta dodelila tako vodji projekta kot tudi upravitelju virov, vodja projekta določi načrtovanje, ki vključuje obrisovanje zahtevanega dela. Upravitelju virov bi moral biti onemogočen vpliv na načrtovanje brez vednosti vodje projekta, kar vključuje spreminjanje krivulje obsega dela pri rezervaciji pravih virov. Če upravitelj virov ne izpolnjuje tistega, kar je od njega zahteval vodja projektov, se morata skupaj dogovoriti, kaj je treba spremeniti pri načrtovanju projekta.

Ker rezervacije in dodelitve niso tesno povezane, je mogoče rezervirati obrise, ki se razlikujejo od obrisov opravil, ali spremeniti dodelitve v okoliščine, kjer rezervacije in dodelitve niso usklajene.

**Pogled za usklajevanje** vodji projekta omogoča pregled nad rezervacijami in dodelitvami za vsakega člana projektne ekipe. V pogledu se lahko uporabijo barve in senčenje, s čimer je mogoče prikazati neujemanje med rezervacijami in dodelitvami članov ekipe. Na podlagi teh podatkov lahko vodja projekta ustrezno ukrepa – lahko razširi rezervacije virov v primerih, kjer obstajajo dodelitve in ni rezervacij, ali prekliče rezervacije, kjer so viri rezervirani, vendar nimajo dodelitev.

> [!NOTE]
> Če premaknete opravilo, ki ste ga sami obrisali, se ti obrisi ne ohranijo. Obrisi se znova ustvarijo v skladu s koledarjem projekta in se tako prilagodijo spremembam, kot so delovne ure in prazniki. Storitev je tako zasnovana, saj sistem ne pozna namena izvirnega obrisa in ne more ugotoviti, ali je smiselno obdržati ta obris v novem časovnem obdobju. Ker povezava med rezervacijami in dodelitvami ni vzpostavljena, rezervacije ohranijo izvirne obrise rezervacij. V tem primeru boste morali razveljaviti obris dodelitve in znova rezervirati novega.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
