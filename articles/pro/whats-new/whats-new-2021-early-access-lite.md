---
title: Novosti pri 2. valu posodobitev izdaje 2021 za zgodnji dostop – poenostavljeno uvajanje storitve Project Operations
description: V tej temi so na voljo informacije o funkcijah, ki so na voljo v 2. valu posodobitev izdaje 2021 za zgodnji dostop poenostavljenega uvajanja storitve Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323931"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novosti pri 2. valu posodobitev izdaje 2021 za zgodnji dostop – poenostavljeno uvajanje storitve Project Operations

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

  - Project Operations v okolju Dataverse različice 4.23.0.4

Izdaja se uporablja le, če je za okolje bil [izbran zgodnji dostop](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

[Upravljanje podizvajalskih pogodb](../subcontracting/subcontracting_EA_scope.md) – Ta funkcija zagotavlja boljšo vidljivost in nadzor nad vsemi vidiki dela na projektu. Predogled upravljanja podizvajalskih pogodb vključuje naslednje zmogljivosti:

  - Vodja projekta lahko z dobaviteljem ustvari podizvajalsko pogodbo. Pri podizvajalski pogodbi se privzeto uporabljajo ceniki, ki so priloženi zapisu dobavitelja. Račun dobavitelja ima vrsto odnosa **Prodajalec** ali **Dobavitelj**.
  - Vodja projekta lahko vse nakupe v podizvajalski pogodbi našteje kot vrstične postavke v podizvajalski pogodbi. Podizvajalske pogodbe so lahko vezane na čas, stroške ali izdelke. Razred transakcije v vsaki podrobnosti podizvajalske pogodbe določa, čemu ta podrobnost služi.
  - Upravljavec računa dobavitelja in vodja projekta lahko ponovita podizvajalsko pogodbo. Cene v nabavnem ceniku, ki so priložene podizvajalski pogodbi, se lahko prilagodijo.
  - Če je podizvajalska pogodba vezana na čas, upravitelj računa dobavitelja lahko med postopkom poveže stike dobavitelja z vsako vrstico podizvajalske pogodbe. Ta povezava posreduje informacije vodji projekta, ki dela na podizvajalski pogodbi. Ko je stik dobavitelja povezan s podrobnostjo podizvajalske pogodbe, sistem iz stika samodejno ustvari vir, ki ga je mogoče rezervirati, če tak vir še ne obstaja.
  - Način obračunavanja v vsaki vrstici podizvajalske pogodbe je lahko fiksna cena ali čas in material. Za podrobnosti podizvajalske pogodbe s fiksno ceno je nastavljen razpored za izdajanje računov, ki temelji na mejnikih.
