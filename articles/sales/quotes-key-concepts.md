---
title: Koncepti, enolični za ponudbe, ki temeljijo na projektih
description: Ta članek vsebuje informacije o ponudbah projektov v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824348"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepti, enolični za ponudbe, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Preden začnete uporabljati projektne ponudbe v Microsoftu Dynamics 365 Project Operations, se morate zavedati naslednjih ključnih pojmov.

## <a name="owning-company"></a>Lastniško podjetje

Podjetje lastnik predstavlja pravno osebo, ki je lastnik izvedbe projekta. Stranka v ponudbi mora biti veljavna stranka te pravne osebe v aplikacijah za finance in poslovanje. Valuta lastnika podjetja in valuta pogodbene enote, ki je izbrana na podlagi ponudbe na podlagi projekta, se morata ujemati.

## <a name="contracting-unit"></a>Pogodbena enota

Naročniška enota predstavlja oddelek ali prakso, ki je lastnik izvedbe projekta. Za vsako pogodbeno enoto lahko nastavite stroške virov. Ko podate stroške virov za vir v pogodbeni enoti, lahko nastavite različne stroškovne stopnje za vire, od katerih si pogodbena enota sposodi, ali za druge oddelke ali prakse v podjetju. Te stopnje stroškov se imenujejo transferne cene, izposoja virov ali menjalne cene. Ko nastavite stroške izposoje virov iz drugih oddelkov, lahko nastavite stopnje stroškov v valuti oddelka, ki posoja.

## <a name="cost-currency"></a>Valuta stroška

Stroškovna valuta v projektnih operacijah je valuta, v kateri se poroča o stroških. Ta valuta izhaja iz valute, ki je priložena polju **Pogodbena enota** v ponudbi, pogodbi in projektu. Stroške projekta je mogoče zabeležiti v kateri koli valuti. Vendar obstaja pretvorba valute iz valute, v kateri so bili zabeleženi stroški, v stroškovno valuto projekta.

Ker menjalni tečaji na platformi Dataverse ne morejo veljati na datum, se lahko skupne vrednosti stroškov na zaslonu sčasoma spremenijo, če posodobite menjalne tečaje valut. Stroški, ki se evidentirajo v bazi, pa ostanejo nespremenjeni, saj so zneski shranjeni v valuti, v kateri so nastali.

## <a name="sales-currency"></a>Prodajna valuta

Prodajna valuta v projektnih operacijah je valuta, v kateri so zabeleženi in prikazani ocenjeni in dejanski zneski prodaje. To je tudi valuta, v kateri se stranki izda račun za posel. Za projektno ponudbo je privzeta prodajna valuta nastavljena iz zapisa stranke ali računa in jo je mogoče spremeniti, ko je ponudba ustvarjena. Vendar prodajne valute ni mogoče spremeniti, ko je ponudba shranjena. Privzeti ceniki izdelkov in projektov so nastavljeni glede na prodajno valuto ponudbe.

Za razliko od stroškov lahko prodajne vrednosti beležimo **samo** v prodajni valuti.

## <a name="billing-method"></a>Način obračunavanja

Projekti imajo običajno pogodbene modele s fiksnimi honorarji in na podlagi porabe. V projektnih operacijah je pogodbeni model projekta predstavljen z metodo zaračunavanja. Način obračunavanja ima dve vrednosti: čas in material ter fiksno ceno.

- **Čas in material** – model sklepanja pogodb na podlagi porabe, kjer je vsak nastali strošek podprt z ustreznim prihodkom. Ko ocenite ali ustvarite več stroškov, se povečata tudi ustrezna predvidena in dejanska prodaja. Za podrobnosti ponudb, ki imajo ta način obračunavanja, lahko določite omejitve, ki se jih ne sme preseči. Na ta način lahko omejite dejanski prihodek. Omejitve, ki jih je treba preseči, ne vplivajo na predvideni prihodek.
- **Fiksna cena** – pogodbeni model s fiksnim honorarjem, pri katerem so prodajne vrednosti neodvisne od nastalih stroškov. Prodajna vrednost je fiksna in se ne spremeni, ko ocenjujete ali ustvarite več stroškov.

## <a name="project-price-lists"></a>Ceniki za projekte

Projektni ceniki so ceniki, ki se uporabljajo za vnos privzetih cen, ne stroškovnih stopenj, za čas, stroške in druge komponente, povezane s projektom. Cenikov je lahko več, vsak seznam pa ima lahko lastno datumsko veljavnost za vsako projektno ponudbo. Project Operations ne podpira prekrivajočih se datumov veljavnosti za cenike projektov.

## <a name="product-price-lists"></a>Ceniki za izdelke

Ceniki izdelkov so ceniki, ki se uporabljajo za vnos privzetih cen, ne stopenj stroškov, za linije izdelkov v ponudbi. Na ponudbo je samo en cenik izdelkov.

## <a name="transaction-classes"></a>Razredi transakcije

Project Operations podpira štiri vrste razredov transakcij:

- Čas
- Stroški
- Material
- Dajatev

Stroške in prodajne vrednosti je mogoče oceniti in nastati ob **Času**, **Odhodkih** in **Material** razredi transakcij. **Provizija** je razred transakcij, ki prinaša samo prihodek.

## <a name="work-entities-and-billing-entities"></a>Entitete za delo in obračunavanje

Projekti in naloge so entitete, ki predstavljajo delo. Vrstice ponudb in pogodbene vrstice so subjekti, ki predstavljajo obračunavanje. Različne delovne entitete lahko povežete z možnostmi zaračunavanja tako, da jih povežete z vrsticami ponudb ali vrsticami pogodbe.

## <a name="multi-customer-deals"></a>Posli za več strank

Posli z več strankami se zgodijo, ko je na račun več kot ena stranka. Tukaj je nekaj tipičnih primerov:

- **Podjetja proizvajalcev originalne opreme (OEM) in njihovi partnerji** – Partnerji in preprodajalci prodajajo izdelek, ki vključuje storitve z dodano vrednostjo. Med dogovorom s stranko OEM običajno ponudi financiranje dela projekta.
- **Projekti javnega sektorja** – Več oddelkov lokalne uprave se strinja, da bodo financirali projekt in se jim izda račun v skladu s predhodno dogovorjeno delitvijo. Na primer šolsko okrožje in mestna ali lokalna javna uprava se strinjata, da bosta financirala gradnjo bazena.

## <a name="invoice-schedules"></a>Razporedi izdajanja računov

Razporedi računov so specifični za vsako vrstico ponudbe in niso obvezni. Razporedi računov so ustvarjeni na podlagi določenih začetnih in končnih datumov ter pogostosti izdajanja računov. Uporabljajo se v fazi pogodbe, ko je konfiguriran postopek samodejnega ustvarjanja računa. V fazi ponudbe so urniki faktur neobvezni. Če so ustvarjeni med fazo ponudbe, se kopirajo v projektno pogodbo, ki je ustvarjena, ko je ponudba za projekt pridobljena.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Razlike od prodajnih ponudb Dynamics 365

Ponudbe za projektne operacije so zgrajene na prodajnih ponudbah Dynamics 365. Obstajajo pa nekatere pomembne razlike v funkcionalnosti, ki se jih morate zavedati:

- Ponudbe projektnih operacij imajo dve različni vrsti vrstic: eno za projekte in eno za izdelke.
- Ponudbe Project Operations imajo lastno stran in elemente uporabniškega vmesnika (UI), poslovna pravila, poslovno logiko v vtičnikih in skripte na strani odjemalca, po katerih se razlikujejo od prodajnih ponudb.
- V prodaji lahko eni prodajni ponudbi pripnete več naročil. V projektnih operacijah lahko projektni ponudbi priložite samo eno projektno pogodbo.
- Ko pridobite prodajno ponudbo, lahko povezana priložnost ostane odprta. Ko je projektna ponudba pridobljena, se povezana priložnost zapre.
- Prodajna ponudba ne vključuje nekaterih področij in konceptov, ki jih vključuje projektna ponudba. Polja vključujejo **pogodbeno enoto**, **upravitelja kupcev** in **ime stika za plačilo**.
- Prodajne ponudbe in ponudbe za projekte so označene s poljem nabor možnosti–based **Type** . Za prodajno ponudbo je vrednost tega polja **Na podlagi predmeta**. Za projektno ponudbo je vrednost **na podlagi dela**.

Zaradi teh razlik vam ne priporočamo, da prodajne ponudbe in ponudbe projektnih operacij uporabljate izmenično.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
