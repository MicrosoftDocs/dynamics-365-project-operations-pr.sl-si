---
title: Ustvarjanje ročnega predračuna
description: Ta tema vsebuje informacije o ustvarjanju predračuna.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896141"
---
# <a name="create-a-manual-proforma-invoice"></a>Ustvarjanje ročnega predračuna

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Zaračunavanje vodjem projektov zagotavlja drugo stopnjo odobritve, preden ustvarijo račune za kupce. Prva stopnja odobritve se zaključi, ko so odobreni časovni vnosi in vnosi stroškov, ki jih predložijo člani projektne ekipe.

Storitev Dynamics 365 Project Operations ni zasnovana za ustvarjanje računov za stranke iz teh razlogov:

- Ne vsebuje davčnih podatkov.
- Ne more pretvoriti drugih valut v valuto računa z uporabo pravilno konfiguriranih menjalnih tečajev.
- Ne more pravilno oblikovati računov, tako da jih je mogoče natisniti.

Namesto tega lahko uporabite finančni ali računovodski sistem za ustvarjanje računov za stranke, ki uporablja informacije iz ustvarjenih predlogov računov.

## <a name="creating-project-invoices"></a>Ustvarjanje računov za projekt

Ustvarite lahko posamezne račune za projekt ali pa več računov hkrati. Ustvarite jih lahko ročno ali pa jih konfigurirate tako, da se ustvarijo samodejno.

### <a name="manually-create-project-invoices"></a>Ročno ustvarjanje računov za projekt 

Na strani s seznamom **Projektne pogodbe** lahko ustvarite račune za projekt ločeno za vsako projektno pogodbo ali pa množično ustvarite račune za več projektnih pogodb.

Če želite ustvariti račun za določeno projektno pogodbo, sledite spodnjemu koraku.

- Na strani s seznamom **Projektne pogodbe** odprite projektno pogodbo in nato izberite **Ustvari račun**.

    Račun se ustvari za vse transakcije za izbrano projektno pogodbo s stanjem **Pripravljeno za izdajanje računov**. Te transakcije vključujejo čas, stroške, mejnike in podrobnosti pogodbe, ki temeljijo na izdelku.

Za množično ustvarjanje računov sledite spodnjim korakom.

1. Na strani s seznamom **Projektne pogodbe** izberite eno ali več projektnih pogodb, za katere morate ustvariti račun, in nato izberite **Ustvari račune za projekt**.

    Opozorilo vas obvešča, da lahko pride do zamude pri ustvarjanju računov. Prikazan je tudi postopek.

2. Izberite **V redu**, da zaprete okno sporočila.

    Račun se ustvari za vse transakcije v podrobnostih pogodbe s stanjem **Pripravljeno za izdajanje računov**. Te transakcije vključujejo čas, stroške, mejnike in podrobnosti pogodbe, ki temeljijo na izdelku.

3. Če si želite ogledati ustvarjene račune, odprite **Prodaja** \> **Obračunavanje** \> **Računi**. Za vsako projektno pogodbo boste videli en račun.

### <a name="set-up-automated-creation-of-project-invoices"></a>Nastavitev avtomatiziranega ustvarjanja računov za projekt 

Če želite konfigurirati avtomatizirano izdajo računa, sledite spodnjim korakom.

1. Odprite **Nastavitve** \> **Paketna opravila**.
2. Ustvarite paketno opravilo in ga poimenujte **Ustvarjanje računov v storitvi Project Operations**. Ime paketnega opravila mora vključevati izraz »Ustvarjanje računov«.
3. V polju **Vrsta posla** izberite **Brez**. Možnosti **Pogostost: dnevno** in **Je aktivno** sta nastavljeni na **Da**.
4. Izberite **Zaženi potek dela**. V pogovornem oknu **Poišči zapis** vidite tri poteke dela:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Izberite **ProcessRunCaller** in nato **Dodaj**.
6. V naslednjem pogovornem oknu izberite **V redu**. Poteku dela **Spanje** sledi potek dela **Proces**.

    V 5. koraku lahko izberete tudi **ProcessRunner**. Ko nato izberete **V redu**, poteku dela **Proces** sledi potek dela **Spanje**.

Poteka dela **ProcessRunCaller** in **ProcessRunner** ustvarita račune. **ProcessRunCaller** prikliče **ProcessRunner**. **ProcessRunner** je potek dela, ki dejansko ustvari račune. Gre skozi vse vrstice pogodbe, za katere je treba ustvariti račune, in ustvari račune za te vrstice. Opravilo preveri datume izdaje računa za vrstice pogodbe, da ugotovi, za katere vrstice pogodbe je treba ustvariti račune. Če imajo vrstice pogodbe, ki pripadajo eni pogodbi, enak datum izdaje računa, se transakcije združijo v en račun, ki ima dve vrstici računa. Če ni transakcij, za katere bi se lahko ustvarili računi, opravilo preskoči ustvarjanje računa.

Ko se potek dela **processrunner** preneha izvajati, prikliče potek dela **ProcessRunCaller**, navede končni čas in se zapre. **ProcessRunCaller** nato zažene časovnik, ki se izvaja 24 ur od navedenega končnega časa. Ko se časovnik preneha izvajati, se **ProcessRunCaller** zapre.

Paketna obdelava za ustvarjanje računov je ponavljajoče se opravilo. Če se paketna obdelava zažene večkrat, se ustvari več primerkov opravila in pride do napak. Zato paketno obdelavo zaženite samo enkrat in jo znova zaženite le, če se preneha izvajati.

> [!NOTE]
> Paketno izdajanje računov se izvaja samo za podrobnosti pogodbe, ki so konfigurirane z razporedi izdajanja računov. V podrobnostih pogodbe z načinom obračunavanja s fiksno ceno morajo biti nastavljeni mejniki. V podrobnostih pogodbe z načinom obračunavanja za časovne in materialne transakcije je treba nastaviti datumski urnik računov. Enako velja v podrobnosti pogodbe za projekt.      
 
### <a name="edit-a-draft-invoice"></a>Urejanje osnutka računa

Ko ustvarite osnutek računa za projekt, se vse neobračunane prodajne transakcije, ki so bile ustvarjene, ko so bili odobreni časovni vnosi in vnosi stroškov, prenesejo v račun. Če je račun še vedno v fazi osnutka, lahko naredite naslednje te prilagoditve:

- Izbrišite ali uredite podrobnosti vrstice računa.
- Uredite in prilagodite količino in vrsto obračunavanja.
- Dodajte čas, stroške in provizije kot transakcije neposredno na račun. To funkcijo lahko uporabite, če je vrstica računa preslikana v vrstico pogodbe, ki podpira te razrede transakcij.

Izberite **Potrdi**, da potrdite račun. Dejanje »Potrdi« je enosmerno dejanje. Ko izberete **Potrdi**, sistem nastavi račun samo za branje in ustvari dejanske vrednosti obračunane prodaje iz vsake podrobnosti vrstice računa za vsako vrstico računa. Če se podrobnost vrstice računa sklicuje na neobračunano dejansko prodajo, sistem tudi stornira neobračunano dejansko prodajo. (Vsaka podrobnost vrstice računa, ki je bila ustvarjena iz časovnega vnosa ali vnosa stroškov, se bo sklicevala na neobračunano dejansko prodajo.) Sistemi za integracijo glavne knjige lahko to storniranje uporabijo za storno projektnega dela v teku (WIP) za računovodske namene.

### <a name="correct-a-confirmed-invoice"></a>Popravek potrjenega računa

Potrjene račune lahko uredite (popravite). Ko popravite potrjeni račun, se ustvari nov osnutek korekcijskega računa. Ker se predpostavlja, da želite stornirati vse transakcije in količine iz izvirnega računa, ta korektivni račun vključuje vse transakcije iz izvirnega računa, vse količine na njem pa imajo vrednost 0 (nič).

Če določene transakcije ne potrebujejo popravka, jih lahko odstranite iz osnutka korektivnega računa. Če želite stornirati ali vrniti le delno količino, lahko uredite polje **Količina** v podrobnosti vrstice. Če odprete podrobnost vrstice računa, si lahko ogledate količino na izvirnem računu. Nato lahko uredite količino na trenutnem računu, tako da je manjša ali večja od količine na izvirnem računu.

Ko potrdite korektivni račun, je prvotna obračunana dejanska prodaja stornirana in ustvari se nova obračunana dejanska prodaja. Če ste zmanjšali količino, se bo zaradi razlike ustvarila tudi nova neobračunana dejanska prodaja. Če je bila na primer prvotna obračunana prodaja za osem ur, v podrobnosti vrstice korekcijskega računa pa je količina zmanjšana na šest ur, se vrstica izvirne obračunane prodaje stornira in ustvarita se dve novi dejanski vrednosti:

- Obračunana dejanska prodaja za šest ur.
- Neobračunana dejanska prodaja za preostali dve uri. Ta transakcija je lahko obračunana pozneje ali označena kot transakcija, ki se ne zaračuna, odvisno od pogajanj s stranko.
