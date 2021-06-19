---
title: Pregled podrobnosti pogodbe, ki temelji na projektu
description: V tej temi so na voljo informacije o delu s podrobnostmi pogodbe, ki temelji na projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003156"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="ac1c9-103">Pregled podrobnosti pogodbe, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="ac1c9-103">Project-based contract lines overview</span></span>

<span data-ttu-id="ac1c9-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="ac1c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac1c9-105">Podrobnosti pogodbe, ki temelji na projektu, v aplikaciji Dynamics 365 Project Operations so zasnovane, da hranijo dogovore o oceni in obračunavanju za določene komponente dela na projektu v interakciji.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="ac1c9-106">Struktura podrobnosti pogodbe, ki temeljijo na projektu, je razširjena za ocene projektov in scenarije obračunavanja z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="ac1c9-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="ac1c9-107">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="ac1c9-107">Billing method</span></span>
- <span data-ttu-id="ac1c9-108">Preslikavanje projektov in opravil</span><span class="sxs-lookup"><span data-stu-id="ac1c9-108">Project and task mapping</span></span>
- <span data-ttu-id="ac1c9-109">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="ac1c9-109">Included transaction classes</span></span>
- <span data-ttu-id="ac1c9-110">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="ac1c9-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="ac1c9-111">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="ac1c9-111">Chargeability setup</span></span>
- <span data-ttu-id="ac1c9-112">Ocene s podrobnosti vrstice pogodbe</span><span class="sxs-lookup"><span data-stu-id="ac1c9-112">Estimates using contract line details</span></span>
- <span data-ttu-id="ac1c9-113">Stranke podrobnosti pogodbe</span><span class="sxs-lookup"><span data-stu-id="ac1c9-113">Contract line customers</span></span>

<span data-ttu-id="ac1c9-114">Naslednja tabela vključuje polja na zavihku **Splošno** podrobnosti pogodbe, ki temeljijo na projektu, ki pomagajo nastaviti podlago za podrobno, celovito oceno in dogovore za obračunavanje za delo, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="ac1c9-115">Polje</span><span class="sxs-lookup"><span data-stu-id="ac1c9-115">Field</span></span> | <span data-ttu-id="ac1c9-116">Opis</span><span class="sxs-lookup"><span data-stu-id="ac1c9-116">Description</span></span> | <span data-ttu-id="ac1c9-117">Nadaljnji vpliv</span><span class="sxs-lookup"><span data-stu-id="ac1c9-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ac1c9-118">**Ime**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-118">**Name**</span></span> | <span data-ttu-id="ac1c9-119">Ime podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-119">Name of the contract line.</span></span> <span data-ttu-id="ac1c9-120">To opredeljuje posamezno komponento pogodbe, ki se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="ac1c9-121">Za projektno pogodbo, ustvarjeno iz ponudbe, je ta vrednost kopirana iz pripadajoče vrednosti podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="ac1c9-122">Ime, kopirano v projektno vrstico računa, ki je ustvarjena iz teh podrobnosti pogodbe, ko je ustvarjen račun.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="ac1c9-123">**Način obračunavanja**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-123">**Billing Method**</span></span> | <span data-ttu-id="ac1c9-124">V projektni pogodbi, ustvarjeni iz ponudbe, je ta vrednost kopirana iz pripadajočega polja podrobnosti ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="ac1c9-125">To je nabor možnosti, ki predstavlja dva glavna pogodbena modela, ki ju podpira Project Operations:</span><span class="sxs-lookup"><span data-stu-id="ac1c9-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="ac1c9-126">- **Fiksna cena**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-126">- **Fixed Price**</span></span></br><span data-ttu-id="ac1c9-127">- **Čas in material**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-127">- **Time and Material**</span></span> | <span data-ttu-id="ac1c9-128">Na podlagi metode obračunavanja v sklicevanih podrobnostih pogodbe bo dejanska transakcija obdelana.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="ac1c9-129">Če imajo podrobnosti pogodbe, sklicevane z dejansko vrednostjo, način obračunavanja časa in materiala, sta ustvarjena zapisa stroška in dejanska vrednost neobračunane prodaje.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="ac1c9-130">Če imajo podrobnosti pogodbe, na katere se sklicuje dejanska vrednost, način obračunavanja fiksne cene, je ustvarjena samo dejanska vrednost stroška.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="ac1c9-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-131">**Project**</span></span> | <span data-ttu-id="ac1c9-132">Uporabite to polje za prepoznavanje projekta, ki bo uporabljen za zagotavljanje dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="ac1c9-133">Ta vrednost se bo uporabljala skupaj z **vključenimi opravili** in **vključenimi razredi transakcij** za razrešitev sklica podrobnosti pogodbe v zapisu dejanske vrstice ali ocene vrstice.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="ac1c9-134">**Vključena opravila**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-134">**Included Tasks**</span></span> | <span data-ttu-id="ac1c9-135">Označuje, ali te podrobnosti pogodbe vključujejo vsa projektna opravila za izbrani projekt ali samo podnabor opravil.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="ac1c9-136">To je nabor možnosti, ki ima naslednje možne vrednosti:</span><span class="sxs-lookup"><span data-stu-id="ac1c9-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="ac1c9-137">- **Vsa opravila projekta**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-137">- **All Project Tasks**</span></span></br><span data-ttu-id="ac1c9-138">- **Samo izbrana opravila projekta**.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="ac1c9-139">Privzeta vrednost v tem polju je enaka izbiri možnosti **Vsa opravila projekta**.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="ac1c9-140">Če je izbrana možnost **Samo izbrana opravila**, lahko izberete določena opravila in jih povežete s temi podrobnostmi pogodbe na zavihku **Nastavitev obračunavanja opravil** strani **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="ac1c9-141">Vrednost bo uporabljena v povezavi z možnostma **Projekt** in **Vključeni razredi transakcij** za odpravljanje sklica podrobnosti pogodbe v zapisu dejanskih ali ocenjenih podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ac1c9-142">**Vključi čas**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-142">**Include Time**</span></span> | <span data-ttu-id="ac1c9-143">Vrednost **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v v tej pogodbeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ac1c9-144">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v te podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="ac1c9-145">Vrednost **Da** označuje, da bodo.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="ac1c9-146">Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ac1c9-147">**Vključi strošek**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-147">**Include Expense**</span></span> | <span data-ttu-id="ac1c9-148">Vrednost **Da**/**Ne** označuje, ali bodo stroški za izbrani projekt vključeni v oceno v tej pogodbeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ac1c9-149">Vrednost **Ne** označuje, da stroški ne bodo vključeni v te podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="ac1c9-150">Vrednost **Da** označuje, da bodo.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="ac1c9-151">Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ac1c9-152">**Vključi materiale**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-152">**Include Materials**</span></span> | <span data-ttu-id="ac1c9-153">Vrednost **Da**/**Ne** označuje, ali bodo stroški materiala za izbrani projekt vključeni v oceno v tej pogodbeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ac1c9-154">Vrednost **Ne** označuje, da stroški materiala ne bodo vključeni v oceno v tej pogodbeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="ac1c9-155">Vrednost **Da** označuje, da bodo.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="ac1c9-156">Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ac1c9-157">**Vključi dajatev**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-157">**Include Fee**</span></span> | <span data-ttu-id="ac1c9-158">Vrednost **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključeni v oceno v tej pogodbeni vrstici.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="ac1c9-159">Vrednost **Ne** označuje, da dajatve ne bodo vključene v te podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="ac1c9-160">Vrednost **Da** označuje, da bodo.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="ac1c9-161">Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="ac1c9-162">**Pogodbeni znesek**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-162">**Contracted Amount**</span></span> | <span data-ttu-id="ac1c9-163">V podrobnostih pogodbe za fiksno ceno je ta znesek dogovorjena vrednost, ki bo zaračunana stranki za vse komponente dela, povezane s temi podrobnostmi pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="ac1c9-164">V podrobnostih pogodbe za čas in material je ta znesek ocenjena vrednost, kaj bo zaračunano stranki za vse komponente dela, povezane s temi podrobnostmi pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="ac1c9-165">V projektni pogodbi, ki je ustvarjena iz ponudbe, je ta vrednost kopirana iz pripadajočega polja podrobnosti ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="ac1c9-166">Ko imajo podrobnosti pogodbe, ki temeljijo na projektu, podrobnosti vrstice, je to polje zaklenjeno za urejanje in je povzeto z zneska v podrobnostih vrstice pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="ac1c9-167">Ko imajo podrobnosti pogodbe podrobnosti vrstice, je mogoče to vrednost spremeniti s spremembo zneskov v podrobnostih vrstice.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="ac1c9-168">V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje zneska pred davkom v rednih mejnikih obračunavanja.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="ac1c9-169">**Predvideni davek**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-169">**Estimated Tax**</span></span> | <span data-ttu-id="ac1c9-170">Uporabnik lahko uredi to polje za vnos ocenjenega zneska davka v podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="ac1c9-171">Ko imajo podrobnosti pogodbe, ki temeljijo na projektu, podrobnosti vrstice, je to polje zaklenjeno za urejanje in je povzeto z zneska davka v podrobnostih vrstice pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="ac1c9-172">Ko imajo podrobnosti pogodbe podrobnosti vrstice, je mogoče to vrednost spremeniti s spremembo zneskov davka v podrobnostih vrstice.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="ac1c9-173">V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje davka v rednih mejnikih obračunavanja.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="ac1c9-174">**Pogodbeni znesek po obdavčitvi**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="ac1c9-175">Znesek podrobnosti pogodbe po obdavčitvi.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-175">The contract line amount after tax.</span></span> <span data-ttu-id="ac1c9-176">To polje je samo za branje in je izračunano kot **Pogodbeni znesek + davek**.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="ac1c9-177">V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje rednih mejnikov obračunavanja.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="ac1c9-178">**Omejitev »Ni dovoljeno preseči«**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="ac1c9-179">Uporabnik lahko to polje ureja ter je na voljo samo za podrobnosti pogodbe, ki temeljijo na projektu, ki imajo način obračunavanja nastavljen na čas in material.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="ac1c9-180">Uporabnik lahko ureja to polje.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-180">The user can edit this field.</span></span> <span data-ttu-id="ac1c9-181">Ko se dejanska vrednost za čas in material sklicuje na te podrobnosti pogodbe za čas in material, je znesek dejanske vrednosti ocenjen glede na omejitev, ki je ni dovoljeno preseči, v podrobnostih pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="ac1c9-182">To ocenjevanje je izvedeno potem, ko so že porabljeni in potrjeni zneski upoštevani.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="ac1c9-183">**Proračun stranke**</span><span class="sxs-lookup"><span data-stu-id="ac1c9-183">**Customer Budget**</span></span> | <span data-ttu-id="ac1c9-184">To polje je mogoče urejati in je kopirano iz pripadajočega polja za podrobnosti ponudbe, če je bila pogodba ustvarjena iz ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="ac1c9-185">To polje se uporablja samo za informacije in nima pomena v poteku navzdol.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="ac1c9-186">Veljavnostna pravila za možnosti na zavihku »Splošno« podrobnosti pogodbe, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="ac1c9-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="ac1c9-187">Pravilo 1: Če je polje **Vključena opravila** prazno ali nastavljeno na **Vsa opravila projekta**, so vsa opravila projekta vključena v podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="ac1c9-188">Pravilo 2: Če je polje **Vključena opravila** prazno ali izrecno nastavljeno na **Vsa opravila projekta**, sta lahko projekt in določen razred transakcije vključena samo v en sklop podrobnosti pogodbe, ki temeljijo na projektu, pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="ac1c9-189">Pravilo 3: Če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, sta lahko projekt in določen razred transakcije vključena v več sklopov podrobnosti pogodbe, ki temeljijo na projektu, pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="ac1c9-190">
                    <strong>Pogodba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ac1c9-191">
                    <strong>Podrobnosti pogodbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ac1c9-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="ac1c9-193">
                    <strong>Vključena opravila</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ac1c9-194">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ac1c9-195">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ac1c9-196">
                    <strong>Vključi materiale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ac1c9-197">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="ac1c9-198">
                    <strong>Dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="ac1c9-199">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="ac1c9-200">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ac1c9-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-201">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-202">CL1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-203">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-204">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-205">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-206">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-207">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-208">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-209">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-210">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-210">Violation of Rule #2.</span></span> <span data-ttu-id="ac1c9-211">Čas, stroški, materiali in dajatve za projekt P1 so vključeni v podrobnostih pogodbe CL1 in CL2.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-212">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-213">CL2</span><span class="sxs-lookup"><span data-stu-id="ac1c9-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-214">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-215">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-216">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-217">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-218">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-219">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-220">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-221">CL1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-222">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-224">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-225">No</span><span class="sxs-lookup"><span data-stu-id="ac1c9-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-226">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-227">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-228">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-229">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-229">Violation of Rule #2.</span></span> <span data-ttu-id="ac1c9-230">Čas, materiali in dajatve za projekt P1 so vključeni v podrobnostih pogodbe CL1 in CL2.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-231">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-232">CL2</span><span class="sxs-lookup"><span data-stu-id="ac1c9-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-233">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-234">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-235">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-236">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-237">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-238">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-239">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-240">CL1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-241">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-242">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-243">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-244">No</span><span class="sxs-lookup"><span data-stu-id="ac1c9-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-245">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-246">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-247">Veljavno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-248">Čas, materiali in dajatve za projekt P1 so vključeni v CL1.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="ac1c9-249">Stroški za projekt P1 so vključeni v CL2.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="ac1c9-250">Ni prekrivanja tega, kar je vključeno v vsako podrobnosti pogodbe in je zato veljavno.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-251">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-252">CL2</span><span class="sxs-lookup"><span data-stu-id="ac1c9-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-253">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-254">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-255">No</span><span class="sxs-lookup"><span data-stu-id="ac1c9-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-256">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-257">No</span><span class="sxs-lookup"><span data-stu-id="ac1c9-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-258">No</span><span class="sxs-lookup"><span data-stu-id="ac1c9-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-259">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-260">CL1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-261">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-262">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="ac1c9-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-263">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-264">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-265">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-266">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-267">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-268">Kršitev 2. pravila</span><span class="sxs-lookup"><span data-stu-id="ac1c9-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="ac1c9-269">C1 vključuje čas, materiale, stroške in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ac1c9-270">CL2 vključuje čas, materiale, stroške in dajatve za celoten projekt P1 in se torej prekriva s tem, kar je vključeno v C1.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-271">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-272">CL2</span><span class="sxs-lookup"><span data-stu-id="ac1c9-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-273">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-274">Prazno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-275">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-276">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-277">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-278">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-279">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-280">CL1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-281">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-282">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="ac1c9-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-283">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-284">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-285">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-286">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-287">Veljavno</span><span class="sxs-lookup"><span data-stu-id="ac1c9-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ac1c9-288">Po 3. pravilu,</span><span class="sxs-lookup"><span data-stu-id="ac1c9-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="ac1c9-289">C1 vključuje čas, stroške, materiale in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ac1c9-290">CL2 vključuje čas, stroške, materiale in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ac1c9-291">Edino dodatno preverjanje se izvaja okoli podmnožice opravil za CL1, ki se razlikuje od podmnožice opravil za CL2, da se prepreči prekrivanje.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="ac1c9-292">To opravi sistem, ko so opravila povezana.</span><span class="sxs-lookup"><span data-stu-id="ac1c9-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="ac1c9-293">C1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ac1c9-294">CL2</span><span class="sxs-lookup"><span data-stu-id="ac1c9-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-295">O1</span><span class="sxs-lookup"><span data-stu-id="ac1c9-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="ac1c9-296">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="ac1c9-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-297">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ac1c9-298">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-299">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ac1c9-300">Da</span><span class="sxs-lookup"><span data-stu-id="ac1c9-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
