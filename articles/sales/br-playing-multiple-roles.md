---
title: Ocena prodaje in stroškov projekta, ko vir, ki ga je mogoče rezervirati, prevzame več vlog v projektu
description: Ta članek vsebuje informacije o tem, kako uporabiti cenovne razsežnosti za podporo ocen cen in stroškov za vir, ki prevzame več vlog v projektu.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923484"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Ocena prodaje in stroškov projekta, ko vir, ki ga je mogoče rezervirati, prevzame več vlog v projektu 

_**Velja za:** Project Operations za primere uporabe z viri/brez zalog, poenostavljeno uvajanje – posel do izstavitve predračuna in Project Operations za primere uporabe z naročili na zalogi/v proizvodnji_ 

Podjetja, ki temeljijo na projektih, pogosto potrebujejo en sam vir, ki bi prevzel več vlog v projektu. Vsaka vloga ima lahko različno ceno in stroške. To pomeni, da lahko čas istega vira na projektu dobi različno finančno oceno, odvisno od obračunske in stroškovne stopnje posamezne vloge. Nastavite lahko vrednosti v zapisu člana ekipe za imenovani vir z različnimi preglasitvami za posamezno opravilo, kateremu je dodeljen član ekipe.

Naslednji primer vam bo prikazal, kako preprosta preglasitev vrednosti omogoča viru, da ima v projektu več vlog z različnimi stroškovnimi in obračunskimi stopnjami.

## <a name="create-tasks"></a>Ustvarjanje opravil
Če želite ustvariti opravila, morate dodati opravila in povzetke opravil ter dodeliti opravilo, preden mu dodate še trajanje. 

### <a name="add-tasks-and-summary-tasks"></a>Dodajanje opravil in povzetkov opravil
Sledite spodnjim korakom, da dodate opravilo.

1. Pojdite v **Projekti** in odprite projekt, ki mu želite dodati opravila.
2. Izberite **Dodaj novo opravilo**. Poimenujte opravilo in pritisnite **Potrdi**.
3. Vnesite še eno ime opravila in pritisnite **Potrdi**. To ponavljajte, dokler ne ustvarite celotnega seznama opravil.
3. Če želite opravila premakniti pod opravila **Povzetek**, izberite tri navpične pike ob imenu opravila in nato izberite **Ustvari podopravilo**. 

  > [!TIP]
  > Če želite izbrati več opravil, izberite opravilo, pritisnite in držite **Ctrl** in nato izberite drugo opravilo.
  >
  > Lahko izberete tudi možnost **Povišaj podopravilo**, da premaknete opravila izpod opravil **Povzetek**.

### <a name="assign-tasks"></a>Dodeljevanje opravil

Izvedite naslednje korake, da dodelite opravila.

1. V stolpcu za opravilo **Dodeljeno** izberite ikono osebe.
2. Na seznamu izberite člana ekipe ali vnesite besedilo za iskanje imena.

### <a name="add-task-duration-and-columns"></a>Dodajanje trajanja opravila in stolpcev

Pogosto je najlažje začeti ustvarjati projekt s trajanjem. Sledite spodnjim korakom, da dodate trajanje opravila.

1. V stolpcu za opravilo **Trajanje** vnesite število dni, kolikor bo izvedba opravila predvidoma trajala. Če želite uporabiti drugo časovno enoto, vnesite številko in besedo **ure**, **tedni** ali **meseci**.
2. Če želite, da se vaše opravilo prikaže v obliki diamantnega mejnika v pogledu **Časovnica**, v stolpec **Trajanje** vnesite **0 dni**.
3. Pritisnite **Potrdi**, da greste na naslednje polje opravila **Trajanje** in nadaljujte z vnosom trajanja.

  > [!NOTE]
  > Trajanj za povzetke opravil ni mogoče vnesti.

Če želite dodati več podrobnosti, projektu dodajte stolpce. Če želite to narediti, izberite **Dodaj stolpec**. 

Za več informacij glejte [Ustvarjanje projekta](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Nastavitev vloge in organizacijske enote za splošnega člana projektne ekipe
Dokončajte naslednje korake za nastavitev vloge in organizacijske enote za splošnega člana ekipe.

1. Na strani **Opravila** izberite vrstico **Opravilo** za **Opravilo A**. 
2. V **Dodeljeno** izberite **Dodaj splošni vir**. S tem se vam bo odprla stran **Hitro ustvarjanje člana ekipe**.
3. Na strani **Hitro ustvarjanje člana ekipe** določite atribute splošnega člana ekipe, ki lahko izvaja to opravilo.
4. Izberite ustrezno vlogo in organizacijsko enoto, nato pa izberite **Shrani in zapri**. Za to opravilo je ustvarjen in dodeljen splošni član ekipe. 
5. Ponovite korake 1–4 za **Opravilo B**. Pri tem upoštevajte, da mora imeti **Opravilo B** za splošnega člana ekipe določeno drugačno vlogo in organizacijsko enoto kot **Opravilo A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Nastavite enoto za vlogo in organizacijo za projektno opravilo
Dokončajte naslednje korake za nastavitev vloge in organizacijske enote za opravilo.

1. Ko ustvarite **Opravilo A**, izberite opravilo in nato ikono **i**, da odprete podokno **Podrobnosti opravila**. 
2. V podoknu **Podrobnosti opravila** se pomaknite na dno in izberite **Ogled podrobnosti**, da odprete stran **Podrobnosti opravila**.
3. Na strani **Podrobnosti opravila** v razdelkih **Vloga** in **Organizacijska enota** dodajte vrednosti, ki so potrebne za izvedbo tega opravila za vir. 

  > [!NOTE]
  > Če boste ta scenarij dokončali z uporabo predstavitvenih podatkov Project Operations, izberite **Svetovalni vodja** kot vlogo in **Fabrikam US** kot organizacijsko enoto.

4. Izberite možnost **Opravilo B** in izberite opravilo.
5. Izberite ikono **i**, da odprete podokno **Podrobnosti opravila**. 
6. V podoknu **Podrobnosti opravila** se pomaknite na dno in izberite **Ogled podrobnosti**, da odprete stran **Podrobnosti opravila**.
7. Na strani **Podrobnosti opravila** v razdelkih **Vloga** in **Organizacijska enota** dodajte vrednosti, ki so obvezne za vir, ki bo izvedel to opravilo. Vrednosti v razdelkih **Vloga** in **Organizacijska enota** za **Opravilo B** morajo biti drugačne od tistih za **Opravilo A**. 

  > [!NOTE]
  > Če boste ta scenarij dokončali z uporabo predstavitvenih podatkov Project Operations, izberite **Omrežni tehnik** kot vlogo in **Fabrikam US** kot organizacijsko enoto.

8. Shranite in zaprite stran **Podrobnosti opravila**. 

## <a name="team-member-and-estimates-behavior"></a>Član ekipe in vedenje ocen 
Če želite razumeti vedenje mreže **Član ekipe** in ocen, izvedite naslednje korake.

1. V mreži **Član ekipe** izberite dva splošna člana ekipe in nato izberite **Ustvari zahteve**. S tem se bodo ustvarile zahteve za vir. 
2. Izberite vrstico člana ekipe za vlogo **Svetovalni vodja** in nato izberite možnost **Rezerviraj**. Odpre se plošča razporeda s seznamom virov. Izberite vir in nato izberite **Rezerviraj**, da rezervirate vir za to zahtevo.
3. Izberite vrstico člana ekipe za vlogo **Omrežni tehnik** in nato izberite možnost **Rezerviraj**. Odpre se plošča razporeda s seznamom virov. Izberite isti vir kot zgoraj in nato kliknite **Rezerviraj**, da rezervirate vir za to zahtevo.

### <a name="team-member-grid"></a>Mreža člana ekipe 

V mreži **Član ekipe** bosta ta dva zapisa splošnih članov ekipe izbrisana in nadomeščena z enim samim virom. Za ta vir obstaja en nabor vrednosti, tj. privzeti nabor vrednosti za atributa **Vloga** in **Organizacijska enota**.

Ko razširite vrstico za ta zapis člana ekipe, lahko v zapisu člana ekipe vidite ločene naloge za obe opravili. V vsaki vrstici dodelitve so vrednosti, specifične za opravilo, za možnosti **Vloga** in **Organizacijska enota**. 

### <a name="estimates-grid"></a>Mreža ocen 

V mreži **Ocene** imata nalogi za isti vir različni ceni. Dodelitev za vir v **Opravilu A** je ocenjena na podlagi vrednosti atributa **Vloga** za možnost **Svetovalni vodja**. Dodelitev za isti vir v **Opravilu B** je ocenjena na podlagi vrednosti atributa **Vloga** za možnost **Omrežni tehnik**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]