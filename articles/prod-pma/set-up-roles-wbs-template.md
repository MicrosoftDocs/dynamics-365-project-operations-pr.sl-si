---
title: Nastavitev vlog za predloge strukturirane členitve dela
description: Ta tema vsebuje informacije o nastavitvi informacij o vlogah na predlogah strukturirane členitve dela.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a8363c1f94a974881df984869ee56bfc198ac5c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288669"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Nastavitev vlog za predloge strukturirane členitve dela

[!include [banner](../includes/banner.md)]

Projektni vodje lahko nastavijo predloge strukturirane členitve dela (SČD), ki jih lahko uporabijo, ko ustvarjajo SČD za nove projekte. Projektni vodje lahko dodajo vloge, ko ustvarijo predlogo. Uporabite naslednji postopek za dodelitev vloge predlogi SČD.

1. Izberite **Vodenje projektov in računovodstvo** > **Nastavitev** > **Projekti** > **Predloge strukturirane členitve dela**.
2. Izberite **Podrobnosti** za izbrano predlogo SČD.
3. Izberite opravilo na seznamu in nato v polju **Vloga** izberite vlogo za dodelitev opravilu.

## <a name="work-with-a-wbs"></a>Delo s SČD

Ustvarite lahko nov SČD, lahko pa kopirate SČD iz obstoječe predloge SČD. Projektni vodja lahko zlahka upravlja vire z dodeljevanjem vlog novim opravilom v SČD. Vloge je mogoče zamenjati po pridobitvi vira ali po prepoznavanju potrjenega vira za delo na opravilu. Ta prilagodljivost omogoča projektnim vodjem izvajanje naslednjih opravil:

- Prepoznavanje števila virov, ki so potrebni za delovne pakete SČD.
- Ocenjevanje stroškov projektov.
- Določanje predhodnega proračuna.
- Ocenjevanje trajanja dejavnosti na podlagi vlog in virov.
- Razvoj nekaterih načrtov vodenja projektov na podlagi razpoložljivih informacij o projektu.

Dodatne možnosti so bile dodane v SČD za boljšo uporabo funkcije iskanja virov.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnost</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dodelitve virov</td>
<td>Oglejte si dodeljene vire, datume, število ur in vrsto rezervacije za opravila v SČD.</td>
</tr>
<tr class="even">
<td>Samodejno ustvarjanje ekipe</td>
<td>Samodejno dodajte načrtovane vire z uporabo vlog, ki so povezane z opravilom. Storitev Finance samodejno predlaga načrtovane vire z uporabo analize odločitev z več merili, ki temelji na vlogah. Ko so bile vloge in obseg (ure) nastavljeni za opravila v SČD ter je bila struktura izdana, izberite <strong>Samodejno ustvarjanje ekipe</strong>. Zahtevano število načrtovanih virov se doda v SČD in zavihek <strong>Načrtovanje projekta in ekipe</strong>.</td>
</tr>
<tr class="odd">
<td>Vir (spustni seznam)</td>
<td>Na strani <strong>Zagon dodelitve vira</strong> lahko izberete vire za veljavne rezervacije ali začasne rezervacije na podlagi določenega trajanja. Prilagodite lahko nastavitve ogleda, da vidite in nastavite trajanje dejavnosti virov. Lahko izberete in dodelite vire na ravni delovnega paketa z uporabo naslednjih možnosti:
<ul>
<li><strong>Sprejem</strong> – Potrdite spremembe vira, ki je dodeljen opravilu.</li>
<li><strong>Preklic</strong> – Prekličite spremembe vira, ki je dodeljen opravilu.</li>
<li><strong>Samodejna dodelitev</strong> – Razpoložljivi zaposleni vir, ki ima ujemajočo se vlogo, je samodejno izbran in dodeljen izbranemu opravilu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na strani **Vsi projekti** izberite projekt **2. faza nadgradnje XYZ**.
2. Izberite **Načrtovanje** > **Dejavnosti** > **Strukturirana členitev dela**.
3. Izberite **Novo**, da dodate naslednje dejavnosti prve stopnje v SČD:

    - Zagon
    - Načrtovanje
    - Izvajanje
    - Spremljanje in nadzor
    - Zaprto

4. Nastavite datume in obseg (ure), kot je prikazano na naslednji sliki.

    [![Nastavitev datumov in obsega](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Izberite vrstico opravila **Zagon** in nato v polju **Vloga** izberite **Višji projektni vodja**.
6. Izberite **Objavi**.
7. V isti vrstici v polju **Vir** izberite **Daniel Goldschmidt**, nato pa izberite **Sprejem**.
8. Izberite vrstico opravila **Načrtovanje** in nato v polju **Vloga** izberite **Poslovni analitik**.
9. Izberite **Objava**, nato pa izberite **Samodejno ustvarjanje ekipe**.
10. V polju za sporočilo, ki se prikaže, izberite **Da**.
11. V polju **Vir** potrdite, da je vrednost **Poslovni analitik 1**.
12. Za vir **Poslovni analitik 1** odprite iskanje in izberite **Zagon dodelitev virov**. Nato izberite delavca za opravilo.
13. Izberite **Začasna rezervacija** &gt; **Polna zmogljivost**.

    > [!NOTE] 
    > Ne prejmete opozorila, da je navedeni vir zdaj 2, ker število virov ostaja 1.

14. Na strani **Strukturirana členitev dela** potrdite dodelitve virov na SČD in nato izberite **Shrani**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]