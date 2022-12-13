---
title: Ustvarjanje dodelitev virov
description: Ta članek vsebuje informacije o ustvarjanju splošnih in imenovanih dodelitev virov.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812014"
---
# <a name="create-resource-assignments"></a>Ustvarjanje dodelitev virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Dodelitev vira je neposredno povezovanje člana projektne skupine z opravilom listnega vozlišča. Ta članek vsebuje informacije o treh različnih načinih dodeljevanja virov.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Ustvarite generičnega člana ekipe z dodeljevanjem opravila


Ko ustvarite splošnega člana ekipe prek dodelitve opravila, ustvarite ogrado ali splošni vir. Ta generični vir opisuje značilnosti imenovanega vira, za katerega končno želite, da dela na nalogah. Nato ustvarite zahtevo ali oddate zahtevo z uporabo zahteve, ki se uporablja za iskanje in rezervacijo imenovanega vira.

1. V mreži za razporejanje opravil izberite ikono za vir v celici **Vir**.
2. Vnesite ime, ki bo služilo kot ime vira mesta. Na primer »Upravitelj programa«.
3. Izberite **Ustvari** in v polju **Hitro ustvarjanje člana projektne ekipe** nastavite vlogo za splošni vir.
4. Po potrebi dodeljuje opravila tej ogradi za vir tako, da v kontrolniku **Izbirnik virov** izberete vir za opravilo. Viri so navedeni pod možnostjo **Člani ekipe**.
5. Ko končate z dodeljevanjem splošnega vira, na zavihku **Ekipa** izberite generični vir in nato izberite **Generate Requirement** za ustvarjanje zahteve za vir za generični vir.
6. Za splošni vir izberite možnost **Rezerviraj**, nato pa prek plošče razporeda poiščite in rezervirajte pravi vir. Prav tako lahko pošljete zahtevo za izpolnitev s strani upravitelja virov.
7. Ko je generični vir v celoti izpolnjen z imenovanim virom, se generični vir odstrani iz ekipe. (Delna izpolnitev zahteve glede vira ne bo povzročila dodelitve vira.) Dodelitve nalog za generični vir so dodeljene imenovanemu sredstvu, ki je izpolnilo zahtevo generičnega vira.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodelite poimenovani vir s seznama vseh virov, ki jih je mogoče rezervirati

Uporabite lahko iskalno polje v kontrolniku **Izbirnik virov**, da poiščete vse razpoložljive vire in jih dodelite kateremu koli opravilu listnega vozlišča. Viri, dodeljeni na ta način, se dodajo ekipi brez rezervacij. To je podobno dodajanju člana ekipe in izbiri možnosti **Brez** kot načina dodeljevanja. Vir je na zavihkih **Ekipa**, **Dodelitev vira** in **Uskladitev** prikazan kot vir samo z dodelitvami in primanjkljajem za rezervacijo. Če želite uporabiti njihovo razpoložljivost, jih rezervirajte.

1. Z mreže opravil, plošče ali časovnice se pomaknite na celico **Dodeljeno osebi**.
2. V iskalno polje začnite vnašati ime. Rezultati iskanja za ime so prikazani v kontrolniku **Izbirnik virov** v možnosti **Drugi viri**.
3. Izberite vir, ki ga želite dodeliti opravilu, ali izberite ime vira pod možnostjo **Drugi viri ekipe**.

## <a name="editing-resource-assignment-contours"></a>Urejanje krivulj dodelitve virov

Ko so viri dodeljeni nalogi v razporedu, je njihov trud linearno porazdeljen na vsak vir na podlagi delovnih ur tega vira in načina urnika projekta. Vodja projekta lahko uporabi mrežo za dodelitev virov, da izboljša ocene napora vsakega vira, ki je dodeljen eni ali več nalogam v različnih časovnih lestvicah. Ta funkcija pomaga vodjem projektov pri izdelavi natančnejših ocen stroškov in prodaje, ki temeljijo na konturah dodelitve virov, ki se ustvarijo, ko je vir dodeljen nalogi. Poleg tega lahko vodje projektov lažje odražajo povpraševanje po virih, ki je potrebno za ustvarjanje povpraševanja v zahtevi po virih.

### <a name="navigation"></a>Krmarjenje

Za dostop do mreže za urejanje obrisov vodja projekta najprej izbere zavihek **Opravila** na glavni strani projekta in nato izbere **Naloge** tab.

![Zavihek Naloge na zavihku Naloge na glavni strani projekta.](media/AssignmentGrid.png)

Mreža podpira dva načina združevanja: **združevanje po viru** in **združevanje po opravilu**. Za razliko od mrežnega pogleda stolpcev ni mogoče konfigurirati. Edini vidni stolpci so **Dodeljeno**, **Ime opravila**, **Začetek dodelitve**,** Dokončanje naloge **in** Trud pri nalogi **.

Ko je mreža prvotno upodobljena, se začne pri najzgodnejši konturi dodelitve. Če vaš urnik ne vsebuje nobenih nalog, ki zahtevajo napor, bo mreža prazna in ne bo upodobila ničesar.

![Prazna mreža za dodelitev.](media/emptyassignmentgrid.png)

Če si želite ogledati svoje konture in različne časovne lestvice, sta na voljo tudi mreža za dodelitev virov samo za branje in mreža za usklajevanje virov.

### <a name="resource-calendars"></a>Koledarji virov

Možnost urejanja obrisa za določen dan urejajo delovni dnevi vira, kot se odraža v njihovem koledarju. Če je celica onemogočena za določen vir, ta vir v tem obdobju nima delovnih dni.

Obrisi vira se lahko razširijo preko trenutnega začetnega in končnega datuma dodeljenega opravila. Če je kontura posodobljena tako, da je po zadnjem končnem datumu opravila ali najzgodnejšem začetnem datumu opravila, bosta končni ali začetni datum opravila ustrezno spremenjena. Če pa je kontura posodobljena tako, da je pred začetnim datumom opravila, ki je povezano s predhodnikom, posodobitev ne bo uspela, ker bo dodelitev sprožila zagon opravila, preden je njegov predhodnik dokončan, in to vedenje trenutno ni podprt.

### <a name="co-authoring"></a>Soavtorstvo

Spremembe mreže za dodelitev virov se samodejno odražajo v vseh povezanih pogledih, vključno s pogledi grafikona, časovnice, tabele in mreže. Če več uporabnikov pregleduje projekt hkrati, bodo vse spremembe, ki jih naredi en uporabnik, prikazane v mreži. Nasprotno pa bodo vse spremembe, narejene v mreži za dodelitev virov, prikazane vsem drugim uporabnikom, ki si ogledujejo projekt v isti seji.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
