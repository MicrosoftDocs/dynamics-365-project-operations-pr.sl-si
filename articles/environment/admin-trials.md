---
title: Prijava za preskusne različice aplikacije Project Operations
description: Ta tema vsebuje informacije o tem, kako uvesti preskusno različico aplikacije Dynamics 365 Project Operations.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418477"
---
# <a name="sign-up-for-project-operations-trials"></a>Prijava za preskusne različice aplikacije Project Operations 

_**Velja za:** Project Operations za primere uporabe z viri/brez zalog, poenostavljeno uvajanje – posel do izstavitve predračuna in Project Operations za primere uporabe z naročili na zalogi/v proizvodnji_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

V tej temi je pojasnjeno, kako se naročiti na partnersko ponudbo predogledne različice in kako uvesti okolje storitve Dynamics 365 Project Operations.

Z novo preskusno različico aplikacije Project Operations lahko samodejno uvedete kateregakoli od treh podprtih primerov uvajanja, in sicer tako, da izpolnite vprašalnik, ki ponuja najboljši pristop uvajanja. Ta tema vam bo podala odgovore na vprašanja, kako:

- Unovčiti ponudbo preskusne različice.
- Začeti z omogočanjem uporabe.
- Konfigurirati dvojno zapisovanje.
- Izvedeti več o aplikaciji Project Operations. 

V naslednji tabeli so opisane podrobnosti nove ponudbe preskusne različice.

| **Predmet ponudbe**               | **Podrobnosti**                                  |
|------------------------------|----------------------------------------------|
| Vrsta ponudbe                   | Gre za vrsto ponudbe z možno stranko skrbnika, zato je za uspešno oddajo naročila potreben skrbnik najemnika. |
| Uporaba ponudbe                    | Enkrat na najemnika                          |
| Trajanje ponudbe               | 30 koledarskih dni                             |
| Koriščenje na vsakega najemnika       | 1                                            |
| Število uporabnikov              | 25                                           |
| Pripona                    | Ena možnost podaljšanja, 30 koledarskih dni               |
| Število preskusnih okolij | 3                                            |


## <a name="admin-trial-details"></a>Podrobnosti o preskusni različici za skrbnika
V spodnji tabeli so navedene podrobnosti o preskusni različici skupaj z načinom, na katerega se nanašajo na vsako vrsto uvajanja.

| **Element**                      | **Poenostavljeno**                                     | **Material, ki ni na zalogi** | **Material, ki je na zalogi** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Podani namestitveni podatki           | Da                                          | Da                       | Da (IUSSI)            |
| Transakcijski podatki            | No                                           | No                        | No                    |
| Čas omogočanja uporabe v minutah  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Zahteve
Za uvajanje preskusne različice aplikacije Dynamics 365 Project Operations morajo biti izpolnjene naslednje zahteve.

- Prijavite se za [Preskus predogledne različice Dynamics 365 Project Operations](https://www.aka.ms/try-po).
- Uporabnik, ki uvede predogled, mora imeti pravice globalnega skrbnika za najemnika imenika Azure.

> [!IMPORTANT]
> To opravilo mora izvesti samo ena oseba iz organizacije, in sicer skrbnik najemnika. Če niste naročnik te izdaje, počakajte, da se organizacija prijavi in prejmete svoje uporabniške poverilnice.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – preskus predogledne različice 

Preden začnete, se s službenim uporabniškim računom prijavite v brskalnik, in sicer v najemniku, v katerem želite imeti predogledno različico aplikacije Project Operations.

1. Unovčite prvo promocijsko kodo **Dynamics 365 Project Operations – preskus predogledne različice**, tako da jo prilepite v URL brskalnika.

    ![Prevzem ponudbe](./media/16RedeemFirstOfferNew.png)

2. Potrdite svoje naročilo.

    ![Potrdite naročilo](./media/17ConfirmOrderNew.png)

  Prikazalo se vam bo potrditveno sporočilo, da je bila ponudba uspešno obdelana.

   ![Potrditev](./media/18OrderConfirmationNew.png)

  Preusmerjeni boste v [skrbniško središče za Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Vprašalnik in omogočanje uporabe

1.  Obiščite [skrbniško središče za Power Platform](https://admin.powerplatform.com/projectoperationstrial) in izpolnite vprašalnik.  
2.  Za začetek omogočanja uporabe preglejte priporočeno vrsto uvajanja in izberite možnost **Začetek namestitve**.
3.  Preglejte pogoje in določila, nato pa izberite **Začetek**.

   Po začetku omogočanja uporabe boste preusmerjeni na seznam okolij v skrbniškem središču za Power Platform. Medtem ko poteka omogočanje uporabe, je stanje vašega okolja naslednje: **PreparingInstance**.
 
  Ko je omogočanje uporabe zaključeno, je stanje vašega okolja naslednje: **Pripravljeno**.
 
4.  Če želite po zaključenem omogočanju uporabe preveriti veljavnost uvajanja, izberite ustrezni URL storitve Microsoft Dataverse ter URL aplikacij Finance and Operations.

## <a name="demo-data-installation"></a>Namestitev predstavitvenih podatkov

Za dostop do paketov predstavitvenih podatkov za material, ki ni na zalogi, in za postopke poenostavljenega uvajanja, uporabite naslednje povezave. 
- [Predstavitveni podatki o materialu, ki ni na zalogi](resource-apply-pro-setup-config-data.md)
- [Poenostavljeni predstavitveni podatki](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Konfiguracija dvojnega zapisovanja
Konfigurirajte preslikave z dvojnim zapisovanjem, in sicer samo za uvajanje materiala, ki ni na zalogi. Za več informacij si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Dodelitev licenc

Potrebovali boste skrbniški dostop do portala Microsoft 365 vaše organizacije, če želite dokončati naslednje korake.

1. Za dodeljevanje licenc uporabnikom obiščite [skrbniško središče za Microsoft 365](https://portal.office.com/).

   ![Začetna stran skrbniškega središča](./media/14AdminPortal.png)

2. Na strani **Aktivni uporabniki** izberite uporabnike, ki jim želite dodeliti licenco.

   ![Dodeljevanje licenc](./media/15AssignLicenses.png)

3. Prepričajte se, da ste izbrali licenco **Dynamics 365 Project Operations – predogledna različica**, nato pa izberite možnost **Shrani spremembe**.

## <a name="additional-resources"></a>Dodatni viri

Na začetku uporabe aplikacije Project Operations si lahko pomagate z uporabnimi napotki, ki so na voljo v naslednjih virih:

- [Serije videoposnetkov – poglobljen pregled aplikacije Project Operations z načrtom](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Določanje vrste uvedbe](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Pogosta vprašanja

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Kaj, če za okolje aplikacije Finance and Operations potrebujem ALM ali ELM?

- Če partnerji potrebujejo zmogljivosti upravljanja za celoten življenjski cikel okolja, si oglejte temo [Zahteva licence za preizkusno okolje partnerja](https://experience.dynamics.com/requestlicense). 
- Če želijo partnerji pridobiti več informacij o pravicah do interne uporabe, si oglejte [Prednost oblaka pravic do interne uporabe in programske opreme (microsoft.com)](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Ali lahko preskusno različico uporabljam več kot 30 dni?
Če želite podaljšati preskusno obdobje, upoštevajte naslednja navodila.

1. Odprite **skrbniško središče za Microsoft 365** in izberite **Obračunavanje** > **Vaši izdelki**.
2. Izberite možnost **Dynamics 365 Project Operations (CE) – preskus predogledne različice**.
3. Pod možnostjo **Datum poteka** izberite **Podaljšanje roka**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Ali lahko poenostavljeno uvajanje nadgradim na uvajanje scenarijev, ki temeljijo na viru/nezalogi?
Nadgradnja okolja s poenostavljenim uvajanjem na okolje z uvajanjem, ki temelji na nezalogi, trenutno ni podprta.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Ali lahko, ko gre za finančna okolja, dostopam do storitve Lifecycle Services (LCS)?  
Ne. Za uvajanje teh preskusnih različic je poskrbljeno v skrbniškem središču za Power Platform. Dostop do finančnega okolja je omejen.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Ali lahko v obstoječe okolje namestim svojo preskusno različico?
Če že imate okolje, boste lahko iz skrbniškega središča za Power Platform v obstoječe prodajno okolje Dataverse namestili poenostavljeno uvajanje.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
