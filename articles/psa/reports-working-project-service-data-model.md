---
title: Delo s podatkovnim modelom storitve Project Service Automation
description: Ta tema vsebuje informacije o delu s podatkovnim modelom.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d8c212ef2c9fd9dcd6be0b8f0a31aa5a948176bc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147673"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Delo s podatkovnim modelom storitve Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation razširja druge entitete aplikacije in uvaja svoje entitete v podatkovni model Common Data Service. Ta tema opisuje nekaj entitet, s katerimi boste imeli opravka v tipičnih scenarijih poročanja PSA.

## <a name="reporting-on-opportunities"></a>Poročanje o priložnostih

Project Service Automation razširja entiteto **Priložnost** v aplikaciji Dynamics 365 Sales, saj ji dodaja polja, ki omogočajo uporabo scenarijev na podlagi projektov. Ta polja je mogoče prepoznati po imenu sheme s predpono **msdyn\_**. Eno izmed pomembnejših novih polj za poročanje o priložnostih PSA je **Vrsta naročila**. To polje ima vrednost **Temelji na delu**, kar pomeni, da gre za priložnost PSA. Entiteti so bila dodana še druga polja, na primer **Pogodbena organizacija**, ki označuje organizacijo te priložnosti, in **Upravitelj kupcev**, ki vsebuje ime upravitelja kupcev, ki je odgovoren za to priložnost.

Entiteta **Vrstica priložnosti** vključuje tudi polja, ki so povezana s storitvijo Project Service. **Način obračunavanja** vsebuje informacijo o tem, ali naj bo vrstica priložnosti zaračunana na osnovi časa in materiala ali fiksne cene, entiteta **Projekt** pa vsebuje ime projekta, ki podpira izbrano priložnost. Poleg naštetih je omogočeno tudi poročanje z drugimi polji, ki zajemajo stroške in višino proračuna strank za vrstično postavko.

## <a name="reporting-on-quotes"></a>Poročanje o ponudbah

PSA razširja entiteto **Prodajna ponudba** z dodajanjem polj, povezanih s projektom. **Vrsta naročila** razlikuje med ponudbami PSA in ponudbami, ki niso PSA. To polje ima vrednost **Temelji na delu**, kar pomeni, da gre za ponudbo PSA. Za poročanje o ponudbah PSA so lahko koristna tudi polja z zneskom, kot so **Stroški, ki se zaračunajo**, **Stroški, ki se ne zaračunajo**, **Stopnja bruto dobička**, **Ocene** in **Proračun**. Druga uporabna polja kažejo, ali je ponudba donosna, ali bo končana v roku in ali ustreza pričakovanjem stranke glede proračuna.

PSA razširja tudi entiteto **Prodajna vrstica ponudbe**. Eno od dodatnih polj v PSA je **Metoda obračunavanja**, ki določa, kako bo zaračunana vrstica ponudbe (glede na čas in material ali po fiksni ceni). Entiteti so bila dodana še druga polja v povezavi s povezanim projektom, ki podpira vrstico ponudbe, izdajo računov, strošek in proračun.

PSA je v podatkovni model aplikacije Dynamics 365 dodal tudi nove entitete, povezane s ponudbami. Tukaj je nekaj primerov:

- **Podrobnosti vrstice ponudbe** – ta entiteta vsebuje podrobnosti o oceni projekta za vrstico ponudbe. Za vsako vrstico ponudbe se ustvarita dva zapisa. En zapis shranjuje stroške in podrobnosti o stroških za vrstico ponudbe, drugi zapis pa znesek prodaje in podrobnosti o prodaji za vrstico ponudbe.
- **Razpored izdajanja računov za vrstico ponudbe** – ta entiteta vsebuje razpored obračunavanja za vrstico ponudbe. Ta razpored je ustvarjen na podlagi pogostosti izdaje računov, ki je dodeljena vrstici ponudbe.
- **Mejnik vrstice ponudbe** – ta entiteta vsebuje mejnike obračunavanja za vrstice ponudb s fiksno ceno.
- **Analitična razčlenitev vrstice ponudbe** – ta entiteta vsebuje finančne podatke o vrstici ponudbe. Ti podatki so lahko uporabni za poročanje o prodaji iz ponudbe in predvidenih zneskih stroškov glede na različne dimenzije.

PSA v ponudbe dodaja tudi druge entitete, kot so **Projektni cenik vrstice ponudbe**, **Kategorija virov vrstice ponudbe** in **Kategorija transakcije vrstice ponudbe**.

![Diagram, ki prikazuje ponudbo, podrobnosti ponudbe in projektne odnose](media/PS-Reporting-image2.png "Diagram, ki prikazuje ponudbo, podrobnosti ponudbe in projektne odnose")

## <a name="reporting-on-project-contracts"></a>Poročanje o projektnih pogodbah

PSA razširja entiteto **Prodajni nalog**, ki se uporablja pri ustvarjanju zapisa projektnih pogodb. Dodano je novo pomembno polje **Vrsta naročila**, ki opredeljuje pogodbo kot projektno pogodbo PSA namesto prodajnega naloga. To polje ima vrednost **Temelji na delu**, kar pomeni, da gre za naročilo, ki je projektna pogodba PSA. V entiteto **Naročilo** so dodana še druga nova polja, ki zajemajo podrobnosti o stroških, stanje pogodbe PSA in organizacijo, ki je lastnica pogodbe.

PSA razširja tudi entiteto **Vrstica prodajnega naloga**. Dodana so tudi polja, ki opredeljujejo način obračunavanja (glede na čas in material ali po fiksni ceni), višino proračuna stranke in temeljni projekt.

PSA dodaja tudi nove entitete, ki so zasnovane za projektne pogodbe. Tukaj je nekaj primerov:

- **Podrobnosti vrstice projektne pogodbe** – ta entiteta vsebuje podrobnosti na ravni vrstice, ki so zbrane pri znesku podrobnosti pogodbe. Te so lahko tako podrobne kot vrstične postavke, ustvarjene iz projektnega razporeda na ravni opravila.
- **Razpored računov za vrstico pogodbe** – ta entiteta vsebuje razpored obračunavanja, ustvarjen na podlagi pogostosti izdaje računov, ki je dodeljena podrobnostim pogodbe.
- **Mejnik pogodbe** – ta entiteta vsebuje mejnike obračunavanja za podrobnosti pogodbe, ki imajo obdobje zaračunavanja s fiksno ceno.

PSA v pogodbe dodaja tudi druge entitete, kot so **Projektni cenik projektnih podrobnosti pogodbe**, **Kategorija virov projektnih podrobnosti pogodbe** in **Kategorija transakcije projektnih podrobnosti pogodbe**.

![Diagram, ki prikazuje naročilo, podrobnosti naročila in projektne odnose](media/PS-Reporting-image3.png "Diagram, ki prikazuje naročilo, podrobnosti naročila in projektne odnose")

## <a name="reporting-on-projects"></a>Poročanje o projektih

Entiteta **Projekti** in povezane entitete so uporabljene izključno v PSA. **Projekt** je entiteta najvišje ravni, ki se uporablja za zajemanje poslovnih procesov, povezanih z delom in stroški. Tu je seznam povezanih entitet:

- **Član projektne ekipe** – ta entiteta vsebuje podrobnosti o virih, ki jih je mogoče rezervirati, dodeljenih projektu. Ti viri so lahko splošni viri, ki jih je mogoče rezervirati, ali pa poimenovani viri, ki jih je vnesel vodja projekta ali so bili ustvarjeni iz projektnega razporeda.
- **Projektno opravilo** – ta entiteta vsebuje opravila, ki sestavljajo projektni načrt ali razpored.
- **Dodelitev vira** – ta entiteta vsebuje dodelitev opravila za vir, ki ga je mogoče rezervirati.
- **Zahtevani pogoj za vir** – ta entiteta vsebuje zahtevane pogoje za vse splošne vire med člani ekipe.
- **Ocena** in **Vrstica ocene** – ti entiteti imata vzpostavljeno razmerje med glavo in vrstico ter vsebujeta ocene stroškov za določen projekt. Ocene opravil so shranjene v entiteti **Ocena vira**.

![Diagram, ki prikazuje zahteve vira in projektne odnose](media/PS-Reporting-image4.png "Diagram, ki prikazuje zahteve vira in projektne odnose")

## <a name="reporting-on-resources"></a>Poročanje o virih

Projektni viri uporabljajo entitete **Vir, ki ga je mogoče rezervirati** iz Universal Resource Scheduling (URS), ki so v skupni rabi z drugimi aplikacijami, kot je Microsoft Dynamics 365 Field Service. Tu je seznam entitet, ki jih boste morda morali uporabiti pri poročanju o projektnih virih:

- **Vir, ki ga je mogoče rezervirati** – ta entiteta predstavlja uporabnika, stik, splošni vir, kupca, skupino ali opremo, ki se uporablja v projektni ekipi.
- **Lastnosti vira, ki ga je mogoče rezervirati** – ta entiteta zajema znanja, potrdila ali izobrazbo vira. Lastnosti imajo lahko vrednosti ocenjevanja na podlagi modela ocenjevanja.
- **Kategorija vira, ki ga je mogoče rezervirati** – ta entiteta označuje vlogo vira, ki ga je mogoče rezervirati.
- **Rezervacije vira, ki ga je mogoče rezervirati** – ta entiteta predstavlja čas, za katerega je posamezen vir rezerviran za delo na projektu. Vsaka rezervacija ima entiteto v glavi in več entitet v vrsticah, vsaka vrstica pa je označena s stanjem, ki predstavlja stanje rezervacije.

![Diagram, ki prikazuje odnose lastnosti virov, ki jih je mogoče rezervirati](media/PS-Reporting-image5.png "Diagram, ki prikazuje odnose lastnosti virov, ki jih je mogoče rezervirati")

## <a name="reporting-on-actual-transactions"></a>Poročanje o dejanskih transakcijah

Ko odobrite časovni list ali strošek oziroma izstavite račun za pogodbo v PSA, je poslovna transakcija zajeta v entiteti **Dejansko**. Ta entiteta lahko služi kot osnova za skoraj vsa finančna poročila v PSA. Entiteta **Dejansko** zajema stroškovne in prodajne transakcije poslovnega dogodka. Poleg tega zajema tudi številne pomembne atribute.

Ko delate z entiteto **Dejansko**, morate razumeti, katere transakcije se zabeležijo v entiteti in kdaj se beležijo. Spodaj je opisan tipičen potek dela s časovnimi vnosi (potek za stroškovne vnose je podoben):

1. Ko shranite časovni vnos, se v entiteti **Dejansko** ne ustvari noben zapis.
2. Ko pošljete časovni vnos, se v entiteti **Dejansko** ne ustvari noben zapis.
3. Ko je časovni vnos odobren, se v entiteti **Dejansko** ustvari en zapis, lahko pa se ustvari še drug zapis. Prvi zapis hrani strošek časovnega vnosa. Drugi zapis hrani znesek nezaračunane prodaje časovnega vnosa. Drugi zapis je odvisen od projekta oziroma dejstva, ali ima dodeljeno stranko, ponudbo ali podrobnosti pogodbe.

    | Datum dokumenta | Vrsta transakcije | Razred transakcije | Stranka         | Pogodba   | Vir     | Vloga vira | Vrsta obračunavanja | Količina | Cena enote | Znesek |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2. 3. 18        | Stroški             | Time              | Alpska smučarska koča | Alpski CRM | Ana Breznik | Vodja projekta   | Se zaračuna   | 8.0      | 50.00      | 400.00 |
    | 2. 3. 18        | Neobračunana prodaja   | Time              | Alpska smučarska koča | Alpski CRM | Ana Breznik | Vodja projekta   | Se zaračuna   | 8.0      | 100.00     | 800.00 |

    Ta dva zapisa sta ločena, a povezana. Ne označujeta ne bremen ne kreditov.

4. Če je pogodba povezana s projektom v času izstavitve računa za časovni vnos, se v entiteti **Dejansko** ustvarita še dva zapisa. Najprej se ustvari zapis z negativnim zneskom za znesek nezaračunane prodaje. Ta zapis v bistvu razveljavi nezaračunano prodajo. Nato se ustvari zapis o transakciji za zaračunano prodajo. Ponavljamo – ti zapisi so ločeni, a medsebojno povezani zapisi, ki ne označujejo ne bremen ne kreditov.

    | Datum dokumenta | Vrsta transakcije | Razred transakcije | Stranka         | Pogodba   | Vir     | Vloga vira | Vrsta obračunavanja | Količina | Cena enote | Znesek   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2. 4. 18        | Neobračunana prodaja   | Time              | Alpska smučarska koča | Alpski CRM | Ana Breznik | Vodja projekta   | Se zaračuna   | - 8,0    | 100.00     | - 800,00 |
    | 2. 4. 18        | Obračunana prodaja     | Time              | Alpska smučarska koča | Alpski CRM | Ana Breznik | Vodja projekta   | Se zaračuna   | 8.0      | 100.00     | 800.00   |

Entiteta **Izvor transakcije** beleži izvor zapisa **Dejansko**, entiteta **Povezava transakcije** pa beleži povezane zapise za zapis **Dejansko**. Poleg tega zapis **Dejansko** vsebuje sklice za projekt, projektno pogodbo (naročilo), vir, ki ga je mogoče rezervirati, in kupca.

![Diagram, ki prikazuje povezavo transakcije, izvor in dejanske odnose](media/PS-Reporting-image6.png "Diagram, ki prikazuje povezavo transakcije, izvor in dejanske odnose")


[!INCLUDE[footer-include](../includes/footer-banner.md)]