---
title: Podrobnosti glave za podizvajalske pogodbe
description: V okviru te teme so pojasnjene funkcije, ki so na voljo v glavi podizvajalske pogodbe v aplikaciji Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: fade0ff876486ad60ffd9ad618be7864c1b28185
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598186"
---
# <a name="header-details-for-subcontracts"></a>Podrobnosti glave za podizvajalske pogodbe

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V okviru te teme so pojasnjene funkcije, ki so na voljo v glavi podizvajalske pogodbe v aplikaciji Dynamics 365 Project Operations.

Vodja projektov, ki načrtuje in izvaja projekte, lahko zaposli podizvajalce in od dobaviteljev kupi izdelke ali naroči storitve. Ko vodja projekta kupuje izdelke ali naroča storitve, lahko v aplikacij Project Operations ustvari podizvajalsko pogodbo.

Če želite ustvariti podizvajalsko pogodbo, upoštevajte naslednja navodila.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe**, na strani **Podizvajalska pogodba** pa možnost **Nova**.
2. Vnesite zahtevane informacije in izberite **Shrani**.

    Spodnja tabela vsebuje informacije o poljih na strani **Glava podizvajalske pogodbe**.

    | Polje | Opis |Funkcionalni vpliv |
    |---|------|---| 
    | Imenu | Ime podizvajalske pogodbe. | Na vseh spustnih seznamih podizvajalskih pogodb je ime podizvajalskih pogodb navedeno v prvem stolpcu, da vam pomaga prepoznati podizvajalske pogodbe. | 
    | Opis | Kratek opis storitev in izdelkov, naročilo katerih je opredeljeno v podizvajalski pogodbi. | Brez |
    | Dobavitelj | Ime podjetja, pri katerem so naročeni izdelki in storitve. Vrsta odnosa za zapis računa je **Prodajalec** ali **Dobavitelj**. | Na podlagi izbranega dobavitelja se privzete vrednosti samodejno vnesejo za naslednja polja:<br/> **• Valuta** </br> **• Ceniki** </br> **• Plačilni pogoji**</br> **• Naslov za plačilo**</br> **• Naslov plačnika**</br> **• Ime plačnika** </br>**• Upravitelj kupcev pri dobavitelju**|
    | Datum podizvajalske pogodbe | Datum ustvarjanja podizvajalske pogodbe. | Datum podizvajalske pogodbe se uporablja za izbiro pravilnega nabavnega cenika bodisi iz cenikov, ki so priloženi sorodnemu dobavitelju, bodisi iz parametrov projekta. |
    | Razlogu stanja | Stanje podizvajalske pogodbe. | Status določa, kje je podizvajalska pogodba v poslovnem procesu in ali jo je mogoče urejati. <br/>Vrednosti vključujejo:<br>• **Osnutek**: Podizvajalsko pogodbo je mogoče urejati. Urejate lahko samo podizvajalske pogodbe s statusom **Osnutek**.<br/>• **Potrjeno**: Pogajanja z dobaviteljem so zaključena in podizvajalska pogodba je odobrena za dostavo. <br/>• **Zaključeno**: Dostava podizvajalske pogodbe je končana.<br/>• **Preklicano**: Podizvajalska pogodba je bila preklicana in dostava ni načrtovana.  | 
    | Valuta | Valuta, v kateri se kupujejo izdelki in storitve. Privzeta vrednost se samodejno vnese iz računa dobavitelja, vendar jo je mogoče spremeniti. | Valuta podizvajalske pogodbe se uporablja za izbiro nabavnega cenika bodisi iz cenikov, ki so priloženi sorodnemu dobavitelju, bodisi iz parametrov projekta. Cenikov v drugi valuti ni mogoče povezati s podizvajalsko pogodbo. Potreben čas, stroški in materiali, ki jih dobaviteljevi viri dostavijo iz te podizvajalske pogodbe, so v projektu zabeleženi v tej valuti. Ko je zapis podizvajalske pogodbe shranjen, valute na podizvajalski pogodbi ni mogoče spremeniti.|
    | Pogodbena enota | Oddelek podjetja, ki z dobaviteljem sklepa prodajno ali podizvajalsko pogodbo. | Brez |
    | Plačilni pogoji | Plačilni pogoji na računih dobaviteljev, ki so izdani s to podizvajalsko pogodbo. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Plačilni pogoji iz podizvajalske pogodbe se kopirajo na vse račune dobaviteljev, ki so povezani s to podizvajalsko pogodbo. Plačilne pogoje je mogoče posodobiti, če ima podizvajalska pogodba status **Osnutek**. | 
    | Naslov za plačilo | Naslov dobavitelja, na katerega je treba poslati plačila. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Naslov za plačilo iz podizvajalske pogodbe se kopira kot naslov za plačilo za vse račune dobaviteljev, ki so ustvarjeni za to podizvajalsko pogodbo. Naslov za plačilo je mogoče posodobiti, če ima podizvajalska pogodba status **Osnutek**.|
    | Ime plačnika | Ime osebe iz dobaviteljevega podjetja, ki bo poslala račun, ali naziv oddelka, iz katerega bo poslan. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Vrednost **Ime plačnika** iz podizvajalske pogodbe se kopira na vse račune dobaviteljev, ki so povezani s to podizvajalsko pogodbo. To polje je mogoče posodobiti, če ima podizvajalska pogodba status **Osnutek**.|
    | Naslov plačnika | Naslov, ki se uporablja na računih dobavitelja. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. | Ta naslov je naslov "račun od" na računih dobaviteljev, ki so ustvarjeni za to podizvajalsko pogodbo. |
    | Delna vsota | Če podizvajalska pogodba nima vrstic, vnesite delno vsoto naročila brez davkov. Če pa jih ima, je to polje namenjeno samo za branje. Prikazani znesek je delna vsota vseh vrstic podizvajalske pogodbe. | Brez |
    | Skupni davek | Če podizvajalska pogodba nima vrstic, vnesite vse davke te podizvajalske pogodbe. Če pa jih ima, je to polje namenjeno samo za branje. Prikazani znesek je vsota davkov vseh vrstic podizvajalske pogodbe. | Brez |
    | Skupni znesek | Polje z izračunom prikazuje skupni znesek v okviru podizvajalske pogodbe po vključitvi davkov. | Brez |
    | Datum potrditve | Datum, ko je bila podizvajalska pogodba potrjena. | Brez |
    | Zahteval(-a) | To polje je privzeto nastavljeno na ime uporabnika, ki ustvari podizvajalsko pogodbo. Ustvarjalec podizvajalske pogodbe pa lahko spremeni vrednost, da označi osebo, v imenu katere ustvarja podizvajalsko pogodbo. | Brez |
    | Upravitelj kupcev pri dobavitelju | Ime glavnega stika za račun dobavitelja. Privzeta vrednost se samodejno vnese iz zapisa računa dobavitelja. Za vodjo upravljanja računa dobavitelja podizvajalske pogodbe lahko izberete drug stik. | Nastavite lahko e-poštna opozorila za obveščanje stika o spremembah podizvajalske pogodbe, do katerih pride zaradi pogajanj o ceni. |
