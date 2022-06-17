---
title: Vrstice računa dobavitelja za mejnike
description: V tem članku je razloženo, kako ustvariti vrstice računov dobavitelja za mejnike podizvajalske pogodbe.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931350"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Vrstice računa dobavitelja za mejnike

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun prodajalca v Microsoftu Dynamics 365 Project Operations lahko ima vrstice računov prodajalca za mejnike, ki so opredeljeni v vrstici podizvajalcev. Vodje projektov lahko uporabljajo vrstice računov prodajalca za mejnike, da evidentirajo stroške storitev, ki so nabavljene, kot stroške na podlagi mejnikov, ki nastanejo pri storitvah ali izdelkih, ki so nabavljeni za projekt.

Vrstice računov prodajalca za mejnike se morajo vedno sklicevati na vrstico podizvajalcev, ki ima način obračunavanja s fiksno ceno. Ko se vrstica faktur prodajalca za mejnike sklicuje na vrstico podizvajalcev, bodo vodje projektov lahko uskladili in preverili osnovne stroške časa, stroškov ali materiala, ki se sklicujejo na to vrstico podizvajalcev, z mejnikom, ki ga zaračunava prodajalec.

Naslednja tabela vsebuje informacije o poljih v vrsticah računov prodajalca za mejnike.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa prodajalca za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računov prodajalca. |
| Description | Kratek opis storitev, ki jih prodajalec zaračunava v vrstici faktur za dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun prodajalca izbrana podizvajalska pogodba, bodo vse vrstice na računu prodajalca podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa prodajalca, ki se sklicujejo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bile storitve naročene. Seznam vrstic podizvajalcev, ki jih je mogoče izbrati, je omejen na vrstice v izbrani podizvajalski pogodbi. | Ko je vrstica podizvajalcev izbrana v vrstici računa prodajalca za mejnike, se **Vloga** in **Kategorija transakcije** polja in polja, povezana z izdelkom, niso pomembna in niso na voljo. The **Količina**, **·**, in **Skupina enot** polja prav tako niso pomembna za vrstice računov dobavitelja, ki temeljijo na mejnikih. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa prodajalca zabeležen v projektu. | Ni priprav ali omejitev |
| Razred transakcije | Izberite **Mejnik** zabeležiti račun prodajalca za zaključen mejnik, ki je bil opredeljen v vrstici podizvajalcev. | Ni priprav ali omejitev |
| Mejnik | Izberite mejnik, ki je opredeljen v povezani vrstici podizvajalcev, ki je označena kot **Pripravljen za fakturiranje**. | Mejniki vrstice podizvajalcev, ki imajo status **Pripravljen za fakturiranje** lahko izberete v vrstici računa prodajalca. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, ki se zaračunavajo. | To polje je obvezno in ga ne morete pustiti prazno. |
| opravilo, | Ime projektne naloge, za katero so bile uporabljene storitve, ki se zaračunavajo. To polje je na voljo samo, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa prodajalca z razredom transakcij v povezani vrstici podizvajalcev, ki je zabeležena pri kateri koli nalogi projekta. Če se vrstica računa prodajalca ne sklicuje na vrstico podizvajalcev in je to polje prazno, dejanski stroški, ki jih ustvari vrstica fakture prodajalca, ne bodo povezani z nobeno nezaračunano dejansko prodajo. V tem primeru, če je nastavljeno obračunavanje na podlagi opravil, stroškov morda ne bo mogoče zaračunati končnemu kupcu. |
| Znesek mejnika | Vnesite vrednost mejnika, ki je opredeljen v vrstici podizvajalcev, ki je pripravljen za fakturiranje. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa prodajalca, vključno z davki. To polje se izračuna kot *Mejni znesek* + *Davek od prodaje*. | Ni priprav ali omejitev |

> [!NOTE]
> Ko je ustvarjena vrstica računa prodajalca, ki se sklicuje na mejnik vrstice podizvajalcev, se stanje mejnika podizvajalske pogodbe posodobi na **Račun prodajalca je ustvarjen**. Nato, ko je ta račun prodajalca potrjen, se status mejnika vrstice podizvajalcev posodobi na **Račun prodajalca potrjen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
