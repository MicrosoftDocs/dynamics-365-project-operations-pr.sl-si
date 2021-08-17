---
title: Predlaganje projektnih virov
description: Ta tema vsebuje informacije o predlaganju projektnih virov.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9fe63f424735f22dc6b525631287e7ff36db17f37aad8e14e926f5cc9be39136
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995061"
---
# <a name="propose-project-resources"></a>Predlaganje projektnih virov

[!include [banner](../includes/psa-now-project-operations.md)]

Upravitelji virov lahko vodji projekta predlagajo vir prek zahteve za vir.

1. V mreži zahtev ali sami zahtevi izberite **Poišči vire**.
2. Na strani **Pomočnik za razporejanje** izberite vir in nato v polju **Stanje rezervacije** v podoknu **Ustvari rezervacijo vira** izberite **Rezerviraj**.

    ![Izbran predlagani vir.](media/Resource-Management-image62.png)

Pojavijo se naslednje posodobitve stanja:

- Na strani **Pomočnik za razporejanje** se kazalniki stanja posodobijo in sporočajo, da je rezervacija šele predlagana in ne potrjena.

    ![Kazalniki stanja za predlagano rezervacijo na strani pomočnika za razporejanje .](media/Resource-Management-image63.png)

- V zahtevi za vir se stanje spremeni v **Potreben pregled**.

    ![Sprememba stanja zahteve za vir v »Potreben pregled«.](media/Resource-Management-image64.png)

- Na zavihku **Ekipa** izbranega projekta se vrednost splošnega člana ekipe **Stanje zahteve** spremeni v **Potreben pregled**.

    ![Sprememba stanja zahteve splošnega člana ekipe v »Potreben pregled« na zavihku »Ekipa«.](media/Resource-Management-image48.png)

Vodja projekta lahko predlog sprejme ali zavrne.

Upravitelji virov lahko za obdelavo zahtev za vire uporabijo katerega koli od spodaj navedenih pristopov:

- Predlagajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil zahtevane ure. Predlagane ure se nato razdelijo med več virov, ki lahko opravijo zahtevane ure. V tem primeru se ure ne morejo prekrivati.
- Predlagajo manj virov, kot jih zahtevajo. V tem primeru je predlagana zmogljivost vira manjša od zahtevanih ur, ki jih je določila oseba, ki je podala zahtevo. Ko torej oseba, ki je podala zahtevo, sprejme predlagane vire, se ustvari neizpolnjena zahteva za vir, ki predstavlja preostalo povpraševanje.
- Rezervirajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil delo.
- Rezervirajo manj virov, kot jih zahtevajo. V tem primeru bo število rezerviranih ur manjše od zahtevanih ur. Sistem vas vodi k predlaganju virov namesto rezervacij, da lahko oseba, ki je podala zahtevo, preveri in spremlja preostalo povpraševanje.

## <a name="billable-utilization"></a>Zaračunana uporaba

Viri lahko imajo ciljno zaračunano uporabo. Ta ciljna uporaba je opredeljena kot atribut privzete vloge vira ali nastavljena v zapisu posameznega vira, ki ga je mogoče rezervirati. Izračuni uporabe temeljijo na dejanskih urah, ki so jih viri poročali na podlagi odobrenih časovnih vnosov.

Za izračun uporabe se uporabljajo naslednje enačbe:

- Zaračunana uporaba = dejanske zaračunane ure ÷ zmogljivost vira
- Nezaračunana uporaba = dejanski čas z ID-jem vrste obračunavanja = se ne zaračuna, brezplačno ali ni na voljo ÷ zmogljivost vira
- Za interno uporabo = dejanski čas brez prodajne pogodbe ÷ zmogljivost vira
- Zmogljivost vira = delovni čas vira – odsotnost – prosti dnevi

Pogled **Uporaba vira** lahko najdete v podoknu **Viri**.

![Ogled uporabe virov.](media/Resource-Management-image65.png)

Vsaka celica v mreži predstavlja delež zaračunane uporabe vira v določenem obdobju, na primer dnevu, tednu ali mesecu. Za obarvanje celic se uporabljajo naslednje enačbe:

- **Zelena:** zaračunana uporaba \>= ciljna uporaba za vir
- **Rumena:** ciljna uporaba – 20 \<= zaračunana uporaba \< ciljna uporaba
- **Rdeča:** zaračunana uporaba \< ciljna uporaba – 20

Ker pogled **Uporaba vira** temelji na plošči razporeda, lahko rezultate filtrirate z možnostmi filtriranja na plošči razporeda.

Zaradi mreže morate nastaviti ciljno uporabo za vlogo ali posamezni vir. To nastavite v možnosti **Viri** \> **Vloge virov**.

Poleg tega morate vsakemu viru, ki ga je mogoče rezervirati, dodati tudi privzeto vlogo. Odprite možnost **Viri** \> **Viri**. Na zavihku **Project Service** preverite, ali je vloga vira določena in ali je polje **Je privzeto** nastavljeno na **Da**. Kjer je vrednost **Je privzeto = Ne**, lahko dodate dodatne vloge. Vloga, pri kateri je vrednost **Je privzeto = Da**, se uporablja za oceno uporabe vira v primerjavi s ciljem za to vlogo.

![Nastavitev privzete vloge.](media/Resource-Management-image67.png)

Na zavihku **Project Service** lahko nastavite tudi posamično ciljno uporabo za vir. Izračun uporabe nato uporabi to ciljno uporabo za oceno cilja vira namesto cilja privzete vloge vira.

Uporaba se za posamezen vir prikaže samo, če je vir odobril čas, ki se zaračuna, v obdobju, ki je prikazan v mreži.

## <a name="resource-availability"></a>razpoložljivosti vira

Upravitelji virov morajo imeti možnost ogleda razpoložljivosti virov in posodobitve rezervacij. V nekaterih primerih ni uradnega povpraševanja (zahteve za vir), vendar se mora upravitelj virov odzvati na nenačrtovano povpraševanje, ki prihaja prek različnih kanalov, na primer elektronske pošte, telefonskih klicev ali neposrednih sporočil. Upravitelji virov uporabljajo ploščo razporeda za posodabljanje virov in rezervacij.

Delovni čas virov se uporablja kot osnova za izračun razpoložljivosti vira. Rezervacije virov porabijo del zmogljivosti virov.

![Plošča razporeda.](media/Resource-Management-image68.png)

Na plošči razporeda so za prikaz rezervacij, razpoložljivosti, prezasedenosti in stanja rezervacij uporabljene različne barve in senčenje. Z izbiro ustrezne nastavitve v nastavitvah plošče razporeda lahko prikažete tudi legendo.

Če je ob posameznem viru, ki ga je mogoče rezervirati, na plošči razporeda prikazana puščica v desno, lahko vir razširite in s tem prikažete podrobnosti o delu, za katerega je vir rezerviran.

![Razširitev vira, ki ga je mogoče rezervirati, na plošči razporeda.](media/Resource-Management-image69.png)

Ker rešitev Dynamics 365 Project Service Automation uporablja mehanizem Universal Resource Scheduling, si lahko tudi vi ogledate podrobnosti o rezervacijah virov za projekte, delovne naloge in vse druge entitete, na katere ste razširili razporejanje, ob predpostavki, da imate nameščeno aplikacijo Dynamics 365 Field Service.

![Podrobnosti o rezervacijah virov za projekte in delovne naloge.](media/Resource-Management-image70.png)

Če si želite ogledati podrobnosti o posameznem viru, ga kliknite z desno tipko miške, da odprete kartico vira.

![Kartica vira.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]