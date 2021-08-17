---
title: Ustvarjanje medpodjetnih transakcij
description: Ta tema vsebuje informacije o tem, kako ustvariti medpodjetne transakcije.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4ce3a45e5a09b7ac5b5663cf9983e3bed7bf7e0d3fedede2e4524c51069a800b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005501"
---
# <a name="create-intercompany-transactions"></a>Ustvarjanje medpodjetnih transakcij

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Medpodjetne transakcije so časovne in stroškovne transakcije iz projektne pogodbe, ki pripadajo enemu podjetju ali organizacijski enoti, medtem ko so viri v projektni pogodbi del drugega podjetja ali organizacijske enote.

Ko je medpodjetna transakcija odobrena, se ustvarijo naslednje dejanske transakcije

| **Vrsta transakcije** | **Uporabljen cenik** | **Valuta transakcije** |
| --- | --- | --- |
| Cena | Cenik z lastnimi cenami za pogodbeno enoto | Valuta na cenovni vrstici |
| Neobračunana prodaja Ustvarjene so samo za dejanske podatke, ki so povezani s podrobnostmi pogodbe z vrsto, časom in materialom obračunavanja. | Prodajni cenik projektne pogodbe | Pogodbena valuta |
| Cena enote vira | Cenik z lastnimi cenami za enoto vira | Valuta na cenovni vrstici |
| Prodaja medorganizacijske enote | Cenik z lastnimi cenami za pogodbeno enoto | Valuta na cenovni vrstici |

Ceno in valuto transakcije za stroške, urno postavko vira in prodajo medorganizacijske enote določa **organizacijska enota**. To morate upoštevati, ko se odločate, kako strukturirati podjetja in organizacijske enote pri svojem izvajanju.

Ko ustvarite zapise o priložnostih, ponudbah, projektnih pogodbah in projektih, sistem preveri, ali se valuta pogodbene enote ujema z računovodsko valuto pogodbenega podjetja. Če nista enaki, zapisov ni mogoče ustvariti. Valuto organizacijske enote določite v Dynamics 365 Project Operations, tako da odprete **Dataverse** > **Nastavitve** > **Organizacijske enote**. Računovodsko valuto podjetja določite v Dynamics 365 Finance, tako da odprete **Glavna knjiga** > **Nastavitev knjige** > **Knjiga**. Valuta je sinhronizirana z vašim okoljem Dataverse prek zemljevida Ledgers Dual Write.

Sistem ustvari dejanske podatke stroškov za enoto vira in prodajo medorganizacijskih enot v naslednjih situacijah:

  - Ko se enota vira razlikuje od pogodbene enote
  - Ko se podjetje, ki zagotavlja vire, razlikuje od pogodbenega podjetja

V okolje Dynamics 365 Finance pa se bodo za dodatne računovodske storitve prenesle samo transakcije, pri katerih se podjetje, ki zagotavlja vire, razlikuje od pogodbenega podjetja.

Računovodstvo za dejanske podatke projekta je zabeleženo v dnevniku integracij Project Operations v aplikaciji Finance. Sistem ustvari naslednje vrstice dnevnika.

| **Vrsta transakcije** | **Pravna oseba** | **Ustvari transakcijo projekta ob objavi** | **Privzeta vrednost finančnih razsežnosti** | **Privzete vrednosti za obračunavanje skupine prometnega davka in obračunavanje skupine davka od prodaje izdelkov** |
| --- | --- | --- | --- | --- |
| Cena | Ni dodano v dnevnik integracije | Ni na voljo | Ni na voljo | Ni na voljo |
| Neobračunana prodaja | Dnevnik integracije izposojevalne pravne osebe | Da | Project | **Obračunavanje skupine prometnega davka**: temelji na **pogodbeni stranki** <br/> **Obračunavanje skupine davka od prodaje izdelkov** : iz trenutne projektne kategorije pravne osebe v vrstici dnevnika |
| Cena enote vira | Dnevnik integracije posojilne pravne osebe | No | Medpodjetna stranka | **Obračunavanje skupine prometnega davka**: temelji na **medpodjetni stranki** <br/> **Obračunavanje skupine davka od prodaje izdelkov** : iz trenutne projektne kategorije pravne osebe v vrstici dnevnika |
| Medorganizacijska prodaja | Dnevnik integracije posojilne pravne osebe | No | Medpodjetna stranka | **Obračunavanje skupine prometnega davka**: temelji na **medpodjetni stranki** <br/> **Obračunavanje skupine davka od prodaje izdelkov** : iz trenutne projektne kategorije pravne osebe v vrstici dnevnika |

### <a name="example-intercompany-transactions"></a>Primer: medpodjetne transakcije

Simona Horvat, razvijalka, ki je zaposlena v GBPM, je zabeležila 10 ur dela za projekt USPM Adventure Works, ki ga odobri vodja projekta. Strošek razvijalca v GBPM znaša 88 GBP na uro. GBPM bo zaračunal USPM 120 USD na uro razvijalca. USPM bo stranki Adventure Works zaračunal 200 USD za delo, ki ga je opravil vir GBPM. Za več informacij glejte [Konfiguracija medpodjetnega izdajanja računov](configure-intercompany-invoicing.md).

1. V aplikaciji Project Operations odprite možnost **Viri** in na seznamu izberite osebo **Simona Horvat**. Na zavihku **Načrtovanje** v polju **Podjetje** izberite **GBPM**.
2. Odprite **Prodaja** > **Stranke** in izberite **Novo**, če želite ustvariti nov zapis o stranki za Adventure Works.
    1. Nastavite podjetje na **USPM**.
    2. Nastavite **Vrsta odnosa** na **Stranka**.
    3. Izberite **Skupina strank 10 – Domači viri**.
    4. Nastavite valuto na **USD**.
    5. Shranjevanje zapisa.
3. Odprite **Prodaja** > **Projektne pogodbe** in ustvarite novo projektno pogodbo za Adventure Works.
    1. Lastniško podjetje nastavite na **USPM** in pogodbeno enoto na **Contoso Robotics US**.
    2. Kot stranko izberite Adventure Works.
    3. Izberite cenik izdelkov in shranite zapis.
    4. V zavihku **Podrobnosti pogodbe** ustvarite nove podrobnosti pogodbe. Nastavite poljubno ime in izberite **Čas in materiali** kot način obračunavanja.
    5. Ustvarite nov projekt in ga povežite s temi podrobnostmi pogodbe.
4. Prijavite se kot vir **Simona Horvat**. Odprite **Projekti** > **Časovni vnosi** in ustvarite časovni vnos za projekt Adventure Works.
5. Prijavite se kot vodja projekta. Odprite **Projekti** > **Odobritve** in odobrite transakcijo časovnega vnosa, ki jo je zabeležila Simona Horvat.
6. Pomaknite se do projekta Adventure Works in izberite **Povezano** > **Dejanske vrednosti**. Ustvarijo se naslednje transakcije dejanskih podatkov.

| **Vrsta transakcije** | **Cena** | **Valuta transakcije** | **Znesek** |
| --- | --- | --- | --- |
| Cena | 120 | USD | 1200 |
| Neobračunana prodaja | 200 | USD | 2000 |
| Cena enote vira | 88 | GBP | 880 |
| Prodaja medorganizacijske enote | 120 | USD | 1200 |

7. Prijavite se kot računovodja USPM. Odprite primerek Finance v aplikaciji Project Operations in izberite podjetje **USPM**. 
8. Pojdite v **Upravljanje projektov in računovodstvo** > **Periodično** > **Project Operations za Customer Engagement** > **Uvoz iz pripravljalnega okolja** in izberite zagon periodičnega postopka. Ta periodični postopek bo izpolnil dnevnik integracije Project Operations.
9. Pojdite v **Upravljanje projektov in računovodstvo** > **Dnevniki** > **Dnevnik integracije Project Operations** in preglejte vrstice dnevnika. Sistem ustvari naslednjo vrstico.

    | **Vrsta transakcije** | **Cena** | **Valuta transakcije** | **Znesek** |
    | --- | --- | --- | --- |
    | Neobračunana prodaja | 200 | USD | 2000 |

    Če je sistem nastavljen za fakturiranje prihodka za ta projekt, je knjiženo naslednje:

    - Bremenitev: projekt – prodajna vrednost WIP 200 USD
    - Dobropis: projekt – fakturirani prihodek 200 USD

    Ta neobračunana prodaja je zdaj pripravljena za izdajo računa. Račun za stranko Adventure Works je lahko knjižen, ko je to potrebno.

10. Prijavite se kot računovodja **GBPM**. Odprite primerek Finance v aplikaciji Project Operations in odprite podjetje **GBPM**. 
11. Odprite razdelek **Upravljanje projektov in računovodstvo** > **Občasno** > **Integracija za Project Operations** > **Uvoz iz pripravljalne tabele** in zaženite občasni postopek za izpolnjevanje dnevnika integracij za Project Operations.
12. Pojdite v **Upravljanje projektov in računovodstvo** > **Dnevniki** > **Dnevnik integracije Project Operations** in preglejte vrstice. Sistem ustvari naslednje vrstice.

    | **Vrsta transakcije** | **Cena** | **Valuta transakcije** | **Znesek** |
    | --- | --- | --- | --- |
    | Cena enote vira | 88 | GBP | 880 |
    | Prodaja medorganizacijske enote | 120 | USD | 1200 |

    Knjiženje teh zapisov povzroči naslednje transakcije s kuponi:

    - Bremenitev: strošek projekta 88 GBP
    - Dobropis: dodelitev plače 88 GBP

    Če je sistem nastavljen za fakturiranje medpodjetnega prihodka, je knjiženo naslednje:

    - Bremenitev: projekt – prodajna vrednost WIP 120 USD
    - Dobropis: projekt – fakturirani prihodek 120 USD

    Sistem je zdaj pripravljen za izdelavo računa za medpodjetno stranko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
