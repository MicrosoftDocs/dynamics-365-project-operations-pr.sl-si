---
title: Vidiki nadgradnje – Microsoft Dynamics 365 Project Service Automation različice 2.x ali 1.x na različico 3
description: Ta članek vsebuje informacije o premislekih, ki jih morate upoštevati pri nadgradnji z različice Project Service Automation 2.x ali 1.x na različico 3.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f67b2fe39c9d0224207e7c655892318ec7e09b8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918930"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Vidiki nadgradnje – nadgradnja storitve PSA različice 2.x ali 1.x na različico 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Storitvi Project Service Automation in Field Service
Storitvi Dynamics 365 Project Service Automation in Dynamics 365 Field Service uporabljata rešitev Universal Resourcing Scheduling (URS) za razporejanje virov. Če imate v svojem primerku Project Service Automation in Field Service, posodobite obe rešitvi na najnovejšo različico. Za Project Service Automation je to različica 3.x. Za Field Service je to različica 8.x. Z nadgradnjo storitve Project Service Automation ali Field Service se namesti najnovejša različica URS. Če nista oba rešitvi, Project Service Automation in Field Service, v istem primerku nadgrajeni na isto različico, je lahko obnašanje nedosledno.

## <a name="resource-assignments"></a>Dodelitve virov
Dodelitve opravil so bile v rešitvi Project Service Automation različic 2 in 1 shranjene kot podrejena opravila (imenovana tudi opravila vrstice) v polju **Entiteta opravila** in neposredno povezane z entiteto **Dodelitev vira**. Opravilo vrstice je bilo prikazano v pojavnem oknu dodelitev v strukturirani členitvi dela (SČD).

![Opravila vrstice v SČD v storitvi Project Service Automation različice 2 in različice 1.](media/upgrade-line-task-01.png)

V storitvi Project Service Automation različice 3 je spremenjena temeljna shema za dodeljevanje virov, ki jih je mogoče rezervirati, opravilom. Opravilo vrstice je zastarelo in neposredno razmerje med opravilom v polju **Entiteta opravila** in članom ekipe v entiteti **Dodelitev vira** je 1:1. Opravila, ki so dodeljena članu projektne ekipe, so zdaj shranjena neposredno v entiteti dodelitve virov.  

Te spremembe vplivajo na nadgradnjo vseh obstoječih projektov, ki imajo dodelitve virov za imenovane vire, ki jih je mogoče rezervirati, in splošne vire v projektni ekipi. Ta članek vsebuje premisleke, ki jih boste morali upoštevati pri svojih projektih, ko nadgradite na različico 3. 

### <a name="tasks-assigned-to-named-resources"></a>Opravila, dodeljena poimenovanim virom
S temeljno entiteto opravila so opravila v različici 2 in različici 1 članom ekipe omogočala uporabo vloge, ki ni njihova privzeta določena vloga. Mateja Hribar, ki ji je na primer privzeto dodeljena vloga upravitelja programa, se lahko dodeli opravilo z vlogo razvijalca. V različici 3 je vloga imenovanega člana ekipe vedno privzeta, zato vsako opravilo, dodeljeno Mateji Hribar, uporablja Matejino privzeto vlogo upravitelja programa.

Če ste vir dodelili opravilu zunaj privzete vloge v različici 2 in različici 1, bo imenovani vir po nadgradnji dodeljen privzeti vlogi za vse dodelitve opravil ne glede na dodelitev vloge v različici 2. Ta dodelitev bo privedla do različnih izračunanih ocen v različici 2 ali različici 1 ter različici 3, ker se ocene izračunajo na podlagi vloge vira in ne na podlagi dodelitve opravila vrstice. V različici 2 sta na primer bili dve opravili dodeljeni Ani Breznik. Vloga v opravilu vrstice za opravilo 1 je »Razvijalec«, za opravilo 2 pa »Upravitelj programa«. Ana Breznik ima privzeto vlogo »Upravitelj programa«.

![Več vlog, dodeljenih enemu viru.](media/upgrade-multiple-roles-02.png)

Ker se vlogi razvijalca in upravitelja programa razlikujeta, so ocene stroškov in prodaje naslednje:

![Ocene stroškov za vloge virov.](media/upggrade-cost-estimates-03.png)

![Ocene prodaje za vloge virov.](media/upgrade-sales-estimates-04.png)

Ko nadgradite na različico 3, bodo opravila vrstice zamenjana z dodelitvami virov v opravilu člana ekipe vira, ki ga je mogoče rezervirati. Dodelitev bo uporabila privzeto vlogo vira, ki ga je mogoče rezervirati. Na naslednjem grafičnem prikazu je vir Ana Breznik, ki ima vlogo upravitelja programa.

![Dodelitev virov.](media/resource-assignment-v2-05.png)

Ker ocene temeljijo na privzeti vlogi za vir, se lahko ocene prodaje in stroškov spremenijo. Naslednji grafični prikaz ne vključuje vloge **Razvijalec**, ker je vloga zdaj izbrana glede na privzeto vlogo vira, ki ga je mogoče rezervirati.

![Ocene stroškov za privzete vloge.](media/resource-assignment-cost-estimate-06.png)
![Ocene prodaje za privzete vloge.](media/resource-assignment-sales-estimate-07.png)

Ko je nadgradnja dokončana, lahko izberete vlogo člana ekipe, ki ni privzeto dodeljena. Če pa spremenite vlogo člana ekipe, se bo spremenila pri vseh njegovih dodeljenih opravilih, ker članom ekipe v različici 3 ni dovoljeno dodeljevati več vlog.

![Posodobitev vloge vira.](media/resource-role-assignment-08.png)

To velja tudi za opravila vrstice, ki so bila dodeljena poimenovanim virom, ko privzeto organizacijsko enoto vira spremenite v drugo organizacijsko enoto. Ko je nadgradnja na različico 3 dokončana, bo dodelitev uporabila privzeto organizacijsko enoto vira namesto tiste, ki je nastavljena v opravilu vrstice.

### <a name="tasks-assigned-to-generic-resources"></a>Opravila, dodeljena splošnim virom
V različici 2 in različici 1 lahko nastavite vlogo in organizacijsko enoto v opravilu ter nato uporabite funkcijo **Ustvari ekipo**, da ustvarite splošne vire na podlagi atributov, ki so nastavljeni v opravilu. V različici 3 lahko ustvarite splošne člane ekipe z vlogo in organizacijsko enoto ter jim nato dodelite opravila.

V različici 2 in različici 1 lahko projekti s splošnimi viri imajo dva stanja ali pa kombinacijo obeh stanj na ravni opravila. Lahko imate na primer naslednje scenarije:

- Nastavljena so opravila z vlogami in organizacijskimi enotami, vendar ni bila ustvarjena nobena povezana dodelitev vira.
- Opravila z dodelitvami virov splošnim članom ekipe, ki so bila dodeljena z ustvarjanjem splošnega vira s funkcijo **Ustvari ekipo**.

Pred nadgradnjo priporočamo, da znova ustvarite ekipo za vsak projekt, ki ima opravila, dodeljena splošnim virom, ali opravila, za katera je še treba izvesti postopek ustvarjanja ekipe.

Pri opravilih, dodeljenih splošnim članom ekipe, ki so bila ustvarjena s funkcijo **Ustvari ekipo**, bo z nadgradnjo ohranjen splošni vir v ekipi in dodelitev temu splošnemu članu ekipe. Priporočamo, da ustvarite zahtevo vira za splošnega člana ekipe po posodobitvi, vendar pred rezervacijo ali pošiljanjem zahteve za vir. Tako bodo ohranjene vse dodelitve organizacijskih enot pri splošnih članih ekipe, ki se razlikujejo od pogodbene organizacijske enote projekta.

Pri projektu Projekt Z je na primer pogodbena organizacijska enota Contoso US. V načrtu projekta je bilo preizkušanje opravil na uvajalni stopnji dodeljeno vlogi »Tehnični svetovalec« in dodeljena organizacijska enota je bila Contoso India.

![Dodelitev organizacije na uvajalni stopnji.](media/org-unit-assignment-09.png)

Po uvajalni stopnji je opravilo preizkusa integracije dodeljeno vlogi »Tehnični svetovalec«, toda organizacijska enota je nastavljena na Contoso US.  

![Dodelitev organizacijske enote za opravilo preizkusa integracije.](media/org-unit-generate-team-10.png)

Ko ustvarite ekipo za projekt, sta zaradi različnih organizacijskih enot v opravilih ustvarjena dva splošna člana ekipe. Tehničnemu svetovalcu 1 bodo dodeljena opravila enote Contoso India, tehničnemu svetovalcu 2 pa opravila enote Contoso US.  

![Ustvarjeni splošni člani ekipe.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Član ekipe v storitvi Project Service Automation različice 2 in različice 1 ne nadzira organizacijske enote, ki je vzdrževana v opravilu vrstice.

![Opravila vrstice v storitvi Project Service Automation različice 2 in različice 1.](media/line-tasks-12.png)

Organizacijsko enoto si lahko ogledate v pogledu ocen. 

![Ocene organizacijskih enot.](media/org-unit-estimates-view-13.png)
 
Ko je nadgradnja dokončana, je organizacijska enota v opravilu vrstice, ki ustreza splošnemu članu ekipe, dodana splošnemu članu ekipe in opravilo vrstice je odstranjeno. Zaradi tega priporočamo, da pred nadgradnjo ustvarite ali znova ustvarite ekipo za vsak projekt, ki vsebuje splošne vire.

Pri opravilih, ki so dodeljena vlogi z organizacijsko enoto, ki se razlikuje od organizacijske enote pogodbenega projekta, in za katere skupina ni ustvarjena, bo z nadgradnjo ustvarjen splošni član ekipe za vlogo, pogodbena enota projekta pa bo uporabljena kot organizacijska enota člana ekipe. Če se sklicujemo na primer s Projektom Z, so pogodbena organizacijska enota Contoso US in opravila preizkusa iz načrta projekta na uvajalni stopnji bila dodeljena vlogi »Tehnični svetovalec« z dodeljeno organizacijsko enoto Contoso India. Opravilo preizkusa integracije, ki je bilo dokončano po uvajalni stopnji, je bilo dodeljeno vlogi »Tehnični svetovalec«. Organizacijska enota je Contoso US in ekipa ni bila ustvarjena. Z nadgradnjo bo ustvarjen en splošni član ekipe, tehnični svetovalec, ki ima dodeljene ure vseh treh opravil, in organizacijska enota Contoso US, ki je pogodbena organizacijska enota projekta.   
 
Zaradi spreminjanja privzetih vrednosti različnih organizacijskih enot virov pri neustvarjenih članih ekipe priporočamo, da pred nadgradnjo ustvarite ali znova ustvarite ekipo za vsak projekt, ki vsebuje splošne vire, tako da dodelitve organizacijskih enot ne bodo izgubljene.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
