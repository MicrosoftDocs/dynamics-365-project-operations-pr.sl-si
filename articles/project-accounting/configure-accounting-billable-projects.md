---
title: Konfiguracija vodenja računov za plačljive projekte
description: Ta tema vsebuje informacije o računovodskih možnostih za plačljive projekte.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 47bb5671c7b80c0e96f3f65e9c4d25f6da8184a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131993"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfiguracija vodenja računov za plačljive projekte

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations podpira različne računovodske možnosti za plačljive projekte, ki vključujejo časovne in materialne transakcije ter transakcije s fiksno ceno.

- **Časovne in materialne transakcije**: za te transakcije se račun izda med napredovanjem dela na podlagi porabe ur, stroškov, postavk ali plačil za projekt. Te transakcijske stroške lahko povežete s prihodki od posamezne transakcije, za projekt pa se račun izda med napredovanjem dela. Prihodki od projekta se lahko vračunajo tudi takrat, ko pride do transakcije. Med izdajanjem računov se prihodek pripozna in, če je primerno, je vnaprej vračunani prihodek razveljavljen.
- **Transakcije s fiksno ceno**: za te transakcije se račun izda v skladu z razporedom obračunavanja na podlagi projektne pogodbe. Prihodke od transakcij s fiksno ceno je mogoče pripoznati ob izdaji računa ali jih izračunati in knjižiti za posamezno obdobje v skladu z načinom **dokončane pogodbe** oz. **dokončanega deleža**.

Projekt se obravnava kot plačljiv, če je povezan z eno ali več pogodbenimi vrsticami. Vrstica projektne pogodbe sama določa, kateri način obračunavanja in vrste transakcij so dovoljene.

Na primer; družba Fabrikam Robotics sklene projektno pogodbo s korporacijo Adatum za optimizacijo opreme. Korporacija Adatum plača fiksni znesek v višini 10.000 USD za kritje nastalih stroškov projekta. To je način obračunavanja s fiksno ceno. Čas in plačila projekta se obračunajo glede na porabo. To je način obračunavanja glede na čas in material. Vsa dela bodo spremljana v okviru enega projekta z imenom Optimizacija opreme Adatum.

Član projektne skupine predloži osem ur dela na projektu Optimizacija opreme Adatum. Ko vodja projekta odobri vnesene ure, sistem z načinom obračunavanja časa in materiala ustvari transakcije dejanskih vrednosti, račun in kupca. Ta transakcija ne bo vključena v izračun ocene prihodka s fiksno ceno.

Drugi član projektne skupine na projektu Optimizacija opreme Adatum predloži potne stroške v vrednosti 2000,00 USD. Ko vodja projekta odobri ta vnos, sistem s fiksnim načinom obračunavanja ustvari dejanske vrednosti transakcij in kupca za ta projektni strošek. Na podlagi te transakcije stranki ne bo izdan račun. Namesto tega bodo stranki računi izdani z ločeno konfiguriranimi mejniki obračunavanja. Ta transakcija stroška bo skupaj z ocenami stroškov vključena v izračun ocene prihodka s fiksno ceno.

Računovodska načela za projektne transakcije so opredeljena v profilih stroškov in prihodkov projekta. Za vsako projektno transakcijo sistem določi ustrezen profil stroškov in prihodkov projekta z upoštevanjem konfiguriranih pravil profila stroškov in prihodkov.

## <a name="define-project-cost-and-revenue-profiles"></a>Določitev profilov stroškov in prihodkov projekta 

V profilih stroškov in prihodkov projekta so opredeljena računovodska pravila za projektne transakcije. Profili so konfigurirani v razdelku Projektno vodenje in računovodstvo. 

Dokončajte naslednje korake, da ustvarite nov profil stroškov in prihodkov projekta. 

1. Odprite razdelek **Vodenje projektov in računovodstvo** > **Nastavitve** > **Knjiženje** > **Profili stroškov in prihodkov projekta**. 
2. Izberite možnost **Novo**, da ustvarite nov profil stroškov in prihodkov projekta.
3. V polje za **ime** vnesite ime in kratek opis profila.
4. V polju za **način obračunavanja** izberite možnost **Čas in material** ali **Fiksna cena**.
5. Razširite zavihek za hitri dostop do **glavne knjige**. Polja na tem zavihku določajo računovodska načela, ki se uporabljajo za projektne transakcije, ki so beležene v dnevniku integracije aplikacije Project Operations in nato obračunane prek predloga za projektni račun.
6. Na zavihku za hitri dostop do **glavne knjige** izberite ustrezne podatke za naslednja polja:

    - **Knjiženje stroškov – ura**:

       - *Brez glavne knjige* : stroški časovnih transakcij ne bodo vknjiženi v glavni knjigi, če se knjižijo vnosi iz dnevnika integracije aplikacije Project Operations. Vendar pa lahko računovodja pozneje vknjiži stroške s funkcijo Knjiženje stroškov.
       - **Saldo** : stroški časovnih transakcij bodo bremenjeni na vrsto računa glavne knjige *Postavka za nedokončano storitev – vrednost stroškov* in knjiženi kot dobropis na *račun za razporeditev plač* v nastavitvah knjiženja v glavni knjigi. Računovodja uporablja funkcijo Knjiženje stroškov za redne premike teh stroškov z bilančnega računa v izkaz poslovnega izida.
       - **Poslovni izid** : pri knjiženju dnevnika integracije aplikacije Project Operations so stroški časovne transakcije bremenjeni na vrsto računa glavne knjige *Stroški* in knjiženi na *račun za razporeditev plač*, ki je določen na zavihku **Stroški** na strani za **nastavitve knjiženja v glavni knjigi** (**Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Knjiženje** \> **Nastavitve knjiženja v glavni knjigi**). To je najpogostejša nastavitev za časovne in materialne transakcije.
        - *Nikoli v glavno knjigo*: stroški časovnih transakcij ne bodo nikoli knjiženi v glavni knjigi.

    - **Knjiženje stroškov – strošek**:

         - **Saldo**: pri knjiženju dnevnika integracije aplikacije Project Operations je strošek transakcije stroškov bremenjen na vrsto računa glavne knjige *Postavka za nedokončano storitev – vrednost stroška*, kot je določeno na zavihu **Strošek** na strani za **nastavitve knjiženja v glavni knjigi**, in knjižen kot dobropis na protikontu v vrstici dnevnika. Privzeti protikonti za stroške so opredeljeni v razdelku **Vodenje projektov in računovodstvo** > **Nastavitve** \> **Knjiženje** \> **Privzeti protikonto za stroške**. Računovodja uporablja funkcijo **Knjiženje stroškov** za redne premike teh stroškov z bilančnega računa v izkaz poslovnega izida.
        - **Poslovni izid**: pri knjiženju dnevnika integracije aplikacije Project Operations so stroški transakcijskih stroškov bremenjeni na vrsto računa glavne knjige *Strošek*, kot je določeno na zavihku **Strošek** na strani **z nastavitvami knjiženja v glavni knjigi**, in knjiženi na protikonto v vrstici dnevnika. Privzeti protikonti za stroške so opredeljeni v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Knjiženje** \> **Privzeti protikonto za stroške**.
       
    - **O izdaji računov za kupce**:

        - **Saldo**: pri knjiženju predloga za projektni račun je transakcija na računu (mejnik obračuna) knjižena v dobro na vrsto računa glavne knjige *Izdan račun za postavko za nedokončano storitev – za kupca*, kot je določeno na zavihku **Prihodki** na strani **z nastavitvami knjiženja v glavni knjigi**, in bremenjena na bilančni račun kupca.
         - **Poslovni izid**: pri knjiženju predloga za projektni račun je transakcija na računu (mejnik obračuna) knjižena v dobro na vrsto računa glavne knjige *Izdani račun za prihodek – za kupca*, kot je določeno na zavihku **Prihodki** na strani **z nastavitvami vnašanja v glavno knjigo**, in bremenjena na bilančni račun kupca. Bilančni računi kupcev so opredeljeni v razdelku **Terjatve** \> **Nastavitve** \> **Profili za knjiženje strank**.

   Ko določate profile knjiženja za načina obračunavanja časa in materiala, lahko prihodke obračunate glede na vrsto transakcije (ura, stroški in plačilo). Če je možnost **Obračunaj prihodke** nastavljena na **Da**, so v dnevniku integracije aplikacije Project Operations Integration neobračunane prodajne transakcije zabeležene v glavni knjigi. Vrednost prodaje je bremenjena na račun **Postavka za nedokončano storitev – vrednost prodaje** in je knjižena v dobro na račun **Obračunani prihodki - vrednost prodaje**, ki je bil ustvarjen na strani **z nastavitvami knjiženja v glavni knjigi** na zavihku **Prihodki**. 
  
  > [!NOTE]
  > Možnost **Obračunaj prihodke** je na voljo samo, če je ustrezna vrsta transakcije za **stroške** knjižena v izkaz poslovnega izida.
    
7. Razširite zavihek za hitri dostop do **ocenjevanja**. Polja na tem zavihku določajo nastavitve izračuna za ocene prihodkov s fiksno ceno. Polja na tem zavihku veljajo samo za profile stroškov in prihodkov projekta z načinom obračunavanja **Fiksna cena**.
8. Na zavihku za hitri dostop do **ocenjevanja** izberite ustrezne podatke za naslednja polja:

    - **Načelo, uporabljeno za izračune zaključka projekta**:

        - **Dokončana pogodba**: do ujemanja stroškov in priznavanja prihodkov pride šele ob koncu projekta. Dokler projekt ni končan, se stroški v saldu prikazujejo kot postavke za nedokončano storitev.
        - **Dokončan delež**: obračunani prihodki se izračunajo in knjižijo v glavno knjigo za vsako obdobje na podlagi deleža napredka projekta. Na voljo je več načinov za izračun deleža napredka. Načini za izračun so lahko samodejni in temeljijo na konfiguraciji ali pa ročni.
        - **Brez postavk za nedokončano storitev**: ta nastavitev se uporablja za krajše projekte s fiksno ceno, pri katerih se izdaja računa in nastali stroški zgodijo v istem obdobju. V tem primeru je vrednost polja **Izdaja računa za kupca** v zavihku za hiter dostop do **glavne knjige** samodejno nastavljena na možnost **Poslovni izid** , da se zagotovi pripoznavanje dohodkov pri izdaji računa. Postopek ocene dohodka ne bo uporabljen za profil stroškov in prihodkov tega projekta.

    - **Načelo ujemanja**: to polje določa, kako bo izračunana vrednost prodaje (vračunani prihodek) knjižena v glavno knjigo.

        - Pri uporabi načela **vrednost prodaje** sistem izračuna vrednost prodaje tako, da uskladi stroške in prihodke, ter rezultat knjiži kot posamezen znesek.
        - Pri uporabi načela **izvedba in dobiček** sistem vrednost prodaje razdeli na realizirane stroške in izračunani dobiček. Ti dve vrednosti sta nato knjiženi ločeno.

    - **Predloge stroškov**: omogočite razvrstitev projektnih transakcij glede na vrsto transakcije in kategorijo projekta ter določite pravila za izračun odstotka napredovanja za posamezno skupino.
    - **Kode obdobij**: določite pogostost izračunavanja ocen prihodkov za posamezen profil stroškov in prihodkov projekta.
    - **Kategorije za ocenjevanje**: uporablja se za knjiženje prodajne vrednosti (vračunanih prihodkov) v razdelku Transakcije projekta. Najprej konfigurirajte namensko kategorijo projekta za vrsto transakcije **Plačilo** in nato za to kategorijo projektov nastavite zastavico **Oceni**. Nato glede na izbrano načelo ujemanja nastavite to kategorijo projekta kot vrednost polja **Prodaja** ali v polju **Dobiček** v profilu stroškov in prihodkov projekta.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Vzorčne konfiguracije za profile stroškov in prihodkov projekta

Čas in materiali - brez postavk za nedokončano storitev

![Profil stroškov in prihodkov: Čas in materiali - brez postavk za nedokončano storitev](media/time-material-no-wip.png)

Čas in materiali – postavka za nedokončano storitev (dohodek)

![Profil stroškov in prihodkov: čas in materiali – brez postavk za nedokončano storitev](media/time-material-with-wip.png)

Fiksna cena – Brez postavk za nedokončano storitev

![Profil stroškov in prihodkov: Fiksna cena – brez brez postavk za nedokončano storitev](media/fixed-price-no-wip.png)

Fiksna cena – dokončana pogodba

![Profil stroškov in prihodkov: Fiksna cena – dokončana pogodba](media/fixed-price-completed-contract.png)

Fiksna cena – delež napredka

![Profil stroškov in prihodkov: Fiksna cena – delež napredka](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Računovodski primeri za vzorčne profile stroškov in prihodkov projekta

| Računovodski dogodek                  | Čas in material – brez postavk za nedokončano storitev                       | Čas in material – postavka za nedokončano storitev                                                                                           | Fiksna cena – Brez postavke za nedokončano storitev                                            | Fiksna cena – dokončana pogodba                                                                            | Fiksna cena – delež napredka                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Vodenje dnevnika za časovne transakcije    | Bremenjenje – stroški <br>Dobropis – Dodelitev plače          | Bremenjenje – stroški <br>Dobropis – Dodelitev plače <br>Bremenjenje – prodajna vrednost postavke za nedokončano storitev <br>Dobropis – Vračunana vrednost podajne vrednosti                | Bremenjenje – stroški <br>Dobropis – Dodelitev plače                         | Bremenjenje – stroški <br>Dobropis – Dodelitev plače                                                                    | Bremenjenje – stroški <br>Dobropis – Dodelitev plače                       |
| Vodenje dnevnika za stroškovne transakcije | Bremenjenje – stroški <br>Dobropis - Protikonto za stroške | Bremenjenje – stroški <br>Dobropis - Protikonto za stroške <br>Bremenjenje – prodajna vrednost postavke za nedokončano storitev <br>Dobropis – Vračunana vrednost podajne vrednosti      | Bremenjenje – stroški <br>Dobropis - Protikonto za stroške                 | Bremenjenje – stroški<br> Dobropis - Protikonto za stroške                                                            | Bremenjenje – stroški <br>Dobropis - Protikonto za stroške               |
| Izstavitev računa stranki                | Bremenjenje - Saldo kupca <br>Bremenjenje – prihodek z izdanim računom | Bremenjenje - Saldo kupca <br>Bremenjenje – prihodek z izdanim računom <br>Dobropis – Bremenjenje vrednosti prodaje postavke za nedokončano storitev – Vrednost vračunanih prihodkov od prodaje | Bremenjenje - Saldo kupca <br>Dobropis – prihodki z izdanim računom – za kupca | Bremenjenje - Saldo kupca <br>Dobropis – postavka za nedokončano storitev – z izdanim računom za kupca                                                  | Bremenjenje - Saldo kupca <br>Dobropis – postavka za nedokončano storitev – z izdanim računom za kupca    |
| Knjižba ocene prihodkov             | Ni na voljo.                                   | Ni na voljo.                                                                                                    | Ni na voljo                                                  | Dobropis – Vrednost stroškov za postavko za nedokončano storitev <br>Dobropis – Stroški                                                                         | Bremenjenje – postavka za nedokončano storitev – prodajna vrednost <br>Dobropis – Vračunan prihodek podajne vrednosti |
| Odstrani                         | Ni na voljo.                                   | Ni na voljo.                                                                                                    | Ni na voljo                                                  | Dobropis – Vrednost stroškov za postavko za nedokončano storitev <br>Bremenjenje – stroški <br>Dobropis – vračunan prihodek – podajna vrednost <br>Bremenjenje – postavka za nedokončano storitev z izdanim računom za kupca | Bremenjenje – postavka za nedokončano storitev – izdan račun za kupca <br>Bremenjenje – prodajna vrednost postavke za nedokončano storitev     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfiguracija pravil za profile stroškov in prihodkov projekta

Pravila za profil stroškov in prihodkov projekta določajo profil stroškov in prihodkov projekta, ki se morajo uporabljati pri obdelavi vseh plačljivih transakcij projekta. Pravila določite v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Knjiženje** \> **Pravila za profil stroškov in prihodkov projekta**.

Pravila so lahko določena glede na projektno pogodbo, projektno skupino za posamezen projekt. Sistem bo vedno najprej izbral pravilo najvišje razdrobljenosti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]