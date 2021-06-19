---
title: Finančne ocene za čase virov v projektih
description: Ta tema vsebuje informacije o tem, kako se izračunajo finančne ocene za čas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010806"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Finančne ocene za čase virov v projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Finančne ocene za čas se izračunajo na podlagi treh dejavnikov: 

- Vrsta splošnega ali imenovanega člana ekipe, dodeljena vsakemu opravilu listnega vozlišča v načrtu projekta. 
- Vrsta ali zapletenost dela.
- Porazdeljenost dela za dodelitev opravila viru. 

Prva dva dejavnika vplivata na stroške na enoto ali delež obračunavanja dodelitve vira. Stroški na enoto ali delež obračunavanja dodelitve vira se določijo z atributi dodeljenega vira. Ti atributi vključujejo organizacijsko enoto, ki ji vir pripada, in standardno vlogo vira. Za vir lahko dodate tudi atribute po meri, pomembne za vaše podjetje, na primer standardni naslov ali raven izkušenj, ki lahko vplivajo na stroške na enoto ali delež obračunavanja dodelitve.
Poleg atributov vira lahko tudi atributi dela, kot je opravilo, vplivajo na stroške na enoto ali delež obračunavanja dodelitve. Na primer, kadar so nekatera opravila bolj zapletena, dodelitev vira tem specifičnim opravilom povzroči višje stroške na enoto ali stopnjo obračunavanja kot opravila, ki so manj zapletena.   

Tretji dejavnik zagotavlja količino ur po tej stopnji. V primerih, ko opravilo zajema dve cenovni obdobji, je verjetno, da se prvi del dodelitve vira za to opravilo obračuna in oceni drugače kot drugi del opravila. Ocena napora pri vsaki dodelitvi virov je zapletena vrednost, shranjena z dnevno porazdelitvijo napora na dan.

Za podrobna navodila o tem, kako nastaviti atribute dela po meri in vire kot dimenzije cen in stroškov, glejte razdelek [Pregled cenovnih razsežnosti](../pricing-costing/pricing-dimensions-overview.md).

Finančna ocena za vsako dodelitev virov se izračuna kot **stopnjo/uro za opravilo, pomnoženo s številom ur.**  Podobno kot ocena napora je tudi finančna ocena stroškov in prihodkov za vsako dodelitev vira kompleksna vrednost, shranjena z dnevno razdelitvijo denarnega zneska na dan. 

## <a name="summarizing-financial-estimates-for-time"></a>Povzetek finančnih ocen za čas
Finančna ocena časa opravila listnega vozlišča je vsota finančnih ocen vseh dodeljenih virov za to opravilo.

Finančna ocena časa povzetka ali nadrejenega opravila je vsota finančnih ocen vseh podrejenih opravil. To so ocenjeni stroški dela na projektu. 

![Ocene virov](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Privzeta lastna cena in valuta cene

Privzeta lastna cena izhaja iz cenikov, priloženih lastniškemu podjetju projekta. Valuta stroškov projekta je vedno valuta pogodbene enote za projekt. Pri dodelitvi virov se finančna ocena stroškov shrani v valuto stroškov projekta. Včasih se valuta, v kateri je v ceniku določena stopnja stroškov, razlikuje od valute stroškov projekta. V teh primerih aplikacija pretvori valuto, v kateri je določena lastna cena, za valuto projekta. Na mreži **Ocene** so prikazane in povzete vse ocene stroškov v valuti stroškov projekta. 

## <a name="default-bill-rate-and-sales-currency"></a>Privzeti delež obračunavanja stroškov in valuta prodaje

Privzeta prodajna cena izhaja iz cenikov projekta, ki so priloženi ustrezni projektni pogodbi, če je posel pridobljen, ali iz povezane ponudbe projekta, če je posel še v fazi predprodaje. Valuta stroškov prodaje je vedno valuta projektne ponudbe ali projektne pogodbe. Pri dodelitvi virov se finančna ocena prodaje shrani v valuto prodaje projekta. Za razliko od stroškov se prodajna cena, določena v ceniku, nikoli ne more razlikovati od prodajne valute projekta. V nobenem primeru ni potrebna pretvorba valut. Na mreži **Ocene** so prikazane in povzete vse ocene prodaje v valuti prodaje projekta. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
