---
title: Pregled priznavanja prihodkov
description: V tej temi so na voljo informacije o priznavanju prihodkov v storitvi Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 51c553ecf45452615cbcadce6386f32be427acaa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601452"
---
# <a name="revenue-recognition-overview"></a>Pregled priznavanja prihodkov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

V storitvi Dynamics 365 Project Operations se načela priznavanja prihodkov razlikujejo glede na izbrani način obračunavanja za projekt ali del projekta. V tej temi so na voljo informacije o priznavanju prihodkov v storitvi Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Knjižene transakcije po načinu obračunavanja časa in materiala

- Priznavanje stroškov in prihodkov sta povezana. Transakcijski stroški in neobračunana prodaja so knjiženi z [dnevnikom integracije za Project Operations](../project-accounting/project-operations-integration-journal.md).
- Profil projektnih stroškov in prihodkov določa, ali se neobračunane prodajne transakcije knjižijo v glavno knjigo. Če je izbrana možnost **Fakturiranje prihodkov**, bo sistem med knjiženjem uporabil računa **Vrednost prodaje WIP** in **Vrednost prodaje fakturiranih prihodkov**. V nadaljevanju je prikazan primer te metode.  

  | Vrsta transakcije | Bremenitev/dobropis | Znesek |
  | --- | --- | --- |
  | Vrednost prodaje WIP | Bremenitev | 100 |
  | Vračunana vrednost prihodkov od prodaje | Dobropis | 100 |

- Prihodki so upoštevani pri izdaji računov. Sistem med knjiženjem uporablja račun **Fakturirani prihodki**. V nadaljevanju je prikazan primer te metode.  

  | Vrsta transakcije | Bremenitev/dobropis | Znesek |
  | --- | --- | --- |
  | Stanje stranke | Bremenitev | 120 |
  | Prometni davek za plačilo | Dobropis | 20 |
  | Fakturirani prihodek | Dobropis | 100 |

- Če so bili prihodki fakturirani ob knjiženju neobračunanih prodaj, bo sistem povrnil obračunane prihodke ob izdaji računa.

  | Vrsta transakcije | Bremenitev/dobropis | Znesek |
  | --- | --- | --- |
  | Vrednost prodaje WIP | Dobropis | 100 |
  | Vračunana vrednost prihodkov od prodaje | Bremenitev | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Knjižene transakcije z načinom obračunavanja s fiksno ceno

- Priznavanje stroškov in prihodkov je ločeno. Transakcijski stroški so knjiženi z [dnevnikom integracije za Project Operations](../project-accounting/project-operations-integration-journal.md). Neobračunane prodajne transakcije niso ustvarjene.
- Prihodke je mogoče upoštevati med izdajanjem računov, če imajo projektni stroški in profil prihodkov atribut **Načelo, uporabljeno za izračune dokončanja projekta** nastavljen na **Brez WIP-a**. To metodo uporabite samo za kratkoročne in preproste projekte.
- Prihodke je mogoče upoštevati z uporabo ocen prihodkov s fiksno ceno, bodisi z metodo **Dokončana pogodba** ali **Priznavanje prihodka glede na odstotek dokončanosti**.

## <a name="additional-resources"></a>Dodatni viri
[Članek Konfiguracija vodenja računov za plačljive projekte](../project-accounting/configure-accounting-billable-projects.md)

[Projekti ocene prihodkov s fiksno ceno](rev-rec-percentage-completion-method.md)

[Upravljanje ocen prihodkov](rev-rec-completed-contract-method.md)

[Metode za izračun stroškov za dokončanje](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]