---
title: Ustvarjanje naprednih pogodb za obračunavanje na podlagi napredka
description: Ta članek pojasnjuje, kako ustvariti projektne pogodbe, da boste lahko ustvarili račune za stranke na podlagi odstotka opravljenega dela.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26fe072b8241c7fdc96629f534e33a8fe53d3164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913686"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Ustvarjanje naprednih pogodb za obračunavanje na podlagi napredka
[!include [banner](../includes/banner.md)]

Ta članek pojasnjuje, kako ustvariti projektne pogodbe, da boste lahko ustvarili račune za stranke na podlagi odstotka opravljenega dela. Zneski računov se samodejno izračunajo za proračunske kategorije dela, ki ste jih nastavili za projekt. Čas računa je nastavljen, ko se s stranko dogovorite za projektno pogodbo.

S postopki v tem članku nastavite pogodbo, z njo povezani projekt in obračunska pravila, ki izračunajo zneske računov za proračunske kategorije del, ki ste jih nastavili za projekt.

Ko ustvarite pogodbo in projekt, lahko nastavite podrobnosti o projektu. Na primer, določite lahko dejavnosti in projektu dodelite delavce.

## <a name="example"></a>Primer

Vaša organizacija je podjetje za razvoj programske opreme. Strinjate se, da boste za stranko razvili paket za obračun plač za skupno plačilo v višini 20.000 ameriških dolarjev. Vaša organizacija se strinja, da bo stranki izdala račune, ko boste izpolnili določene odstotke projekta. Za delo nastavite naslednje projektne kategorije, da jih lahko uporabite v postopku obračunavanja:

- Svetovanje
- Oblikovanje
- Namestitev

Nastavite tudi obračunska pravila, ki samodejno izračunajo zneske računov za delež opravljenega projektnega dela za posamezno kategorijo.

Upravitelj proračuna izdela proračun za kategorije projekta. Količina opravljenega dela se samodejno izračuna kot odstotek dejanskega dela v primerjavi s predvidenimi zneski.

## <a name="prerequisites"></a>Zahteve

Preden ustvarite projekt, ki uporablja obračunska pravila, morate nastaviti zaporedja števil za obračunska pravila in dnevnik dajatev, ki se uporablja za knjiženje obračuna napredka.

1. Odprite **Vodenje projektov in računovodstvo** \> **Nastavitev** \> **Vodenje projekta in računovodski parametri**.
2. Na strani **Vodenje projekta in računovodski parametri** na zavihku **Zaporedja števil** nastavite zaporedje števil, ki ga želite uporabiti pri ustvarjanju obračunskih pravil.
3. Odprite **Vodenje projektov in računovodstvo** \> **Dnevniki** \> **Dajatev**.
4. Na strani **Dnevnik dajatev** izberite **Novo** in vnesite ime dnevnika.

## <a name="create-a-contract-for-progress-billings"></a>Ustvarjanje pogodbe za obračun napredka

S tem postopkom ustvarite projektno pogodbo za projekt s fiksno ceno. Račun za projekt ustvarite, ko je opravljen določen odstotek dela za projekt.

1. Odprite **Vodenje projektov in računovodstvo** \> **Projekti** \> **Projektne pogodbe**.
2. Na strani **Projektne pogodbe** izberite **Novo**.
3. V pogovornem oknu **Nova projektna pogodba** nastavite naslednja polja:

    - **Ime**
    - **Vrsta financiranja**
    - **Vir financiranja**
    - **Prodajna valuta** – ta valuta se privzeto uporablja za račune strank, ki so povezani s projektno pogodbo. Vendar lahko prodajno valuto spremenite za posamezen račun za stranko.

4. Izberite **V redu**. Podatki se kopirajo v glavo strani **Projektne pogodbe**.
5. Na strani **Projektne pogodbe** izpolnite ostale potrebne podatke za projekt.

## <a name="create-a-project-for-progress-billings"></a>Ustvarjanje projekta za obračun napredka

Upoštevajte ta navodila, da ustvarite projekt in morebitne podprojekte, povezane s projektno pogodbo.

1. Odprite **Vodenje projekta in računovodstvo** \> **Projekti** \> **Vsi projekti**.
2. Na strani **Vsi projekti** izberite **Novo**.
3. V pogovornem oknu **Nov projekt** v polju **Vrsta projekta** izberite **Čas in material**.
4. Izberite skupino projektov. Skupina projektov opredeli podatke o objavljanju za projekte, ki so dodeljeni skupini.
5. Izberite **Ustvarjanje projekta**.
6. Ko je projekt ustvarjen, nastavite stopnjo projekta na **V teku**.

## <a name="create-a-budget-for-a-project"></a>Ustvarjanje proračuna za projekt

Kategorije proračuna se uporabljajo za samodejni izračun zneskov računov za delež opravljenega dela za posamezno kategorijo. Upoštevajte ta navodila, da ustvarite kategorije proračuna za ocenjene stroške.

1. Odprite **Vodenje projekta in računovodstvo** \> **Projekti** \> **Vsi projekti**.
2. Na strani **Vsi projekti** izberite in odprite želeni projekt.
3. Na strani **Projekti** v podoknu za dejanja se pomaknite do zavihka **Načrt** in v skupini **Proračun** izberite **Proračun projekta**.
4. Na strani **Proračun projekta** vnesite ocenjeni strošek za vsako kategorijo v projektu.

## <a name="create-billing-rules-for-progress-billings"></a>Ustvarjanje obračunskih pravil za obračun napredka

1. Odprite **Vodenje projektov in računovodstvo** \> **Projekti** \> **Projektne pogodbe**.
2. Na strani **Projektne pogodbe** izberite in odprite projektno pogodbo.
3. Na strani projektne pogodbe na zavihku za hitri dostop **Obračunska pravila** izberite **Dodaj**.
4. Na strani **Obračunsko pravilo** v polju **Vrsta vrstice** izberite **Napredek**.
5. Na zavihku za hitri dostop **Podrobnosti vrstice obračunskega pravila** v polje **Vrednost pogodbe** vnesite skupno vrednost pogodbe.
6. V polju **Kategorija** izberite kategorijo, v katero želite objaviti transakcijo dajatve.
7. V polju **Projekt** izberite projekt, ki uporablja to obračunsko pravilo.
8. Izbirno: obračunsko pravilo dodelite dodatnim projektom. Na zavihku za hitri dostop **Projekt** v razdelku **Razpoložljivi projekti** izberite projekt in nato izberite puščico desno, da dodate projekt v razdelek **Izbrani projekti**.
9. Izbirno: izračunajte odstotno vrednost, ki jo kupec zadrži pri plačilih za račun. Na zavihku za hitri dostop **Pogoji zadržanja plačila** izberite vir financiranja in nato v polju **Odstotek zadrževanja** vnesite odstotek zadrževanja.
10. Ponovite te korake, da ustvarite dodatna obračunska pravila za projektno pogodbo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]