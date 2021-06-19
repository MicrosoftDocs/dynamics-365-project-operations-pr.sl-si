---
title: Delo z osebnimi stroški v poročilu o stroških
description: V tej temi so na voljo informacije o delu z osebnimi stroški, ki jih imajo zaposleni med poslovnimi potovanji.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025704"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="ee6a7-103">Delo z osebnimi stroški v poročilu o stroških</span><span class="sxs-lookup"><span data-stu-id="ee6a7-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="ee6a7-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="ee6a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee6a7-105">Med službenim potovanjem lahko zaposleni za osebne stroške bremeni kreditno kartico podjetja.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="ee6a7-106">Če postopek ni določen za obravnavo osebnih stroškov, se lahko postopek odobritve poročila o stroških prekine, ko zaposleni predloži svoje razčlenjeno poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="ee6a7-107">Za delo z osebnimi stroški zaposlenega lahko uporabite dve metodi:</span><span class="sxs-lookup"><span data-stu-id="ee6a7-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="ee6a7-108">**Plača zaposleni**: vaša organizacija ne plačuje osebnih stroškov, ki so navedeni na računu za kreditno kartico podjetja.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="ee6a7-109">Namesto tega zaposleni poravna stroške neposredno pri ponudniku kreditne kartice.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="ee6a7-110">**Plača podjetje**: vaša organizacija plača celoten račun za kreditno kartico podjetja in nato bremeni račun delavca za osebne stroške.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="ee6a7-111">Način, ki ga vaša organizacija uporablja, lahko izberete na strani **Parametri upravljanja stroškov**.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="ee6a7-112">Omogočanje funkcije deljenih stroškov, če ima polje z osebnim zneskom določeno vrednost</span><span class="sxs-lookup"><span data-stu-id="ee6a7-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="ee6a7-113">Funkcija **Omogočanje funkcije deljenih stroškov, če ima polje z osebnim zneskom določeno vrednost** velja samo za poročila o stroških, ki so odobrena s potekom dela na ravni vrstice.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="ee6a7-114">Poročila odobrite tako, da odprete zavihek **Obdelava poročila o stroških** > **Poročila o stroških, ki so mi dodeljena** > **Odpri poročilo o stroških**.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="ee6a7-115">Če želite omogočiti to funkcijo, odprite zavihek **Delovni prostori** > **Upravljanje funkcij**, izberite možnost **Omogočanje funkcije deljenih stroškov, če ima polje z osebnim zneskom določeno vrednost** in nato **Omogoči zdaj**.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="ee6a7-116">Ko je funkcija omogočena, vrstice stroškov, ki uporabljajo to funkcijo, ob oddaji poročila ustvarijo dve vrstici.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="ee6a7-117">Ustvarita se dve vrstici, tako da lahko odobritelj odobri vsako vrstico posebej.</span><span class="sxs-lookup"><span data-stu-id="ee6a7-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
