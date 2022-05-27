---
title: Ključni pojmi pri oddajanju naročil podizvajalcem
description: V članku so pojasnjeni nekateri ključni koncepti, ki veljajo za podizvajalske pogodbe v storitvi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578177"
---
# <a name="key-concepts-in-subcontracting"></a>Ključni pojmi pri oddajanju naročil podizvajalcem

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V članku so razloženi nekateri ključni koncepti, ki jih morate poznati, preden začnete uporabljati funkcijo podizvajalske pogodbe v storitvi Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Pogodbene enote pri podizvajalski pogodbi

Pogodbena enota predstavlja oddelek ali prakso, ki je lastnica dostave morebitnega projekta. Pogodbena enota je tudi oddelek, ki sklene pogodbeno razmerje z dobaviteljem.

## <a name="purchase-currency"></a>Nakupna valuta

V storitvi Project Operations je nakupna valuta tista valuta, v kateri je sklenjena podizvajalska pogodba. To je tudi valuta, v kateri so zajeti stroški podizvajalca pri projektu. Nakupna valuta se lahko razlikuje od valute projekta, projektna valuta pa se lahko razlikuje tudi od prodajne valute.

## <a name="billing-methods-on-subcontract-lines"></a>Načini obračunavanja v podizvajalski pogodbi

Za projekte običajno obstajajo pogodbeni modeli s fiksnimi pristojbinami in porabo. Storitev Project Operations podpira te metode obračunavanja prodaje in nakupa. Metode obračunavanja so pri nakupu naslednje:

- **Čas in material** - Ko podrobnosti podizvajalske pogodbe uporabljajo način obračunavanja **Čas in material**, se stroški časa zabeležijo pri projektu takrat, ko podizvajalci delajo na tem projektu in si beležijo čas. Te transakcije stroškov s podizvajalci se nato ujemajo s postavkami na računih dobaviteljev. V tem modelu lahko vodje projektov, ki uporabljajo storitev "Project Operations", preverijo, ali se vrstice računov dobavitelja ujemajo s časom podizvajalca, ki je zabeležen in odobren. Po končanem preverjanju se prejšnje dejanske vrednosti, ki so bile zabeležene po odobritvi, razveljavijo, in v projektu se ustvarijo nove dejanske vrednosti, ki temeljijo na računu dobavitelja.
- **Fiksna cena** – V tem modelu pogodbe s fiksnimi provizijami računi dobaviteljev temeljijo na fiksnih mejnikih. Viri podizvajalcev pa lahko poročajo tudi o času. Čas nato pregleda in odobri vodja projekta. Ko je projekt odobren, storitev Project Operations ustvari začasne dejanske stroške projekta. Ko dobavitelj pošlje račun za mejnik, lahko vodja projekta primerja predhodno zabeležene dejanske stroške z mejnikom. Ko je preverjanje končano, se dejanski stroški razveljavijo in zabeležijo se stroški, ki temeljijo na mejnikih.

## <a name="project-price-lists-on-subcontracts"></a>Ceniki projektov podizvajalske pogodbe

Ceniki projektov so ceniki, ki se uporabljajo za določanje nabavnih cen za čas, stroške in druge komponente, povezane s projektom. Cenikov je lahko več, od katerih ima vsak lahko svoj datum začetka veljavnosti podizvajalske pogodbe v storitvi Project Operations. Storitve Project Operations ne podpirajo prekrivanja datumov začetka veljavnosti cenikov podizvajalskih pogodb.

## <a name="transaction-classes-on-subcontracts"></a>Razredi transakcij pri podizvajalcih

Project Operations podpira štiri vrste razredov transakcij:

- Čas
- Stroški
- Material
- Dajatev

Nakupne stroške je mogoče oceniti in nastanejo le v razredih transakcije **Čas**, **Strošek** in **Material**. **Dajatev** je razred transakcije, ki velja samo za prihodke in ni na voljo v vsebini nakupa.

## <a name="purchase-pricing-dimensions"></a>Pregled cen nakupov

Cenovne razsežnosti vam omogočajo, da se odločite, kateri atributi se uporabljajo za nastavitev nakupne cene in pri nastavljanju privzetih časovnih transakcij. Storitev Project Operations podpira le niz fiksnih dimenzij za nastavitev nabavne in privzete cene. Za nastavitev nabavne in privzete cene se pri podizvajalskih pogodbah in časovnih transakcijah podizvajalcev uporabljata atributa **Vloga** in **Vir, ki ga je mogoče rezervirati**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
