---
title: Nastavitev predlog stroškov
description: Ta tema vsebuje informacije o tem, kako ustvariti in uporabljati predloge stroškov v storitvi Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4a515db31a31028af4a60927ab360be6c261a3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013911"
---
# <a name="set-up-cost-templates"></a>Nastavitev predlog stroškov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Ta tema vsebuje informacije o tem, kako ustvariti in uporabljati predloge stroškov v storitvi Project Operations. Predloga stroškov določa:

- Kategorije projektov za napovedi in dejanske transakcije se vključijo v izračun odstotka dokončanosti projekta. Odstotna vrednost dokončanosti se nato uporabi za izračun upoštevanega prihodka.
- Ali je mogoče odstotek dokončanja spremeniti, če se izračuna samodejno.
- Ali se odstotek dokončanja izračuna na podlagi zneskov ali enot.

## <a name="cost-template-example"></a>Primer predloge stroškov

Za stranko pripravljate projekt zasnove spletnega mesta, pri katerem zaračunavate pavšal v višini 10.000 dolarjev. Predvidevate, da bo potrebnih 100 ur (5.000 USD) za dokončanje projekta. Predvidevate, da bosta potrebni tudi dve letalski karti in štiri nočitve za potovanja na lokacijo stranke (1800 USD). Skupni napovedani stroški tako znašajo 6.800 dolarjev.

Ko ob koncu meseca zaženete postopek priznavanja prihodkov s fiksno ceno, da ustvarite oceno, ugotovite, da ste na projektu delali 35 ur. To še ne vključuje letov ali hotelskih stroškov. Imeli ste tudi pomočnika, ki je za projekt izvedel pet ur raziskav po ceni 100 USD, česar niste predvideli.

Ko izračunate odstotno vrednost dokončanja za ta projekt, se morate odločiti glede naslednjih dejavnikov:

- Ali želite vključiti vse stroške (ure in stroški) ali samo ure?
- Ali želite vključiti vse ure ali samo predvidene ure?
- Ali želite izračunati odstotek dokončanja na podlagi dolarskih stroška predvidenih ur v dolarjih (5000 USD) ali samo na podlagi števila ur (100)?

Odgovori na ta vprašanja določajo možnosti, ki ste jih nastavili v predlogi stroškov, in kategorije, ki jih izberete v podrobnostih predlog stroškov.

Naslednja tabela prikazuje rezultate različnih načinov za izračun odstotne vrednosti dokončanja za ta primer.

| Dokončanje na podlagi | Stroški ali enote v dolarjih | Odstotek dokončanja | Izračun |
| --- | --- | --- | --- |
| Vse ure, brez stroškov | Stroški v dolarjih | 37 % 35 x USD 50 + USD 100 = USD 1.850 USD 1.850/USD 5.000 |
| Vse ure, brez stroškov | Enote | 40 % | 40 ur/100 ur (vključno s petimi nenačrtovanimi urami) |
| Načrtovane ure, brez stroškov | Stroški ali enota v dolarjih | 35 % | 35/100 ur ali 35 x 50/5.000 USD |
| Vse ure in stroški | Stroški v dolarjih | 27,2 % | 1.850/6.800 USD |

Odločitev, kateri pristop uporabiti za izdelavo predloge stroškov, je lahko odvisna od več razlogov:

- Če v predlogo stroškov vključite nenačrtovane ure, tvegate, da boste dosegli 100-odstotno dokončanost še pred zaključkom projekta. Do tega bo prišlo zato, ker bo število dejanskih ur večje od načrtovanih. Če uporabite katero od prvih dveh metod iz tabele, morate spremeniti načrt (napovedane enote), ko ugotovite, da obstajajo odstopanja. V tem primeru bi ure dodali ali odšteli na podlagi vaše seznanjenosti s tem, kaj je potrebno za dokončanje projekta. Če bo za dokončanje projekta potrebnih še 65 ur, bi načrtu dodali pet ur za skupno 105 ur. Če veste, da bo vaš pomočnik opravil še pet ur raziskav, se bo skupno število povečalo na 110 ur.
- Če uporabite tretjo metodo v tabeli, bi morali predvidene ure posodobiti le za svoj čas, da bi bil izračun dokončanja v odstotkih natančen. Dobičkonosnost se bo z vpisom nepredvidenih ur spremenila, vendar boste točno vedeli, kakšen je vaš odstotek dokončanja.
- Če uporabite četrto metodo iz tabele, obstaja tveganje, da se bodo stroški pojavili ob neenakomernih trenutkih in se ne bodo odražali v napredku v obliki odstotka dokončanja. Če so vključeni tudi stroški, lahko to povzroči večje nihanje odstotka dokončanja, kot je zaželeno. Ker še niste potovali z letalom, je vaš odstotek dokončanja znašal 27 odstotkov in ne 35 ali 37 odstotkov, če bi izračun naredili le na podlagi časa. Če bi se odpravili na potovanje z dvema nočitvama in natančno napovedali stroške leta in hotela, bi celotni odstotek dokončanja znašal 40,4 odstotka (1850 USD za delo in 900 USD za stroške = 2750 USD/6800 USD = 40,4 odstotka). Zato bi upoštevanje stroškov samo enega potovanja z letalom spremenilo odstotek dokončanja s 27 na 40 odstotkov.

## <a name="create-cost-templates"></a>Ustvarjanje predlog stroškov
Za ustvarjanje predlog stroškov sledite spodnjim navodilom:

1. Za dostop do predlog stroškov v okolju Dynamics 365 Finance pojdite v razdelek **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Ocene** > **Predloga stroškov**.
2. Če želite ustvariti novo predlogo stroškov, izberite **Novo**. Vnesite Ime in opis.
3. Navedite ID vrstice cene za vsako vrsto transakcije.
4. Izberite privzeti način dokončanja:

  - **Samodejno**: odstotek dokončanja projekta se samodejno izračuna. Ustvarjene vrednosti ni mogoče spremeniti.
  - **Ročno**: odstotek dokončanja projekta se samodejno izračuna. Ustvarjene vrednosti ni mogoče spremeniti.

  > [!NOTE]
  > Pri ročnih izračunih se odstotek dokončanja ohrani v polju **Ročni izračun** v zavihku **Splošno** na strani **Ocena**.

5. V polju **Dokončanje na podlagi** izberite eno od naslednjih vrednosti:

  - **Znesek**: znesek v računovodski valuti izračuna odstotek dokončanja.
  - **Enota**: količina izračuna odstotek dokončanja.
  - **Ravna črta**: sistem izračuna odstotek dokončanja glede na uporabo začetnega in končnega datuma projekta za določitev dolžine projekta.

6. Izberite **Vrstice cene** za pregled vrstic cene na predlogi stroškov. Za vsako vrsto transakcije je potrebna vsaj ena vrstica cene. Lahko pa ustvarite več vrstic cene za isto vrsto transakcij in nastavite želene atribute za te vrstice.
7. V zavihku **Kategorije** izberite kategorije projektov, ki jih želite vključiti v predlogo vrstic cene.
8. V zavihku **Splošno** izberite, ali bo ta vrstica vključena v izračun odstotka dokončanja.
9. Izberite metodo za izračun cene za dokončanje, ki bo uporabljena pri izračunu odstotka dokončanja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]