---
title: Ponudbe – ključni pojmi – poenostavljeno
description: Ta tema vsebuje informacije o uporabi projektnih ponudb v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e86f1a5a7b2859df5bf9569ee9ca306c6dcc6293
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178026"
---
# <a name="quotes---key-concepts---lite"></a>Ponudbe – ključni pojmi – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Sledijo ključni koncepti, ki se jih morate zavedati, preden začnete uporabljati projektne ponudbe v storitvi Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Pogodbena enota

Pogodbena enota predstavlja oddelek ali prakso, ki je lastnik izvedbe projekta. Za vsako pogodbeno enoto lahko nastavite stroške virov. Ko določite stroške virov za vir v pogodbeni enoti, boste lahko tudi nastavili različne stopnje stroškov za vire, ki si jih ta pogodbena enota izposodi, ali druge oddelke ali prakse v podjetju. Te se imenujejo cene prenosa, izposoja virov ali cene menjave. Ko nastavite stroške izposojanja virov od drugih oddelkov, lahko tudi določite te mere stroškov v valuti oddelka, ki je posojilodajalec.

## <a name="cost-currency"></a>Valuta stroška

Valuta stroška v storitvi Project Operations je valuta, v kateri se poročajo stroški. Ta valuta izhaja iz valute, priložene k polju **Pogodbena enota** na ponudbi, pogodbi in projektu. Stroški se lahko zabeležijo v kateri koli valuti za projekt. Vendar obstaja pretvorba valute iz valute, v kateri so bili zabeleženi stroški, v valuto stroškov projekta.

Ker menjalni tečaji na platformi CDS ne morejo imeti datuma začetka veljavnosti, se lahko skupni stroški na zaslonu sčasoma spremenijo, če posodobite menjalne tečaje valut. Vendar stroški, zabeleženi v zbirki podatkov, ostanejo nespremenjeni, ker so zneski shranjeni v valuti, v kateri so nastali.

## <a name="sales-currency"></a>Prodajna valuta

Prodajna valuta v storitvi Project Operations je valuta, v kateri se zabeležijo ter prikažejo predvideni in dejanski zneski prodaje. To je tudi valuta, v kateri bo stranki fakturiran za posel. Pri projektni ponudbi je privzeto prodajna valuta nastavljena na podlagi zapisa stranke ali kupca ter jo je mogoče spremeniti, ko je ponudba ustvarjena. Ko je ponudba shranjena, prodajne valute ni mogoče spremeniti. Ceniki izdelkov in projektov so privzeto nastavljeni na podlagi prodajne valute ponudbe.

V nasprotju s stroški je prodajne vrednosti mogoče zabeležiti samo v prodajni valuti.

## <a name="billing-method"></a>Način obračunavanja

Projekti imajo običajno fiksne pogodbene modele, ki temeljijo na dajatvah in potrošnji. To je v storitvi Project Operations predstavljeno kot **Način obračunavanja** ter ima dve vrednosti, čas in material ter fiksno ceno.

- **Čas in material:** to je pogodbeni model, ki temelji na potrošnji, pri katerem so vsi nastali stroški podprti z ustreznimi prihodki. Ko ocenite ali ustvarite več stroškov, se bosta povečali tudi ustrezna predvidena in dejanska prodaja. Za podrobnosti ponudb, ki imajo ta način obračunavanja, lahko določite omejitve, ki se jih ne sme preseči. To bo navzgor omejilo dejanski prihodek. Omejitev »Ni dovoljeno preseči« ne vpliva na ocenjene prihodke.
- **Fiksna cena:** to je pogodbeni model s fiksnimi dajatvami, ki kaže, da bodo prodajne vrednosti neodvisne od nastalih stroškov. Prodajna vrednost je fiksna in se ne spreminja, ko ocenjujete ali ustvarite več stroškov.

## <a name="project-price-lists"></a>Ceniki za projekte

Ceniki za projekte so ceniki, ki se uporabljajo za privzeto nastavitev cen, ne pa mer stroškov, za čas, stroške in druge komponente, povezane s projektom. Cenikov je lahko več, vsak seznam pa ima lahko lastno datumsko veljavnost za vsako projektno ponudbo. Project Operations ne podpira prekrivajočih se datumov začetka veljavnosti pri cenikih projektov.

## <a name="product-price-lists"></a>Ceniki za izdelke

Ceniki izdelkov so ceniki, ki se uporabljajo za privzeto nastavitev cen in ne mer stroškov, za podrobnosti ponudbe, ki temeljijo na izdelkih. Na ponudbo je samo en cenik izdelkov.

## <a name="transaction-classes"></a>Razredi transakcije

Project Operations podpira štiri vrste razredov transakcij:

- Čas
- Stroški
- Material
- Dajatev

Vrednosti stroškov in prodaje je mogoče oceniti ter ustvariti za razrede časovnih, stroškovnih in materialnih transakcij. Dajatev je razred transakcij, ki omogoča le zapis prihodkov.

## <a name="work-entities-and-billing-entities"></a>Entitete za delo in obračunavanje

Entitete, ki predstavljajo delo, so projekti in opravila. Entitete, ki predstavljajo obračunavanje, so podrobnosti ponudb in podrobnosti pogodb. Različne entitete za delo lahko povežete z možnostmi obračunavanja tako, da jih povežete s podrobnostmi ponudb ali pogodb.

## <a name="multi-customer-deals"></a>Posli za več strank

Do poslov za več strank pride, če je za izdajo računov na voljo več strank. Pogosti primeri so npr.:

- **Podjetja OEM in njihovi partnerji:** partnerji in prodajalci prodajajo izdelek s storitvami z dodano vrednostjo. To je ponavadi scenarij, ko OEM med posameznim dogovorom s stranko ponudi financiranje dela projekta. 

- **Projekti javnega sektorja:** več oddelkov lokalne javne uprave se strinja, da bo financirala projekt in se ji fakturira v skladu s predhodno dogovorjeno razdelitvijo. Na primer šolsko okrožje in mestna ali lokalna javna uprava se strinjata, da bosta financirala gradnjo bazena.

## <a name="invoice-schedules"></a>Razporedi izdajanja računov

Razporedi izdajanja računov so specifični za vsako podrobnost ponudbe in so tudi neobvezni. Razporedi izdajanja računov so ustvarjeni na podlagi določenih datumov začetka in konca ter pogostosti računov. Razporedi izdajanja računov se uporabljajo v fazi pogodbe, ko je konfiguriran samodejni postopek ustvarjanja računov. V fazi ponudbe so razporedi neobvezni. Ko se v fazi **Ponudba** ustvarijo razporedi izdajanja računov, se kopirajo v projektno pogodbo, ki je ustvarjena, ko se pridobi projektna ponudba.

## <a name="changes-from-dynamics-365-sales-quote"></a>Spremembe od ponudbe v storitvi Dynamics 365 Sales:

Ponudbe Project Operations temeljijo na ponudbah Dynamics 365 Sales. Obstajajo pa nekatere pomembne razlike v funkcionalnosti, ki se jih morate zavedati:

- Dejanji **Preglej** in **Aktiviraj** nista podprti.
- Ponudbe Project Operations imajo dve različni vrsti podrobnosti. Ena je za projekte in druga je za izdelke.
- Ponudbe Project Operations imajo lastno obliko in elemente uporabniškega vmesnika, pravila poslovanja, poslovno logiko v vtičnikih in skripte na strani odjemalca, s čimer se razlikujejo od ponudb Sales.

Iz teh razlogov ni priporočljivo, da se ponudba Sales in ponudba Project Operations uporabljata izmenično.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]