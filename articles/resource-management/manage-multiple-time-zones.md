---
title: Upravljanje časovnih pasov
description: Ko je ustvarjen projekt, njegov časovni pas temelji na časovnem pasu, določenem v uporabljeni predlogi za delovne ure.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279563"
---
# <a name="manage-time-zones"></a>Upravljanje časovnih pasov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


## <a name="projects"></a>Projekti

Ko je ustvarjen projekt, njegov časovni pas temelji na časovnem pasu, določenem v uporabljeni predlogi za delovne ure. Pri možnosti **Projekt** so datumi vedno odvisni od časovnega pasu uporabnika, ki je prijavljen v vsak zavihek, z izjemo zavihka **Opravilo**. Ko si ogledate strukturirano členitev dela, bodo datumi vedno prikazani v časovnem pasu projekta.

## <a name="tasks"></a>Opravila

Ko je ustvarjeno opravilo, so začetni in končni čas ter ure/dan upravljane prek delovnega časa za projekt. Če na primer ustvarite opravilo s projektom, katerega časovni pas je -8 PST in ima naslednji delovni čas: od 9.00 do 17.00 od ponedeljka do petka, bo vsako opravilo, ustvarjeno brez dodelitev, upoštevalo začetni in končni čas koledarja projekta.

## <a name="manage-resources-with-time-zones"></a>Upravljanje virov s časovnimi pasovi

Za natančne in predvidljive rezultate pri uporabi možnosti **Podaljšaj rezervacijo** morata biti izpolnjena dva ključna predpogoja:  

- Uporabnik mora konfigurirati časovni pas svoje naprave, da se ujema s časovnim pasom, določenim v sistemski možnosti **Nastavitve za prilagoditev**.
 
  ![Nastavitve časovnega pasu v sistemu Windows 10](media/reconcile-assignments-03.png)

  ![Nastavitve časovnega pasu v nastavitvah za prilagoditev](media/reconcile-assignments-04.png)
 
- Vir, ki ga je mogoče rezervirati, mora imeti najmanj eno minuto delovnega časa, ki se prekriva z obrisi, ki se uporabijo za opredelitev zahtevanega podaljšanja. Primer: naslednji viri z delovnim časom med 9:00 in 19:00. 

  ![Primerjava obrisov virov](media/reconcile-assignments-05.png)

V spodnji tabeli so prikazani:

- Predloga koledarja projekta
- Vir A: ta vir ima isti koledar in je v istem časovnem pasu kot projekt. Začetni čas rezervacij bo 9.00.
- Vir B: ta vir se nahaja v drugačnem časovnem pasu kot projekt in se začne ob 7:00 v svojem časovnem pasu. Toda rezervacije se bodo začele ob 9.00, saj je to najzgodnejši čas za obris dodelitve.
- Vira C in D: vira se nahajata v različnih časovnih pasovih, ki se razlikujeta med seboj in od projekta, njune rezervacije pa se ne začnejo prej kot njihovi razpoložljivi začetni časi.

|Entiteta  |Koledar  |
|-|-|
|Predloga projektnega koledarja   | ![projektni koledar](media/reconcile-assignments-06.png) |
|Vir A  | ![Koledar vira A](media/reconcile-assignments-06.png) |
|Vir B  |  ![Koledar vira B](media/reconcile-assignments-07.png) |
|Vir C  |  ![Koledar vira C](media/reconcile-assignments-08.png) |
|Vir D  | ![Koledar vira D](media/reconcile-assignments-09.png)  |
 
Ko se pomaknete do pogleda **Uskladitev**, so prikazane dodelitve virov in s tem povezani primanjkljaj rezervacij.

![Pogleda usklajevanja pred podaljšanjem](media/reconcile-assignments-10.png)

Ko je bila za vsak vir uporabljena funkcija podaljšanja rezervacije, se rezervacije uspešno podaljšajo za vsak vir, ker se delovni čas vsakega vira prekriva z obrisi primanjkljaja.

![Pogled usklajevanja po podaljšanju rezervacije](media/reconcile-assignments-11.png) 

Upoštevajte, da natančnejši pregled podrobnosti rezervacij pokaže razlike v začetnih časih rezervacij. Rezervacije se začnejo šele ob začetnem času obrisa dodelitve in šele ob razpoložljivem začetnem času vira.

![Nove rezervacije virov v plošči razporeda](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]