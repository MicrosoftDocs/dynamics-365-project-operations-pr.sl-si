---
title: Mejniki vrstice podizvajalske pogodbe
description: Ta tema pojasnjuje, kako pri podizvajalskih pogodbah z dobaviteljem ustvarite in vzdržujete razpored za izstavljanje računov, ki temelji na mejnikih.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558522"
---
# <a name="subcontract-line-milestones"></a>Mejniki vrstice podizvajalske pogodbe

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Vrstica podizvajalske pogodbe z načinom obračunavanja s fiksno ceno v storitvi Dynamics 365 Project Operations lahko pri dobavitelju določi razpored za izstavljanje računov, ki temelji na mejnikih.

Mejniki za izstavljanje računov dobaviteljem se lahko ustvarijo samodejno, z nastavljeno pogostostjo, ali pa jih ustvarite ročno.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Samodejno ustvarite razpored za izstavljanje računov, ki temelji na mejnikih, za vrstico podizvajalske pogodbe

Dokončajte spodnje korake za samodejno ustvarjanje razporeda za izstavljanje računov, ki temelji na mejnikih, za nespremenljivi nabor enakomerno razporejenih mejnikov.

1. Izberite **Nastavitve** > **Pogostosti računov** in nastavite pogostost računov za vrstico podizvajalske pogodbe.
2. Odprite stran **Podizvajalske pogodbe**, odprite podizvajalsko pogodbo, s katero želite delati, nato pa odprite vrstico podizvajalske pogodbe s fiksno ceno, za katero boste ustvarili razpored mejnikov.
3. V zavihku **Mejniki vrstice podizvajalske pogodbe** izberite **Ustvari periodične mejnike**.
4. V pogovornem oknu vnesite ali izberite datumski obseg, število mejnikov in pogostost računov. Izberete lahko začetni datum ali število mejnikov in pogostost računa ali datum začetka, lahko pa izberete tudi končni datum in pogostost računa. Ne morete izbrati končnega datuma in števila mejnikov.
Z uporabo teh informacij sistem ustvari mejnike in zapise, ki so prikazani v mreži **Mejniki**.

   - **Ime mejnika** – Ime mejnika je na podlagi pogostosti računov nastavljeno na datum mejnika.
   - **Datum mejnika** – Datum, ki temelji na pogostosti računa.
   - **Znesek mejnika** – Izračunan z deljenjem delnega zneska v vrstici podizvajalske pogodbe s številom mejnikov.

Če je v vrstici podizvajalske pogodbe določena vrednost v polju **Predvideni znesek davka**, bo ta vrednost pri ustvarjanju periodičnih mejnikov vsem dodana enakomerno.

Vsota zneskov mejnikov vrstice podizvajalske pogodbe mora biti enaka vrednosti vrstice podizvajalske pogodbe. Če niso enaki, pride do napake. Napako lahko odpravite in preverite, ali je vsota mejnikov enaka vrednosti vrstice podizvajalske pogodbe, tako da ustvarite, uredite ali izbrišete zneske mejnikov in davkov. Ko ste končali s spremembami, stran shranite in osvežite, da se prepričate, da ni več napak.

## <a name="manually-create-subcontract-line-milestones"></a>Ročno ustvarite mejnike vrstice podizvajalske pogodbe

Mejniki s fiksnimi cenami v vrstici podizvajalske pogodbe se lahko ustvarijo ročno, če se ne delijo redno. Če želite ročno ustvariti mejnik vrstice podizvajalske pogodbe, izvedite naslednje korake.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe** in nato odprite podizvajalsko pogodbo, s katero želite delati.
2. Odprite vrstico podizvajalske pogodbe s fiksno ceno, za katero želite ustvariti mejnik.
3. Na podmreži, v zavihku **Mejniki vrstice podizvajalske pogodbe** izberite **+ Nov mejnik vrstice podizvajalske pogodbe**.
4. Na strani **Nov mejnik vrstice podizvajalske pogodbe** na podlagi naslednje tabele vnesite zahtevane podatke.

    | Polje | Opis |Funkcionalni vpliv|
    | --- | --- |----------------------|
    | Ime mejnika | Ime mejnika |To bo prikazano kot prvi stolpec v vseh iskanjih na podlagi mejnikov podrobnosti podizvajalske pogodbe. Vrstica računa dobavitelja, ki je ustvarjena na podlagi tega mejnika, bo prav tako uporabljala ime mejnika podrobnosti podizvajalske pogodbe kot privzeto ime vrstice računa dobavitelja.|
    | Opis | Opis mejnika. |Vrstica računa dobavitelja, ki je ustvarjena na podlagi tega mejnika, bo prav tako uporabljala opis mejnika podrobnosti podizvajalske pogodbe kot privzeti opis vrstice računa dobavitelja.|
    | Datum mejnika | Datum, ko bi moral postopek samodejnega ustvarjanja računa preveriti stanje tega mejnika, da bi ga upoštevali pri izstavljanju računov.| Ta vrednost bo uporabljena kot privzeti datum vrstice računa dobavitelja pri izstavljanju računov za te podrobnosti podizvajalske pogodbe. |
    | Znesek | Znesek ali vrednost mejnika, ki bo zaračunan stranki. |Ta vrednost je uporabljena kot privzeti znesek v vrstici računa dobavitelja pri izstavljanju računov za te podrobnosti podizvajalske pogodbe. |
    | Davek | Znesek davka, ki se uporablja za mejnik.| Ta vrednost je uporabljena kot privzeti znesek davka v vrstici računa dobavitelja pri izstavljanju računov za te podrobnosti podizvajalske pogodbe. |
    | Znesek po obdavčitvi | To polje samo za branje se izračuna kot znesek + davek.|Ta vrednost je uporabljena kot privzeta v vrstici računa dobavitelja pri izstavljanju računov za te podrobnosti podizvajalske pogodbe. |
    | Stanje računa | Ko je mejnik ustvarjen, je to stanje vedno nastavljeno na **Ni pripravljen za izstavljanje računov**.|  V stanju **Pripravljen za izdajo računa** je ta mejnik pri ustvarjanju računa dobavitelja vključen na računu dobavitelja. |

5. Izberite možnost **Shrani in zapri**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
