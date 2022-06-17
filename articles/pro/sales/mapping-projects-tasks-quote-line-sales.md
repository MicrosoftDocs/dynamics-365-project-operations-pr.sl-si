---
title: Preslikava projektov in opravil v podrobnosti ponudbe, ki temelji na projektih
description: Ta članek vsebuje informacije o tem, kako preslikati projekte in naloge v vrstico opravil, ki temelji na projektu.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8971a334bd19f0ef106f88034a1abbb3c338de22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917182"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Preslikava projektov in opravil v podrobnosti ponudbe, ki temelji na projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V podrobnostih ponudbe, ki temeljijo na projektu, lahko preslikate določena opravila projekta, ki je že povezan s podrobnostjo ponudbe.

Ko preslikate opravila v podrobnost ponudbe, bodo naslednji elementi, ki ste jih določili v podrobnosti ponudbe, veljali samo za ta opravila:

- Način obračunavanja
- Možnosti zaračunavanja
- Omejitve »Ni dovoljeno preseči«
- Stranke

Na primer, morda imate projekt, pri katerem je ena faza fiksna cena, vse druge faze pa so čas in materiali. V tem primeru lahko prvo fazo in vsa njena podrejena opravila povežete s podrobnostjo ponudbe za to fazo z načinom obračunavanja po fiksni ceni. Nato lahko vse ostale faze povežete s podrobnostjo ponudbe, ki temelji na ceni in materialih.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Povezava opravil s podrobnostmi ponudb, ki temeljijo na projektih

Opravila lahko povežete s podrobnostmi ponudb na naslednjih lokacijah:

- Stran **Projekt** > zavihek **Obračunavanje opravil** (optimalno)
- Stran **Podrobnost ponudbe** > zavihek **Opravila, ki se zaračunajo** 

### <a name="from-the-project-page"></a>S strani Projekt

Stran **Projekt** ponuja optimalno izkušnjo za povezovanje opravil s podrobnostmi ponudbe. Na tej strani lahko izberete več opravil in vse skupaj z njihovimi podrejenimi opravili povežete z izbrano podrobnostjo ponudbe.

1. Na zavihku **Splošno** podrobnosti ponudbe, ki temelji na projektu, preverite, ali je izpolnjeno polje **Projekt**.
2. V polju **Vključena opravila** izberite **Samo izbrana opravila**.
3. Shranite podrobnost ponudbe, ki temelji na projektu. Ko se obrazec osveži, se prikaže zavihek **Opravila, ki se zaračunajo**.
4. Na zavihku **Splošno** izberite povezavo do projekta v polju **Projekt**.
5. Na strani **Projekt** izberite zavihek **Obračunavanje opravil**.
6. V drugi mreži, ki velja za nastavitev obračunavanja za posamezna opravila, izberite eno ali več opravil ter nato izberite **Povezava podrobnosti ponudb**.
7. V pogovornem oknu, ki se prikaže, izberite podrobnost ponudbe, ki v ponudbi prikazuje podrobnosti ponudbe, ki temeljijo na projektu.
8. V polju **Vrsta obračunavanja** navedite, ali so ta opravila plačljiva ali ne.
9. Izberite potrditveno polje, da označite, ali naj povezava vključuje podrejena opravila izbranih opravil. Če potrdite polje, bodo podrejena opravila izbranih opravil povezana v podrobnost ponudbe.
10. Izberite **V redu**, da zaprete pogovorno okno.

### <a name="from-the-quote-line-page"></a>Na strani »Podrobnost ponudbe«

Projektna opravila lahko povežete s podrobnostmi ponudbe z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnost ponudbe**.

>[!NOTE]
>Optimalno mesto za povezovanje projektnih opravil s podrobnostmi ponudbe je na zavihku **Obračunavanje opravil** na strani **Projekt**. Če opravila povežete z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnost ponudbe**, morate ročno povezati vsak projekt.

1. Na zavihku **Splošno** podrobnosti ponudbe, ki temelji na projektu, preverite, ali je v polju **Projekt** izbran projekt.
2. V polju **Vključena opravila** izberite **Samo izbrana opravila**.
3. Shranite podrobnost ponudbe, ki temelji na projektu. Ko se obrazec osveži, se prikaže zavihek **Opravila, ki se zaračunajo**.
4. Na zavihku **Opravila, ki se zaračunajo** izberite **Dodaj opravilo za podrobnost ponudbe**.
5. Na strani **Opravilo za podrobnost ponudbe** v polju **Opravila** izberite opravilo in v polju **Vrsta obračunavanja** izberite **Shrani**. 
6. Zaprite stran. Izbrano opravilo je zdaj povezano s podrobnostjo ponudbe.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Prekinite povezavo opravil s podrobnostmi ponudb, ki temeljijo na projektih

### <a name="from-the-project-page"></a>S strani Projekt

Ta način ponuja optimalno izkušnjo za prekinitev povezave opravil s podrobnostmi ponudbe. Izberete lahko več opravil in prekinete povezavo vseh, tudi njihovih podrejenih opravil, z izbrano podrobnostjo ponudbe.

1. Na zavihku **Splošno** podrobnosti ponudbe, ki temelji na projektu, v polju **Projekt** izberite povezavo projekta.
2. Na strani **Projekt** izberite zavihek **Obračunavanje opravil**.
3. V drugi mreži, ki velja za nastavitev obračunavanja za posamezna opravila, izberite eno ali več opravil ter nato izberite **Prekini povezavo podrobnosti ponudb**.
4. Na pogovornem oknu, ki se odpre, izberite podrobnost ponudbe.
5. Izberite potrditveno polje, da označite, ali naj se povezava odstrani tudi od podrejenih opravil izbranih opravil. Če potrdite polje, bo prekinjena povezava podrejenih opravil izbranih opravil s podrobnostjo ponudbe.
6. Izberite **V redu**. Opozorilno sporočilo vas obvešča, da če odstranite to povezavo, se lahko vse dejanske vrednosti, ki so bili predhodno zabeleženi pri opravilu, razveljavijo. 
7. Izberite **V redu** za potrditev in odstranjevanje povezave med opravilom in podrobnostjo ponudbe, ki temelji na projektu.

### <a name="from-the-quote-line-page"></a>Na strani »Podrobnost ponudbe«

Povezavo projektnih opravil s podrobnostmi ponudbe lahko tudi prekinete z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnost ponudbe**.

1. Na zavihku **Opravila, ki se zaračunajo** izberite **Izbriši opravilo za podrobnost ponudbe**.
2. Izberite **V redu**. Opozorilno sporočilo vas obvešča, da če odstranite to povezavo, se lahko vse dejanske vrednosti, ki so bili predhodno zabeleženi pri opravilu, razveljavijo. 
3. Izberite **V redu** za potrditev in odstranjevanje povezave med opravilom in podrobnostjo ponudbe, ki temelji na projektu.

>[!NOTE]
> Ta postopek ne izbriše opravila iz projekta. Zgolj odstrani povezavo opravila od podrobnosti ponudbe, ki temelji na projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]