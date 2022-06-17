---
title: Konfiguriranje medpodjetnega izstavljanja računov
description: Ta članek vsebuje informacije in primere o konfiguriranju medpodjetniškega izdajanja računov za projekte.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929418"
---
# <a name="configure-intercompany-invoicing"></a>Konfiguriranje medpodjetnega izstavljanja računov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Izvedite naslednje korake za nastavitev medpodjetnega izstavljanja računov za projekte v Dynamics 365 Project Operations. Medpodjetne transakcije so časovne in stroškovne transakcije iz projektne pogodbe, ki pripadajo enemu podjetju ali organizacijski enoti, medtem ko so viri v projektni pogodbi del drugega podjetja ali organizacijske enote.

## <a name="example-configure-intercompany-invoicing"></a>Primer: Konfiguriranje medpodjetnega izstavljanja računov

V naslednjem primeru je Contoso Robotics USA (USPM) izposojevalna pravna oseba, Contoso Robotics UK (GBPM) pa posojilna pravna oseba. 

1. **Konfiguriranje medpodjetnega računovodstva med pravnimi osebami**. Vsak par izposojevalnih in posojilnih pravnih oseb mora biti konfiguriran v glavni knjigi na strani [Medpodjetno računovodstvo](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. V Dynamics 365 Finance pojdite na **Glavna knjiga** > **Nastavitev objave** > **Medpodjetniško računovodstvo**. Ustvarite zapis z naslednjimi informacijami:

        - **Izvorno podjetje** = **GBPM**
        - **Ciljno podjetje** = **USPM**

2. **Konfigurirajte trgovalno razmerje med pravnima osebama**. Zapis o stranki, ki predstavlja izposojevalno pravno osebo, mora biti ustvarjen v posojilni pravni osebi. Zapis o dobavitelju, ki predstavlja posojilno pravno osebo, mora biti ustvarjen v izposojevalni pravni osebi.

     1. V razdelku Finance izberite pravno osebo **GBPM**.
     2. Pojdite na **Terjatve** > **Stranka** > **Vse stranke**. Ustvarite nov zapis za pravno osebo **USPM**.
     3. Razširite **Ime**, filtrirajte zapise po atributu **Vrsta** in izberite **Pravne osebe**. 
     4. Poiščite in izberite zapis stranke za **Contoso Robotics ZDA (USPM)**.
     5. Izberite **Uporabi ujemanje**. 
     6. Izberite skupino strank **50 - Medpodjetne stranke** in shranite zapis.
     7. Izberite pravno osebo **USPM**.
     8. Pojdite v **Obveznosti** > **Dobavitelji** > **Vsi dobavitelji**. Ustvarite nov zapis za pravno osebo **GBPM**.
     9. Razširite **Ime**, filtrirajte zapise po atributu **Vrsta** in izberite **Pravne osebe**. 
     10. Poiščite in izberite zapis stranke za **Contoso Robotics UK (GBPM)**.
     11. Izberite **Uporabi ujemanje**, izberite skupino dobaviteljev in shranite zapis.
     12. V zapisu o dobavitelju izberite **Splošno** > **Nastavitev** > **Medpodjetno**.
     13. V zavihku **Trgovalno razmerje** nastavite **Dejavno** na **Da**.
     14. Polje **Podjetje stranke** nastavite na **GBPM**, v polju **Zapis mojega računa** pa izberite zapis stranke, ki ste ga ustvarili prej v postopku.

3. **Konfigurirajte medpodjetne nastavitve v Parametrih za upravljanje projektov in računovodstvo**. 

    1. Izberite pravno osebo **USPM** in odprite **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Parametri za upravljanje projektov in računovodstvo**.
    2. V zavihku **Medpodjetno** izberite kategorijo nabave, da se bo ujemala z računi dobaviteljev, ki se samodejno ustvarijo.
    3. V razdelku **Privzeta kategorija** izberite **Medpodjetni viri**.
    4. Izberite pravno osebo **GBPM** in odprite **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Parametri za upravljanje projektov in računovodstvo**.
    5. V zavihku **Medpodjetno** izberite privzeto projektno kategorijo za vsako vrsto transakcije. Kategorije projektov se uporabljajo za konfiguracijo davka, če fakturirana kategorija v transakcijah med podjetji obstaja samo v pravni osebi, ki si izposoja. Izberete lahko obračun prihodkov za transakcije med podjetji. Do razmejitev pride, ko so transakcije knjižene prek dnevnika integracij Project Operations v posojilni pravni osebi. Dnevnik je razveljavljen ob knjiženju medpodjetnega računa.
    6. V skupini **V primeru posojanja virov** izberite **...** > **Novo**. 
    7. V mreži izberite naslednje podatke:

          - **Izposojevalna pravna oseba** = **USPM**
          - **Fakturiranje prihodkov** = **Da**
          - **Privzeta kategorija časovnega lista** = **Privzeto – ura**
          - **Privzeta kategorija stroškov** = **Privzeto – stroški**

4. **Nastavite račune medpodjetnih stroškov in prihodkov v Nastavitvah knjiženja v glavni knjigi**. Račun medpodjetnega prihodka se knjiži v dobro, ko je račun medpodjetne stranke knjižen v posojilni pravni osebi. Račun medpodjetnega stroška se bremeni, ko je čakajoč račun za dobavitelja knjižen v izposojevalni pravni osebi. Ti računi so nastavljeni v ustreznih pravnih osebah. 
      
     1. V razdelku Finance izberite izposojevalno pravno osebo **USPM**. 
     2. Pojdite v **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Knjiženje** > **Nastavitev knjiženja knjige**. 
     3. V zavihku **Računi stroškov** v razdelku **Vrsta računa knjige** izberite **Medpodjetni stroški**. Ustvarite nov zapis z naslednjimi informacijami:
      
        - **Posojilna pravna oseba** = **GBPM**
        - **Glavni račun** = Izberite glavni račun za medpodjetne stroške. Ta nastavitev je obvezna. Nastavitev se uporablja za medpodjetne tokove v aplikaciji Finance, ne pa tudi za komunikacijske medpodjetne tokove, povezane s projekti. Ta izbor nima nadaljnjega vpliva. 
        
     4. Izberite posojilno pravno osebo **GBPM**. 
     5. Pojdite v **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Knjiženje** > **Nastavitev knjiženja knjige**. 
     6. V zavihku **Računi prihodkov** v razdelku **Vrsta računa knjige** izberite **Medpodjetni prihodki**. Ustvarite nov zapis z naslednjimi informacijami:

        - **Izposojevalna pravna oseba** = **USPM**
        - **Glavni račun** = Izberite glavni račun za medpodjetne prihodke. Ta nastavitev je obvezna. Nastavitev se uporablja za medpodjetne tokove v aplikaciji Finance, ne pa tudi za komunikacijske medpodjetne tokove, povezane s projekti. Ta izbor nima nadaljnjega vpliva. 

5. **Nastavitev prenosnih cen za delo**. Medpodjetne prenosne cene so konfigurirane v storitvi Project Operations v okolju Dataverse. Konfigurirajte [stroške za delo](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) in [obračunske stopnje za delo](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) za medpodjetno izstavljanje računov. Prenosne cene niso podprte pri medpodjetnih transakcijah stroškov. Prodajna cena medorganizacijske enote bo vedno nastavljena na enako vrednost kot lastna cena enote, ki zagotavlja vire.

      Strošek za vire razvijalce v podjetju Contoso Robotics UK znaša 88 GBP na uro. Contoso Robotics UK bo zaračunal Contoso Robotics USA 120 USD za vsako uro, ko je ta vir delal na ameriških projektih. Contoso Robotics USA bo stranki Adventure Works zaračunal 200 USD za delo, ki ga je opravil vir razvijalec Contoso Robotics UK.

      1. V storitvi Project Operations v okviru Dataverse odprite **Prodaja** > **Ceniki**. Ustvarite nov cenik z imenom **Stroški podjetja Contoso Robotics UK.** 
      2. V ceniku ustvarite zapis z naslednjimi podatki:
         - **Vloga** = **Razvijalec**
         - **Strošek** = **88 GBP**
      3. Odprite **Nastavitve** > **Organizacijske enote** in ta cenik priložite v organizacijsko enoto **Contoso Robotics UK**.
      4. Pojdite v razdelek **Prodaja** > **Ceniki**. Ustvarite nov cenik z imenom **Stroški podjetja Contoso Robotics USA**. 
      5. V ceniku ustvarite zapis z naslednjimi podatki:
          - **Vloga** = **Razvijalec**
          - **Podjetje, ki zagotavlja vire** = **Contoso Robotics UK**
          - **Strošek** = **120 USD**
      6. Odprite **Nastavitve** > **Organizacijske enote** in cenik **Stroški podjetja Contoso Robotics USA** priložite v organizacijsko enoto **Contoso Robotics USA**.
      7. Pojdite v razdelek **Prodaja** > **Ceniki**. Ustvarite prodajni cenik z imenom **Obračunske stopnje za Adventure Works**. 
      8. V prodajnem ceniku ustvarite zapis z naslednjimi podatki:
          - **Vloga** = **Razvijalec**
          - **Podjetje, ki zagotavlja vire** = **Contoso Robotics UK**
          - **Delež obračunavanja** = **200 USD**
      9. Odprite razdelek **Prodaja** > **Projektne pogodbe** in pritrdite cenik **Obračunske stopnje za Adventure Works** v cenik projektne pogodbe z Adventure Works.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
