---
title: Integracija računa projekta
description: Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za zaračunavanje strank.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996586"
---
# <a name="project-invoice-integration"></a>Integracija računa projekta

Ta tema vsebuje informacije o integraciji za dvojno zapisovanje za Project Operations za zaračunavanje strank.

V aplikaciji Project Operations vodja projekta upravlja nedokončana opravila obračunavanja v projektu in ustvari predračun za stranko v storitvi Microsoft Dataverse. Na podlagi tega predračuna uradnik za terjatve ali računovodja projekta ustvari račun za stranko. Integracija za dvojno zapisovanje zagotavlja sinhronizacijo podrobnosti predračuna z aplikacijami Finance and Operations. Po knjiženju računa za stranko, sistem posodobi ustrezne dejanske vrednosti projekta v storitvi Dataverse s podrobnostmi računovodstva. Naslednji grafični prikaz predstavlja konceptualni pregled te integracije na visoki ravni.

   ![Integracija računa projekta](./media/DW5Invoicing.png)

Ko vodja projekta potrdi predračun v storitvi Dataverse, se podatki o glavi predračuna sinhronizirajo z aplikacijami Finance and Operations s preslikavo tabele za dvojno zapisovanje **Predlog za račune projekta V2 (računi)**. To je enosmerna integracija iz storitve Dataverse v aplikacije Finance and Operations. Ustvarjanje ali brisanje predlogov za račune projekta neposredno v aplikacijah Finance and Operations ni podprto.

Ko potrdite račun v storitvi Dataverse, poslovna logika ustvari zapise, povezane z obračunavanjem, v entiteti **Dejanske vrednosti**. Ti zapisi se sinhronizirajo z aplikacijami Finance and Operations s preslikavo tabele za dvojno zapisovanje **Dejanske vrednosti integracije za Project Operations (msdyn\_actuals).** Za več informacij si preberite razdelek [Ocene in dejanske vrednosti projekta](resource-dual-write-estimates-actuals.md). 

Vrstice predlogov za račune projekta se ustvarijo z občasnim postopkom, **Uvoz iz pripravljalne tabele**. Ta postopek temelji na podrobnostih dejanske vrednosti obračunane prodaje v tabeli **Pripravljalne dejanske vrednosti**. Za več informacij glejte [Upravljanje predlogov za račune projekta](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
