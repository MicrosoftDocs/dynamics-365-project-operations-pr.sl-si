---
title: Usklajevanje rezervacij in dodelitev
description: Ta članek vsebuje informacije o opravljenem delu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 04c238527006daab4c55f17280ce46b7df2aa649
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920402"
---
# <a name="reconcile-bookings-and-assignments"></a>Usklajevanje rezervacij in dodelitev

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rezervacije in dodelitve projektnih opravil posameznega člana projektne skupine so ohlapno povezane. Zato ima lahko vir dodelitve opravil, ki ne ustrezajo rezervacijam, in rezervacije, ki ne ustrezajo dodelitvam opravil. V idealnem primeru so rezervacije in dodelitve projektov usklajene, tako da imajo viri določeno zmogljivost za izvajanje opravil. V resnici pa se lahko rezervacije pojavijo glede na razpoložljivost, poleg tega pa se lahko v teku življenjskega cikla projekta spremeni tudi njegov časovni razpored. Zato je ohlapna povezava koristna, saj omogoča prilagodljivost.

Zaradi ohlapne povezave projektnih rezervacij in dodelitev opravil je v entiteto projekta vključen tudi zavihek **Usklajevanje**. Ta zavihek omogoča vodjam projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektno ekipo.

Za vsakega člana ekipe se v zavihku **Usklajevanje** poimensko prikažejo vse rezervacije in dodelitve, vse do zadnje dodelitve opravila. Ure so prikazane v celicah, ki lahko predstavljajo različna obdobja, tako mesece kot posamezne dni.

V polju **Časovno obdobje** lahko izberete možnosti **Mesec**, **Teden** ali **Dan**. Privzeto je nastavljena možnost **Teden**. Privzeto vrednost pa lahko tudi spremenite, tako da izberete gumb **Nastavitve**. Ko je odprt zavihek **Usklajevanje**, se prikaže trenutni datum, vendar pa se lahko s kontrolnikom za koledar pomikate naprej ali nazaj v času. Če je začetni datum projekta postavljen v prihodnost, se bo prikazal ta datum, ko boste odprli zavihek. Kontrolnik za koledar vam omogoča tudi premikanje na začetni in končni datum projekta.

Za prikaz podrobnosti o rezervacijah določenega vira lahko uporabite kontrolnike razširjevalnika za posamezen vir. Razširite lahko tudi dodelitve posameznih virov, vse do ravni posameznega opravila.

Na dnu zavihka **Usklajevanje** je prikazana skupna neto vsota za projekt, zavihek pa vključuje tudi stolpec s skupnim izračunom. V zavihku so za vsak vir ločeno navedene projektne rezervacije posameznega člana ekipe in skupna vrednost dodelitev opravil tega člana ekipe. V idealnem primeru bi morala biti razlika 0 (nič). To pomeni, ne bi smelo biti razlike med rezervacijami vira in njegovimi dodelitvami opravil. Vse razlike so obarvane in osenčene, kar označuje dve stanji:

- **Primanjkljaj rezervacij** – do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij. Ker ta zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to stanje tako, da razširi rezervacije vira za kritje primanjkljaja.
- **Odvečne rezervacije** – do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom. To stanje je lahko sprejemljivo, če je bil vir na primer rezerviran pred dodelitvijo opravila. V drugih primerih pa vir morda ne bo načrtovan za dodelitev. V takem primeru bi moral upravitelj projekta razmisliti o preklicu rezervacij vira, da se lahko zmogljivost uporabi za drug projekt.

> [!NOTE]
> Legenda za te pogoje je morda skrita, da ostane več prostora za mrežo. V tem primeru lahko legendo vidite tako, da izberete gumb **Nastavitve**.

V primerih, ko je polje **Časovno obdobje** nastavljeno na raven, višjo od **Dan**, lahko izračunana razlika znaša 0 (nič). Na ravni **Mesec** lahko neto razlika za vir znaša 0 (nič), kar označuje, da je število rezervacij enako številu dodelitev. Če pa nato pogledate raven **Teden**, boste morda videli, da obstajajo dodelitve z 0 (nič) urami in rezervacije s 40 urami v prvem tednu meseca ter dodelitve s 40 urami in rezervacije z 0 (nič) urami v drugem tednu meseca. Čeprav je skupna vrednost rezervacij in dodelitev za posamezni mesec enaka, se lahko po tednih razlikujejo.

Ko gledate višje časovne ravni, se v zavihku **Usklajevanje** prikaže celični kazalnik, ki vas obvesti, da obstajajo razlike v nižjih časovnih ravneh. Na tej sliki se celični kazalnik na primer prikaže v celici za oktober 2018 za vir, imenovan Neja Petelinc. Tako lahko torej vidite, da so lahko rezervacije in dodelitve vira enake po skupni vrednosti na ravni **Mesec**, a hkrati različne na nižjih ravneh.

![Neusklajene rezervacije in dodelitve na mesečni ravni.](media/reconcile-assignments-01.JPG)

Dvokliknite celico, da jo razširite na naslednjo nižjo raven in si ogledate razliko. Če na primer dvokliknete razliko za Nejo Petelinc v oktobru 2018, se bo raven **Teden** prikazala na ravni z več podrobnostmi. Vidite lahko, da ima vir 16 ur rezervacij, a nič dodelitev v prvih dveh tednih oktobra, ter 16 ur dodelitev, a nič rezervacij v tretjem tednu oktobra.

![Neusklajene rezervacije in dodelitve na tedenski ravni.](media/reconcile-assignments-02.JPG)

Kliknite desno tipko miške, če želite celico pomanjšati na naslednjo višjo raven. Celični kazalnik lahko tudi izklopite, in sicer tako, da izberete gumb **Nastavitve**. 

Z uporabo gumbov **Nazaj** in **Naprej** nad mrežo se lahko tudi pomikate med vsemi razlikami v projektu. Za uporabo teh gumbov najprej izberite vir. Izberite **Naprej**, če želite preiti na naslednjo razliko med rezervacijami in dodelitvami za izbran vir. Če se želite vrniti na prejšnjo razliko, izberite **Nazaj**.

Kadar imate dodelitve opravil za vir, a nimate rezervacij, lahko izberete primanjkljaj rezervacij in izberete možnost **Podaljšaj rezervacijo**. Nato boste videli rezervacijo, ki je potrebna za odpravo primanjkljaja tistega vira. Ogledate si lahko tudi rezervacije vira v trenutnem projektu in vseh drugih projektih. Izberite možnost **V redu**, če želite ustvariti rezervacijo za vir, ne glede na trenutno razpoložljivost. Vodja projekta ali upravitelj virov lahko nato s ploščo razporeda reši primere, ko ima vir preveliko število rezervacij glede na svojo zmogljivost zaradi podaljšanja njegovih rezervacij.

## <a name="managing-with-time-zones"></a>Upravljanje s časovnimi pasovi
Za zagotovitev točnih in predvidljivih rezultatov ob uporabi podaljšanja rezervacij morata biti izpolnjeni dve ključni zahtevi:  

- Uporabnik mora konfigurirati časovni pas svoje naprave tako, da se ujema s časovnim pasom, opredeljenim v nastavitvah za prilagoditev vašega sistema.
 
  ![Nastavitve časovnega pasu v sistemu Windows 10.](media/reconcile-assignments-03.png)

  ![Nastavitve časovnega pasu v nastavitvah osebnega prilagajanja.](media/reconcile-assignments-04.png)
 
- Vir, ki ga je mogoče rezervirati, mora imeti najmanj eno minuto delovnega časa, ki se prekriva z obrisi, ki se uporabijo za opredelitev zahtevanega podaljšanja. V naslednjem primeru je recimo prikazan pregled virov z delovnim časom od 9.00 do 19.00. 

  ![Primerjava obrisov virov.](media/reconcile-assignments-05.png)

V spodnji tabeli so prikazani:

- Predloga projektnega koledarja.
- Vir A: ta vir ima isti koledar in je v istem časovnem pasu kot projekt. Začetni čas rezervacij bo 9.00.
- Vir B: ta vir je v drugem časovnem pasu kot projekt in zato začne ob 7.00 v svojem časovnem pasu. Toda rezervacije se bodo začele ob 9.00, saj je to najzgodnejši čas za obris dodelitve.
- Vira C in D: vira sta prav tako v različnih časovnih pasovih, ki se med seboj in projektom razlikujeta, njune rezervacije se začnejo z zadevnim razpoložljivim začetnim časom.

|Entity  |Koledar  |
|-|-|
|Predloga projektnega koledarja   | ![Koledar projekta.](media/reconcile-assignments-06.png) |
|Vir A  | ![Koledar vira A.](media/reconcile-assignments-06.png) |
|Vir B  |  ![Koledar vira B.](media/reconcile-assignments-07.png) |
|Vir C  |  ![Koledar vira C.](media/reconcile-assignments-08.png) |
|Vir D  | ![Koledar vira D.](media/reconcile-assignments-09.png)  |
 
Ko se pomaknete na pogled usklajevanja, so prikazane dodelitve virov in povezani primanjkljaj rezervacij.
 ![Uskladitev pogleda pred podaljšanjem rezervacije.](media/reconcile-assignments-10.png)

Ko je funkcionalnost podaljšanja rezervacije izvedena za vsak vir, so rezervacije uspešno podaljšane za vsak vir. To pa zato, ker se je delovni čas vsakega vira prekrival z obrisi primanjkljaja.
 ![Uskladitev pogleda po podaljšanju rezervacije.](media/reconcile-assignments-11.png) 

Podrobnejši pogled rezervacij pa prikazuje razlike v začetnem času rezervacij. Rezervacije se začnejo z začetnim časom obrisa dodelitve in razpoložljivim začetnim časom vira.
 ![Nove rezervacije virov v plošči za načrtovanje.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
