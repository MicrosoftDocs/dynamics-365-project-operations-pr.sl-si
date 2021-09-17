---
title: Upravljanje podizvajalskih pogodb v aplikaciji Project Operations
description: V tem članku je predstavljen postopek upravljanja celovite podizvajalske pogodbe, in sicer v organizacijah, v katerih poslovanje poteka na podlagi projektov.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323616"
---
# <a name="subcontract-management-in-project-operations"></a>Upravljanje podizvajalskih pogodb v aplikaciji Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek prikazuje pregled postopka upravljanja celovite podizvajalske pogodbe v organizacijah, v katerih poslovanje poteka na podlagi projektov. Izdajanje podizvajalskih pogodb za storitve navadno sledi poteku poslovnega procesa, ki je prikazan v naslednjem diagramu.

![Potek procesa podizvajalskih pogodb](../media/SubcontractingProcessFlow.png)

Na naslednjem seznamu je postopek oddajanja naročil podizvajalcem opisan po korakih.

1. Vodja projekta sklene podizvajalsko pogodbo z dobaviteljem. Pri podizvajalski pogodbi se privzeto uporabljajo ceniki, ki so priloženi zapisu dobavitelja. Račun dobavitelja ima vrsto odnosa **Prodajalec** ali **Dobavitelj**.
2. Vodja projekta lahko vse nakupe v podizvajalski pogodbi razvrsti kot postavke izdelka. Podizvajalske pogodbe so lahko vezane na čas, stroške ali izdelke. Razred transakcije v vsaki podrobnosti podizvajalske pogodbe določa, čemu ta podrobnost služi.
3. Upravljavec računa dobavitelja in vodja projekta lahko ponovita podizvajalsko pogodbo. Cene v nabavnem ceniku, ki so priložene podizvajalski pogodbi, se lahko prilagodijo.
4. Če je podrobnost podizvajalske pogodbe namenjena za časovni vnos, upravitelj računa dobavitelja na tej točki ali pozneje stike dobavitelja poveže z vsako vrstico podizvajalske pogodbe. Ta povezava posreduje informacije vodji projekta, ki dela na podizvajalski pogodbi. Ko je stik dobavitelja povezan s podrobnostjo podizvajalske pogodbe, sistem iz stika samodejno ustvari vir, ki ga je mogoče rezervirati, če tak vir še ne obstaja.
5. Način obračunavanja na vsaki vrstici podizvajalske pogodbe je lahko **Fiksna cena** ali **Čas in material**. Za podrobnosti podizvajalske pogodbe s fiksno ceno je nastavljen razpored za izdajanje računov, ki temelji na mejnikih.
6.  Vse skupaj je potrjeno, ko je podizvajalska pogodba nastavljena, pogajanje pa zaključeno. Potrjenih podizvajalskih pogodb ni mogoče urejati, če pride do sprememb, pa je tovrstno pogodbo mogoče »ponovno odpreti za urejanje«, pri čemer se status **Potrjeno** spremeni nazaj v status **Osnutek**, in ponovno se odpre prostor za pogajanja. 
7.  Ko za projekt ustvarite generičnega člana ekipe, se lahko zgodi, da je član ekipe povezan s podrobnostjo podizvajalske pogodbe. To nakazuje na potrebo po oskrbi generičnega člana z zmogljivostjo podizvajalca.
8.  Poimenovane člane ekipe je mogoče ustvariti neposredno v sklopu projekta ali pa tako, da jih rezervirate s pomočjo izkušenj z razporejanjem virov. Če je poimenovani član projektne ekipe pogodbeni delavec, je mogoča povezava s podrobnostjo podizvajalske pogodbe. S tem bo zmanjšana razpoložljiva zmogljivost v podrobnosti pogodbe.
9.  Viri podizvajalcev lahko za projekte in projektne naloge beležijo čas, stroške in uporabljen material, nato pa vse skupaj pošljejo v odobritev. Podobno velja za zaposlene. Pri beleženju časa lahko pogodbeni delavec izbere določeno podizvajalsko pogodbo in podrobnost pogodbe.
10. Po odobritvi bodo s pomočjo časa, potrjenega s podizvajalskimi pogodbami, na podlagi nabavne cene pogodbenega delavca ali njegove vloge pri projektu zabeležene dejanske vrednosti projektnih stroškov.
11. Za delo, ki ga opravijo viri dobavitelja, ali izdelke, ki jih dobavi dobavitelj, se lahko v sistem zabeležijo računi dobaviteljev in vrstične postavke takih računov. Vrstične postavke dobaviteljev morajo ustrezati projektu in razredu transakcije za čas, stroške, izdelek/material, mejnik ali dajatev. Izbirno se lahko vrstice računov sklicujejo na podrobnosti podizvajalske pogodbe.
12. Sistem bo vse dejanske stroške, ki se ujemajo s podrobnostmi podizvajalske pogodbe, in projekt samodejno povezal z računom dobavitelja. To bo olajšalo postopek ujemanja na tri načine in postopek preverjanja.
13. Vodja projekta lahko nato pregleda dejanske podatke za projekt, ki so se med seboj samodejno povezali, ter odstrani ali doda druge dejanske vrednosti projektnih stroškov in konča postopek preverjanja.
14. Po končanem postopku preverjanja vseh vrstic bo račun dobavitelja dobil status **Pripravljeno za plačilo**. Na tej stopnji se lahko račun dobavitelja in vrstice prenesejo v računovodski sistem ali sistem dolgov in plačilo za dobavitelja bo obdelano. Predhodno zabeleženi stroški projekta bodo razveljavljeni, dejanski stroški iz vrstice računa dobavitelja pa zabeleženi k projektu.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Podrobnosti podizvajalske pogodbe, ki temeljijo na količini, in tiste, ki temeljijo na delu

Podrobnosti podizvajalske pogodbe lahko temeljijo na količini ali na delu. 

Če podrobnosti podizvajalske pogodbe **temeljijo na količini**, je lahko količina, ki je v podrobnostih podizvajalske pogodbe naročena za čas, stroške ali material, uporabljena za katerikoli projekt.

Če podrobnosti podizvajalske pogodbe **temeljijo na delu**, se preslikajo v delo, ki ga predstavlja vozlišče v načrtu projekta. Vrednost podrobnosti podizvajalske pogodbe sestavlja vsota vseh komponent, ki so potrebne, da je to delo opravljeno. Te so oblikovane kot podrobnosti vrstice podizvajalske pogodbe in lahko obsegajo zbirko za čas, stroške ali material. Podrobnosti podizvajalske pogodbe, ki temeljijo na delu, so prav tako namenjene enemu projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

