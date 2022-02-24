---
title: Izdaja računa za honorar ali predujem
description: Ta tema vsebuje informacije o izdajanju računov za honorar ali predujem v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596212"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Izdaja računa za honorar ali predplačilo

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations podpira pogodbe za honorar in enkratna predplačila. Pri projektni pogodbi lahko zabeležite razpored honorarjev ali enkratnih predujmov. Vendar beleženje na ravni projektne pogodbe ne omogoči, da bi bil honorar ali predujem takoj na voljo za uporabo. Če želite uporabiti honorar ali predujem na računu, s katerim stranki dejansko zaračunate, morate račun za honorar ali predujem najprej izstaviti.

Za izdajo računa za honorar ali predujem, naredite naslednje.

1. Izberite **Prodaja** > **Obračunavanje** > **Honorarji in predujmi**. 
2. Na strani **Predujmi in honorarji** s filtrom izberite določeni honorar ali predujem, za katerega želite izdati račun, in ga označite kot **Pripravljeno za izdajanje računa**.
3. Ustvarite račun bodisi ročno s seznama **Projektna pogodba** ali strani s podrobnostmi. Honorar ali predujem je prikazan na osnutku računa v razdelku **Predujmi in honorarji** na strani **Račun**.
4. Potrdite račun. S tem boste honorar ali predujem dali na voljo za uporabo. Račun lahko preverite na strani s seznamom **Honorarji in predujmi**. Za fakturirani predujem ali honorar se razpoložljivi znesek prikaže v mreži.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Ustvarjanje honorarja ali predujma iz mreže računa

Honorar ali predujem lahko ustvarite neposredno na računu.

1. Na osnutku računa in nato na podmreži **Predujmi in honorarji** izberite **Novo**, da ustvarite nov honorar ali predujem. 
2. Na strani **Hitro ustvarjanje** dodajte potrebne informacije in nato izberite **Shrani**. Honorar ali predujem se ustvari na projektni pogodbi, povezani z računom. Honorar ali predujem se samodejno označi kot **Pripravljeno za izdajanje računa** in nato doda na podmrežo **Predujmi in honorarji** na strani **Račun**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Uskladitev fakturiranega honorarja ali predujma

Ko je honorar ali predujem fakturiran, ga je mogoče uporabiti ali uskladiti na računu s časom, stroški, mejniki ali drugimi stroški na podlagi projekta. Stranki se bo znesek računa zmanjšal za znesek honorarja ali predujma, uporabljenega na tem računu.

Pri vsakem računu, ki se ustvari za projektno pogodbo, v kateri so fakturirani honorarji ali predujmi, aplikacija Project Operation samodejno doda honorar ali predujem na račun.

To je razvidno iz mreže **Uporabljeni honorarji in predujmi** na strani **Račun**. Naslednja tabela vsebuje informacije o poljih na mreži **Uporabljeni honorarji in predujmi** na strani **Račun projekta**.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Opis | Mreža **Uporabljeni predujmi in honorarji** na strani **Račun projekta** |To polje, ki je na voljo samo za branje, vsebuje opis honorarja ali predujma, uporabljenega na tem računu. Te vrednosti ni mogoče spremeniti na računu. To vrednost lahko posodobite v podmreži na strani **Projektna pogodba**. | To polje se lahko stranki prikaže na natisnjenem računu, da jo seznani s tem, kateri honorar ali predujem je uporabljen na računu. |
| Dostavljeno: | Mreža **Uporabljeni predujmi in honorarji** na strani **Račun projekta**  | To polje, ki je na voljo samo za branje, vsebuje datum računa za honorar ali predujem, uporabljen na tem računu. Te vrednosti ni mogoče spremeniti na računu. To vrednost lahko posodobite v podmreži na strani **Projektna pogodba**. | To polje se lahko stranki prikaže na natisnjenem računu za označitev datuma, ko je bil honorar ali predujem prvič zaračunan stranki. |
| Znesek | Mreža **Uporabljeni predujmi in honorarji** na strani **Račun projekta**  | To polje, ki je na voljo samo za branje, vsebuje višino honorarja ali predujma, uporabljenega na tem računu. Te vrednosti ni mogoče spremeniti na računu. To vrednost lahko posodobite v podmreži na strani **Projektna pogodba**. | To polje se lahko stranki prikaže na natisnjenem računu, da jo seznani s prvotno višino honorarja ali predujma, ki ga je plačala stranka. |
| Uporabljen znesek | Mreža **Uporabljeni predujmi in honorarji** na strani **Račun projekta**  | To polje, ki je na voljo samo za branje, vsebuje izračunano vrednost, ki povzema, koliko honorarja ali predujma je bilo porabljenega. | To polje se lahko stranki prikaže na natisnjenem računu, da jo seznani z višino honorarja ali predujma, ki je bil že uporabljen. |
| Skupna vrednost postavk na računu | Mreža **Uporabljeni predujmi in honorarji** na strani **Račun projekta**  | To polje, ki ga je mogoče urediti, vsebuje višino honorarja ali predujma, ki se uporablja za ta račun projekta. Ta znesek ne sme biti večji od tistega, ki je na voljo s predujmom. Sistem samodejno izračuna to vrednost kot razliko med poljema **Znesek** in **Uporabljeni znesek** na mreži. Ta znesek lahko zmanjšate tako, da porabite manj, kot je na voljo, ne morete pa povečati zneska, da porabite več, kot je na voljo. | To polje se lahko stranki prikaže na natisnjenem računu, da jo seznani z višino honorarja ali predujma, ki je uporabljen na računu. |
| Znesek salda honorarja. | Mreža **Uporabljeni predujmi in honorarji** na strani **Račun projekta**  | V tem polju, ki je na voljo samo za branje, je navedena vrednost honorarja ali predujma, ki bo ostala po potrditvi računa. | To polje se lahko stranki prikaže na natisnjenem računu, da jo seznani z višino honorarja ali predujma, ki bo ostala po potrditvi in plačilu računa. |
