---
title: Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systémech iOS a Android
description: Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073834"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="90f2b-103">Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systémech iOS a Android</span><span class="sxs-lookup"><span data-stu-id="90f2b-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90f2b-104">Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="90f2b-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="90f2b-105">Jsou zahrnuta následující témata:</span><span class="sxs-lookup"><span data-stu-id="90f2b-105">The following topics are covered:</span></span>

- <span data-ttu-id="90f2b-106">Různé datové typy, které podporuje rámec vlastního pole</span><span class="sxs-lookup"><span data-stu-id="90f2b-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="90f2b-107">Jak zobrazit pole jen pro čtení nebo upravitelná pole v záznamech časového výkazu a uložit hodnoty poskytnuté uživatelem zpět do databáze</span><span class="sxs-lookup"><span data-stu-id="90f2b-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="90f2b-108">Jak zobrazit pole jen pro čtení v záhlaví časového výkazu</span><span class="sxs-lookup"><span data-stu-id="90f2b-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="90f2b-109">Jak integrovat další vlastní obchodní logiku, abyste do polí zadali výchozí hodnoty a provedli další ověření</span><span class="sxs-lookup"><span data-stu-id="90f2b-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="90f2b-110">Cílová skupina</span><span class="sxs-lookup"><span data-stu-id="90f2b-110">Audience</span></span>

<span data-ttu-id="90f2b-111">Toto téma je určeno pro vývojáře, kteří integrují svá vlastní pole do mobilní aplikace Microsoft Dynamics 365 Project Timesheet, která je k dispozici pro Apple iOS a Google Android.</span><span class="sxs-lookup"><span data-stu-id="90f2b-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="90f2b-112">Předpokládá se, že čtenáři jsou obeznámeni s vývojem X ++ a funkcemi časového výkazu projektu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="90f2b-113">Smlouva na data - třída TSTimesheetCustomField X ++</span><span class="sxs-lookup"><span data-stu-id="90f2b-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="90f2b-114">Třída **TSTimesheetCustomField** je třída smlouvy na data X ++, která představuje informace o vlastním poli pro funkčnost časového výkazu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="90f2b-115">Seznamy objektů vlastního pole jsou předávány jak ve smlouv na data TSTimesheetDetails, tak ve smlouvě na data TSTimesheetEntry pro zobrazení vlastních polí v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="90f2b-116">**TSTimesheetDetails** - Smlouva záhlaví časového výkazu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="90f2b-117">**TSTimesheetEntry** - Smlouva o transakci časového výkazu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="90f2b-118">Skupiny těchto objektů, které mají stejné informace o projektu a hodnota **timesheetLineRecId** tvoří řádek.</span><span class="sxs-lookup"><span data-stu-id="90f2b-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="90f2b-119">fieldBaseType (typy)</span><span class="sxs-lookup"><span data-stu-id="90f2b-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="90f2b-120">Vlastnost **FieldBaseType** v objektu **TsTimesheetCustom** určuje typ pole, které se zobrazí v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="90f2b-121">Následující hodnoty **Typy** , které jsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="90f2b-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="90f2b-122">Hodnota Typy</span><span class="sxs-lookup"><span data-stu-id="90f2b-122">Types value</span></span> | <span data-ttu-id="90f2b-123">Typ</span><span class="sxs-lookup"><span data-stu-id="90f2b-123">Type</span></span>              | <span data-ttu-id="90f2b-124">Poznámky</span><span class="sxs-lookup"><span data-stu-id="90f2b-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="90f2b-125">0</span><span class="sxs-lookup"><span data-stu-id="90f2b-125">0</span></span>           | <span data-ttu-id="90f2b-126">Řetězec (a výčet)</span><span class="sxs-lookup"><span data-stu-id="90f2b-126">String (and Enum)</span></span> | <span data-ttu-id="90f2b-127">Pole se zobrazí jako textové pole.</span><span class="sxs-lookup"><span data-stu-id="90f2b-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="90f2b-128">0</span><span class="sxs-lookup"><span data-stu-id="90f2b-128">1</span></span>           | <span data-ttu-id="90f2b-129">Integer</span><span class="sxs-lookup"><span data-stu-id="90f2b-129">Integer</span></span>           | <span data-ttu-id="90f2b-130">Hodnota je zobrazena jako číslo bez desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="90f2b-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="90f2b-131">2</span><span class="sxs-lookup"><span data-stu-id="90f2b-131">2</span></span>           | <span data-ttu-id="90f2b-132">Reálné</span><span class="sxs-lookup"><span data-stu-id="90f2b-132">Real</span></span>              | <span data-ttu-id="90f2b-133">Hodnota je zobrazena jako číslo s desetinnými místy.</span><span class="sxs-lookup"><span data-stu-id="90f2b-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="90f2b-134">Chcete-li zobrazit skutečnou hodnotu jako měnu v aplikaci, použijte vlastnost **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="90f2b-135">Můžete použít vlastnost **numberOfDecimals** pro nastavení počtu zobrazených desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="90f2b-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="90f2b-136">3</span><span class="sxs-lookup"><span data-stu-id="90f2b-136">3</span></span>           | <span data-ttu-id="90f2b-137">Datum</span><span class="sxs-lookup"><span data-stu-id="90f2b-137">Date</span></span>              | <span data-ttu-id="90f2b-138">Formáty data jsou určeny nastavením **Formát data, času a čísla** uživatele, které je uvedeno pod **Předvolby jazyka a země / regionu** v poli **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="90f2b-139">4</span><span class="sxs-lookup"><span data-stu-id="90f2b-139">4</span></span>           | <span data-ttu-id="90f2b-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="90f2b-140">Boolean</span></span>           | |
| <span data-ttu-id="90f2b-141">15</span><span class="sxs-lookup"><span data-stu-id="90f2b-141">15</span></span>          | <span data-ttu-id="90f2b-142">GUID</span><span class="sxs-lookup"><span data-stu-id="90f2b-142">GUID</span></span>              | |
| <span data-ttu-id="90f2b-143">16</span><span class="sxs-lookup"><span data-stu-id="90f2b-143">16</span></span>          | <span data-ttu-id="90f2b-144">Int64</span><span class="sxs-lookup"><span data-stu-id="90f2b-144">Int64</span></span>             | |

- <span data-ttu-id="90f2b-145">Pokud není vlastnost **stringOptions** poskytnuta v objektu **TSTimesheetCustomField** , je uživateli poskytnuto pole s volným textem.</span><span class="sxs-lookup"><span data-stu-id="90f2b-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="90f2b-146">Vlastnost **stringLength** lze použít k nastavení maximální délky řetězce, kterou mohou uživatelé zadat.</span><span class="sxs-lookup"><span data-stu-id="90f2b-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="90f2b-147">Pokud je vlastnost **stringOptions** poskytnuta v objektu **TSTimesheetCustomField** , tyto prvky seznamu jsou jediné hodnoty, které mohou uživatelé vybrat pomocí tlačítek s možnostmi (přepínačů).</span><span class="sxs-lookup"><span data-stu-id="90f2b-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="90f2b-148">V takovém případě může pole řetězce fungovat jako hodnota výčtu pro účely vstupu uživatele.</span><span class="sxs-lookup"><span data-stu-id="90f2b-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="90f2b-149">Chcete-li uložit hodnotu do databáze jako výčet, ručně namapujte hodnotu řetězce zpět na hodnotu výčtu před uložením do databáze pomocí řetězce příkazů (viz „Použití řetězce příkazů ve třídě TSTimesheetEntryService k uložení záznamu časového výkazu z aplikace zpět do databáze" dále v tomto tématu).</span><span class="sxs-lookup"><span data-stu-id="90f2b-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="90f2b-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="90f2b-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="90f2b-151">Tuto vlastnost můžete použít k formátování skutečných hodnot jako měny.</span><span class="sxs-lookup"><span data-stu-id="90f2b-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="90f2b-152">Tento přístup je použitelný pouze tehdy, když hodnota **fieldBaseType** **Reálné**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="90f2b-153">**TSCustomFieldExtendedType: Žádný** - Není použito žádné formátování.</span><span class="sxs-lookup"><span data-stu-id="90f2b-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="90f2b-154">**TSCustomFieldExtendedType::Měna** - Formátujte hodnotu jako měnu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="90f2b-155">Pokud je aktivní formátování měny, lze pole **stringValue** použít pro předání kódu měny, který by měl být zobrazen v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="90f2b-156">Hodnota je hodnota jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="90f2b-156">The value is a read-only value.</span></span>

    <span data-ttu-id="90f2b-157">Pole **realValue** obsahuje peněžní částku, která by měla být uložena do databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="90f2b-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="90f2b-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="90f2b-159">Tuto vlastnost můžete použít k určení, kde se má vlastní pole v aplikaci objevit.</span><span class="sxs-lookup"><span data-stu-id="90f2b-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="90f2b-160">**TSCustomFieldSection::Záhlaví** - Pole se objeví v části **Zobrazit více podrobností** v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="90f2b-161">Tato pole jsou vždy jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="90f2b-161">These fields are always read-only.</span></span>
- <span data-ttu-id="90f2b-162">**TSCustomFieldSection::Řádek** - Pole se objeví za všemi integrovanými poli řádku v záznamech časového výkazu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="90f2b-163">Tato pole mohou být upravitelná nebo pouze pro čtení.</span><span class="sxs-lookup"><span data-stu-id="90f2b-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="90f2b-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="90f2b-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="90f2b-165">Tato vlastnost identifikuje pole, když jsou hodnoty, které aplikace poskytuje, uloženy zpět do databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="90f2b-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="90f2b-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="90f2b-167">Tato vlastnost identifikuje pole, když jsou hodnoty, které aplikace poskytuje, uloženy zpět do databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="90f2b-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="90f2b-168">isEditable (NoYes)</span></span>

<span data-ttu-id="90f2b-169">Nastavte tuto vlastnost na **Ano** k určení, že by uživatelé měli upravit pole v sekci zadávání časového výkazu .</span><span class="sxs-lookup"><span data-stu-id="90f2b-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="90f2b-170">Nastavte vlastnost na **Ne** , aby bylo jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="90f2b-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="90f2b-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="90f2b-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="90f2b-172">Nastavte tuto vlastnost na **Ano** k určení, že by pole v sekci zadávání časového výkazu mělo být povinné.</span><span class="sxs-lookup"><span data-stu-id="90f2b-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="90f2b-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="90f2b-173">label (str)</span></span>

<span data-ttu-id="90f2b-174">Tato vlastnost určuje štítek, který se zobrazuje vedle pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="90f2b-175">stringOptions (seznam řetězců)</span><span class="sxs-lookup"><span data-stu-id="90f2b-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="90f2b-176">Tato vlastnost je použitelná pouze v případě, že je vlastnost **fieldBaseType** nastavena na **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="90f2b-177">Pokud je vlastnost **stringOptions** nastavená, hodnoty řetězců, které jsou k dispozici pro výběr pomocí přepínačů, jsou určeny řetězci v seznamu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="90f2b-178">Pokud nejsou k dispozici žádné řetězce, je povoleno zadávání volného textu do pole řetězce (příklad najdete v části „Použití řetězce příkazů ve třídě TSTimesheetEntryService k uložení záznamu časového výkazu z aplikace zpět do databáze“ dále v tomto tématu).</span><span class="sxs-lookup"><span data-stu-id="90f2b-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="90f2b-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="90f2b-179">stringLength (int)</span></span>

<span data-ttu-id="90f2b-180">Tato vlastnost určuje maximální délku pole řetězce.</span><span class="sxs-lookup"><span data-stu-id="90f2b-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="90f2b-181">Je použitelná pouze v případě, že je vlastnost **fieldBaseType** nastavena na **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="90f2b-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="90f2b-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="90f2b-183">Tato vlastnost určuje počet desetinných míst, která se zobrazují pro skutečné pole.</span><span class="sxs-lookup"><span data-stu-id="90f2b-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="90f2b-184">Je použitelná pouze v případě, že je vlastnost **fieldBaseType** nastavena na **Reálné**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="90f2b-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="90f2b-185">orderSequence (int)</span></span>

<span data-ttu-id="90f2b-186">Tato vlastnost řídí pořadí, ve kterém se vlastní pole zobrazují v aplikaci, když je zadáno více než jedno vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="90f2b-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="90f2b-187">Nejprve se zobrazí pole, která mají nižší čísla.</span><span class="sxs-lookup"><span data-stu-id="90f2b-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="90f2b-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="90f2b-188">booleanValue (boolean)</span></span>

<span data-ttu-id="90f2b-189">Pro pole typu **Booleovský** tato vlastnost předá booleovskou hodnotu pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="90f2b-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="90f2b-190">guidValue (guid)</span></span>

<span data-ttu-id="90f2b-191">Pro pole typu **GUID** tato vlastnost předá hodnotu globálně jedinečný identifikátor (GUID) pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="90f2b-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="90f2b-192">int64Value (int64)</span></span>

<span data-ttu-id="90f2b-193">Pro pole typu **int64** tato vlastnost předá hodnotu int64 pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="90f2b-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="90f2b-194">intValue (int)</span></span>

<span data-ttu-id="90f2b-195">Pro pole typu **Int** tato vlastnost předá hodnotu Int pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="90f2b-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="90f2b-196">realValue (real)</span></span>

<span data-ttu-id="90f2b-197">Pro pole typu **Reálné** tato vlastnost předá reálnou hodnotu pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="90f2b-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="90f2b-198">stringValue (str)</span></span>

<span data-ttu-id="90f2b-199">Pro pole typu **Řetězec** tato vlastnost předá hodnotu řetězec pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="90f2b-200">Používá se také pro pole typu **Reálný** , která jsou formátována jako měna.</span><span class="sxs-lookup"><span data-stu-id="90f2b-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="90f2b-201">U těchto polí se vlastnost používá k předání kódu měny do aplikace.</span><span class="sxs-lookup"><span data-stu-id="90f2b-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="90f2b-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="90f2b-202">dateValue (date)</span></span>

<span data-ttu-id="90f2b-203">Pro pole typu **Datum** tato vlastnost předá datovou hodnotu pole mezi serverem a aplikací.</span><span class="sxs-lookup"><span data-stu-id="90f2b-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="90f2b-204">Zobrazení a uložení vlastního pole v sekci zadávání časového výkazu</span><span class="sxs-lookup"><span data-stu-id="90f2b-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="90f2b-205">Níže je snímek obrazovky z mobilní aplikace vytvoření záznamu časového výkazu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="90f2b-206">Zobrazuje integrovaná pole a vlastní pole v sekci „Zadání času“ s názvem „Testovací řetězec“ s již nastavenou hodnotou výčtu „Druhá možnost“.</span><span class="sxs-lookup"><span data-stu-id="90f2b-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Otestujte vlastní pole řetězce v aplikaci](media/timesheet-entry.jpg)



<span data-ttu-id="90f2b-208">Níže je snímek obrazovky z mobilní aplikace uživatele, který si vybral jednu z možností výčtu dostupných pro vlastní pole „Testovací řetězec“.</span><span class="sxs-lookup"><span data-stu-id="90f2b-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="90f2b-209">Dvě možnosti jsou „První možnost“ a „Druhá možnost“ zobrazené jako přepínače.</span><span class="sxs-lookup"><span data-stu-id="90f2b-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="90f2b-210">Druhá možnost je aktuálně vybrána.</span><span class="sxs-lookup"><span data-stu-id="90f2b-210">The second option is currently selected.</span></span>

![Volitelná tlačítka (přepínače) pro vlastní pole Testovací řetězec](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="90f2b-212">Rozšiřte tabulku TSTimesheetLine tak, aby měla vlastní pole</span><span class="sxs-lookup"><span data-stu-id="90f2b-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="90f2b-213">V typických scénářích je pravděpodobné, že data pro vlastní pole v sekci zadávání časového výkazu budou uložena do tabulky TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="90f2b-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="90f2b-214">Lze však použít jiné tabulky, pokud lze data načíst na základě poskytnutého záznamu TSTimesheetTrans nebo pokud nemá konkrétní kontext záznamu (například pokud je pole v parametrech projektu nastaveno jako jen pro čtení).</span><span class="sxs-lookup"><span data-stu-id="90f2b-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="90f2b-215">Všimněte si, že vlastní pole nemusí mít žádné záložní záznamy databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="90f2b-216">Mohou být dynamicky generovány na základě logiky X++.</span><span class="sxs-lookup"><span data-stu-id="90f2b-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="90f2b-217">Tento přístup může být užitečný ve scénářích jen pro čtení (příklad dynamicky generovaných hodnot vlastního pole viz část „Použití řetězce příkazů ve třídě TSTimesheetDetails, metoda buildCustomFieldListForHeader k vyplnění podrobností časového výkazu“.)</span><span class="sxs-lookup"><span data-stu-id="90f2b-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="90f2b-218">Níže je snímek obrazovky ze stromu aplikačních objektů Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90f2b-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="90f2b-219">Zobrazuje rozšíření tabulky TSTimesheetLine s polem TestLineString přidaným jako vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="90f2b-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Řádek řetězce](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="90f2b-221">Pomocí řetězce příkazů v metodě buildCustomFieldList třídy TSTimesheetSettings zobrazíte pole v části zadání časového výkazu</span><span class="sxs-lookup"><span data-stu-id="90f2b-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="90f2b-222">Tento kód řídí nastavení zobrazení pro pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="90f2b-223">Například řídí typ pole, štítek, zda je pole povinné a v jaké části se pole zobrazuje.</span><span class="sxs-lookup"><span data-stu-id="90f2b-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="90f2b-224">Následující příklad ukazuje pole řetězce pro časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="90f2b-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="90f2b-225">Toto pole má dvě možnosti, **První možnost** a **Druhá možnost** , které jsou k dispozici prostřednictvím volitelných tlačítek (přepínačů).</span><span class="sxs-lookup"><span data-stu-id="90f2b-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="90f2b-226">Pole v aplikaci je přidruženo k poli **TestLineString** , které je přidáno do tabulky TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="90f2b-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="90f2b-227">Všimněte si metody **TSTimesheetCustomField::newFromMetatdata()** ke zjednodušení inicializace vlastností vlastního pole: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** a **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="90f2b-228">Tyto parametry můžete také nastavit ručně, jak chcete.</span><span class="sxs-lookup"><span data-stu-id="90f2b-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="90f2b-229">Pomocí řetězce příkazů v metodě buildCustomFieldListForEntry třídy TSTimesheetEntry zadejte hodnoty do záznamu časového výkazu</span><span class="sxs-lookup"><span data-stu-id="90f2b-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="90f2b-230">Metoda **buildCustomFieldListForEntry** se používá k zadávání hodnot na uložené řádky časového výkazu v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="90f2b-231">Jako parametr vezme záznam TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="90f2b-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="90f2b-232">Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="90f2b-233">Pomocí řetězce příkazů ve třídě TSTimesheetEntryService uložíte záznam časového výkazu z aplikace zpět do databáze</span><span class="sxs-lookup"><span data-stu-id="90f2b-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="90f2b-234">Chcete-li uložit vlastní pole zpět do databáze v obvyklém použití, musíte rozšířit více metod:</span><span class="sxs-lookup"><span data-stu-id="90f2b-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="90f2b-235">Metoda **timesheetLineNeedsUpdating** se používá k určení, zda byl záznam řádku změněn uživatelem v aplikaci a musí být uložen do databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="90f2b-236">Pokud výkon není problém, lze tuto metodu zjednodušit, aby se vždy vrátila hodnota **true**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="90f2b-237">Metody **populateTimesheetLineFromEntryDuringCreate** a **populateTimesheetLineFromEntryDuringUpdate** lze rozšířit tak, aby zadávaly hodnoty v databázovém záznamu TSTimesheetLine ze záznamu smlouvy TSTimesheetEntry, který je poskytnut.</span><span class="sxs-lookup"><span data-stu-id="90f2b-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="90f2b-238">V následujícím příkladu si všimněte, jak se mapování mezi databázovým polem a vstupním polem provádí ručně pomocí kódu X++.</span><span class="sxs-lookup"><span data-stu-id="90f2b-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="90f2b-239">Metodu **populateTimesheetWeekFromEntry** lze také rozšířit, pokud vlastní pole, které je namapováno na objekt **TSTimesheetEntry** , musí zapisovat zpět do databázové tabulky TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="90f2b-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="90f2b-240">Následující příklad uloží hodnotu **firstOption** nebo **secondOption** , kterou uživatel vybere pro databázi jako nezpracovanou hodnotu řetězce.</span><span class="sxs-lookup"><span data-stu-id="90f2b-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="90f2b-241">Pokud je databázové pole pole typu **Výčet** , lze tyto hodnoty ručně namapovat na hodnotu výčtu a poté uložit do pole výčtu v databázové tabulce.</span><span class="sxs-lookup"><span data-stu-id="90f2b-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="90f2b-242">Zobrazení vlastního pole v sekci záhlaví časového výkazu</span><span class="sxs-lookup"><span data-stu-id="90f2b-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="90f2b-243">Níže je snímek obrazovky z mobilní aplikace uživatele, který prohlíží časový výkaz.</span><span class="sxs-lookup"><span data-stu-id="90f2b-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="90f2b-244">V pravém horním rohu bylo vybráno tlačítko „Další informace“ pro zobrazení možnosti „Zobrazit další podrobnosti“.</span><span class="sxs-lookup"><span data-stu-id="90f2b-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Příkaz Zobrazit více podrobností](media/show-more.png)

<span data-ttu-id="90f2b-246">Níže je snímek obrazovky z mobilní aplikace zobrazující část Více časového výkazu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="90f2b-247">Do sekce záhlaví časového výkazu bylo přidáno vlastní pole s názvem „Míra využití tohoto časového výkazu (vypočítané vlastní pole)“.</span><span class="sxs-lookup"><span data-stu-id="90f2b-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="90f2b-248">Ve vlastním poli je nastavena hodnota jen pro čtení „0,667“.</span><span class="sxs-lookup"><span data-stu-id="90f2b-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sekce Další](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="90f2b-250">Rozšiřte tabulku TSTimesheetTable tak, aby měla vlastní pole</span><span class="sxs-lookup"><span data-stu-id="90f2b-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="90f2b-251">V typických scénářích je pravděpodobné, že data pro vlastní pole v sekci záhlaví budou vybrána z tabulky TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="90f2b-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="90f2b-252">Lze však použít jiné tabulky, pokud lze data načíst na základě poskytnutého záznamu TSTimesheetTable nebo pokud nemá konkrétní kontext záznamu (například pokud je pole v parametrech projektu nastaveno jako jen pro čtení).</span><span class="sxs-lookup"><span data-stu-id="90f2b-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="90f2b-253">Všimněte si, že vlastní pole nemusí mít žádné záložní záznamy databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="90f2b-254">Mohou být dynamicky generovány na základě logiky X++.</span><span class="sxs-lookup"><span data-stu-id="90f2b-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="90f2b-255">Následující příklad ukazuje tento přístup.</span><span class="sxs-lookup"><span data-stu-id="90f2b-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="90f2b-256">Pole v sekci záhlaví jsou v aplikaci vždy jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="90f2b-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="90f2b-257">Pomocí řetězce příkazů v metodě buildCustomFieldList třídy TSTimesheetSettings zobrazíte pole v části záhlaví</span><span class="sxs-lookup"><span data-stu-id="90f2b-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="90f2b-258">Tento kód řídí nastavení zobrazení pro pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="90f2b-259">Například řídí typ pole, štítek, zda je pole povinné a v jaké části se pole zobrazuje.</span><span class="sxs-lookup"><span data-stu-id="90f2b-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="90f2b-260">Následující příklad ukazuje vypočítanou hodnotu v sekci záhlaví v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="90f2b-261">Pomocí řetězce příkazů v metodě buildCustomFieldListForHeader třídy TSTimesheetDetails vyplňte detaily časového výkazu</span><span class="sxs-lookup"><span data-stu-id="90f2b-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="90f2b-262">Metoda **buildCustomFieldListForHeader** se používá k vyplnění podrobností v záhlaví časového výkazu v mobilní aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="90f2b-263">Jako parametr vezme záznam TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="90f2b-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="90f2b-264">Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="90f2b-265">Následující příklad nenačte žádné hodnoty z databáze.</span><span class="sxs-lookup"><span data-stu-id="90f2b-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="90f2b-266">Místo toho používá logiku X++ ke generování vypočítané hodnoty, která se poté zobrazí v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="90f2b-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="90f2b-267">Další možnosti konfigurovatelnosti / rozšiřitelnosti</span><span class="sxs-lookup"><span data-stu-id="90f2b-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="90f2b-268">Přidání dalšího ověření pro aplikaci</span><span class="sxs-lookup"><span data-stu-id="90f2b-268">Adding additional validation for the app</span></span>

<span data-ttu-id="90f2b-269">Existující logika funkce časového výkazu na úrovni databáze bude i nadále fungovat podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="90f2b-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="90f2b-270">Chcete-li přerušit dokončení operací ukládání nebo odeslání a zobrazit konkrétní chybovou zprávu, můžete do kódu přidat hodnotu **chyba zahození („zpráva pro uživatele“)** pomocí řetězce rozšíření příkazů.</span><span class="sxs-lookup"><span data-stu-id="90f2b-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="90f2b-271">Tady jsou tři příklady užitečných rozšiřitelných metod:</span><span class="sxs-lookup"><span data-stu-id="90f2b-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="90f2b-272">Pokud příkaz **validateWrite** v tabulce TSTimesheetLine vrací hodnotu **false** , během operace ukládání časového řádku se v mobilní aplikaci zobrazí chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="90f2b-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="90f2b-273">Pokud příkaz **validateSubmit** v tabulce validateSubmit vrací hodnotu **false** , během odesílání časového výkazu do aplikace se uživateli zobrazí chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="90f2b-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="90f2b-274">Logika, která vyplňuje pole (například **Vlastnost řádku** ) během metody **vložit** v tabulce TSTimesheetLine bude stále spuštěna.</span><span class="sxs-lookup"><span data-stu-id="90f2b-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="90f2b-275">Skrytí a označení předem připravených polí jako jen pro čtení prostřednictvím konfigurace</span><span class="sxs-lookup"><span data-stu-id="90f2b-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="90f2b-276">Z parametrů projektu můžete v mobilní aplikaci nastavit pole připravená k použití pouze ke čtení nebo skrytá.</span><span class="sxs-lookup"><span data-stu-id="90f2b-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="90f2b-277">Nastavte možnosti v části **Mobilní časové rozvrhy** na kartě **Časový výkaz** stránky **Parametry řízení projektu a účetnictví**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parametry projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="90f2b-279">Změna aktivit, které jsou k dispozici pro výběr prostřednictvím rozšíření</span><span class="sxs-lookup"><span data-stu-id="90f2b-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="90f2b-280">Aktivity, které jsou k dispozici pro výběr projektu, se vyplňují prostřednictvím metod **getActivitiesForProject()** a **getActivityQuery()** ve třídě **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="90f2b-281">Pomocí řetězce příkazů můžete toto chování změnit tak, aby odpovídalo vašemu obchodnímu scénáři pro aktivity, které jsou k dispozici pro výběr pro konkrétní projekt.</span><span class="sxs-lookup"><span data-stu-id="90f2b-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="90f2b-282">Zadání výchozí kategorie projektu do záznamů časového rozvrhu</span><span class="sxs-lookup"><span data-stu-id="90f2b-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="90f2b-283">K zadání výchozí kategorie projektu do záznamů časového výkazu dochází na třech úrovních.</span><span class="sxs-lookup"><span data-stu-id="90f2b-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="90f2b-284">Pomocí řetězce příkazů můžete rozšířit chování na kterékoli nebo všech těchto úrovních a dosáhnout požadovaného chování.</span><span class="sxs-lookup"><span data-stu-id="90f2b-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="90f2b-285">Používá se následující hierarchie:</span><span class="sxs-lookup"><span data-stu-id="90f2b-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="90f2b-286">Aplikace se pokusí vložit výchozí kategorii ze zdroje projektu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="90f2b-287">Tato výchozí kategorie je nastavena v metodách **getCurrentUserResource** a **getDelegatedResourcesForCurrentUser** ve třídě **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="90f2b-288">Pokud není výchozí kategorie poskytnuta na úrovni zdrojů projektu, aplikace se ji pokusí vytáhnout z aktivity projektu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="90f2b-289">Tato výchozí kategorie je nastavena v metodě **getActivitiesForProject** třídy **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="90f2b-290">Pokud není výchozí kategorie poskytnuta na úrovni aktivity projektu, je výchozí kategorie převzata z parametrů projektu.</span><span class="sxs-lookup"><span data-stu-id="90f2b-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="90f2b-291">Tato výchozí kategorie je nastavena v metodě **getProjectDetailsbyRule** třídy **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="90f2b-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
