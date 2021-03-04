---
title: Skupine enot in enote
description: V tej temi so na voljo informacije o skupinah enot in enotah.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145603"
---
# <a name="unit-groups-and-units"></a>Skupine enot in enote

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Skupine enot in enote so osnovne entitete v Microsoft Dynamics 365. Enota je posamezna merska enota, več enot pa je mogoče združiti v skupine enot. Skupina enot se uporabniškem vmesniku Dynamics 365 včasih imenuje razpored enot. 

Tukaj je nekaj primerov enot in skupin enot:
 
- **Skupina enot**: razdalja 
    - **Enote**: milja, kilometer itd.
- **Skupina enot**: čas
    - **Enote**: ura, dan, teden itd. 

Ko nastavite več enot v skupini enot, morate nastaviti tudi faktor pretvorbe med njimi, tako da določite prvo enoto, ki ste jo nastavili, kot privzeto ali glavno enoto za to skupino enot. 

Če na primer v skupini enot **Čas** kot prvo enoto nastavite možnost **Ura**, sistem določi enoto **Ura** kot privzeto enoto. Če kot naslednjo enoto nastavite možnost **Dan**, morate nastaviti faktor za pretvorbo **dneva** v **uro.** Če nato kot tretjo enoto dodate **Teden**, morate za **Teden** nastaviti faktor za pretvorbo v enoti **Dan** ali **Ura**. 

Naslednja slika prikazuje primer nastavitve za enoto **Dan**, kjer je v polju **Količina** prikazano število ur v dnevu, in enoto **Teden**, kjer je v polju **Količina** prikazano število dni v tednu.

> ![Skupina enot: stran z informacijami](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Uporaba skupin enot in enot

Dynamics 365 Project Service Automation uporablja enote in skupine enot za obdelavo ocen in vnosov za stroške in čas. 

Pri stroških ima vsaka kategorija stroškov privzeto skupino enot in enoto. Te vrednosti so vnesene kot privzete vrednosti v vnosih v cenik za kategorije stroškov. 

Tako lahko na primer imate kategorijo stroškov, ki se imenuje **Kilometrina.** Ima skupino enot, ki se imenuje **Razdalja** in privzeto enoto **Milja**. Če nastavite skupino enot **Razdalja** tako, da ima dve enoti (**Milja** in **Kilometer**), lahko za kategorijo **prevožene razdalje** na enem ceniku nastavite dve ceni: ceno na miljo in ceno na kilometer.

| Kategorija stroška  | Skupina enot  | Enota      | Način oblikovanja cen  | Cena na enoto  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometrina           | Razdalja      | Milja      | Cena na enoto    | 10 USD            |
| Kilometrina           | Razdalja      | Kilometer | Cena na enoto    |  6 USD            |

Ko za projekt vnesete strošek, sistem določi ceno na podlagi kombinacije kategorije in enote stroška. 

| Opis stroška        | Kategorija stroška  | Enota  | Količina  | Cena enote   |
|----------------------------|---------------------|-------|-----------|----------------|
| Prevoz k stranki | Kilometrina             | Milja  | 10        | 10 USD         |

Za čas ima glava vsakega cenika polje **Privzeta časovna enota**. Vrednost je nastavljena, ko ustvarite glavo cenika. Ta enota se nato uporabi za nastavitev vseh cen na podlagi vlog v tem ceniku.

Vrstice ocen za polje **Čas v ponudbi** so lahko izražene v kateri koli časovni enoti. Vendar pa lahko vrstice ocen za projekte in časovne vnose za projekte uporabljajo samo časovno enoti **Ura**. Če se enota v časovnem vnosu ali vrstici ocene ujema z enoto v vrstici cenika za to vlogo, sistem pretvori ceno v enote, ki so določene v oceni projekta ali v dejanski transakciji projekta.

Ta primer prikazuje, kako PSA uporablja skupino enot, enote in faktorje za pretvorbo.
- Enote

   - **Skupina enot**: čas 
   - **Enote**: ura 
    
    - **Dan** – faktor za pretvorbo: 8 ur       
    - **Teden** – faktor za pretvorbo: 40 ur  
        
- Nastavitev cenika za projekt A:

    - **Ime**: prodajne cene v Združenem kraljestvu za 2016 
    - **Privzeta časovna enota**: dan 
    - **Valuta**: GBP

| Vloga      | Skupina enot | Enota | Organizacijska enota | Cena   |
|-----------|------------|------|---------------------|---------|
| Developer | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Časovni vnos

V spodnji tabeli je prikazana posledična transakcija prodaje, ki jo je aplikacija PSA ustvarila za triurni projekt.


| Project   | Opravilo    | Vloga      | Količina | Enota  | Cena enote | Neobračunani znesek prodaje |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Načrt  | Developer | 3        | Ura  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Pogosta vprašanja o časovnih enotah

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Ali PSA v primeru stroškov izvaja pretvorbo v različne enote?
Ne. Pretvorba enot deluje samo za časovne enote. Za stroške pa velja, da če sistem ne more najti ceno za kombinacijo kategorije stroška in enote, je cena privzeto nastavljena na 0,00.

### <a name="why-does-psa-convert-time-units"></a>Zakaj PSA pretvarja časovne enote?
V nekaterih državah ali regijah predpisi določajo, da so zneski računov določeni v dnevih. Pogajanja o cenah in popustih na stopnji ponudbe se izvajajo z dnevnimi cenami za vsako posamezno vlogo za obračun. Ocena razporeda in časovni vnos se opravita v urah. Za podporo pri tej razliki v časovnih enotah PSA izvede pretvorbo časovnih enot.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Ali je v ocenah projektov mogoče spremeniti časovne enote?
Ne. Ocena razporeda je trenutno omejena na ure in tega ni mogoče spremeniti.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Ali je enote in skupine enot mogoče urediti, izbrisati in dodajati?
Da. Z izjemo skupine enot **Čas** in enote **Ura** lahko vse enote izbrišete ali uredite ter dodate nove enote. V PSA skupine enot **Čas** in enote **Uda** ni mogoče izbrisati. Vendar pa jih je mogoče posodobiti s prevedenim besedilo za polje **Ime**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]