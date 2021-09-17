---
title: Viri vrstic podizvajalske pogodbe
description: Ta tema pojasnjuje, kako določiti namenska sredstva, ki jih ponudnik zagotovi določenim vrsticam podizvajalske pogodbe, vezane na čas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323391"
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
4. Na strani **Nov mejnik vrstice podizvajalske pogodbe** vnesite zahtevane podatke in nato izberite **Shrani in zapri**.

Naslednja tabela pojasnjuje polja na viru vrstice podizvajalske pogodbe.

| Polje |  Opis |
| ----- | ------------ |
| Vir, ki ga je mogoče rezervirati | Izberite vir vrste »Pogodbeni delavec«, ki ga je mogoče rezervirati in ga želite uporabiti kot vir v vrstici podizvajalske pogodbe. Če za pogodbenega delavca še niste ustvarili vira, ki ga je mogoče rezervirati, to polje pustite prazno. Vir, ki ga je mogoče rezervirati, se ustvari, ko shranite zapis.  |
| Stik | Če je polje **Vir, ki ga je mogoče rezervirati** prazno, lahko iz obstoječega stika ustvarite vrstico podizvajalske pogodbe. Za ogled seznama aktivnih stikov v sistemu uporabite iskanje. Izberite stik za dobavitelja te podizvajalske pogodbe. Stik, ki ga izberete, se potrdi, ko shranite zapis. Če stik, ki ste ga izbrali, ni veljaven, se vaš zapis ne shrani. Če za izbrani stik ni vira, ki ga je mogoče rezervirati, sistem za izbrani stik ustvari vir, ki ga je mogoče rezervirati, preden ustvari vir vrstice podizvajalske pogodbe. |
| Uporabnik | Če je polje **Vir, ki ga je mogoče rezervirati** prazno, lahko z izbiro dejavnega uporabnika ustvarite vir vrstice podizvajalske pogodbe. Za ogled seznama dejavnih uporabnikov v sistemu uporabite iskanje. Če za izbranega uporabnika ni vira, ki ga je mogoče rezervirati, sistem za izbranega uporabnika ustvari vir, ki ga je mogoče rezervirati, preden je ustvarjen vir vrstice podizvajalske pogodbe. |
| Datum začetka | Datum, ko se bo začelo delo delavca podizvajalske pogodbe. Če je ta vir rezerviran za obdobje pred tem datumskim obsegom, se prikaže opozorilo. |
| Datum konca | Datum, ko se bo končalo delo delavca podizvajalske pogodbe. Če je ta vir rezerviran za obdobje po tem datumskem obsegu, se prikaže opozorilo. |
| Obseg dela | Skupno število delovnih ur, ki jih bo delavec podizvajalske pogodbe porabil za to vrstico podizvajalske pogodbe. Če je ta vir rezerviran kljub pogojem, ki so mu dodeljeni v tej podizvajalski pogodbi, se prikaže opozorilo. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
