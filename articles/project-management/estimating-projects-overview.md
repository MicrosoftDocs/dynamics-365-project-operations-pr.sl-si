---
title: Koncepti finančnih ocen
description: Ta članek vsebuje informacije o finančnih ocenah projektov v Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931028"
---
# <a name="financial-estimation-concepts"></a>Koncepti finančnih ocen

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V storitvi Dynamics 365 Project Operations, lahko v dveh fazah finančno ocenite svoje projekte: 
1. V fazi predprodaje, preden je dogovor sklenjen. 
2. V fazi izvedbe po izdelavi projektne pogodbe. 

Finančno oceno za delo, ki temelji na projektu lahko ustvarite na kateri koli od naslednjih 3 strani:
- Na strani **Vrstica ponudbe** s podrobnostmi vrstice ponudbe.  
- Na strani **Podrobnosti pogodbe projekta** s podrobnostmi pogodbe. 
- Na strani **Projekt** v zavihkih **Opravila** ali **Ocene stroškov**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Za izdelavo ocene uporabite projektno ponudbo
V ponudbi, ki temelji na projektu, lahko uporabite entiteto **Podrobnosti vrstice ponudbe**, da ocenite, koliko dela je potrebnega za dokončanje projekta. To oceno lahko nato delite s stranko.

Vrstice ponudbe na osnovi projekta lahko imajo nič do mnogo podrobnosti vrstice ponudbe. Podrobnosti vrstice ponudbe se uporabljajo za oceno časa, stroškov ali pristojbin. Aplikacija Microsoft Dynamics 365 Project Operations v podrobnostih vrstice ponudbe ne dovoli ocen za material. Te se imenujejo razredi transakcije. Predvideni znesek davka je prav tako mogoče vnesti v razred transakcij.

Poleg razredov transakcij vsebujejo podrobnosti vrstice ponudbe tudi vrsto transakcije. Podprti sta dve vrsti transakcij za podrobnosti vrstice ponudbe: **Strošek** in **Projektna pogodba**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Za izdelavo ocene uporabite projektno pogodbo

Če ste uporabili ponudbo, ko ste ustvarili pogodbo na osnovi projekta, se ocena, ki ste jo naredili za vsako vrstico ponudbe v ponudbi, kopira v projektno pogodbo. Struktura projektne pogodbe je podobna strukturi projektne ponudbe, ki ima vrstice, podrobnosti vrstice in razporede izdajanja računov.

Ocene je mogoče izvesti neposredno v projektni pogodbi ali v projektni ponudbi. Pri projektni ponudbi je ocena narejena z uporabo vrstic pogodbe in podrobnosti vrstic pogodbe. Podrobnosti vrstice pogodbe lahko ustvarite tudi iz načrta projekta, ki je bil ustvarjen s pristopom ocenjevanja od spodaj navzgor.

Podrobnosti vrstice ponudbe se lahko uporabijo za oceno časa, stroškov ali pristojbin. Predvideni znesek davka je prav tako mogoče vnesti v podrobnostih vrstice pogodbe.

V podrobnostih vrstice pogodbe ocene za material niso dovoljene.

## <a name="use-a-project-to-create-an-estimate"></a>Za izdelavo ocene uporabite projekt 

Pri projektih lahko ocenite čas in stroške. Project Operations ne podpira ocen materiala ali dajatev za projekte.

Ocene časa se ustvarijo, ko ustvarite opravilo in določite atribute splošnega vira, ki je potreben za izvedbo opravila. Ocene časa se ustvarijo iz opravil razporeda. Ocene časa se ne ustvarijo, če ustvarite generične člane ekipe izven konteksta razporeda.

Ocene stroškov se vnesejo v mrežo na strani **Ocene stroškov**.

Ustvarjanje ocene za projekt velja za najboljšo prakso, saj lahko za vsako nalogo v načrtu projekta od spodaj navzgor sestavite podrobne ocene dela ali časa in stroškov. Nato lahko s to podrobno oceno ustvarite ocene za vsako vrstico ponudbe in sestavite bolj verodostojno ponudbo za stranko. Ko s projektnim načrtom uvozite ali ustvarite podrobno oceno v vrstici ponudbe, aplikacija Project Operations uvozi vrednosti prodaje in stroškov teh ocen. Po uvozu si lahko ogledate meritve dobičkonosnosti, marže in izvedljivosti za ponudbo projekta.

## <a name="understanding-estimates"></a>Razumevanje ocen

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

Če ste v podrobnosti vrstice ponudbe dodali polje po meri in želite, da sistem vnese vrednost polja kot privzeto vrednost v povezani vrstici cene, ki jo ustvari, uporabite orodja za registracijo vtičnikov **PreOperationContractLineDetailUpdate** in **PreOperationQuoteLineDetailUpdate**. Po spremembi podrobnosti vrstice ponudbe ali vrstice pogodbe morate znova registrirati te vtičnike. Za dokončanje postopka sledite spodnjim korakom.

1. Odprite PluginRegistrationTool in se povežite s spletnim primerkom.
2. Izberite **Iskanje** in poiščite vtičnik, ki ga želite posodobiti.
3. Izberite vtičnik in nato na glavni strani kliknite **Izberi**.
4. V vtičniku izberite korak za posodobitev, ga kliknite z desno miškino tipko in nato izberite **Posodobi**.
5. V pogovornem oknu **Posodobi obstoječi korak** v polju **Atributi filtriranja** izberite gumb s tremi pikami (**...**):
6. V pogovornem oknu **Izberite atribute** izberite potrditvena polja za atribute po meri.
7. Izberite **V redu**, da zaprete pogovorno okno, in nato **Posodobi korak**.
8. Ponovite korake od 1 do 7 za drugi vtičnik.
9. Zaprite **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
