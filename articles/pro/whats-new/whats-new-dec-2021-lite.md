---
title: Kaj je novega december 2021 – uvajanje Project Operations lite
description: Ta tema ponuja informacije o posodobitvah kakovosti, ki so na voljo v izdaji različice Project Operations lite decembra 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942997"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Kaj je novega december 2021 – uvajanje Project Operations lite

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema velja za naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno delovanje v a Dataverse različica okolja 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

### <a name="subcontract-management"></a>Upravljanje podizvajalcev 

- [Podizvajalec članov projektne skupine](../subcontracting/subcontracting-project-team-members.md) : Vodja projekta lahko ustvari imenovane ali splošne člane ekipe s podizvajalci in podizvajalci, da vpliva na kadrovanje in oceno.
- [Možnosti podizvajalcev za člane projektne skupine](../subcontracting/subcon-options.md) : Pri izbiri osebja za imenovane ali splošne člane projektne skupine lahko vodja projekta pregleda obstoječe podizvajalske pogodbe ali ustvari nove podizvajalske pogodbe za enega ali več članov projektne skupine. 
- [Ocena stroškov podizvajalskih dodelitev virov](../subcontracting/costing-subcon-ra.md) : Ocena stroškov projekta bo upoštevala dodelitve virov podizvajalcem in jih bo stala na podlagi nabavnih cenikov, povezanih s podizvajalci. 
- [Konfigurirajte tablo razporeda, da prikaže pogodbene delavce in podizvajalske zmogljivosti](../subcontracting/configure-sb-subcon.md) : Tablo razporeda v Project Operations je zdaj mogoče konfigurirati za iskanje in predlaganje pogodbenih delavcev vrste virov, ki jih je mogoče rezervirati, in zmogljivosti podizvajalcev skupaj z zaposlenimi. To konfiguracijo je mogoče uporabiti pri iskanju virov v kontekstu kadrovanja za posebne zahteve projekta ali pri iskanju zunaj konteksta zahtev projekta.
- [Zaposlovanje projekta s pogodbenimi delavci in podizvajalci](../subcontracting/staffing-cw.md) : Pogodbene delavce je zdaj mogoče rezervirati za projekte, ki izkoriščajo izkušnje s tablo z urniki.
- [Beleženje časa, stroškov in porabe materiala pri projektih za podizvajalske komponente](../subcontracting/recording-subcon-actuals.md) : Pogodbeni delavci lahko beležijo čas in stroške, člani projektne skupine pa lahko beležijo tudi porabo materiala, kupljenega s podizvajalcem pri projektu. To bo povzročilo natančno beleženje stroškov pri projektih, ki uporabljajo kupljene zmogljivosti ali materiale.
- [Prehodi držav na podlagi podizvajalske pogodbe](../subcontracting/subcon-states.md) : Podizvajalske pogodbe se lahko potrdijo za dokončanje pogajanj s prodajalcem, zaprejo, da se označi zaključek dobave, ali prekinejo, da se nakaže prekinitev pogodbe s prodajalcem pred zaključkom dobave.

### <a name="task-planning"></a>Načrtovanje opravil
- Izboljšano odpravljanje težav za sistemske skrbnike. Ko uporabnik ne more odpreti projekta, lahko skrbnik pregleda napake, ki niso povezane z licenco, ustvarjene iz Project za splet v [Dnevniki načrtovanja projekta](../../project-management/schedule-api-logs.md).
- [Uporabite kontrolne sezname opravil v Microsoft Projectu za splet](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). V Microsoft Project za splet lahko opravilu dodate kontrolni seznam, da spremljate določene elemente.

## <a name="quality-updates"></a>Posodobitve kakovosti

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Načrtovanje in sledenje | 2392596 | API-ji za načrtovanje zdaj omogočajo posodobitve **Preostanek truda**, **končano**, in **% Dokončano** polja. |
| Načrtovanje in sledenje | 2478497 | Načrtujte API-je **Številka dejavnosti** in **ID opravila** polja so lahko ob vnosu prazna, ker jih bo sistem zapolnil z avtomatskim številčenjem.|
| Čas in strošek | 2468135 | Število ponovnih poskusov odobritve se zmanjša s pet na tri. |
| Čas in strošek | 2468188 | Odpravljena je težava z besedilom dnevnika, ki presega največjo dolžino v **besedilo beležke** atribut **opomba** entiteta. |
