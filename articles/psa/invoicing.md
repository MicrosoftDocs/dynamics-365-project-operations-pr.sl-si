---
title: Zaračunavanje v storitvi Project Service Automation
description: Ta tema vsebuje informacije o zaračunavanju.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e0dc911bb0ca72af547262a5716ef1091ea81c81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015081"
---
# <a name="invoicing-in-project-service-automation"></a>Zaračunavanje v storitvi Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Zaračunavanje v storitvi Dynamics 365 Project Service Automation je uporabno, ker vodjem projektov zagotavlja drugo stopnjo odobritve, preden ustvarijo račune za kupce. Prva stopnja odobritve se zaključi, ko so odobreni časovni vnosi in vnosi stroškov, ki jih predložijo člani projektne ekipe.

Storitev PSA ni zasnovana za ustvarjanje računov za stranke iz teh razlogov:

- Ne vsebuje davčnih podatkov.
- Ne more pretvoriti drugih valut v valuto računa z uporabo pravilno konfiguriranih menjalnih tečajev.
- Ne more pravilno oblikovati računov, tako da jih je mogoče natisniti.

Namesto tega lahko uporabite finančni ali računovodski sistem za ustvarjanje računov za stranke, ki uporablja informacije iz predlogov računov, ustvarjenih v PSA.

## <a name="creating-project-invoices-in-psa"></a>Ustvarjanje računov za projekt v PSA

Ustvarite lahko posamezne račune za projekt ali pa več računov hkrati. Ustvarite jih lahko ročno ali pa jih konfigurirate tako, da se ustvarijo samodejno.

### <a name="manually-create-project-invoices-in-psa"></a>Ročno ustvarjanje računov za projekt v PSA

Na strani s seznamom **Projektne pogodbe** lahko ustvarite račune za projekt ločeno za vsako projektno pogodbo ali pa množično ustvarite račune za več projektnih pogodb.

Če želite ustvariti račun za določeno projektno pogodbo, sledite spodnjemu koraku.

- Na strani s seznamom **Projektne pogodbe** odprite projektno pogodbo in nato izberite **Ustvari račun**.

    ![Ustvarjanje računov za projekt za določeno projektno pogodbo](media/CreateProjectInvoicesOneByOne.png)

    Račun se ustvari za vse transakcije za izbrano projektno pogodbo s stanjem **Pripravljeno za izdajanje računov**. Te transakcije vključujejo čas, stroške, mejnike in podrobnosti pogodbe, ki temeljijo na izdelku.

Za množično ustvarjanje računov sledite spodnjim korakom.

1. Na strani s seznamom **Projektne pogodbe** izberite eno ali več projektnih pogodb, za katere morate ustvariti račun, in nato izberite **Ustvari račune za projekt**.

    ![Množično ustvarjanje računov za projekt](media/CreateProjectInvoicesBulk.png)

    Opozorilo vas obvešča, da lahko pride do zamude pri ustvarjanju računov. Prikazan je tudi postopek.

2. Izberite **V redu**, da zaprete okno sporočila.

    Račun se ustvari za vse transakcije v podrobnostih pogodbe s stanjem **Pripravljeno za izdajanje računov**. Te transakcije vključujejo čas, stroške, mejnike in podrobnosti pogodbe, ki temeljijo na izdelku.

3. Če si želite ogledati ustvarjene račune, odprite **Prodaja** \> **Obračunavanje** \> **Računi**. Za vsako projektno pogodbo boste videli en račun.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Nastavitev avtomatiziranega ustvarjanja računov za projekt v PSA

Če želite konfigurirati avtomatizirano izdajo računa v PSA, sledite spodnjim korakom.

1. Odprite **Project Service** \> **Nastavitve** \> **Paketna opravila**.
2. Ustvarite paketno opravilo in ga poimenujte **Ustvarjanje računov v PSA**. Ime paketnega posla mora vključevati izraz »Ustvarjanje računov«.
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
> Paketno izdajanje računov v storitvi Project Service Automation se izvaja samo za podrobnosti pogodb, ki so konfigurirane z razporedi računov. V podrobnostih pogodbe z načinom obračunavanja s fiksno ceno morajo biti nastavljeni mejniki. V podrobnostih pogodbe z načinom obračunavanja za časovne in materialne transakcije je treba nastaviti datumski urnik računov. Informacije o nastavitvi pogostosti izdajanja računov v okviru projekta, ki temelji na vrstici s ponudbo, so na voljo v temi [Ponudbe in vrstice s ponudbo](basic-quote-lines.md#invoice-schedule). Enako velja v podrobnosti pogodbe za projekt.      
 
### <a name="edit-a-draft-psa-invoice"></a>Urejanje osnutka računa v PSA

Ko ustvarite osnutek računa za projekt, se vse neobračunane prodajne transakcije, ki so bile ustvarjene, ko so bili odobreni časovni vnosi in vnosi stroškov, prenesejo v račun. Če je račun še vedno v fazi osnutka, lahko naredite naslednje te prilagoditve:

- Izbrišite ali uredite podrobnosti vrstice računa.
- Uredite in prilagodite količino in vrsto obračunavanja.
- Dodajte čas, stroške in provizije kot transakcije neposredno na račun. To funkcijo lahko uporabite, če je vrstica računa preslikana v vrstico pogodbe, ki podpira te razrede transakcij.

Izberite **Potrdi**, da potrdite račun. Dejanje »Potrdi« je enosmerno dejanje. Ko izberete **Potrdi**, sistem nastavi račun samo za branje in ustvari dejanske vrednosti obračunane prodaje iz vsake podrobnosti vrstice računa za vsako vrstico računa. Če se podrobnost vrstice računa sklicuje na neobračunano dejansko prodajo, sistem tudi stornira neobračunano dejansko prodajo. (Vsaka podrobnost vrstice računa, ki je bila ustvarjena iz časovnega vnosa ali vnosa stroškov, se bo sklicevala na neobračunano dejansko prodajo.) Sistemi za integracijo glavne knjige lahko to storniranje uporabijo za storno projektnega dela v teku (WIP) za računovodske namene.

### <a name="correct-a-confirmed-psa-invoice"></a>Popravek potrjenega računa v PSA

Potrjene račune PSA lahko uredite (popravite). Ko popravite potrjeni račun, se ustvari nov osnutek korekcijskega računa. Ker se predpostavlja, da želite stornirati vse transakcije in količine iz izvirnega računa, ta korektivni račun vključuje vse transakcije iz izvirnega računa, vse količine na njem pa imajo vrednost 0 (nič).

Če določene transakcije ne potrebujejo popravka, jih lahko odstranite iz osnutka korektivnega računa. Če želite stornirati ali vrniti le delno količino, lahko uredite polje **Količina** v podrobnosti vrstice. Če odprete podrobnost vrstice računa, si lahko ogledate količino na izvirnem računu. Nato lahko uredite količino na trenutnem računu, tako da je manjša ali večja od količine na izvirnem računu.

Ko potrdite korektivni račun, je prvotna obračunana dejanska prodaja stornirana in ustvari se nova obračunana dejanska prodaja. Če ste zmanjšali količino, se bo zaradi razlike ustvarila tudi nova neobračunana dejanska prodaja. Če je bila na primer prvotna obračunana prodaja za osem ur, v podrobnosti vrstice korektivnega računa pa je količina zmanjšana na šest ur, PSA stornira vrstico izvirne obračunane prodaje in ustvari dve novi dejanski vrednosti:

- Obračunana dejanska prodaja za šest ur.
- Neobračunana dejanska prodaja za preostali dve uri. Ta transakcija je lahko obračunana pozneje ali označena kot transakcija, ki se ne zaračuna, odvisno od pogajanj s stranko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]