---
title: Vrstice računa dobavitelja za mejnike
description: V tem članku je razloženo, kako ustvariti vrstice računa dobavitelja za mejnike v podizvajalski pogodbi.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261049"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Vrstice računa dobavitelja za mejnike

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun dobavitelja v Microsoftu Dynamics 365 Project Operations lahko ima vrstice računa dobavitelja za mejnike, ki so opredeljeni v vrstici podizvajalca. Vodje projektov lahko uporabijo vrstice računa dobavitelja za mejnike, da zabeležijo stroške storitev, ki so nabavljene kot stroški na podlagi mejnikov, ki nastanejo pri storitvah ali izdelkih, nabavljenih za projekt.

Vrstice računa dobavitelja za mejnike se morajo vedno sklicevati na vrstico podizvajalca, ki ima metodo zaračunavanja po fiksni ceni. Ko se vrstica računa dobavitelja za mejnike sklicuje na vrstico podizvajalske pogodbe, bodo vodje projektov lahko primerjali in preverili osnovne stroške časa, izdatke ali materiale, ki se sklicujejo na to vrstico podizvajalske pogodbe, z mejnikom, ki ga je fakturiral prodajalec.

Naslednja tabela ponuja informacije o poljih v vrsticah računa dobavitelja za mejnike.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa dobavitelja za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec pri vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis storitev, ki jih prodajalec fakturira v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bile naročene storitve. Seznam podizvajalskih postavk, ki jih je mogoče izbrati, je omejen na postavke na izbrani podizvajalski pogodbi. | Ko je v vrstici računa dobavitelja za mejnike izbrana podizvajalska vrstica, se **Vloga** in **Kategorija transakcije** polja in polja, povezana z izdelkom, niso pomembna in niso na voljo. The **Količina**, **·**, in **Skupina enot** polja prav tako niso ustrezna za vrstice računa dobavitelja na podlagi mejnikov. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. | Ni priprav ali omejitev |
| Razred transakcije | Izberite **Mejnik** za evidentiranje računa dobavitelja za opravljen mejnik, ki je bil opredeljen v podizvajalski vrstici. | Ni priprav ali omejitev |
| Mejnik | Izberite mejnik, ki je definiran v povezani podizvajalski vrstici, ki je označena kot **Pripravljen za fakturiranje**. | Mejniki podizvajalske linije, ki imajo status **Pripravljen za fakturiranje** lahko izberete v vrstici računa dobavitelja. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, ki se fakturirajo. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime projektne naloge, za katero so bile uporabljene storitve, ki se fakturirajo. To polje je na voljo le, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja z razredom transakcij v povezani vrstici podizvajalske pogodbe, ki je zabeležena pri kateri koli nalogi projekta. Če se vrstica računa dobavitelja ne sklicuje na vrstico podizvajalca in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z nobenimi neobračunanimi dejanskimi vrednostmi prodaje. V tem primeru, če je nastavljeno obračunavanje na podlagi nalog, stroškov morda ne bo mogoče zaračunati končnemu kupcu. |
| Znesek mejnika | Vnesite vrednost mejnika, ki je definiran na podizvajalski vrstici, ki je pripravljena za fakturiranje. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa dobavitelja, vključno z davki. To polje se izračuna kot *Znesek mejnika* + *Davek od prodaje*. | Ni priprav ali omejitev |

> [!NOTE]
> Ko je ustvarjena vrstica računa dobavitelja, ki se sklicuje na mejnik vrstice podizvajalca, se status mejnika podizvajalca posodobi na **Ustvarjen račun dobavitelja**. Potem, ko je ta račun dobavitelja potrjen, se status mejnika podizvajalske vrstice posodobi na **Račun dobavitelja potrjen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
