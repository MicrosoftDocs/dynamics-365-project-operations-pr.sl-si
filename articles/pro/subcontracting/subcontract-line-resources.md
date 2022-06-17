---
title: Viri vrstic podizvajalske pogodbe
description: Ta članek pojasnjuje, kako določiti namenske vire, ki jih zagotovi prodajalec za določeno vrstico podizvajalcev za čas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 84fbbd6e1a82db2b2d998b5f41579396df884ec3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924174"
---
# <a name="subcontract-line-resources"></a>Viri vrstic podizvajalske pogodbe

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Dobavitelj lahko v storitvi Dynamics 365 Project Operations določi vire, ki bodo dobavljali zmogljivost virov, kupljeno z vrstico podizvajalske pogodbe, vezane na čas.

## <a name="create-subcontract-line-resources"></a>Ustvarjanje virov vrstice podizvajalske pogodbe

Če želite ustvariti vire vrstice podizvajalske pogodbe, izvedite naslednje korake.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe** in nato odprite podizvajalsko pogodbo, s katero želite delati.
2. Odprite vrstico podizvajalske pogodbe, vezane na čas, za katero želite določiti vire dobavitelja.
3. Na podmreži, v zavihku **Viri vrstice podizvajalskih pogodb** izberite **+ Nov vir vrstice podizvajalske pogodbe**.
4. Na strani **Nov vir podrobnosti podizvajalske pogodbe** vnesite zahtevane informacije in nato izberite **Shrani in zapri**.

Naslednja tabela pojasnjuje polja na viru vrstice podizvajalske pogodbe.

| Polje | Opis | Funkcionalni vpliv |
| ----- | ----------- | ----------------- |
| Vir, ki ga je mogoče rezervirati | Izberite vir vrste **Pogodbeni delavec**, ki ga je mogoče rezervirati in ga želite uporabiti kot vir v podrobnosti podizvajalske pogodbe.| Če za pogodbenega delavca niste ustvarili vira, ki ga je mogoče rezervirati, pustite to polje prazno. Ko shranite zapis, bo ustvarjen vir, ki ga je mogoče rezervirati.  |
| Stik | Vir podrobnosti pogodbe lahko ustvarite iz obstoječe pogodbe. Za ogled seznama aktivnih stikov v sistemu uporabite iskanje. Izberite stik za dobavitelja te podizvajalske pogodbe. Če stik, ki ste ga izbrali, ni veljaven stik za dobavitelja za podizvajalsko pogodbo, zapis vira podizvajalske pogodbe ne bo shranjen.| Če za izbrani stik ni vira, ki ga je mogoče rezervirati, sistem za izbrani stik ustvari vir, ki ga je mogoče rezervirati, preden ustvari vir vrstice podizvajalske pogodbe. |
| Uporabnik | Vir podrobnosti podizvajalske podobe lahko ustvarite tako, da izberete aktivnega uporabnika. Za ogled seznama dejavnih uporabnikov v sistemu uporabite iskanje.| Če za izbranega uporabnika ni vira, ki ga je mogoče rezervirati, sistem za izbranega uporabnika ustvari vir, ki ga je mogoče rezervirati, preden je ustvarjen vir vrstice podizvajalske pogodbe. |
| Datum začetka | Datum, ko se bo začelo delo delavca podizvajalske pogodbe.| Če je ta vir rezerviran za obdobje pred tem datumskim obsegom, se prikaže opozorilo. |
| Datum konca | Datum, ko se bo končalo delo delavca podizvajalske pogodbe.| Če je ta vir rezerviran za obdobje po tem datumskem obsegu, se prikaže opozorilo. |
| Obseg dela | Skupno število ur dela, ki jih bo pogodbeni delavec porabil za to podrobnost podizvajalske pogodbe.| Če rezervacija tega vir presega delo, ki je dodeljeno tej podizvajalski pogodbi, se prikaže opozorilo. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
