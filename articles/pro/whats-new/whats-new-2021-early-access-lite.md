---
title: Novosti pri 2. valu posodobitev izdaje 2021 za zgodnji dostop – poenostavljeno uvajanje storitve Project Operations
description: Ta članek vsebuje informacije o funkcijah, ki so na voljo v izdaji zgodnjega dostopa 2. vala 2021 uvajanja Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924128"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novosti pri 2. valu posodobitev izdaje 2021 za zgodnji dostop – poenostavljeno uvajanje storitve Project Operations

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek velja za naslednje Dynamics 365 Project Operations komponente in različice:

  - Project Operations v okolju Dataverse različice 4.23.0.4

Izdaja se uporablja le, če je za okolje bil [izbran zgodnji dostop](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

[Upravljanje podizvajalskih pogodb](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) – Ta funkcija zagotavlja boljšo vidljivost in nadzor nad vsemi vidiki dela na projektu. Predogled upravljanja podizvajalskih pogodb vključuje naslednje zmogljivosti:

  - Vodja projekta lahko z dobaviteljem ustvari podizvajalsko pogodbo. Pri podizvajalski pogodbi se privzeto uporabljajo ceniki, ki so priloženi zapisu dobavitelja. Račun dobavitelja ima vrsto odnosa **Prodajalec** ali **Dobavitelj**.
  - Vodja projekta lahko vse nakupe v podizvajalski pogodbi našteje kot vrstične postavke v podizvajalski pogodbi. Podizvajalske pogodbe so lahko vezane na čas, stroške ali izdelke. Razred transakcije v vsaki podrobnosti podizvajalske pogodbe določa, čemu ta podrobnost služi.
  - Upravljavec računa dobavitelja in vodja projekta lahko ponovita podizvajalsko pogodbo. Cene v nabavnem ceniku, ki so priložene podizvajalski pogodbi, se lahko prilagodijo.
  - Če je podizvajalska pogodba vezana na čas, upravitelj računa dobavitelja lahko med postopkom poveže stike dobavitelja z vsako vrstico podizvajalske pogodbe. Ta povezava posreduje informacije vodji projekta, ki dela na podizvajalski pogodbi. Ko je stik dobavitelja povezan s podrobnostjo podizvajalske pogodbe, sistem iz stika samodejno ustvari vir, ki ga je mogoče rezervirati, če tak vir še ne obstaja.
  - Način obračunavanja v vsaki vrstici podizvajalske pogodbe je lahko fiksna cena ali čas in material. Za podrobnosti podizvajalske pogodbe s fiksno ceno je nastavljen razpored za izdajanje računov, ki temelji na mejnikih.
