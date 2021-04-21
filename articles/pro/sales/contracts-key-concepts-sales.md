---
title: Projektne pogodbe – ključni pojmi – poenostavljena različica
description: Ta tema vsebuje informacije o ključnih pojmih projektnih pogodb.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75c4b90e47c0b90ed3fea8dce1533057aa6137b9
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663794"
---
# <a name="concepts-unique-to-project-contracts"></a>Koncepti, enolični za projektne pogodbe

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ta tema vsebuje ključne koncepte, ki jih morate upoštevati, preden začnete uporabljati Projektne pogodbe v aplikaciji Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Pogodbena enota

Pogodbena enota predstavlja oddelek ali prakso, ki je lastnica izvedbe projekta. Za vsako pogodbeno enoto lahko nastavite stroške virov. Ko določite stroške virov za vir, lahko nastavite tudi različne stopnje stroškov za vire. Ta pogodbena enota si sredstva izposodi od drugih oddelkov ali praks znotraj podjetja. Stroški virov se imenujejo cene prenosa, izposoja virov ali cene menjave. Ko nastavite stroške izposojanja virov od drugih oddelkov, uporabite valuto oddelka, ki je posojilodajalec.

## <a name="cost-currency"></a>Valuta stroška

Valuta stroška je valuta, v kateri so na zaslonu poročani stroški. Ta valuta izhaja iz valute, priložene k polju **Pogodbena enota** na pogodbi in projektu. Stroški se lahko zabeležijo v kateri koli valuti za projekt. Vendar za prikaz na zaslonu obstaja možnost pretvorbe iz valute, v kateri so bili zabeleženi stroški, v valuto stroškov projekta.

Ker menjalni tečaji na platformi Common Data Service (CDS) ne morejo imeti datuma začetka veljavnosti, se lahko, če posodobite menjalne tečaje valut, skupne vrednosti stroškov na zaslonu sčasoma spremenijo. Vendar stroški, zabeleženi v zbirki podatkov, ostanejo nespremenjeni, saj so zneski shranjeni v valuti, v kateri so nastali.

## <a name="sales-currency"></a>Prodajna valuta

Prodajna valuta v storitvi Project Operations je valuta, v kateri se zabeležijo ter prikažejo predvideni in dejanski zneski prodaje. Valuta prodaje je tudi valuta, v kateri bo stranki izdan račun za posel. V projektni pogodbi je prodajna valuta privzeto nastavljena na podlagi zapisa stranke ali kupca in jo je mogoče spremeniti, ko je pogodba ustvarjena. Če pogodbo ustvarite tako, da zaprete ponudbo kot pridobljeno, je valuta v pogodbi privzeta od valute v ponudbi.

Če ustvarite projektno pogodbo od začetka, polja **Valuta prodaje** ni mogoče urejati. Ceniki izdelkov in projektov so privzeto nastavljeni na podlagi valute v pogodbi.

V nasprotju s stroški je prodajne vrednosti mogoče beležiti samo v valuti prodaje.

## <a name="billing-method"></a>Način obračunavanja

Za projekte običajno obstajata dva tipa pogodbenih modelov, fiksni model in model na podlagi potrošnje. Modela sta v aplikaciji Project Operations predstavljena kot načina obračunavanja z dvema možnima vrednostma:

- Čas in material: to je pogodbeni model na podlagi potrošnje, pri katerem so vsi nastali stroški podprti z ustreznimi prihodki. Ko ocenite ali ustvarite več stroškov, se povečata tudi ustrezna predvidena in dejanska prodaja. Določite omejitve, ki ne smejo biti presežene, v podrobnostih pogodbe, ki imajo določen način obračunavanja, ki omejuje dejanski prihodek. Omejitve »Ni dovoljeno preseči« ne vplivajo na ocenjene prihodke.
- Fiksna cena: pogodbeni model s fiksnimi dajatvami, ki nakazuje, da bodo prodajne vrednosti neodvisne od nastalih stroškov. Prodajna vrednost je fiksna in se ne spremeni, ko ocenjujete ali ustvarite več stroškov.

## <a name="project-price-lists"></a>Projektni ceniki

Za privzeto nastavitev cen so uporabljeni projektni ceniki in ne mere stroškov za čas, stroške ter druge komponente, povezane s projektom. Cenikov je lahko več. Vsak cenik ima lastno datumsko veljavnost za posamezno projektno pogodbo. V aplikaciji Project Operations niso podprti prekrivajoči se datumi začetka veljavnosti cenikov projektov.

Če je projektna pogodba ustvarjena s pridobitvijo projektne ponudbe, se ceniki projekta kopirajo z navedenim imenom pogodbe in datumom. Kopiranje teh podatkov predstavlja prilagojeno določanje cen za komponente projekta v tej projektni pogodbi.

## <a name="product-price-lists"></a>Ceniki za izdelke

Za privzeto nastavitev cen so uporabljeni ceniki izdelkov in ne mere stroškov za podrobnosti pogodbe, ki temeljijo na izdelkih. Za posamezno pogodbo pogodbo obstaja samo en cenik izdelkov.

## <a name="transaction-classes"></a>Razredi transakcije

Project Operations podpira štiri vrste razredov transakcij:

- Čas
- Stroški
- Material
- Dajatev

Vrednosti stroškov in prodaje je mogoče oceniti ter ustvariti za razrede časovnih, stroškovnih in materialnih transakcij. Dajatev je razred transakcij, ki omogoča le zapis prihodkov.

## <a name="work-entities-and-billing-entities"></a>Entitete za delo in obračunavanje

Entitete, ki predstavljajo delo, so projekti in opravila. Entitete, ki predstavljajo vidike obračunavanja, so podrobnosti pogodbe. Različne entitete za delo lahko povežete z možnostmi obračunavanja tako, da jih povežete s podrobnostmi pogodb.

## <a name="multi-customer-deals"></a>Posli za več strank

Za posle za več strank pride pri posameznem poslu do izdaje računov za več strank. Nekateri pogosti primeri:

- Družba OEM in njihovi partnerji: partnerji in prodajalci tržijo izdelek prek storitev z dodano vrednostjo, ki običajno vključujejo posamezen posel za stranko. Družba OEM ponudi finančna sredstva za del projekta. 

- Projekti javnega sektorja: več oddelkov lokalne javne uprave se strinja, da bo financirala projekt in se ji fakturira v skladu s predhodno dogovorjeno razdelitvijo. Šolsko okrožje in lokalna javna uprava se na primer strinjata, da bosta finančno podprla gradnjo bazena.

## <a name="invoice-schedules"></a>Razporedi izdajanja računov

Razporedi izdajanja računov so določeni za vsako podrobnost pogodbe in so potrebni za delovanje samodejnega izdajanja računov. Razporedi izdajanja računov so ustvarjeni na podlagi določenih datumov začetka in konca ter pogostosti računov. Razporedi se uporabljajo v fazi pogodbe pri konfiguraciji samodejnega postopka ustvarjanja računov. Če je projektna pogodba ustvarjena na podlagi ponudbe, se razpored izdajanja računov iz ponudbe kopira v projektno pogodbo.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Spremembe v pogodbi iz aplikacije Dynamics 365 Sales

Pogodbe v aplikaciji Project Operations temeljijo na pogodbah iz aplikacije Dynamics 365 Sales. Vendar pa med njima obstajajo nekatere pomembne razlike v funkcionalnosti, ki se jih morate zavedati:

- Pogodbe iz aplikacije Project Operations imajo dve različni vrsti podrobnosti, eno za projekte in drugo za izdelke.
- Ponudbe iz aplikacije Project Operations imajo lastne obrazce in elemente uporabniškega vmesnika, pravila poslovanja, poslovno logiko v vtičnikih in skripte na strani odjemalca, s katerimi se razlikujejo od ponudb iz aplikacije Sales.

Iz teh razlogov pogodb iz aplikacij Sales in Project ne smete uporabljati zamenljivo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
