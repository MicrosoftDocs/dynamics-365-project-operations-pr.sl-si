---
title: Valuta
description: Ta tema vsebuje informacije o dodajanju in odstranjevanju vrst valut v storitvi Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d53bae2f64e7b427f762161ff08917598217bb5a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898371"
---
# <a name="currency"></a>Valuta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Valute določajo cene za izdelke v katalogu izdelkov in stroške transakcij, kot so prodajni nalogi. Če vaše stranke živijo na različnih geografskih območjih, dodajte njihove valute, da boste lahko upravljali svoje transakcije. Dodajte valute, ki so najprimernejše za vaše trenutne in prihodnje poslovne potrebe.  

> [!NOTE]
> Če je vaše okolje okolje Common Data Service, ste v skrbniškem središču Power Platform in izberete stran **Valute** (**Okolja** > [izberite okolje] > **Nastavitve** > **Poslovno** > **Valute**), bo stran prazna. To je zato, ker nastavitev valute ni podprta v okoljih Common Data Service.

## <a name="add-a-currency"></a>Dodajanje valute  
Preden začnete s tem postopkom, preverite, ali vaša varnostna vloga vključuje dovoljenja skrbnika sistema. 

1. Izberite okolje v skrbniškem središču za Power Platform. 
2. Izberite **Nastavitve** > **Posel**.
3. Izberite **Valute**.  
4. Izberite **Novo**.  
5. Vnesite potrebne podatke.  


   |          Polje          |                                                                                                                                                                                                                                                                                                                                                                            Opis                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Vrsta valute**    | - **Sistem** – izberite to možnost, če želite uporabiti valute, ki so na voljo v aplikacijah na osnovi modela v storitvi Dynamics 365. Izberite **Iskanje**, da poiščete valuto. Ko izberete kodo valute, se za izbrano valuto samodejno dodata **Ime valute** in **Simbol valute**.<br />- **Po meri** – izberite to možnost, če želite dodati valuto, ki ni na voljo v aplikacijah na osnovi modela v storitvi Dynamics 365. V tem primeru morate ročno vnesti vrednosti za polja **Koda valute**, **Natančnost valute**, **Ime valute**, **Simbol valute** in **Pretvarjanje valut**. |
   |    **Koda valute**    |                                                                                                                                                                                                                                                                                                                                            Kratka oblika za valuto. Na primer **USD** za ameriški dolar.                                                                                                                                                                                                                                                                                                                                            |
   | **Natančnost valute**  |                                                                                                                                                                                  Vnesite število decimalk, ki jih želite uporabiti za valuto.  Dodate lahko vrednost med 0 in 4. **Opomba:** Če ste vrednost natančnosti nastavili v pogovornem oknu **Sistemske nastavitve**, se bo vrednost prikazala tukaj.                                                                                                                                                                                  |
   |    **Ime valute**    |                                                                                                                                                                                                                                         Če ste kodo valute izbrali na seznamu razpoložljivih valut v aplikacijah na osnovi modela v storitvi Dynamics 365, je ime valute za izbrano kodo prikazano tukaj. Če ste izbrali **Po meri** kot vrsto valute, vnesite ime valute.                                                                                                                                                                                                                                          |
   |   **Simbol valute**   |                                                                                                                                                                                                                                                                      Če ste kodo valute izbrali na seznamu razpoložljivih valut, je simbol za izbrano valuto prikazan tukaj. Če ste izbrali **Po meri** kot vrsto valute, vnesite simbol za novo valuto.                                                                                                                                                                                                                                                                       |
   | **Pretvarjanje valut** |                                                                                                                                                                                                                                     Vnesite vrednost izbrane valute po en ameriški dolar. To je znesek, pri katerem se izbrana valuta pretvori v osnovno valuto. **Pomembno:** To vrednost morate posodobiti tako pogosto, kot je to potrebno, saj se tako izognete netočnim izračunom v transakcijah.                                                                                                                                                                                                                                      |


6. Ko končate, v ukazni vrstici izberite **Shrani** ali **Shrani in zapri**.  

   > [!TIP]
   >  Če želite urediti valuto, kliknite valuto in nato vnesite ali izberite nove vrednosti.  

## <a name="delete-a-currency"></a>Izbrišite valuto  

1. Izberite okolje v skrbniškem središču Power Platform. 
2. Izberite **Nastavitve** > **Posel**.
3. Izberite **Valute**.  
4. Na prikazanem seznamu valut izberite valuto, ki jo želite izbrisati.  
5. Izberite **Izbriši**.  
6. Potrdite brisanje.  

> [!IMPORTANT]
>  Valut, ki so uporabljene v drugih zapisih, ne morete izbrisati; lahko jih le deaktivirate. Če deaktivirate zapise valut, ne odstranite podatkov o valuti, shranjenih v obstoječih zapisih, kot so priložnosti ali naročila. Vendar deaktivirane valute ne boste mogli izbrati za nove transakcije.  
