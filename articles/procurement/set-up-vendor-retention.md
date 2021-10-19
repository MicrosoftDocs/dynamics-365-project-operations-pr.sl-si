---
title: Nastavitev zadrževanja dobaviteljev
description: Ta tema pojasnjuje, kako nastaviti zadrževanje dobaviteljev.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594630"
---
# <a name="set-up-vendor-retention"></a>Nastavitev zadrževanja dobaviteljev

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema zagotavlja informacije o tem, kako nastaviti zadrževanje dobaviteljev.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>V glavni knjigi ustvarite račun za zadrževanje dobaviteljev

1. V aplikaciji Dynamics 365 Finance odprite možnost **Glavna knjiga** > **Nastavitev objave** > **Računi za samodejne transakcije**.
2. Dodaj novo vrstico.
3. V polju **Vrsta objave** izberite možnost **Zadrževanje dobaviteljev**.
4. Izberite glavni račun za objavo zadrževanja dobaviteljev.

## <a name="create-vendor-retention-terms"></a>Ustvarite pogoje zadrževanja dobaviteljev

Uporabite stran **Pogoji zadrževanja dobaviteljev** za nastavitev in vzdrževanje pogojev zadrževanja plačil dobaviteljem. Vnesite odstotek plačila dobaviteljem, ki ga želite zadržati, in odstotek predhodno zadržanih zneskov za sprostitev. Zneski se samodejno zadržijo na računih dobaviteljev, dokler pogodba ne doseže dogovorjenega stanja izpolnitve. Ko so za dobavitelja nastavljeni pogoji zadrževanja, jih lahko uporabite za kateri koli projekt, v katerem dobavitelj deluje.

1. V razdelku za finance izberite možnost **Upravljanje projektov in vodenje računov** > **Nastavitev** > **Zadrževanje** > **Pogoji zadrževanja za plačila dobaviteljem**.
2. Izberite **Novo**, da dodate nov pogoj za zadržanje plačila dobavitelju. Vrednost v polju **ID pravila** za nov izraz je samodejno vnesena. 
3. V polje **Opis** vnesite opisno ime za novi izraz.
4. V zavihku **Pogoji** izberite možnost **Dodaj vrstico** za vnos izraza zadrževanja dobaviteljev.
5. V polje **Odstotek dobavljenih enot** vnesite odstotek dokončanja za pravilo. Zneski se samodejno zadržijo na računih dobaviteljev, dokler stopnja zaključka projekta ni enaka odstotku, ki ga vnesete. Če na primer vnesete 50,00, se zneski zadržijo, dokler projekt ni dokončan do 50 odstotkov.
6. V polju **Odstotek za zadržanje** vnesite odstotek zneska računa dobavitelja, ki ga želite zadržati. Če v to polje vnesete na primer 10.00, se zadrži 10 odstotkov zneska na računih dobavitelja, dokler projekt ne doseže odstotka zaključka, ki ga izberete v polje **Odstotek dobavljenih enot**.
7. V polje **Odstotek za sprostitev** vnesite odstotek predhodno ohranjenih zneskov za sprostitev na izbrani ravni zaključka projekta.

> [!NOTE]
> Če imate za različne stopnje zaključka projekta več kot en mejnik, za vsako pravilo zadrževanja vnesite ločeno vrstico pogojev zadrževanja dobavitelja. Vsaka vrstica lahko določi drugačen odstotek za zadrževanje in drugačen odstotek za sprostitev za vsako določeno stopnjo zaključka projekta.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Nastavite pogodbo z dobaviteljem za projekt

Nastavite pogoje hranjenja dobaviteljev, ki veljajo za projekt. Pogoji za zadrževanje plačila dobavitelju so prikazani tudi v naročilnicah, ki jih ustvarite za dobavitelja.

1. V razdelku za finance odprite možnost **Upravljanje projektov in vodenje računov** > **Projekti** > **Vsi projekti**. 
2. Izberite projekt in v podoknu za dejanja izberite **Skupina projekta** > **Pogodbe z dobavitelji**.
3. Na strani **Pogodbe z dobavitelji** dodajte novo vrstico.
4. V polju **Koda kupca** izberite eno od naslednjih možnosti:
   - **Tabela**: pogoji za zadrževanje plačila dobavitelju veljajo za enega dobavitelja.
   - **Skupina**: pogoji za zadrževanje plačila dobavitelju veljajo za vse dobavitelje v skupini dobaviteljev.
   - **Vsi**: pogoji za zadrževanje plačila dobavitelju veljajo za vse dobavitelje.
5. V polju **Dobavitelj/skupina dobaviteljev** izberite dobavitelja ali skupino dobaviteljev, za katero naj se uporabijo pogoji zadrževanja dobavitelja. Če ste v prejšnjem koraku izbrali možnost **Vsi**, to polje ne bo na voljo.
6. V polju **Pogoji zadrževanja dobavitelja** izberite ID pravila za pogoje zadrževanja, ki veljajo za tega dobavitelja.

