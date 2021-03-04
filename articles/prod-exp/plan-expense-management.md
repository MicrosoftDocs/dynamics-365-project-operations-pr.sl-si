---
title: Konfiguracija upravljanja stroškov
description: V tem članku so opisani dejavniki in odločitve, ki jih morate upoštevati med postopkom načrtovanja, preden konfigurirate upravljanje stroškov v storitvi Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960357"
---
# <a name="configure-expense-management"></a>Konfiguracija upravljanja stroškov

V tej temi so opisani dejavniki in odločitve, ki jih morate upoštevati med postopkom načrtovanja, preden konfigurirate upravljanje stroškov. V prostoru za upravljanje stroškov lahko shranite podatke o načinih plačila, zahtevah za pot, poročilih o stroških, pravilnikih itd.

Ker veliko odločitev, ki jih sprejmete, ko načrtujete konfiguracijo upravljanja odhodkov, temelji na hierarhiji in finančni strukturi vaše organizacije, se morate sklicevati na dokumente načrtovanja za ta področja.

## <a name="intercompany-expenses"></a>Medpodjetniški stroški

Ko omogočite medpodjetniške stroške, pravnim osebam in zaposlenim omogočite, da ustvarijo stroške v imenu druge pravne osebe in poberejo plačilo od pravne osebe za zaposlitev v vaši organizaciji. Na primer, zaposleni prek pravne osebe A zaključi projekt za pravno osebo B, v okviru projekta pa nastanejo stroški, povezani s potovanjem. Če so medpodjetniški stroški omogočeni, lahko zaposleni nato vloži poročilo o stroških, ki bo stroške knjižilo pravni osebi B, strošek pa mora plačati pravna oseba A. Če vaša organizacija nima več kot ene pravne osebe, vam ni treba omogočiti medpodjetniške stroške.

**Odločitev:** Ali želite omogočiti medpodjetniške stroške?

## <a name="financial-management"></a>Finančno upravljanje

Upravljanje stroškov je tesno povezano s finančnim upravljanjem vaše organizacije. Veliko konfiguracije za upravljanje stroškov bo temeljilo na odločitvah, ki ste jih sprejeli glede financ vaše organizacije. Naslednji razdelki opisujejo različna področja, ki zahtevajo načrtovanje in odločitve, ki temeljijo na finančnih odločitvah vaše organizacije in navodilih vodstvene ekipe.

### <a name="per-diems"></a>Dnevnice

Določiti morate dnevnice za zaposlene, ki jih zagotavlja vaša organizacija. Ker se dnevnice običajno uporabljajo za kritje stroškov, kot so prehrana, nastanitev in drugi nepredvideni stroški, lahko ustvarite pravila za dnevnice, ki jih ponuja vaša organizacija. Dnevnice lahko temeljijo na letnem času, kraju potovanja ali obojem. Ko ustvarite pravilo za dnevnice, lahko določite, da se izbrani odstotek od dnevnice zadrži, če delavec prejme brezplačne obroke ali storitve. Določite lahko tudi stopnje za vrednost dnevnic, da nastavite najmanjše in največje število ur, za katera lahko velja dnevnica za potovanje delavca.

**Odločitve:**

- Privzeta pravila za dnevnice za prvi in zadnji dan:

    - Kolikšno je najmanjše število ur, ki jih lahko zaposleni zahteva na dan in še vedno prejme dnevnico?
    - Ali je znesek, ki je na voljo za obroke, nižji za prvi in zadnji dan? Če je nižji, kolikšen je odstotek znižanja?
    - Ali je znesek, ki je na voljo za hotel, nižji za prvi in zadnji dan? Če je nižji, kolikšen je odstotek znižanja?
    - Ali je znesek, ki je na voljo za druge stroške, ki nastanejo na prvi in zadnji dan, nižji? Če je nižji, kolikšen je odstotek znižanja?

- Privzeta pravila za dnevnice:

    - Ali pride do znižanja odstotka pri dnevnici za vsak obrok, če je na primer obrok brezplačen? Če je nižji, kolikšen je odstotek znižanja za vsak obrok?
    - Ali se znižanje za obrok izračuna na dan, na potovanje ali glede na število obrokov na dan?
    - Ali je treba zneske dnevnic zaokrožiti na običajen način ali zaokrožiti navzgor?
    - Ali se dnevnice izračunajo za 24-urno obdobje ali za koledarski dan?

- Pravila za dnevnice, ki temeljijo na lokaciji:

    - Ali se stopnje dnevnic razlikujejo glede na lokacijo? Katere lokacije so vključene?
    - Če se stopnje dnevnic razlikujejo glede na lokacijo, kolikšen odstotek zneska je pri vsaki lokaciji na voljo za naslednje vrste stroškov:

        - Obroki
        - Hotel
        - Drugi stroški

### <a name="expense-management-journals-and-accounts"></a>Dnevniki in računi za upravljanje stroškov

Upravljanje stroškov zahteva uporabo več dnevnikov in računov. Odločiti se morate na primer, ali se isti račun uporablja za denarne predujme in spore v zvezi s kreditnimi karticami.

**Odločitve:**

- V kateri glavni knjigi se beležijo odobrena poročila o stroških?
- Kateri račun se uporablja za denarne predujme?
- Ali je treba denarne predujme zabeležiti takoj?

### <a name="payment-methods"></a>Načini plačila

Ko dovolite zaposlenim, da ustvarijo stroške v imenu vašega podjetja, morate določiti načine plačila, ki jih zaposleni smejo uporabljati. Na primer, zaposlenim lahko dovolite uporabo gotovine ali kreditne kartice podjetja. Prav tako lahko zaposlenim dovolite uporabo osebnih kreditnih kartic in nato zaposlenim povrnete stroške. Za vsak dovoljen način plačila morate sprejeti naslednje odločitve.

**Odločitve:**

- Kateri načini plačila so dovoljeni?
- Kdo je lastnik stroškov za način plačila?
- Ali je na voljo vrsta protikonta? Če je na voljo vrsta protikonta, katera je na voljo?
- Če je na voljo protikonto, kateri račun je na voljo?
- Če je način plačila kreditna kartica, ali naj se način plačila uporablja samo pri uvoženih transakcijah?

### <a name="expense-categories-and-shared-categories"></a>Kategorije stroškov in skupne kategorije

Ko zaposleni ustvarijo poročilo o stroških, morajo biti vsi zabeleženi stroški povezani s kategorijo stroškov. Kategorije stroškov izhajajo iz skupnih kategorij, ki si jih delijo vse pravne osebe v vaši organizaciji. Te kategorije lahko delite tudi v razdelku za upravljanje projektov in računovodstvo, odvisno od načina, kako je opredeljena vaša organizacija. Na podlagi strukture vaše organizacije in navodil ekipe za uvajanje določite, ali se bodo kategorije, ki se uporabljajo pri upravljanju stroškov, uporabljale samo pri upravljanju stroškov ali jih želite deliti med funkcijami za upravljanje projektov, računovodstvo in upravljanje stroškov. Upoštevajte, da si te kategorije si lahko delita funkciji »Projekt« in »Strošek« ali »Projekt« in »Proizvodnja«, ne pa funkciji »Strošek« in »Proizvodnja«. Za vsako kategorijo stroškov morate sprejeti naslednje odločitve.

**Odločitve:**

- Katera kategorija stroška je izbrana? Primeri vključujejo kategorije za lete, hotele ali kilometrino.
- Ali lahko kategorijo stroškov uporabljajo tudi na oddelku »Vodenje projektov in računovodstvo«?
- Katera vrsta stroška je izbrana?
- Kateri je privzeti način plačila za kategorijo stroškov?
- Ali je treba razčleniti stroške v kategoriji stroškov?
- Kateri je glavni privzeti račun za kategorijo stroškov?
- Katera je privzeta davčna skupina za prodajo izdelka za kategorijo stroškov?
- Ali so za kategorijo stroškov dovoljeni dodatni načini plačila? Če so dovoljeni dodatni načini plačila, kateri so na voljo?
- Ali obstajajo podkategorije v tej kategoriji stroškov? Če obstajajo podkategorije, morate določiti tudi naslednje:

    - Ali je katera od podkategorij izključena iz davčne olajšave?
    - Katera davčna skupina za prodajo izdelka velja za podkategorije?

Če se kategorija stroškov uporablja tudi pri upravljanju projektov in računovodstvu, odgovorite na preostala vprašanja. V nasprotnem primeru pojdite na naslednji razdelek.

- Kateri računi stroškov bodo uporabljeni za naslednje stroške?

    - Cena
    - Dodelitev plače
    - Vrednost cene WIP
    - Element stroška
    - Element vrednosti cene WIP
    - Vračunana izguba
    - Vračunana izguba WIP

- Kateri računi prihodkov bodo uporabljeni za naslednje?

    - Fakturirani prihodek
    - Vračunana vrednost prihodkov od prodaje
    - Vrednost prodaje WIP
    - Vračunano razmerje med prihodkom in proizvodnjo
    - Proizvodnja WIP
    - Vračunano razmerje med prihodkom in dobičkom
    - Dobiček WIP
    - Vračunano razmerje med prihodkom in naročnino
    - Naročnina WIP

### <a name="taxes"></a>Davki

Za davke, povezane s stroški, morate določiti, kaj je vključeno ali omogočeno v poročilih o stroških.

**Odločitve:**

- Ali je prometni davek vključen v zneske stroškov?
- Ali je treba omogočiti izterjavo davkov na stroške?

    > [!NOTE]
    > Če ste se odločili za uporabo ameriškega prometnega davka in uporabo davčnih pravil, ko ste načrtovali glavno knjigo, ne morete omogočiti izterjave davka na stroške. (Če želite uporabljati ameriški prometni davek in davčna pravila, nastavite možnost **Uporabi pravila za prometni davek** na **Da**.)

## <a name="policies"></a>Pravilniki

Z ustvarjanjem pravilnikov za poročanje o stroških lahko svoji organizaciji pomagate prihraniti čas in denar, ko zaposleni ustvarijo stroške v njenem imenu. Pravilniki zagotavljajo, da zaposleni ne presežejo proračunu, zagotavljajo vse zahtevane informacije in denar porabijo le, ko ga potrebujejo. Za vsak pravilnik poročanja o stroških in vsak pravilnik odobritve poročila o stroških, ki jih ustvarite, morate sprejeti naslednje odločitve.

**Odločitve:**

- Kako se imenuje pravilnik?
- Kakšen je namen pravilnika o stroških?
- Če ste se prej odločili, da boste omogočili medpodjetniške stroške, za katera podjetja v vaši organizaciji bo veljal ta pravilnik?
- Kdaj začne pravilnik veljati?
- Kdaj pravilnik poteče?
- Kakšno je pravilo pravilnika?
- Kakšen je rezultat pravila pravilnika?


[!INCLUDE[footer-include](../includes/footer-banner.md)]