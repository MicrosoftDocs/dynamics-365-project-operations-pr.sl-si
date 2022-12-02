---
title: Načrtovanje dela v programu Microsoft Project z dodatkom Project Service
description: V tem članku najdete informacije o uporabi dodatka Microsoft Project za Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 779d83a896dd7d92c6584e6f1c57b1ea567e9051
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911018"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Načrtovanje dela v programu Microsoft Project z dodatkom Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] omogoča lažje načrtovanje projektov, vključno z ocenami. Delo lahko določite tako, da so stroški, zmogljivost in prodajna vrednost jasni, ko je predložen končni predlog.  

Namestite [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] in začnite načrtovati v znanem okolju programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Uporabite zanesljive zmogljivosti načrtovanja in upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in nato posodobite svoj načrt projekta v rešitvi Project Service Automation.  

> [!IMPORTANT]
> - Če želite uporabljati funkcijo upravljanja dokumentov SharePoint za shranjevanje datotek [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] za projekte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], mora vaš skrbnik za [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vklopiti funkcijo upravljanja dokumentov. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je združljiv le s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Prenos in namestitev dodatka  
 Pripravite svoje vpisne podatke za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Te podatke potrebujete, da se s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] lahko povežete v rešitev [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Iz središča za prenose prenesite dodatek za podprto različico aplikacije Project Service, [V2. X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) ali [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Izberite povezavo za prenos.  

3.  Ko je prenos končan, izberite **Da**, da namestite dodatek.  

## <a name="configure-the-add-in"></a>Konfiguracija dodatka  

1. Odprite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in izberite zavihek **Project Service**.  

2. Izberite **Vzpostavljanje povezave**.  

3. Vnesite podatke za vpis in nato izberite **Vpis**.  

   Zdaj lahko začnete uporabljati dodatek.  

## <a name="read-from-a-template"></a>Branje iz predloge  
 Berite iz predloge, ki ste jo ustvarili v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in kopirali v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], ter začnite načrtovanje projektov. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Ustvarjanje projektne predloge (Project Service Automation)](../psa/create-project-template.md)  

1.  Na zavihku **Project Service** izberite **Branje** > **Projektna predloga rešitve Project Service Automation**.  

2.  Na seznamu izberite projektno predlogo in nato še **Odpri**.  

    > [!NOTE]
    >  Opravila, ki ste jih iz predloge kopirali v Projekt, so privzeto nastavljena kot ročno razporejena.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Dodeljevanje vlog rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] virom projekta  

1.  Odprite projekt in izberite trak **Opravilo**.  

2. Izberite meni **Ganttov grafikon** in nato še **List z viri**.  

3. Na listu z viri izberite spustni meni **Vloga vira rešitve Project Service** in nato še vlogo rešitve Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Dodajanje virov za projekt  

1.  Na zavihku rešitve Project Service izberite vrstico in **Poišči vire**.  

2.  Na zaslonu **Rezerviraj vir** izberite vir, ki ga želite uporabiti za projekt.  

3.  Izberite **Rezerviraj** in nato **V redu**.  

## <a name="publish-your-project"></a>Objava projekta  
Ko končate z načrtovanjem projekta, sledi uvoz in objava projekta v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt se bo uvozil v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Oblikovati je treba ceno in ustvariti ekipo. Odprite projekt v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], da preverite, ali so ekipa, ocene za projekte in strukturirana členitev dela ustvarjene. Spodnja tabela prikazuje, kje lahko najdete rezultate.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttov grafikon**   | Uvoze na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Strukturirane členitve dela**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **List z viri** |   Uvozi na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Člani projektne ekipe**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Uporaba uporabe**    |    Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Ocene projekta**.     |

**Uvoz in objava projekta**  
1. Na zavihku **Project Service** izberite **Objavi** > **Nov projekt rešitve Project Service Automation**.  

2. V pogovornem oknu **Objavi v nov projekt rešitve Project Service** vnesite **Ime projekta** in izberite možnost **Stranka**.  

3. Po želji izberite možnost **Poveži načrt projekta z rešitvijo Project Service Automation**, da datoteko za načrtovanje projekta povežete z rešitvijo Project Service Automation.  

4. Izberite **Objavi**.  

   Če povežete projektno datoteko z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projektna datoteka postane glavna datoteka in strukturirano členitev dela v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nastavi samo za branje.  Če želite spremeniti načrt projekta, morate to storiti v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in spremembe objaviti kot posodobitve za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Urejanje projekta, ki je bil uvožen  
 Če želite spremeniti načrt projekta, ki je bil uvožen v rešitev [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], imate dve možnosti:  

- Odprite glavno datoteko in jo uredite v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Odstranite povezavo do datoteke in jo uredite neposredno v rešitvi Project Service. Projekt, ki je bil prenesen iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], je privzeto zaklenjen in ga je mogoče urejati le v projektu. Če želite urediti datoteko v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], mora biti povezava do datoteke odstranjena.  

### <a name="edit-in-pn_microsoft_project"></a>Urejanje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. V glavnem meniju izberite **Project Service** > **Projekti**.  

2. Na seznamu projektov odprite tistega, ki ste ga ustvarili v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na traku izberite **Odpri v programu MS Project**. V programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se bo odprla glavna povezana datoteka.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Odstranjevanje povezave do datoteke in urejanje datoteke v storitvi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. V glavnem meniju izberite **Project Service** > **Projekti**.  

2. Na seznamu projektov odprite tistega, ki ste ga ustvarili v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na traku izberite **Odstrani povezavo s programom MS Project**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Nalaganje projektne datoteke v skupine storitve SharePoint ali Office  
 Projektno datoteko lahko naložite v SharePoint, kjer jo v možnosti »Povezani dokumenti« najdete za svoj projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Skrbnik mora nastaviti funkcijo upravljanja dokumentov SharePoint in jo vklopiti za entiteto »Projekt«. 

 Prav tako lahko svojo projektno datoteko naložite v [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], če imate nastavljene skupine storitve Office.

### <a name="upload-a-file-for-sharepoint"></a>Nalaganje datoteke za SharePoint  

1. V glavnem meniju izberite **Project Service** > **Naloži**.  

2. Izberite **V projektne dokumente rešitve Project Service Automation**.  

3. V pogovornem oknu **Omogoči odpiranje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izberite **Da** ali **Ne**.  

   - Če izberete **Da**, lahko izberete **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v rešitvi Project Service Automation, zaženete [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in naložite projektno datoteko iz knjižnice dokumentov SharePoint.  

   - Če izberete **Ne**, povezava za **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne bo delovala.  

4. Datoteko [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je mogoče najti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v možnosti **Dokumenti** za določen projekt rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Nalaganje datoteke za skupine storitve Office  

1. V glavnem meniju izberite **Project Service** > **Naloži**.  

2. Izberite **V projektne dokumente rešitve Project Service Automation**.  

3. V pogovornem oknu **Omogoči odpiranje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izberite **Da** ali **Ne**.  

   - Če izberete **Da**, lahko izberete **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v rešitvi Project Service Automation, zaženete [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in naložite projektno datoteko iz knjižnice dokumentov SharePoint.  

   - Če izberete **Ne**, povezava za **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne bo delovala.  

4. Datoteko [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je mogoče najti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v možnosti **Dokumenti** za določen projekt rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Objava projekta kot predloge  
 Svoj projekt lahko shranite in ga znova uporabite tako, da ga shranite kot projektno predlogo v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projektne predloge so načrti projektov, ki jih je mogoče znova uporabiti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Za več informacij glejte [Ustvarjanje projektne predloge (Project Service Automation)](../psa/create-project-template.md). 

1. Na zavihku **Project Service** izberite **Objavi** > **Nova projektna predloga rešitve Project Service Automation**.  

2. V pogovornem oknu **Objavi v nov projekt predloge rešitve Project Service** vnesite **Ime projektne predloge**.  

3. Po želji izberite možnost **Poveži načrt projekta z rešitvijo Project Service Automation**, da povežete datoteko projekta z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Izberite **Objavi**.  

Če povežete projektno datoteko z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projektna datoteka postane glavna datoteka in strukturirano členitev dela v predlogi rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nastavi samo za branje.  Če želite spremeniti načrt projekta, morate to storiti v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in spremembe objaviti kot posodobitve za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Preberite razpored naloženih virov

Ko berete projekt iz storitve Project Service Automation, koledar vira ni sinhroniziran z namiznim odjemalcem. Če obstajajo razlike v trajanju, količino dela ali koncu opravila, je to verjetno zato, ker viri in namizni odjemalec nimata iste predloge koledarja za delovne ure projekta.


## <a name="data-synchronization"></a>Sinhronizacija podatkov
V tabelah v tem razdelku so informacije o sinhronizaciji podatkov entitet med rešitvijo Project Service Automation in namiznim dodatkom za Microsoft Project.

### <a name="project-task-entity-table"></a>Tabela entitete projektnega opravila
Spodnja tabela prikazuje, kako se sinhronizirajo podatki entitete projektnega opravila med rešitvijo Project Service Automation in namiznim dodatkom za Microsoft Project.

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Projektno opravilo | Datum zapadlosti | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Predviden obseg dela | Synchronized | Ni sinhronizirano |
| Projektno opravilo | ID odjemalca za MS Project | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Nadrejeno opravilo | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Project | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Projektno opravilo | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Ime projektnega opravila | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Enota vira (zastarelo od različice 3.0) | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Načrtovano trajanje | Synchronized | Ni sinhronizirano |
| Projektno opravilo | Datum začetka | Synchronized | Ni sinhronizirano |
| Projektno opravilo | ID SČD | Synchronized | Ni sinhronizirano |

### <a name="team-member-entity-table"></a>Tabela entitete člana ekipe
Spodnja tabela prikazuje, kako se sinhronizirajo podatki entitete člana ekipe med rešitvijo Project Service Automation in namiznim dodatkom za Microsoft Project.

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Član ekipe | ID odjemalca za MS Project | Synchronized | Ni sinhronizirano |
| Član ekipe | Naziv delovnega mesta | Synchronized | Ni sinhronizirano |
| Član ekipe | projekt | Synchronized | Synchronized |
| Član ekipe | Projektna ekipa | Synchronized | Synchronized |
| Član ekipe | Enota vira | Ni sinhronizirano | Synchronized |
| Član ekipe | Vloga | Ni sinhronizirano | Synchronized |
| Član ekipe | Delovni čas | Ni sinhronizirano | Ni sinhronizirano |

### <a name="resource-assignment-entity-table"></a>Tabela entitete dodelitve virov
Spodnja tabela prikazuje, kako se sinhronizirajo podatki entitete dodelitve virov med rešitvijo Project Service Automation in namiznim dodatkom za Microsoft Project.

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Dodelitev vira | Od datuma | Synchronized | Ni sinhronizirano |
| Dodelitev vira | ur | Synchronized | Ni sinhronizirano |
| Dodelitev vira | ID odjemalca za MS Project | Synchronized | Ni sinhronizirano |
| Dodelitev vira | Načrtovano delo | Synchronized | Ni sinhronizirano |
| Dodelitev vira | Project | Synchronized | Ni sinhronizirano |
| Dodelitev vira | Projektna ekipa | Synchronized | Ni sinhronizirano |
| Dodelitev vira | Dodelitev vira | Synchronized | Ni sinhronizirano |
| Dodelitev vira | Opravilo | Synchronized | Ni sinhronizirano |
| Dodelitev vira | Do danes | Synchronized | Ni sinhronizirano |

### <a name="project-task-dependencies-entity-table"></a>Tabela entitete odvisnosti projektnih opravil
Spodnja tabela prikazuje, kako se sinhronizirajo podatki entitete odvisnosti projektnih opravil med rešitvijo Project Service Automation in namiznim dodatkom za Microsoft Project.

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Odvisnosti projektnih opravil | Odvisnost projektnega opravila | Synchronized | Ni sinhronizirano |
| Odvisnosti projektnih opravil | Vrsta povezave | Synchronized | Ni sinhronizirano |
| Odvisnosti projektnih opravil | Predhodno opravilo | Synchronized | Ni sinhronizirano |
| Odvisnosti projektnih opravil | Project | Synchronized | Ni sinhronizirano |
| Odvisnosti projektnih opravil | Naslednje opravilo | Synchronized | Ni sinhronizirano |

### <a name="additional-resources"></a>Dodatni viri
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
