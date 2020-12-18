---
title: Ustvarjanje medpodjetniških računov za stranke in dobavitelje
description: Ta tema vsebuje informacije o tem, kako ustvariti medpodjetne račune za stranke in dobavitelje.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595556"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Ustvarjanje medpodjetniških računov za stranke in dobavitelje

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Projektni računovodja v izposojevalni pravni osebi ustvari medpodjetni račun za stranko za stroške projekta, ki se prenesejo na izposojevalno pravno osebo. Po odobritvi in knjiženju medpodjetnega računa za stranko posojilna pravna oseba pošlje medpodjetni račun izposojevalni pravni osebi.

Projektni računovodja za posojilno pravno osebo lahko vzpostavi paketni postopek za redno generiranje medpodjetnih računov. Projektni računovodja določi merila, kot so posebni projekti, za izdelavo medpodjetnih računov v paketu.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Ročno ustvarite medpodjetni račun za stranke za projektne transakcije 

Uporabite ta postopek za ročno ustvarjanje medpodjetnega računa za stranke za projektne transakcije. Poiščite ure, ki so si jih pisali delavci na projektih v izposojevalnih pravnih osebah, in stroške, ki jih je imela vaša pravna oseba v imenu izposojevalnih pravnih oseb. Iščete lahko po imenu pravne osebe, številki projektne pogodbe, številki projekta, časovnem obdobju ali kateri koli kombinaciji teh možnosti. V rezultatih iskanja izberite transakcije, ki jih želite dodati na medpodjetni račun.

1. V aplikaciji Dynamics 365 Finance odprite **Upravljanje projektov in računovodstvo** > **Računi za projekt** > **Medpodjetni računi za stranke**. Na strani s seznamom **Medpodjetni računi za stranke** v akcijskem podoknu izberite **Novo**.
2. Na strani **Ustvarjanje medpodjetnega računa** v polju **Pravna oseba** izberite posojilno pravno osebo.
3. Izbirno: Vnesite izbrano projektno pogodbo in številko projekta.
4. Izberite časovno obdobje, da zožite iskanje. V polji **Začetni datum** in **Končni datum** vnesite želene datume. V rezultatih iskanja so prikazane samo medpodjetne transakcije, ki so bile knjižene v tem časovnem obdobju.
5. Nastavite **Napredni parameter vrstice dnevnika projekta** na **Da** in izberite **Iskanje**.
6. V rezultatih iskanja izberite transakcije, ki jih želite vključiti v predlog medpodjetnega računa in nato izberite **V redu**.
7. Na strani **Medpodjetni račun za stranko** se prikažejo medpodjetne projektne transakcije, ki ste jih izbrali med prikazanimi rezultati iskanja. Če želite spremeniti transakcije, preden pošljete račun posojilni pravni osebi, naredite naslednje:
  
    1. Odprite stran **Ustvarjanje predloga računa**. Izberite dodatne medpodjetne transakcije za trenutni račun in izberite **Dodaj vrstico**.
    2. Če želite odstraniti vrstico, jo izberite in kliknite **Odstrani**.
    3. Oglejte si komentarje, razloge, finančne razsežnosti in druge informacije o izbrani vrstici na hitrem zavihku **Vrstice računov**.
    
8. Za knjiženje medpodjetnega računa za stranko izberite **Knjiži** v akcijskem podoknu.

> [!NOTE]
> Če vaša organizacija zahteva pregled medpodjetnih računov pred knjiženjem, lahko skrbnik sistema nastavi potek dela za medpodjetne račune. Če potek dela ni nastavljen za medpodjetne račune, lahko poknjižite medpodjetni račun.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Ustvarjanje paketnega opravila za medpodjetne račune

Za vse izposojevalne pravne osebe lahko ustvarite več medpodjetnih računov hkrati. Z uporabo funkcije iskanja lahko na primer iščete vse transakcije, ki jih knjižijo zaposleni v izposojevalni pravni osebi in ki so povezane s projekti, ki jih upravljajo druge pravne osebe. Nato lahko za vsako izposojevalno pravno osebo ustvarite medpodjetni račun za transakcije, ki so navedene v rezultatih iskanja.

1. Odprite **Upravljanje projektov in računovodstvo** > **Periodično** > **Računi za projekt** > **Ustvarjanje medpodjetnih računov za stranke**.
2. Na strani **Ustvarjanje medpodjetnih računov za stranke** v polju **Podjetje** izberite pravno osebo, ki ji boste izdali račun. Če ne izberete podjetja, se bodo pri vseh izposojevalnih pravnih osebah prikazale vse transakcije, ki ustrezajo iskalnim pogojem.
3. V možnosti **Ustvari en račun na** izberite, ali želite ustvariti račun za medpodjetne transakcije, ki temeljijo na projektu ali izposojevalni pravni osebi.
4. Izbirno: Če želite izbrati določen projekt in projektno pogodbo, za katero želite ustvariti medpodjetne račune, kliknite **Izberi**. Na strani **Povpraševanje** v polju **Merila** izberite projektno pogodbo, številko projekta ali oboje in nato kliknite **V redu**.
5. V zavihku **Paket** nastavite paketni postopek za ustvarjanje medpodjetnih računov v rednem časovnem zamiku. Za več informacij glejte [Pošiljanje obdelave paketnega opravila iz obrazca](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Za knjiženje medpodjetnih računov izberite **Knjiži** v akcijskem podoknu.

> [!NOTE]
> Če vaša organizacija zahteva pregled medpodjetnih računov pred knjiženjem, lahko skrbnik sistema nastavi potek dela za medpodjetne račune. Če potek dela ni nastavljen za medpodjetne račune, lahko poknjižite medpodjetne račune.

## <a name="post-the-intercompany-vendor-invoice"></a>Knjiženje medpodjetnega računa za dobavitelja

Računovodja računa v izposojevalni pravni osebi lahko pregleda medpodjetne čakajoče račune za dobavitelje, ko je knjižen ustrezen medpodjetni račun za stranko. V storitvi Finance v izposojevalni pravni osebi odprite **Obveznosti** > **Računi** > **Čakajoči račun za dobavitelja**. Številka čakajočega računa se bo ujemala s številko medpodjetnega računa za stranko. Preverite, ali je račun pravilen, in ga poknjižite. S knjiženjem medpodjetnega računa za dobavitelja se ustvari projektna transakcija v podknjigi in glavni knjigi, ki odraža transakcijske stroške v izposojevalni pravni osebi.
