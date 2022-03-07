---
title: Ustvarjanje in uporaba pogojev za zadrževanje plačila dobaviteljem
description: Ta tema vsebuje informacije o tem, kako nastaviti in vzdrževati pogoje za zadrževanje plačila dobaviteljem.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 4ff725512aa0bcc87ff4670d6bb072f3bf780786c1f71b332914887f4d4ccf13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991236"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Ustvarjanje in uporaba pogojev za zadrževanje plačila dobaviteljem

[!include [banner](../includes/banner.md)] 

Nastavitev pogojev za zadrževanje plačila dobaviteljem za projekt je koristna, če želi vaša organizacija obdržati del plačil dobavitelju. Na primer ko želite zadržati plačilo dobavitelju, dokler dobavljeni izdelki ne izpolnijo vaših pričakovanj. Pogoje za zadrževanje plačila dobavitelju lahko določite med pogajanjem za pogodbo z dobaviteljem.

## <a name="create-vendor-payment-retention-terms"></a>Ustvarjanje pogojev za zadrževanje plačila dobaviteljem

Vnesete lahko delež plačila dobavitelju, ki ga želite zadržati, in delež predhodno zadržanih zneskov, ki jih želite sprostiti. Zneski se samodejno zadržijo na računih dobaviteljev, dokler pogodba ne doseže dogovorjenega stanja izpolnitve. Ko nastavite pogoje za zadržanje, lahko te pogoje uporabite za kateri koli projekt tega dobavitelja.

Uporabite naslednje korake za nastavitev in vzdrževanje pogojev za zadrževanje plačila dobavitelju. 

1. Odprite **Vodenje projektov in računovodstvo** > **Zadrževanje** > **Pogoji za zadrževanje plačila dobavitelju**.
2. Izberite **Novo**, da dodate nov pogoj za zadržanje plačila dobavitelju. Vrednost **ID pravila** za novi pogoj se samodejno vnese. 
3. Vnesite kratek opis v polje **Opis** in v zavihku za hitri dostop **Pogoji** izberite **Dodaj vrstico**, da vnesete vrednosti pogojev za naslednje entitete:

   - **Delež dobavljenih enot**: vnesite delež izpolnitve pogoja. Zneski se samodejno zadržijo na računih dobaviteljev, dokler stanje izpolnitve projekta ne doseže dogovorjenega deleža. Če na primer vnesete 50,00, se zneski zadržijo, dokler projekt ni dokončan do 50 odstotkov.
   - **Delež, ki ga je treba zadržati**: vnesite delež zneska računa dobavitelju, ki ga je treba zadržati. Če na primer vnesete 10.00, se 10 odstotkov zneska na računu dobavitelja zadrži, dokler projekt ne doseže deleža izpolnitve, kot je določeno v polju **Delež dobavljenih enot**.
   - **Delež za sprostitev**: izberite **Dodaj vrstico** za vnos odstotka predhodno zadržanih zneskov, ki se sprostijo ob določeni stopnji dokončanosti projekta.

> [!NOTE]
> Če imate več kot en mejnik za različne stopnje dokončanosti projekta, vnesite ločeno vrstico pogoja za zadrževanje plačila dobavitelju za vsako pravilo za zadrževanje. Vsaka vrstica lahko določa drugačen odstotek zadrževanja in drugačen odstotek sprostitve za vsako določeno stopnjo dokončanja projekta.

Ko ustvarite pogoje za zadržanje plačila dobavitelju, lahko te pogoje uporabite tudi za projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Uporaba pogojev za zadrževanje plačila dobaviteljem

1. Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Vsi projekti** in odprite projekt s strani s seznamom projektov.
2. Na zavihku za hitri dostop **Pogodbe dobaviteljev** izberite **Dodaj vrstico**.
3. V polju **Koda kupca** izberite eno od naslednjih možnosti: 

   - **Tabela**: pogoji za zadrževanje plačila dobavitelju veljajo za enega dobavitelja.
   - **Skupina**: pogoji za zadrževanje plačila dobavitelju veljajo za vse dobavitelje v skupini dobaviteljev.
   - **Vsi**: pogoji za zadrževanje plačila dobavitelju veljajo za vse dobavitelje.

4. V polju **Dobavitelj/skupina dobaviteljev** izberite dobavitelja ali skupino dobaviteljev, za katero naj se uporabijo pogoji za zadrževanje plačila dobavitelju. Če ste v prejšnjem koraku izbrali možnost **Vsi**, to polje ne bo na voljo.
5. V polju **Pogoji za zadrževanje plačila dobavitelju** izberite pogoje za zadrževanje, ki ste jih ustvarili v prejšnjem postopku.
6. Če ima projekt za dobavitelja nastavljene tudi pogoje po načinu plačila ob izvedenem plačilu (PWP), vnesite mejni odstotek za projekt v polju **Mejni odstotek za PWP**.

Pogoji za zadrževanje plačila dobavitelju so prikazani tudi v naročilnicah, ki jih ustvarite za dobavitelja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]