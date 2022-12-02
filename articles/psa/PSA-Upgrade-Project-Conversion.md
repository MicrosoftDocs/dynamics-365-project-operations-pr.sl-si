---
title: Proces pretvorbe načrtovanja projekta Project Service Automation v Project Operations
description: Ta članek ponuja pregled sprememb funkcij za Microsoft Dynamics 365 Project Service Automation v Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces pretvorbe načrtovanja projekta Project Service Automation v Project Operations

Ko je bil projekt uspešno nadgrajen iz Microsoft Dynamics 365 Project Service Automation 3.X v Dynamics 365 Project Operations Lite, urejanje projektnih opravil v mreži opravil »Strukturirana členitev dela (SČD)« ni mogoče. Stranke bodo lahko pregledale SČD-je v mreži za sledenje, kamor so bila dodana nova polja za zagotavljanje vseh podrobnosti, povezanih z opravilom. Za projekte, pri katerih so potrebne spremembe SČD, lahko selektivno pretvorite primerne projekte v novo izkušnjo načrtovanja Project for the web.

## <a name="project-conversion-process"></a>Postopek pretvorbe projekta

Za pretvorbo projekta sledite tem korakom.

1. Odprite glavno stran projekta in izberite **Pretvori** v podoknu za dejanja.
1. V polju za potrditveno sporočilo izberite **V redu**, da začnete pretvorbo projekta. Zgodijo se naslednja dejanja:

    1. Vrstica za sporočila, ki se prikaže na glavni strani projekta, navaja: »Razpored projekta se pretvarja. Projekta ne morete spreminjati, dokler ni pretvorba končana.«
    1. Preusmerjeni ste na seznam projektov.

    Ko je pretvorba projekta končana, se zgodijo naslednja dejanja:

    1. Dodeljeni vodja projektov prejme obvestilo na desni strani aplikacije.
    1. Vrstica za sporočila, ki navaja, da pretvorba poteka, je odstranjena.
    1. Zavihek **Razpored** prikazuje novo izkušnjo načrtovanja s storitvijo Project for the web. Vsak uporabnik, ki ima ustrezne licence in varnostne vloge, lahko ureja SČD.
    1. Polje **Mehanizem za načrtovanje** je posodobljeno na **Project for the web**.
    1. Gumb **Pretvori** je odstranjen iz podokna za dejanja.

> [!IMPORTANT]
> Množična pretvorba projektov ni dovoljena. Vsak poskus posodobitve velike količine projektov hkrati bo omejen. Ta omejitev pomaga zagotoviti visoko zmogljivost za vse stranke.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ročna opravila v primerjavi s samodejnimi opravili

Ko je okolje nadgrajeno iz Project Service Automation na Project Operations, se vsa opravila v SČD štejejo za samodejno načrtovana. Koncept ročno načrtovanih opravil ni na voljo v storitvi Project for the web. Vendar pa lahko določite želeno vedenje načrtovanja za svoje projekte z uporabo nastavitve [način načrtovanja](/project-management/scheduling-modes.md), ko ustvarjate nove projekte.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Omejeni postopki za projekte pred pretvorbo

V tem razdelku so opisane funkcionalne razlike, ki jih lahko pričakujete, če projekti niso bili pretvorjeni.

### <a name="copy-project"></a>Kopiranje projekta

Postopek **Kopiraj** je podprt samo pri pretvorjenih projektih. Nadgrajenih projektov ni mogoče kopirati pred pretvorbo.

### <a name="move-project"></a>Premikanje projekta

Sprememba začetnega datuma projekta ne bo sorazmerno premaknila začetka opravil, razen če je bil projekt pretvorjen.

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kakšne so razlike med pretvorjenimi projekti in novimi projekti, ki so ustvarjeni po končani nadgradnji?

Za projekte, ki so pretvorjeni po nadgradnji okolja, bo nastavljena zastavica, ki razporedu naroča, naj upošteva samo koledar projekta. To vedenje se ujema z vedenjem v storitvi Project Service Automation. Vendar pa zastavica ne bo nastavljena za nove projekte, ustvarjene po nadgradnji. Zato bo razpored upošteval delovne ure virov, ko so dodeljeni opravilu.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Kaj naj storim, če mojega projekta ni mogoče pretvoriti?

Če vašega projekta ni mogoče pretvoriti, je prvi korak, da pregledate dnevnike napak in prepoznate morebitne pogoste težave, povezane z vašo SČD. Če dnevniki ne kažejo na določeno napako, glede katere bi lahko ukrepali, se obrnite na podporo uporabnikom, da bo vaš primer mogoče nadalje pregledati.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kako se v storitvi Project for the web obravnavajo zaprtja podjetij?

Project for the web ne upošteva zaprtij podjetij, ki jih podjetje določa na ravni organizacije. Vendar bo upošteval druge vrste prostih dni, ki so opredeljeni v dani predlogi za delovne ure.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kakšne so omejitve storitve Project for the web?

Glejte [Ustvarjanje strukturirane členitve dela: omejitve projekta](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Ali lahko pričakujem spremembe svojih ocen stroškov in prodaje?

V redkih primerih, ko so krivulje dodelitve virov ponovno izračunane ali kjer padejo na drugo omejitev datuma kot izvorni projekt, boste morda opazili razlike v ocenah prodaje in stroškov. Kot del postopka nadgradnje se od strank pričakuje, da preskusijo reprezentativen vzorčni nabor projektov, da lahko razumejo morebitne spremembe razporeda.
