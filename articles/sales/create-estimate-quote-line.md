---
title: Ustvarjanje ocen za podrobnosti ponudbe
description: Ta tema vsebuje informacije o tem, kako ustvariti oceno za podrobnosti ponudbe za projekt.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8d7e7df4830612f5a7c43adf37f75bdb623959ffe00fe219441d8e394ddecac3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996456"
---
# <a name="create-estimates-on-a-quote-line"></a>Ustvarjanje ocen za podrobnosti ponudbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V ponudbi, ki temelji na projektu, lahko uporabite entiteto podrobnosti vrstice ponudbe, da ocenite, koliko dela je potrebnega za dokončanje projekta. To oceno lahko nato delite s stranko.

Vrstice ponudbe na osnovi projekta ne potrebujejo podrobnosti vrstice ponudbe. Lahko pa imajo več podrobnosti vrstice ponudbe. Podrobnosti vrstice ponudbe se uporabljajo za oceno časa, stroškov ali pristojbin. Aplikacija Dynamics 365 Project Operations v podrobnostih vrstice ponudbe ne dovoli ocen za material. Te se imenujejo razredi transakcije. Predvideni znesek davka je prav tako mogoče vnesti v razred transakcij.

Poleg razredov transakcij vsebujejo podrobnosti vrstice ponudbe tudi vrsto transakcije. Obstajata dve vrsti transakcij za podrobnosti vrstice ponudbe, **Strošek** in **Projektna pogodba**.

## <a name="estimate-by-using-a-contract"></a>Ocena z uporabo pogodbe

Če ste uporabili ponudbo v storitvi Project Operations, ko ste ustvarili pogodbo na osnovi projekta, se ocena, ki ste jo naredili za vsako podrobnost ponudbe v ponudbi, kopira v projektno pogodbo. Struktura projektne pogodbe je podobna strukturi projektne ponudbe, ki ima vrstice, podrobnosti vrstice in razporede izdajanja računov.

Ocene je mogoče izvesti neposredno v projektni pogodbi ali v projektni ponudbi. Pri projektni ponudbi je ocena narejena z uporabo vrstic pogodbe in podrobnosti vrstic pogodbe. Podrobnosti vrstice pogodbe lahko ustvarite tudi iz načrta projekta, ki je bil ustvarjen s pristopom ocenjevanja od spodaj navzgor.

Podrobnosti vrstice ponudbe se lahko uporabijo za oceno časa, stroškov ali pristojbin. Predvideni znesek davka je prav tako mogoče vnesti v podrobnostih vrstice pogodbe.

V podrobnostih vrstice pogodbe ocene za material niso dovoljene.

Med procese, ki so podprti v projektni pogodbi, spadata ustvarjanje računov in potrditev. Ustvarjanje računa ustvari osnutek računa na osnovi projekta, ki vključuje vse neobračunane dejanske vrednosti prodaje do trenutnega datuma.

Po potrditvi je pogodba samo za branje, njeno stanje pa se spremeni z **Osnutek** na **Potrjeno**. Tega dejanja ne morete razveljaviti. Ker je to dejanje trajno, je najbolje, da pogodbo ohranite v stanju **Osnutek**.

Edina razlika med osnutkom pogodbe in potrjeno pogodbo je stanje in dejstvo, da je osnutek pogodbe mogoče urejati, potrjene pogodbe pa ne. Ustvarjanje računov in spremljanje dejanskih vrednosti se lahko izvede v osnutku pogodbe in v potrjeni pogodbi.

Spremembe naročil v pogodbah ali projektih niso podprte.

## <a name="estimating-projects"></a>Ocenjevanje projektov

Ocenite lahko čas in stroške za projekte, ne pa materialov ali provizij.

Ocene časa se ustvarijo, ko ustvarite opravilo in določite atribute splošnega vira, ki je potreben za izvedbo opravila. Ocene časa se ustvarijo iz opravil razporeda. Ocene časa se ne ustvarijo, če ustvarite generične člane ekipe izven konteksta razporeda.

Ocene stroškov so vnesejo v mrežo na strani **Ocene**.

## <a name="understand-estimation"></a>Razumevanje ocenjevanja

Spodnja tabela vam bo v pomoč pri razumevanju poslovne logike v fazi ocenjevanja.

| Scenarij                                                                                                                                                                                                                                                                                                                                          | Zapis entitete                                                                                                                                                                                                       | Vrsta transakcije | Razred transakcije | Dodatne informacije                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Pri ocenjevanju prodajne vrednosti časa v ponudbi.                                                                                                                                                                                                                                                                                    | Ustvari se zapis podrobnosti vrstice ponudbe.                                                                                                                                                                               | Projektna pogodba | Time        | Polje izvora transakcije v vrstici s podrobnostmi vrstice ponudbe za prodajo se sklicuje na podrobnosti vrstice ponudbe za ceno. |
|                                                                                                                                                                                                                                                                                     | Drugi zapis podrobnosti vrstice ponudbe ustvari sistem za shranjevanje ustreznih vrednosti stroškov. Vsa nedenarna polja sistem kopira iz podrobnosti vrstice ponudbe za prodajo v podrobnosti vrstice ponudbe za ceno.                                                                                                                                                                               | Stroški | Time        | Polje izvora transakcije v vrstici s podrobnostmi vrstice ponudbe za prodajo se sklicuje na podrobnosti vrstice ponudbe za ceno. |
| Pri ocenjevanju prodajne vrednosti časa v pogodbi.                                                                                                                                                                                                                                                                                 | Ustvari se zapis podrobnosti vrstice projektne ponudbe.                                                                                                                                                                    | Projektna pogodba | Time        | Polje izvora transakcije v vrstici s podrobnostmi vrstice ponudbe za prodajo se sklicuje na podrobnosti vrstice ponudbe za ceno.      |
|                                                                                                                                                                                                                                                                                  | Drugi zapis podrobnosti vrstice ponudbe ustvari sistem za shranjevanje ustreznih vrednosti stroškov. Vsa nedenarna polja sistem kopira iz podrobnosti vrstice ponudbe za prodajo v podrobnosti vrstice ponudbe za ceno.                                                                                                                                                                    | Stroški | Time        | Polje izvora transakcije v vrstici s podrobnostmi vrstice ponudbe za prodajo se sklicuje na podrobnosti vrstice ponudbe za ceno.      |
| Ko uporabnik opiše vir v projektnem opravilu.                                                                                                                                                                                                                                                                                            | Ko je opravilo ustvarjeno z vsemi zahtevanimi cenovnimi razsežnostmi, se ustvari zapis vrstice ocene, ki prikazuje prodajno vrednost opravila. Vloga in organizacijske enote so cenovne razsežnosti | Projektna pogodba | Čas        |                                                                                   |
|     | Ko je opravilo ustvarjeno z vsemi zahtevanimi cenovnimi razsežnostmi, se ustvari zapis vrstice ocene, ki prikazuje vrednost stroškov opravila. Vsa nedenarna polja sistem kopira iz vrstice ocene za prodajo v vrstico ocene za ceno. Vloga in organizacijska enota sta cenovni razsežnosti za stroške in zneske računov.                                                                                                                                                                                                                | Cena             | Čas           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Prilagajanje entitet za podrobnosti vrstice ponudbe in podrobnosti vrstici pogodbe

Če ste v podrobnosti vrstice ponudbe dodali polje po meri in želite, da sistem vnese vrednost polja kot privzeto vrednost v povezani vrstici cene, ki jo ustvari, uporabite orodja za registracijo vtičnikov PreOperationContractLineDetailUpdate in PreOperationQuoteLineDetailUpdate. Po spremembi podrobnosti vrstice ponudbe ali vrstice pogodbe morate znova registrirati te vtičnike. Za dokončanje postopka sledite spodnjim korakom.

1. Odprite PluginRegistrationTool in se povežite s spletnim primerkom.
2. Izberite **Iskanje** in poiščite vtičnik, ki ga želite posodobiti.
3. Izberite vtičnik in nato na glavni strani izberite **Izberi**.
4. V vtičniku izberite korak za posodobitev, ga kliknite z desno miškino tipko in nato izberite **Posodobi**.
5. V pogovornem oknu **Posodobi obstoječi korak** v polju **Atributi filtriranja** izberite gumb s tremi pikami (**...**):
6. V pogovornem oknu **Izberite atribute** izberite potrditvena polja za atribute po meri.
7. Izberite **V redu**, da zaprete pogovorno okno, in nato **Posodobi korak**.
8. Ponovite korake od 1 do 7 za drugi vtičnik.
9. Zaprite PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]