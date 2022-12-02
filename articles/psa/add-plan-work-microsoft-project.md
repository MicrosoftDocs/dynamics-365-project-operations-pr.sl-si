---
title: Uporaba dodatka za rešitev Project Service za načrtovanje dela v programu Microsoft Project | MicrosoftDocs
description: V tem članku najdete informacije o dodajanju, konfiguriranju in uporabi dodatka Microsoft Project za Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: d286adfdffa6a0b5f0c96eb14be588c6cedb80c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925554"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Uporaba dodatka za rešitev Project Service Automation za načrtovanje dela v Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] omogoča lažje načrtovanje projektov, vključno z ocenami. Delo lahko določite tako, da so stroški, zmogljivost in prodajna vrednost jasni, ko je predložen končni predlog.  

 Zdaj lahko namestite program [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] in začnete načrtovati v znanem okolju [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Uporabite zanesljive zmogljivosti načrtovanja in upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in nato posodobite svoj načrt projekta v rešitvi Project Service Automation.  

> [!IMPORTANT]
> - Če želite uporabljati funkcijo upravljanja dokumentov SharePoint za shranjevanje datotek [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] za projekte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], mora vaš skrbnik za [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vklopiti funkcijo upravljanja dokumentov. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je združljiv le s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Prenos in namestitev dodatka  
 Pripravite svoje vpisne podatke za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Te podatke potrebujete, da se s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] lahko povežete v rešitev [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Iz središča za prenose prenesite dodatek za podprto različico aplikacije Project Service, [V2. X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) ali [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Kliknite povezavo za prenos.  

3.  Ko je prenos končan, kliknite **Da**, da namestite dodatek.  

## <a name="configure-the-add-in"></a>Konfiguracija dodatka  

1. Odprite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in kliknite zavihek **Project Service**.  

2. Kliknite **Poveži**.  

3. Vnesite podatke za vpis in nato kliknite **Vpis**.  

   Zdaj lahko začnete uporabljati dodatek.  

## <a name="read-from-a-template"></a>Branje iz predloge  
 Berite iz predloge, ki ste jo ustvarili v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in kopirali v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], ter začnite načrtovanje projektov. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Ustvarjanje projektne predloge (Project Service Automation)](../psa/create-project-template.md)  

1.  Na zavihku **Project Service** kliknite **Branje** > **Projektna predloga rešitve Project Service Automation**.  

2.  Na seznamu izberite projektno predlogo in nato kliknite **Odpri**.  

    > [!NOTE]
    >  Opravila, ki ste jih iz predloge kopirali v Projekt, so privzeto nastavljena kot ročno razporejena.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Dodeljevanje vlog rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] virom projekta  

1.  Odprite projekt in kliknite trak **Opravilo**.  

2.  Kliknite meni **Ganttov grafikon** in nato izberite **List z viri**.  

3.  Na listu z viri kliknite spustni meni **Vloga vira rešitve Project Service** in izberite vlogo rešitve Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Dodajanje virov za projekt  

1.  Na zavihku rešitve Project Service izberite vrstico in kliknite **Poišči vire**.  

2.  Na zaslonu **Rezerviraj vir** izberite vir, ki ga želite uporabiti za projekt.  

3.  Kliknite **Rezerviraj** in nato **V redu**.  

## <a name="publish-your-project"></a>Objava projekta  
Ko končate z načrtovanjem projekta, sledi uvoz in objava projekta v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt se bo uvozil v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Oblikovati je treba ceno in ustvariti ekipo. Odprite projekt v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], da preverite, ali so ekipa, ocene za projekte in strukturirana členitev dela ustvarjene. Spodnja tabela prikazuje, kje lahko najdete rezultate:

| Projekt | Details |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttov grafikon**   | Uvoze na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Strukturirane členitve dela**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **List z viri** |   Uvozi na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Člani projektne ekipe**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Uporaba uporabe**    |    Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Ocene projekta**.     |

**Uvoz in objava projekta**  
1. Na zavihku **Project Service** kliknite **Objavi** > **Nov projekt rešitve Project Service Automation**.  

2. V pogovornem oknu **Objavi v nov projekt rešitve Project Service** vnesite **Ime projekta** in izberite možnost **Stranka**.  

3. Po želji potrdite možnost **Poveži načrt projekta z rešitvijo Project Service Automation**, da datoteko za načrtovanje projekta povežete z rešitvijo Project Service Automation.  

4. Kliknite **Objavi**.  

   Če povežete projektno datoteko z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projektna datoteka postane glavna datoteka in strukturirano členitev dela v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nastavi samo za branje.  Če želite spremeniti načrt projekta, morate to storiti v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in spremembe objaviti kot posodobitve za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Urejanje projekta, ki je bil uvožen  
 Če želite spremeniti načrt projekta, ki je bil uvožen v rešitev [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], imate dve možnosti:  

- Odprite glavno datoteko in jo uredite v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Odstranite povezavo do datoteke in jo uredite neposredno v rešitvi Project Service. Projekt, ki je bil prenesen iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], je privzeto zaklenjen in ga je mogoče urejati le v projektu. Če želite urediti datoteko v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], mora biti povezava do datoteke odstranjena.  

### <a name="edit-in-pn_microsoft_project"></a>Urejanje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. V glavnem meniju kliknite **Project Service** > **Projekti**.  

2. Na seznamu projektov odprite tisti projekt, ki ste ga ustvarili v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na traku kliknite **Odpri v programu MS Project**. V programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se bo odprla glavna povezana datoteka.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Odstranjevanje povezave do datoteke in urejanje datoteke v storitvi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. V glavnem meniju kliknite **Project Service** > **Projekti**.  

2. Na seznamu projektov odprite tisti projekt, ki ste ga ustvarili v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na traku kliknite **Odstrani povezavo s programom MS Project**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Nalaganje projektne datoteke v skupine storitve SharePoint ali Office  
 Projektno datoteko lahko naložite v SharePoint, kjer jo v možnosti »Povezani dokumenti« najdete za svoj projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Skrbnik mora nastaviti funkcijo upravljanja dokumentov SharePoint in jo vklopiti za entiteto »Projekt«. 

 Prav tako lahko svojo projektno datoteko naložite v [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], če imate nastavljene skupine storitve Office.

### <a name="upload-a-file-for-sharepoint"></a>Nalaganje datoteke za SharePoint  

1. V glavnem meniju kliknite **Project Service** > **Naloži**.  

2. Izberite **V projektne dokumente rešitve Project Service Automation**.  

3. V pogovornem oknu **Omogoči odpiranje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izberite **Da** ali **Ne**.  

   - Če kliknete **Da**, boste lahko izbrali gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v rešitvi Project Service Automation ter tako zagnali [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in naložili projektno datoteko iz knjižnice dokumentov SharePoint.  

   - Če kliknete **Ne**, povezava za gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne bo delovala.  

4. Datoteko [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je mogoče najti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v možnosti **Dokumenti** za določen projekt rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Nalaganje datoteke za skupine storitve Office  

1. V glavnem meniju kliknite **Project Service** > **Naloži**.  

2. Izberite **V projektne dokumente rešitve Project Service Automation**.  

3. V pogovornem oknu **Omogoči odpiranje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izberite **Da** ali **Ne**.  

   - Če kliknete **Da**, boste lahko izbrali gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v rešitvi Project Service Automation ter tako zagnali [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in naložili projektno datoteko iz knjižnice dokumentov SharePoint.  

   - Če kliknete **Ne**, povezava za gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne bo delovala.  

4. Datoteko [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je mogoče najti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v možnosti **Dokumenti** za določen projekt rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Objava projekta kot predloge  
 Svoj projekt lahko shranite in ga znova uporabite tako, da ga shranite kot projektno predlogo v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Projektne predloge so načrti projektov, ki jih je mogoče znova uporabiti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Ustvarjanje projektne predloge (Project Service Automation)](../psa/create-project-template.md)  

1. Na zavihku **Project Service** kliknite **Objavi** > **Nova projektna predloga rešitve Project Service Automation**.  

2. V pogovornem oknu **Objavi v nov projekt predloge rešitve Project Service** vnesite **Ime projektne predloge**.  

3. Po želji potrdite možnost **Poveži načrt projekta z rešitvijo Project Service Automation**, da datoteko projekta povežete z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Kliknite **Objavi**.  

Če povežete projektno datoteko z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projektna datoteka postane glavna datoteka in strukturirano členitev dela v predlogi rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nastavi samo za branje.  Če želite spremeniti načrt projekta, morate to storiti v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in spremembe objaviti kot posodobitve za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Preberite razpored naloženih virov

Ko berete projekt iz storitve Project Service Automation, koledar vira ni sinhroniziran z namiznim odjemalcem. Če obstajajo razlike v trajanju, količino dela ali koncu opravila, je to verjetno zato, ker viri in namizni odjemalec nimata iste predloge koledarja za delovne ure projekta.


## <a name="data-synchronization"></a>Sinhronizacija podatkov

Naslednja tabela prikazuje, kako se sinhronizirajo podatki med storitvijo Project Service Automation in namiznim vtičnikom Microsoft Project.

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Projektno opravilo | Datum zapadlosti | ● | - |
| Projektno opravilo | Predviden obseg dela | ● | - |
| Projektno opravilo | ID odjemalca za MS Project | ● | - |
| Projektno opravilo | Nadrejeno opravilo | ● | - |
| Projektno opravilo | Project | ● | - |
| Projektno opravilo | Projektno opravilo | ● | - |
| Projektno opravilo | Ime projektnega opravila | ● | - |
| Projektno opravilo | Enota vira (zastarelo od različice 3.0) | ● | - |
| Projektno opravilo | Načrtovano trajanje | ● | - |
| Projektno opravilo | Datum začetka | ● | - |
| Projektno opravilo | ID SČD | ● | - |

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Član ekipe | ID odjemalca za MS Project | ● | - |
| Član ekipe | Naziv delovnega mesta | ● | - |
| Član ekipe | projekt | ● | ● |
| Član ekipe | Projektna ekipa | ● | ● |
| Član ekipe | Enota vira | - | ● |
| Član ekipe | Vloga | - | ● |
| Član ekipe | Delovni čas | Ni sinhronizirano | Ni sinhronizirano |

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Dodelitev vira | Od datuma | ● | - |
| Dodelitev vira | ur | ● | - |
| Dodelitev vira | ID odjemalca za MS Project | ● | - |
| Dodelitev vira | Načrtovano delo | ● | - |
| Dodelitev vira | Project | ● | - |
| Dodelitev vira | Projektna ekipa | ● | - |
| Dodelitev vira | Dodelitev vira | ● | - |
| Dodelitev vira | Opravilo | ● | - |
| Dodelitev vira | Do danes | ● | - |

| **Entiteta** | **Polje** | **Microsoft Project v Project Service Automation** | **Project Service Automation v Microsoft Project** |
| --- | --- | --- | --- |
| Odvisnosti projektnih opravil | Odvisnost projektnega opravila | ● | - |
| Odvisnosti projektnih opravil | Vrsta povezave | ● | - |
| Odvisnosti projektnih opravil | Predhodno opravilo | ● | - |
| Odvisnosti projektnih opravil | Project | ● | - |
| Odvisnosti projektnih opravil | Naslednje opravilo | ● | - |

### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
