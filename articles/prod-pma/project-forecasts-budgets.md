---
title: Napovedi projektov in proračuni
description: Microsoft Dynamics 365 Finance zagotavlja napovedi projektov in proračune projektov za upravljanje in nadzor vaših projektov.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47ea4c49a76a2bb0a1855fce2e9a874b4044e429d963c08392ec0ab471f89329
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988086"
---
# <a name="project-forecasts-and-budgets"></a>Napovedi projektov in proračuni

[!include [banner](../includes/banner.md)]

Obstajata dva načina za upravljanje in nadzor vaših projektov: napovedi projektov in proračuni projektov. 

Uporabite projektno napovedovanje, če ima vaša organizacija operativno perspektivo in se osredotoča na prihodke in stroške, ki izhajajo iz določenih transakcij. Uporabite načrtovanje proračuna za projekte, če se vaša organizacija bolj osredotoča na finančne zneske. 

Tako napovedi projektov kot proračuni projektov uporabljajo modele napovedi za zadrževanje predvidenih zneskov transakcij. 

Vsaka metoda ima svoje prednosti. Pred izbiro metode za svojo organizacijo upoštevajte naslednje točke.

|   Način dodelitve       |           Projektno napovedovanje            |        Načrtovanje proračuna za projekte                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Dodelitev obdobja**     | Transakcij ne morete izrecno dodeliti znotraj proračunskega obdobja. Namesto tega napoved in nadzor napovedi temeljita na življenjski dobi projekta. Ker napovedi temeljijo na določenem datumu, morate zanemariti obdobje od izbranega datuma naprej. | Transakcij ne morete dodeliti znotraj celotnega trajanja projekta ali proračunskega obdobja. Če jih dodelite v določenem obdobju, lahko neuporabljene zneske prenesete v naslednje proračunsko obdobje. |
| **Ogled transakcij**  | Transakcije si lahko ogledate v obrazcih za napovedi, kjer vidite napovedi za celotno podjetje in za vse projekte, ne glede na hierarhijo. Če se želite osredotočiti na določen projekt, morate filtrirati podatke.                                       | Ogledate si lahko načrtovane transakcije za eno hierarhijo projekta. To pomeni, da si lahko ogledate podrobnosti o transakcijah za nadrejeni projekt ali njegove podprojekte.                 |
| **Transakcijske spremenljivke** | Ko vnesete napovedane transakcije, lahko uporabite vse atribute, ki obstajajo za dejansko transakcijo. To omogoča vnos več podrobnosti v napoved. Vnesete lahko na primer podrobnosti o količinah, delavcih, izdelkih ali lastnostih vrstic.         | Pri vnosu podrobnosti proračuna lahko uporabite samo zneske, kategorije in dejavnosti.                    |
| **Varnost**              | Napovedovanje temelji na transakcijah, ki jih vnesete v obrazce za napovedi, in ne vključuje mehanizma za nadzor procesa. Vsak delavec, ki ima dovoljenja za obrazec za napoved, lahko popravi informacije brez predhodne odobritve.                                        | Načrtovanje proračuna uporablja sistem poteka dela, ki omogoča upravljanje sprememb in hrambo zgodovine sprememb.         |
| **Vrste vnosov**           | Vnosi napovedanih transakcij temeljijo na številu enot ter stroških in cenah prodajnih enot.  | Podrobnosti proračuna temeljijo na zneskih, ki so razdeljeni med stroške in prihodke.                                          |
| **Modeli napovedi**       | Ker mora biti vsaka napoved povezana z modelom, lahko ustvarite več modelov napovedi in nastavite tudi podmodele.           | Načrtovanje proračuna projekta omejuje modele napovedi, ki se uporabljajo za načrtovanje proračuna. Manj modelov napovedi lahko pripomore k večji doslednosti napovedi.                           |
| **Prekoračitev stroškov**         | Vnos transakcij, ki bodo povzročile prekoračitev stroškov, lahko samo odobrite ali zavrnete.   | Načrtovanje proračuna projekta uporabnikom zagotavlja dodatne možnosti nadzora. Omogočite lahko opozorila in prekoračitve.                    |
| **Kontrolnik**               | Nadzor napovedi se izvaja s funkcijo za zmanjšanje napovedi. Dejanski zneski se odštejejo od stanja napovedanih transakcij brez spremljanja sprememb. Zaradi tega je težje ugotoviti, kje so se dejansko izvedle transakcije.                   | V orodju za spremljanje proračuna projekta se dejanski zneski odštejejo od zneskov v preostalem proračunu. To omogoča jasnejšo sled za spremljanje sprememb.                                   |

## <a name="project-forecasts"></a>Projektne napovedi
Ko uporabljate projektno napovedovanje, lahko napovedi transakcij vnesete v obrazce za napovedi za vsako vrsto transakcije. Vsak atribut, ki je na voljo za dejansko transakcijo, je mogoče uporabiti za napovedano transakcijo – na primer donosnost vrstic, atribute vrstic, delavce ali opise. Lahko tudi napoveste, kako dolgo po nastalem strošku boste stranki izdali račun. 

Napovedane transakcije projektov temeljijo na enotah in zneskih. 

Vsako projektno napoved morate povezati z modelom napovedi. Ko vnesete napovedano transakcijo, se samodejno predlaga model napovedi. Model napovedi deluje kot vsebnik za napovedane transakcije. 

Modele napovedi lahko določite kot podmodele za model. To vam omogoča izdelavo napovedi glede na regijo, časovno obdobje ali oddelek. Napovedane transakcije lahko kopirate v model, da ustvarite nov model, transakcije pa lahko prenesete tudi v glavno knjigo. Ker sta napoved in model v enakovrednem razmerju, vsak model napovedi velja kot ločen proračun za projekt. 

Modeli napovedi lahko uporabijo funkcijo za zmanjšanje napovedi kot nadzorni mehanizem projektov. Pri zmanjšanju napovedi dejanske transakcije zmanjšajo stanje napovedanih transakcij. Ker pa se zmanjšanje napovedi uporablja za najvišje projekte v hierarhiji, nudi le omejen ogled sprememb v napovedi. Če je delavec na primer povezan s podprojektom, se dejanske transakcije za delavca vknjižijo v nadrejeni projekt. To lahko oteži sledenje spremembam, ker ne morete zlahka ugotoviti, katera transakcija v katerem podprojektu je povzročila zmanjšanje napovedanega zneska. Zato je dobro ustvariti kopijo modela napovedi za zmanjšanje napovedi, ki ga boste uporabili. Nato lahko v poročilih pogledate, kaj je bilo sprva napovedano. 

Napovedi projektov lahko popravite, kopirate, izbrišete ali prenesete v proračun glavne knjige. Nadzora nad temi procesi pa ni. Vsak delavec, ki ima dovoljenje za obrazec za napoved, lahko vnese popravke brez predhodnega pregleda.

-   **Popravljanje** – napovedano transakcijo lahko popravite v istih obrazcih, kjer so bili prvotni vnosi.
-   **Kopirajte ali brisanje** – pri kopiranju napovedanih transakcij kopirate vrstice transakcij enega modela napovedi v drug model napovedi. Ko izbrišete napoved, izbrišete napovedane transakcije iz modela napovedi. Če želite omejiti napovedane transakcije, ki se kopirajo ali brišejo, izberite točno določene vrste transakcij in datume. Tako lahko kopirate ali izbrišete samo določene dele napovedi.
-   **Prenos** – ko prenesete projektno napoved v proračun glavne knjige, prenesete napovedane transakcije modela napovedi v proračun glavne knjige. Vse predhodno prenesene transakcije lahko prepišete v proračunu glavne knjige, v katero prenesete projektno napoved.

## <a name="project-budgets"></a>Proračuni projektov
Načrtovanje proračuna projekta je enostavnejša metoda od napovedovanja, čeprav vključuje modele napovedi. Ta funkcija uporablja en obrazec za vnos podrobnosti in popravkov prvotnega proračuna ter omogoča izdelavo napovedi, ki temeljijo samo na znesku, kategoriji ali dejavnosti. 

Pri načrtovanju proračuna za projekte je treba vse prvotne proračune in popravke poslati v odobritev v potek dela projekta. Poteki dela vam omogočajo večji nadzor nad postopkom in ustvarijo zgodovino sprememb zapisov. 

Načrtovanje proračuna za projekte je podobno načrtovanju proračuna za glavno knjigo, le da je njegova nastavitev enostavnejša in hitrejša. Številnih možnosti pri načrtovanju proračuna za glavno knjigo, kot so zaporedja številk ali valuta, ni treba ločeno nastaviti za projekte.

Proračuni projektov so samodejno povezani z dvema modeloma napovedi, enim za prvotni proračun in drugim za preostanek proračuna. Zato lahko poročila, ki temeljijo na modelih napovedi, uporabljajo podatke proračuna. Ko je proračun projekta določen, sistem ustvari napovedane transakcije na podlagi povezanih modelov, ki se uporabljajo za poročanje in nadzor.

## <a name="forecast-models"></a>Modeli napovedi
Modeli napovedi imajo enoslojno hierarhijo. To pomeni, da mora biti ena projektna napoved povezana z enim modelom napovedi.

Če uporabljate napovedovanje projektov, lahko modele opredelite kot podmodele. Nato lahko izdelate napovedi glede na oddelek, časovno obdobje ali regijo. Tako lahko na primer ustvarite model napovedi za posamezno leto in ustvarite podmodele za regionalne napovedi za severovzhod, jugovzhod, severozahod in jugozahod, ki jih predložijo regionalni vodje. Z izbiro različnih možnosti v razpoložljivih poročilih si lahko ogledate informacije po skupnih napovedih ali podmodelih.





[!INCLUDE[footer-include](../includes/footer-banner.md)]