---
title: Poizvedba glede načrta porabe zveznih subvencij
description: Ta članek vsebuje informacije o poizvedbi glede načrta porabe zveznih subvencij.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 00f9e97b9a6b3e8fe5e9cf9143e670612869b84c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916676"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Poizvedba glede načrta porabe zveznih subvencij

[!include [banner](../includes/banner.md)]

V skladu z okrožnico Urada za upravljanje proračuna A-133 (OMB) za agencije, ki prejemajo zvezna sredstva, veljajo revizijske zahteve, ki so znane tudi kot enotne revizije. Revizijski postopek se uporablja za redno poročanje o prihodkih in odhodkih glede zveznih subvencij. Del poročila o enotni reviziji vključuje načrt porabe zveznih subvencij (SEFA).

Poizvedba glede načrta porabe subvencij zveznih držav vključuje naziv in številko kataloga za zvezno pomoč domačim entitetam (CFDA), številko subvencije, leto dodelitve, ime zvezne agencije, ki zagotavlja sredstva, in ime prehodne entitete. Povpraševanje je za določeno obdobje. To obdobje je običajno enako obdobju računovodskega izkaza, ki je proračunsko leto.

Poizvedba vključuje subvencije, ki imajo datume projekcije v izbranem časovnem obdobju. Stolpec poizvedbe **Agencija, ki podeljuje subvencijo** prikazuje prejemnika subvencije oz. v primeru prehodne entitete za podelitev agencijo, ki podeljuje subvencijo. V primeru prisotnosti prehodne entitete stolpec **Prehodna agencija** prikazuje prejemnika subvencije. V primeru odsotnosti prehodne entitete je stolpec **Prehodna agencija** prazen.

## <a name="set-up-the-cfda-clusters"></a>Nastavitev gruč CFDA

Nastaviti morate gruče CFDA, ki jih je mogoče povezati s številkami CFDA pri poizvedbi glede načrta porabe zveznih subvencij.

1. Izberite **Vodenje projektov in računovodstvo \> Nastavitev \> Subvencije \> Gruče kataloga za zvezno pomoč domačim entitetam**.
2. Izberite **Novo**, da ustvarite gručo CFDA.
3. Vnesite ime gruče.
4. Izberite **Shrani**, da shranite spremembe.

## <a name="set-up-cfda-numbers"></a>Nastavitev številk CFDA

Nastaviti morate številke CFDA, ki jih je mogoče dodati subvencijam in vključiti v poizvedbo glede načrta porabe zveznih subvencij.

1. Izberite **Vodenje projektov in računovodstvo \> Nastavitev \> Subvencije \> Številke kataloga za zvezno pomoč domačim entitetam**.
2. Izberite **Novo**, da ustvarite številko CFDA.
3. V stolpec **Številka** vnesite številko CFDA.
4. Pritisnite **tabulatorko**.
5. V stolpec **Opis** vnesite naziv CFDA.
6. Pritisnite **tabulatorko**.
7. Izbirno: v polje **Programska gruča** dodajte ustrezno gručo CFDA.
8. Izberite **Shrani**, da shranite spremembe.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Vzpostavitev subvencij za poročanje glede poizvedbe glede načrta porabe zveznih subvencij

1. Izberite **Vodenje projektov in računovodstvo \> Subvencije \> Subvencije** in izberite obstoječo subvencijo.
2. Na zavihku za hitri dostop **Nastavitev** v polju **Katalog za zvezno pomoč domačim entitetam** dodelite številko CFDA. Številka CFDA pri subvenciji določa gručo CFDA za poročanje.
3. Na zavihku za hitri dostop **Podatki za stik** vnesite podatke o dajalcu subvencije tako, da upoštevate ta navodila:

    1. V polju **Prejemnik subvencije** vnesite prejemnika, ki je odgovoren za subvencijo. Za obstoječo subvencijo so ti podatki morda že vneseni.
    2. Navedite, ali prejemnik subvencije zagotavlja tudi sredstva. Če prejemnik subvencije zagotavlja tudi sredstva, pustite potrditveno polje **Prehodno** prazno. Če sredstva zagotavlja druga stranka ter je prejemnik subvencije odgovoren za porabo in spremljanje denarja, izberite potrditveno polje **Prehodno**.

4. Če ste izbrali potrditveno polje **Prehodno** v prejšnjem koraku, v polje **Agencija, ki podeljuje subvencijo** vnesite stranko, ki je zagotovila subvencijo. Agencija, ki podeljuje subvencijo, in prejemnik subvencije ne moreta biti ista stranka.

Tu je primer subvencije s prehodno entiteto:

Zvezna vlada je financirala infrastrukturni projekt za zvezno državo. Zvezna vlada je zvezni državi dala denar, da bi ga slednja porabila. V tem primeru je zvezna vlada agencija, ki podeljuje subvencijo, zvezna država pa prejemnik subvencije.

> [!NOTE] 
> Ko prvič vklopite funkcijo, bodo začetne številke CFDA vnesene z uporabo obstoječih številk pri subvencijah.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Izključitev subvencij v zvezi s poročanjem SEFA glede na vrsto subvencije

1. Odprite razdelek **Vodenje projektov in računovodstvo \> Nastavitev \> Subvencije \> Vrste subvencij**.
2. Na zavihku za hitri dostop **Privzeti podatki** izberite potrditveno polje **Izključi iz načrta porabe zveznih subvencij**.
3. Izberite **Shrani**, da shranite spremembe.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Zagon poizvedbe glede načrta porabe zveznih subvencij

1. Izberite **Vodenje projektov in računovodstvo \> Poizvedbe in poročila \> Poizvedba glede subvencije \> Načrt porabe zveznih subvencij**.
2. V razdelku **Parametri** upoštevajte ta navodila:

    1. V polju **Datumski interval** izberite kodo za datumski interval. Lahko pa določite datumski interval tudi prek polj **Začetni datum** in **Končni datum**.
    2. Izbirno: če želite v poizvedbo kot prihodek vključiti samo obračunane transakcije, nastavite možnost **Vključi samo obračunane prihodke** na **Da**.

## <a name="columns"></a>Št. stolpcev

Poizvedba glede načrta porabe zveznih subvencij vključuje naslednje stolpce:

- Ime gruče kataloga za zvezno pomoč domačim entitetam
- Agencija, ki podeljuje subvencijo
- Prehodna agencija
- Ime subvencije
- ID subvencije
- ID vloge za subvencijo
- Katalog za zvezno pomoč domačim entitetam
- Potrdila
- Izdatki


[!INCLUDE[footer-include](../includes/footer-banner.md)]