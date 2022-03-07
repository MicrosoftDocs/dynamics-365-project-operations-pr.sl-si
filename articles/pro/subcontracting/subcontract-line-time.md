---
title: Vrstice podizvajalske pogodbe, vezane na čas
description: Ta tema pojasnjuje, kako zapisati vrstice podizvajalske pogodbe, vezane na čas, in zabeležiti odkup časa od dobaviteljev.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323886"
---
# <a name="subcontract-lines-for-time"></a>Vrstice podizvajalske pogodbe, vezane na čas

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podizvajalska pogodba v storitvi Dynamics 365 Project Operations lahko vsebuje vrstico podizvajalske pogodbe, vezane na čas. Vrstice podizvajalske pogodbe, vezane na čas, vodji projekta omogočajo, da kupi čas dobaviteljevih virov za osebje projektnih nalog in zahteve za vir.

Dokončajte spodnje korake, da v storitvi Project Operations ustvarite vrstico podizvajalske pogodbe, vezane na čas.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe** in odprite podizvajalsko pogodbo.
2. V zavihku **Vrstice podizvajalske pogodbe** izberite **+ Novo**, da ustvarite novo vrstico podizvajalske pogodbe.
3. Na strani **Hitro ustvarjanje**, v polju **Razred transakcije**, izberite **Čas**.
4. Vnesite preostale podatke o polju in kliknite **Shrani**.

  Spodnja tabela vsebuje informacije o poljih na straneh **Vrstica podizvajalske pogodbe** in **Hitro ustvarjanje**.

| **Polje** | **Opis** |
| --- | --- |
| Imenu | Ime podrobnosti podizvajalske pogodbe. |
| Opis | Kratek opis storitev, ki jih naročate v vrstici podizvajalske pogodbe. | 
| Vrsta vrstice | To polje je nastavljeno na privzeto vrednost.  |
| Način obračunavanja | Izberite način obračunavanja. Na podlagi načina obračunavanja podizvajalske pogodbe z virom je za metodo obračunavanja s fiksno ceno na voljo razpored za izstavljanje računov, ki temelji na mejnikih. |
| Razred transakcije | To polje je nastavljeno na privzeto vrednost, ki označuje, ali se vrstica podizvajalske pogodbe uporablja za beleženje nakupa časa podizvajalca. |
| Vloga | Vloga virov podizvajalske pogodbe, katerih čas se kupuje. Vloga, dodeljena virom podizvajalske pogodbe, odloča o ceni nakupa. |
| Zahtevani datum začetka | Datum, ko bi podizvajalčevi viri morali začeti delovati. Zahtevani datum začetka je relevanten tudi za izbiro cenika projekta iz nabora tistih cenikov, ki so priloženi podizvajalski pogodbi. Cena vloge v vrstici podizvajalske pogodbe nato izvira iz tega cenika. |
| Zahtevani datum konca | Datum, ko se zaključi delo virov podizvajalca. Ta datum se uporablja za prikaz opozoril, ko vodja projekta iz te zmogljivosti črpa zahteve po virih, ki se pojavijo po tem datumu. |
| Naročena količina | Število ur vloge, ki jih kupite pri prodajalcu. Ta vrednost se uporablja za prikaz opozoril, ko vodja projekta preseže zmogljivosti zahteve po virih. |
| Skupina enot | Ta vrednost polja je privzeto nastavljena na skupino časovne enote in je ni mogoče spremeniti.  |
| Enota | To polje je privzeto nastavljeno na osnovno enoto ur iz skupine časovne enote. To vrednost lahko spremenite, če želite kupiti katero koli enoto skupine časovnih enot, na primer dan ali teden. Kombinacija vloge in enote se uporablja za izračun cene enote vrstice podizvajalske pogodbe. |
| Cena enote | Cena enote izvira iz kombinacija vloge in enote, zapisane na ceniku projekta, ki velja za zahtevani datum začetka vrstice podizvajalske pogodbe. Kadar je cena v veljavnem ceniku projekta določena v drugačni enoti kot enota v vrstici podizvajalske pogodbe, sistem za izračun cene na enoto uporabi pretvorbo enote. |
| Delna vsota | To je polje samo za branje, ki se samodejno izračuna kot **Količina x cena enote**, če sta vneseni vrednosti tako količine kot cene enote. Če je prazno bodisi polje količina, cena enote ali pa sta prazna oba, lahko vrednost vnesete v polje. |
| Prometni davek |  Vnesite znesek prometnega davka. |
| Skupni znesek | Skupni znesek vrstice podizvajalske pogodbe po obdavčitvi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
