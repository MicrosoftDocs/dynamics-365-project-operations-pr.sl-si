---
title: Delovni prostor za vnos časa v projektu prek mobilne naprave
description: Ta tema vsebuje informacije o delovnem prostoru za vnos časa v projektu prek mobilne naprave. Ta delovni prostor omogoča uporabnikom, da vnesejo čas v projektu in ga shranijo prek mobilne naprave.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 04024cc005b67b8f4e5821b22be65cfd1822b2414c85e1fbb75c3b2ac4339dc4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989571"
---
# <a name="project-time-entry-mobile-workspace"></a>Delovni prostor za vnos časa v projektu prek mobilne naprave

[!include [banner](../includes/banner.md)]

Ta tema vsebuje informacije o delovnem prostoru za **vnos časa v projektu** prek mobilne naprave. Ta delovni prostor omogoča uporabnikom, da vnesejo čas v projektu in ga shranijo prek mobilne naprave.

Ta mobilni delovni prostor je namenjen uporabi z mobilno aplikacijo Dynamics 365 Unified Ops. 

## <a name="overview"></a>Pregled
Projektni viri so v okviru njihovega vsakdanjega dela pogosto na lokaciji ali poti. Delovni prostor za **vnos časa v projektu** prek mobilne naprave omogoča uporabnikom, da v projektu vnesejo porabljeni čas, ali čas, ki se ne obračunava, prek želene mobilne naprave. Zato lahko projektni viri beležijo vnose časa kadar koli in kjer koli. Ogledajo si lahko tudi že zapisane vnose časa. 

Natančneje, v delovnem prostoru za **vnos časa v projektu** prek mobilne naprave lahko uporabniki izvajajo ta opravila:

-   Za kateri koli izbrani datum vnesite število ur, ki ste jih porabili za določeno opravilo.
-   Iščite po imenu projekta ali stranki, da najdete projekt, za katerega želite vnesti čas.
-   Določite kategorijo in dejavnost za porabljeni čas.
-   Za projekt določite čas kot porabljeni čas ali čas, ki se ne obračunava.
-   Po želji vnesite kakršne koli zunanje ali notranje komentarje.

## <a name="prerequisites"></a>Zahteve
Predpogoji se razlikujejo glede na različico rešitve Microsoft Dynamics 365, ki je uvedena za organizacijo.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Predpogoji, če uporabljate Dynamics 365 Finance
Če je bila za vašo organizacijo uvedena rešitev Finance, mora skrbnik sistema objaviti delovni prostor za **vnos časa v projektu** prek mobilne naprave. Za navodila glejte [Objava mobilnega delovnega prostora](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Predpogoji, če uporabljate različico 1611 s posodobitvijo platforme na 3 ali novejšo
Če je bila za vašo organizacijo uvedena različica 1611 s posodobitvijo platforme na 3 ali novejšo, mora sistemski skrbnik izpolniti naslednje predpogoje. 

<table>
<thead>
<tr class="header">
<th>Predpogoj</th>
<th>Vloga</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Uvedba hitrega popravka KB 4018050.</td>
<td>Skrbnik sistema</td>
<td>KB 4018050 je posodobitev X ++ ali hitri popravek za metapodatke, ki vsebuje delovni prostor za <strong>vnos časa v projektu</strong> prek mobilne naprave. Za uvedbo hitrega popravka KB 4018050 v sistem mora skrbnik sistema upoštevati naslednje korake.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Prenos hitrega popravka za metapodatke iz portala Lifecycle Services (LCS) storitve Microsoft Dynamics</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Namestitev hitrega popravka za metapodatke</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Ustvarjanje paketa za uvajanje</a> z modeloma <strong>ApplicationSuite</strong> in <strong>ProjectMobile</strong>, ki ga nato naložite na portal LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Uporaba paketa za uvajanje</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Objava delovnega prostora za<strong> vnos časa v projektu</strong> prek mobilne naprave.</td>
<td>Skrbnik sistema</td>
<td>Glejte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Objava mobilnega delovnega prostora</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Prenos in namestitev mobilne aplikacije

Prenos in namestitev mobilne aplikacije Finance and Operations:

-   [Za telefone s sistemom Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Za naprave iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijavite se v mobilno aplikacijo
1.  Zaženite aplikacijo v mobilni napravi.
2.  Vnesite URL za Dynamics 365.
3.  Ko se prvič prijavite, boste pozvani k vnosu uporabniškega imena in gesla. Vnesite svoje poverilnice.
4.  Po prijavi se prikažejo razpoložljivi delovni prostori za vaše podjetje. Če skrbnik sistema pozneje objavi nov delovni prostor, boste morali osvežiti seznam mobilnih delovnih prostorov.

[![Povlecite za osvežitev.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Vnesite čas z uporabo delovnega prostora za vnos časa v projektu prek mobilne naprave
1.  V mobilni napravi izberite delovni prostor za **vnos časa v projektu**.
2.  Izberite možnost **Vnos časa**. Prikazani so koledarski datumi za trenutni teden.
3.  Za izbrani datum izberite **Dejanja** &gt; **Nov vnos**.
4.  Vnesite število ur, ki jih želite zabeležiti.
5.  Izberite projekt za vnos časa. Seznam prikazuje projekte, ki so naloženi v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Če želite več informacij, preberite [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Če vašega projekta ni na seznamu, izberite **Iskanje**. Iščite po imenu ali preklopite na iskanje po imenu projekta ali kupcu.
7.  Izberite kategorijo. Seznam prikazuje kategorije, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Če želite več informacij, preberite [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Če vaše kategorije ni na seznamu, izberite **Iskanje**. Poiščite po kategoriji ali preklopite na iskanje po imenu kategorije.
9.  Izberite dejavnost. Seznam prikazuje kategorije, ki so naložene v vašo aplikacijo za uporabo brez povezave. Privzeto je naloženih 50 elementov, vendar jih lahko razvijalec spremeni. Če želite več informacij, preberite [Platforma Mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Če vaše dejavnosti ni na seznamu, izberite **Iskanje**. Iščite po številki dejavnosti ali preklopite na iskanje po namenu.

11. Izberite lastnost vrstice.
12. Izbirno: vnesite kakršne koli zunanje in notranje komentarje.
13. Izberite **Dokončano**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]