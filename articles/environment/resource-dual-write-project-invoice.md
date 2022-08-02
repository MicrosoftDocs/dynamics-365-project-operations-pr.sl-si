---
title: Integracija računa projekta
description: Ta članek vsebuje informacije o integraciji dvojnega pisanja za Project Operations za izdajanje računov strankam.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029044"
---
# <a name="project-invoice-integration"></a>Integracija računa projekta

Ta članek vsebuje informacije o integraciji dvojnega pisanja za Project Operations za izdajanje računov strankam.

V aplikaciji Project Operations vodja projekta upravlja nedokončana opravila obračunavanja v projektu in ustvari predračun za stranko v storitvi Microsoft Dataverse. Na podlagi tega predračuna uradnik za terjatve ali računovodja projekta ustvari račun za stranko. Integracija dvojnega pisanja zagotavlja, da so podrobnosti predračuna sinhronizirane z aplikacijami za finance in poslovanje. Po knjiženju računa za stranko, sistem posodobi ustrezne dejanske vrednosti projekta v storitvi Dataverse s podrobnostmi računovodstva. Naslednji grafični prikaz predstavlja konceptualni pregled te integracije na visoki ravni.

   ![Integracija računa projekta.](./media/DW5Invoicing.png)

Ko vodja projekta potrdi predračun v Dataverse, se informacije o glavi predračuna sinhronizirajo z aplikacijami za finance in poslovanje z uporabo preslikave tabele z dvojnim pisanjem, **Projektni predlog računa V2 (računi)**. To je enosmerna integracija iz Dataverse v aplikacije za finance in poslovanje. Ustvarjanje ali brisanje predlogov računov za projekt neposredno v aplikacijah za finance in operacije ni podprto.

Ko potrdite račun v storitvi Dataverse, poslovna logika ustvari zapise, povezane z obračunavanjem, v entiteti **Dejanske vrednosti**. Ti zapisi so sinhronizirani s financami in operacijami z uporabo preslikave tabele z dvojnim pisanjem, **Dejanski podatki o integraciji projektnih operacij (msdyn\_ dejansko stanje).** Za več informacij si preberite razdelek [Ocene in dejanske vrednosti projekta](resource-dual-write-estimates-actuals.md). 

Vrstice predlogov za račune projekta se ustvarijo z občasnim postopkom, **Uvoz iz pripravljalne tabele**. Ta postopek temelji na podrobnostih dejanske vrednosti obračunane prodaje v tabeli **Pripravljalne dejanske vrednosti**. Za več informacij glejte [Upravljanje predlogov za račune projekta](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
