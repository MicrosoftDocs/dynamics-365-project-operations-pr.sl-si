---
title: Proces pretvorbe razporejanja projekta Project Service Automation v Project Operations
description: Ta članek ponuja pregled sprememb funkcij za Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642589"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces pretvorbe razporejanja projekta Project Service Automation v Project Operations

Ko je bil projekt uspešno nadgrajen iz Microsoft Dynamics 365 Project Service Automation 3.X do Dynamics 365 Project Operations Lite, urejanje projektnih nalog v strukturi razčlenitve dela (WBS) mreže opravil ni mogoče. Stranke bodo lahko pregledale WBS-je v mreži za sledenje, kjer so bila dodana nova polja za zagotavljanje vseh podrobnosti, povezanih z nalogo. Za projekte, pri katerih so potrebne spremembe v WBS, lahko selektivno pretvorite primerne projekte v nov projekt za izkušnjo spletnega razporejanja.

## <a name="project-conversion-process"></a>Postopek pretvorbe projekta

Če želite pretvoriti projekt, sledite tem korakom.

1. Odprite glavno stran projekta in izberite **Pretvorba** v podoknu dejanj.
1. V polju za potrditveno sporočilo izberite **v redu** za začetek pretvorbe projekta. Pojavijo se naslednja dejanja:

    1. Vrstica s sporočili, ki se prikaže na glavni strani projekta, navaja: »Urnik projekta se pretvarja. Projekta ne morete spreminjati, dokler pretvorba ni končana."
    1. Preusmerjeni ste na seznam projektov.

    Ko je pretvorba projekta končana, se zgodijo naslednja dejanja:

    1. Dodeljeni vodja projekta prejme obvestilo na desni strani aplikacije.
    1. Vrstica s sporočili, ki navaja, da pretvorba poteka, je odstranjena.
    1. The **Urnik** zavihek prikazuje novo izkušnjo razporejanja s Projectom za splet. Vsak uporabnik, ki ima ustrezne licence in varnostne vloge, lahko ureja WBS.
    1. The **Motor za razporejanje** polje je posodobljeno na **Projekt za splet**.
    1. The **Pretvorba** je odstranjen iz podokna dejanj.

> [!IMPORTANT]
> Množična pretvorba projektov ni dovoljena. Vsak poskus posodobitve velike količine projektov hkrati bo zadušen. Ta omejitev pomaga zagotoviti visoko zmogljivost za vse stranke.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ročna opravila v primerjavi s samodejnimi opravili

Ko je okolje nadgrajeno s Project Service Automation na Project Operations, se vse naloge v WBS štejejo za samodejno načrtovane. Koncept ročno načrtovanih opravil ni na voljo v Projectu za splet. Vendar pa lahko določite želeno vedenje razporejanja za svoje projekte z uporabo [način razporejanja](/project-management/scheduling-modes.md) nastavitev, ko ustvarjate nove projekte.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Omejene operacije za projekte pred pretvorbo

V tem razdelku so opisane funkcionalne razlike, ki jih lahko pričakujete, če projekti niso bili pretvorjeni.

### <a name="copy-project"></a>Kopiraj projekt

The **Kopirati** delovanje je podprto samo pri pretvorjenih projektih. Nadgrajenih projektov ni mogoče kopirati pred konverzijo.

### <a name="move-project"></a>Premakni projekt

Sprememba začetnega datuma projekta ne bo sorazmerno premaknila začetka opravil, razen če je bil projekt pretvorjen.

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kakšne so razlike med pretvorjenimi projekti in novimi projekti, ki so ustvarjeni po končani nadgradnji?

Za projekte, ki so pretvorjeni po nadgradnji okolja, bo nastavljena zastavica, ki urniku naroča, naj upošteva samo koledar projekta. To vedenje se ujema z vedenjem v storitvi Project Service Automation. Vendar pa zastavica ne bo nastavljena za nove projekte, ustvarjene po nadgradnji. Zato bo urnik upošteval delovne ure virov, ko so dodeljeni opravilu.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Kaj naj storim, če mojega projekta ni mogoče pretvoriti?

Če vašega projekta ni mogoče pretvoriti, je prvi korak, da pregledate dnevnike napak, da prepoznate morebitne pogoste težave, povezane z vašim WBS. Če dnevniki ne kažejo na določeno napako, glede katere bi lahko ukrepali, se obrnite na podporo za stranke, da bo vaš primer mogoče nadalje pregledati.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kako se v Projectu za splet obravnavajo zaprtja podjetij?

Project za splet ne upošteva zaprtja podjetij, ki jih podjetje definira na ravni organizacije. Vendar bo upošteval druge vrste prostih dni, ki so opredeljeni v dani predlogi delovnega časa.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kakšne so omejitve Projecta za splet?

glej [Ustvarite strukturo razčlenitve dela: Omejitve projekta](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Ali lahko pričakujem spremembe svojih ocen stroškov in prodaje?

V redkih primerih, ko so obrisi dodelitve virov ponovno izračunani ali kjer padejo na drugo datumsko mejo kot izvorni projekt, boste morda opazili razlike v ocenah prodaje in stroškov. Kot del procesa nadgradnje se od strank pričakuje, da preizkusijo reprezentativen vzorčni nabor projektov, tako da lahko razumejo morebitne spremembe urnika.
