---
title: Integracija računa projekta
description: Ta članek vsebuje informacije o integraciji dvojnega pisanja Project Operations za izdajanje računov strankam.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912122"
---
# <a name="project-invoice-integration"></a>Integracija računa projekta

Ta članek vsebuje informacije o integraciji dvojnega pisanja Project Operations za izdajanje računov strankam.

V aplikaciji Project Operations vodja projekta upravlja nedokončana opravila obračunavanja v projektu in ustvari predračun za stranko v storitvi Microsoft Dataverse. Na podlagi tega predračuna uradnik za terjatve ali računovodja projekta ustvari račun za stranko. Integracija dvojnega pisanja zagotavlja, da so podrobnosti o predračunu sinhronizirane z aplikacijami Finance in Operations. Po knjiženju računa za stranko, sistem posodobi ustrezne dejanske vrednosti projekta v storitvi Dataverse s podrobnostmi računovodstva. Naslednji grafični prikaz predstavlja konceptualni pregled te integracije na visoki ravni.

   ![Integracija računa projekta.](./media/DW5Invoicing.png)

Ko vodja projekta potrdi predračun v Dataverse, se informacije glave predračuna sinhronizirajo z aplikacijami Finance in Operations z uporabo preslikave tabele z dvojnim pisanjem, **Predlog računa projekta V2 (računi)**. To je enosmerna integracija iz Dataverse v aplikacije Finance in Operations. Ustvarjanje ali brisanje predlogov računov projekta neposredno v aplikacijah Finance in Operations ni podprto.

Ko potrdite račun v storitvi Dataverse, poslovna logika ustvari zapise, povezane z obračunavanjem, v entiteti **Dejanske vrednosti**. Ti zapisi so sinhronizirani s financami in poslovanjem z uporabo preslikave tabele z dvojnim zapisovanjem, **Dejanski podatki o integraciji projektnih operacij (msdyn\_ dejansko stanje).** Za več informacij si preberite razdelek [Ocene in dejanske vrednosti projekta](resource-dual-write-estimates-actuals.md). 

Vrstice predlogov za račune projekta se ustvarijo z občasnim postopkom, **Uvoz iz pripravljalne tabele**. Ta postopek temelji na podrobnostih dejanske vrednosti obračunane prodaje v tabeli **Pripravljalne dejanske vrednosti**. Za več informacij glejte [Upravljanje predlogov za račune projekta](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
