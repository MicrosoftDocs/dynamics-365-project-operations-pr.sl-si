---
title: Novosti in spremembe v storitvi Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji (julij 2021)
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v julijski (2021) izdaji storitve Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992721"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novosti in spremembe v storitvi Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji (julij 2021)

_**Velja za:** storitev Project Operations za scenarije, ki temeljijo na zalogi/proizvodnji_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

- Upravljanje projektov in računovodstvo v različici okolja 10.0.20 storitve Dynamics 365 Finance
 
### <a name="quality-updates"></a>Posodobitve kakovosti
                                                                                                                                                                                  
| Območje funkcij                      | Številka sklica| Posodobitev kakovosti                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upravljanje projektov in računovodstvo | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Zapisi o obveznostih s stroški v zahtevi za nabavo so izbrisani, takoj ko pri naročilnici ni več težav z zahtevo za nabavo.                                                                           |
| Upravljanje projektov in računovodstvo | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Proračun je v zahtevi za nabavo preverjen dvakrat. Podvajanje pomeni,da zahteve ne gre zapreti in da ustrezna naročilnica ni bila ustvarjena.                                                                                                                        |
| Upravljanje projektov in računovodstvo | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Pravila za izstavitev računa **Odstotki za obračun** ni bilo mogoče dokončati zaradi težave pri zaokroževanju.                                                                              |
| Upravljanje projektov in računovodstvo | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Ko prilagodite transakcijo in odstotek vsebuje decimalke, stroški in prodajna cena niso pravilno prilagojeni.                                      |
| Upravljanje projektov in računovodstvo | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Raziskovalec računovodskih virov prikazuje ure za vsako vrstico časovnega lista, in sicer za več vrstic časovnega lista za različne dejavnosti.                                      |
| Upravljanje projektov in računovodstvo | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Zaradi shranjenih pogledov in prilagajanja podrobnosti vrstice časovnega lista lahko sistem med poskusom odpiranja časovnega lista vedno odprte podrobnosti za prvi časovni list na seznamu.  |
| Upravljanje projektov in računovodstvo | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Korensko vozlišče projekta po uvozu izgine, zapisi o strukturirani členitvi dela pa so izbrisani.                                                                                             |
| Upravljanje projektov in računovodstvo | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Ko so elementi prejeti in delno izhajajo iz zahteve postavke, sistem posodobi napačen saldo za proračunsko porabo. |
| Upravljanje projektov in računovodstvo | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Na naročilnicah s predujmom projekta v podoknu **Vsote** ali v mreži **Čakajoči račun** niso popolnoma pravilno prikazane vsote.                                                                  |
| Upravljanje projektov in računovodstvo | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Pri zapiranju zalog se prilagoditve stroškov postavk projekta knjižijo na bilančni račun namesto v izkaz poslovnega izida.                                                            |
| Upravljanje projektov in računovodstvo | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Kupon za knjiženo projektno transakcijo in ocenjeni kupon kot računovodsko valuto uporabljata USD, kakšen je ekvivalent CAD, pa prikazuje znesek.              |
| Upravljanje projektov in računovodstvo | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Potrjena cena z zahtevo postavke in naročilnico je napačna znotraj procesa v računu za naročilnico z delnim računom za izdelek in delnim zaračunavanjem.       |
| Upravljanje projektov in računovodstvo | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Projektna prilagoditev prodajnih zneskov ne posodablja pravilno s posrednimi stroški.                                                                                    |
| Upravljanje projektov in računovodstvo | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabela **Časovni list** nima opredeljenega odnosa s pogledom **Delavec/Vir**.                                                                                   |
| Upravljanje projektov in računovodstvo | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Polja **Številka dejavnosti** ni mogoče izpolniti, ko ga izberete na spustnem meniju za časovni list med podjetji.                                                                 |
| Upravljanje projektov in računovodstvo | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Prilagojeno polje **Namen** ali **Opis dejavnosti** lahko dodate na naslednje strani: **Knjižena projektna transakcija**, **Ustvarjanje predloga za račun** ali **Predlog za račun**.  |
| Upravljanje projektov in računovodstvo | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Ko z uporabo možnosti upravljanja podatkov ustvarite zahteve postavk (**ProjSalesItemRequirementEntity**), je naveden napačen kontrolnik datuma dostave.                                              |
| Upravljanje projektov in računovodstvo | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Ko v storitvi Finance izberete ID projektne pogodbe, integrirano okolje Project Operations odpre stran in tako ustvari nov zapis, namesto da bi odprlo obstoječo projektno pogodbo.                                                                                                                 |
| Upravljanje projektov in računovodstvo | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Oznaka, »@SYS4083080« (»Enoličnega zapisa »Delavec«, ki ustreza vnesenim vrednostim«, ni mogoče najti) ni prevedena v danščino.                                |
| Upravljanje projektov in računovodstvo | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Polja **Skupina davka od prodaje izdelkov** v predlogu za račun ni mogoče urejati.                                                                               |
| Upravljanje projektov in računovodstvo | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Potrjena cena je previsoka, saj od nje ni odbit znesek davka.                                                                                                    |
| Upravljanje projektov in računovodstvo | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Knjiženje časovnega lista med podjetji z več projekti in različnimi finančnimi razsežnostmi v glavni knjigi ustvari nepričakovane vrednosti.                             |
| Upravljanje projektov in računovodstvo | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Vrstice predlogov za račune se podvojijo zaradi velikega števila primerkov periodičnega postopka, hkrati pa se izvaja storitev **Uvoz iz pripravljanja**.                                      |
| Upravljanje projektov in računovodstvo | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Pri knjiženju predloga za račun za dobropis je prišlo do napake, zato transakcije na kuponu niso uravnotežene.    |
| Upravljanje projektov in računovodstvo | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Potrjena cena v okviru projekta postane napačna, potem ko so izdani čakajoči računi na čakanju.                                                                             |
| Upravljanje projektov in računovodstvo | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Dobropisa za prodajni nalog projekta ne morete ustvariti, ko za davek ni uporabljena valuta podjetja.                                      |
| Upravljanje projektov in računovodstvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Če izbrišete pogodbo, se izbriše tudi s stranko povezan naslov.                                                                                     |
| Upravljanje projektov in računovodstvo | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Predloga za račun, ki je posledica negativnega popravka časovne transakcije, ni mogoče knjižiti.                                                                    |
| Pot in stroški                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Davek je v poročilih o stroških izračunan na drugačen način.                                                                                                                  |
| Pot in stroški                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Posodobitev izdaje **DB72_Expense.updateTrvExpTransProjTransId()**   elementu **trvExpTrans.ReferenceDataAreaId** ne dovoli, da bi ustvaril novo zaporedje števil.                    |
| Pot in stroški                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Polje z zneskom se ne prikaže skupaj z obveznim poljem.                                                                                                             |
| Pot in stroški                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Izboljšave učinkovitosti dodajanja stroška v poročilo o stroških ob uporabi uporabniškega vmesnika za prenovljene stroške.                                                            |
| Pot in stroški                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Knjižena poročila o stroških lahko izbrišete.                                                                                           |
| Pot in stroški                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Sporočilo o pravilniku glede stroškov se prikaže večkrat.                                                                                                       |
| Pot in stroški                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Polje **Način plačila** je vključeno v podokno **Nov strošek**.                                                                                                      |
| Pot in stroški                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Če poteka dela ni mogoče najti, mora orodje **Ponastavi stanje dokumenta o stroških** stanje poročila o stroških ponastaviti na možnost **Osnutek**. 

### <a name="regulatory-updates"></a>Regulativne posodobitve
Za informacije o regulativnih posodobitvah za aplikacije Finance and Operations glejte [Regulativne posodobitve](/dynamics365/finance/localizations/regulatory-updates). Prav tako se lahko prijavite v storitev Lifecycle Services (LCS) in si s pomočjo orodja za iskanje težav ogledate načrtovane regulativne posodobitve. Iskanje težav omogoča iskanje po državi, vrsti funkcije in izdaji.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
