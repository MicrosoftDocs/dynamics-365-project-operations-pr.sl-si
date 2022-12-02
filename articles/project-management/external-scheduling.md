---
title: Zunanje načrtovanje
description: Ta članek vsebuje informacije o zunanjem načrtovanju.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736996"
---
# <a name="external-scheduling"></a>Zunanje načrtovanje

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Način zunanjega načrtovanja omogoča izvorno ustvarjanje, posodabljanje in brisanje entitet, ki so povezane s strukturiranimi členitvami dela (SČD), vendar brez trenutnih omejitev, ki jih uveljavlja storitev Microsoft Project for the Web. Zagotavlja tudi omejeno preverjanje veljavnosti. Ta način naj uporabljajo samo naslednje stranke:

- Stranke, ki imajo orodja, potrebna za določanje SČD izven logike načrtovanja, ki jo zagotavlja aplikacija Project Operations
- Stranke, ki morajo upravljati hierarhijo načrtovanja, odvisnosti ali trajanje opravila

> [!IMPORTANT]
> Podatki, ki niso pravilno vneseni v entitete, povezane s SČD, morda ne bodo upodobljeni v mreži za usklajevanje virov, mreži ocen, mreži za sledenje ali mreži za dodelitev virov.

## <a name="configuration"></a>Konfiguracija

Ta funkcija je privzeto omogočena. Vendar na vnaprej pripravljeni glavni strani za projekte povezano polje privzeto ni vidno. Če želite omogočiti polje, na portalu Maker Portal odprite glavno stran za entiteto projekta in izberite polje **Mehanizem za načrtovanje** in nato spremenite polje v **Privzeto vidno**. Če ne uporabljate vnaprej pripravljene glavne strani projekta, uredite obstoječo stran in ji dodajte polje **Mehanizem za načrtovanje**.

## <a name="settings"></a>Nastavitve

Če želite uporabiti način zunanjega načrtovanja, morate najprej ustvariti nov projekt in izbrati mehanizem za načrtovanje **Zunanje načrtovano** na spustnem seznamu na glavni strani projekta. Ko je ta način nastavljen za projekt, ga ni več mogoče spremeniti.

## <a name="viewing-the-wbs"></a>Ogled SČD

Če je projekt zunanje načrtovan, je dostop do storitve Project for the Web za ta projekt omejen. Če si želite ogledati SČD, morate iti na mrežo za sledenje, kjer je prikazan celoten SČD.

## <a name="creating-and-editing-the-wbs"></a>Ustvarjanje in urejanje SČD

Če je za projekt omogočeno zunanje načrtovanje, morate opredeliti podatke za vse entitete, povezane s SČD, vključno z opravili, člani ekipe, dodelitvami virov in odvisnostmi.

Naslednja slika prikazuje podatkovni model za načrtovanje projekta.

![Podatkovni model za načrtovanje projekta.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkcionalne omejitve

Naslednji postopki niso dovoljeni za projekte, načrtovane zunaj.

### <a name="project-planning"></a>Načrtovanje projekta

- **Kopiraj projekt** – ta postopek ni podprt za projekte, načrtovane zunaj.
- **Premakni projekt** – spremembe začetnega datuma projekta ne bodo premaknile začetka opravil ali dodelitev virov v SČD.
- **Posodabljanje vodje projektov** – spremembe vodje projektov na glavni strani projekta ne bodo samodejno ustvarile novega člana projektne ekipe, dokler projekt ni pretvorjen.
- **Posodabljanje predloge za delovne ure projekta** – spremembe predloge za delovne ure projekta ne bodo ponovno izračunale razporeda projekta.
- **Krivulje dodelitve virov** – ustvarjanje dodelitev virov ne bo samodejno posodobilo polja **mdyn\_PlannedWork**. To polje se uporablja za shranjevanje krivulj za prizadevanja za dodelitev virov. Če v mreži za dodelitev virov ali mreži za usklajevanje virov prikažete časovno razporejeno delo, morate določiti veljavne krivulje dodelitve virov. Te krivulje morajo biti pravilno oblikovane, tako da sprožijo izračun tako krivulj stroškov kot krivulj prodajne cene. Priporočamo, da ustvarite preskusni projekt, ki ga načrtuje storitev Project for the Web, in nato pregledate povezane podatke, da potrdite zahteve in oblikovanje.

### <a name="resource-management"></a>Upravljanje virov

- **Dopolnitev splošnih virov** – dopolnitev splošnih virov ni podprta za projekte, načrtovane zunaj. Poskusi dopolnitve aktivnih odprtih zahtev bodo ustvarili nove člane projektne ekipe, vendar ne bodo izbrisali splošnega člana ekipe ali zamenjali splošnega člana ekipe pri kateri koli obstoječi dodelitvi virov.
- **Brisanje člana ekipe** – izbris člana ekipe ne bo samodejno izbrisal dodelitev virov.

### <a name="quoting-and-contracting"></a>Ponudbe in sklepanje pogodb

- **Uvoz podrobnosti vrstice ponudbe in pogodbe** – ko se iz projekta uvozijo podrobnosti ponudbe ali pogodbe, je bila aplikacija preskušena tako, da podpira največ 500 nalog v WBA, na podlagi omejitve 20 dodelitev na opravilo.

### <a name="actuals-and-invoicing"></a>Dejanske vrednosti in izdaja računov

- Čeprav ni sprememb obstoječih preverjanj veljavnosti med SČD in finančnimi transakcijami, je pomembno, da se uskladite z vnaprej pripravljenim podatkovnim modelom, da zagotovite, da vse transakcije na nižji stopnji potekajo po pričakovanjih.
