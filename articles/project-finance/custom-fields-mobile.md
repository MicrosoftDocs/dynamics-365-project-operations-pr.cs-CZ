---
title: Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systémech iOS a Android
description: Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750295"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementace vlastních polí pro mobilní aplikaci Microsoft Dynamics 365 Project Timesheet na systémech iOS a Android

[!include [banner](../includes/banner.md)]

Toto téma poskytuje běžné vzory pro použití rozšíření k implementaci vlastních polí. Jsou zahrnuta následující témata:

- Různé datové typy, které podporuje rámec vlastního pole
- Jak zobrazit pole jen pro čtení nebo upravitelná pole v záznamech časového výkazu a uložit hodnoty poskytnuté uživatelem zpět do databáze
- Jak zobrazit pole jen pro čtení v záhlaví časového výkazu
- Jak integrovat další vlastní obchodní logiku, abyste do polí zadali výchozí hodnoty a provedli další ověření

## <a name="audience"></a>Cílová skupina

Toto téma je určeno pro vývojáře, kteří integrují svá vlastní pole do mobilní aplikace Microsoft Dynamics 365 Project Timesheet, která je k dispozici pro Apple iOS a Google Android. Předpokládá se, že čtenáři jsou obeznámeni s vývojem X ++ a funkcemi časového výkazu projektu.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Smlouva na data - třída TSTimesheetCustomField X ++

Třída **TSTimesheetCustomField** je třída smlouvy na data X ++, která představuje informace o vlastním poli pro funkčnost časového výkazu. Seznamy objektů vlastního pole jsou předávány jak ve smlouv na data TSTimesheetDetails, tak ve smlouvě na data TSTimesheetEntry pro zobrazení vlastních polí v mobilní aplikaci.

- **TSTimesheetDetails** - Smlouva záhlaví časového výkazu.
- **TSTimesheetEntry** - Smlouva o transakci časového výkazu. Skupiny těchto objektů, které mají stejné informace o projektu a hodnota **timesheetLineRecId** tvoří řádek.

### <a name="fieldbasetype-types"></a>fieldBaseType (typy)

Vlastnost **FieldBaseType** v objektu **TsTimesheetCustom** určuje typ pole, které se zobrazí v aplikaci. Následující hodnoty **Typy**, které jsou podporovány.

| Hodnota Typy | Typ              | Poznámky |
|-------------|-------------------|-------|
| 0           | Řetězec (a výčet) | Pole se zobrazí jako textové pole. |
| 0           | Integer           | Hodnota je zobrazena jako číslo bez desetinných míst. |
| 2           | Reálné              | Hodnota je zobrazena jako číslo s desetinnými místy.<p>Chcete-li zobrazit skutečnou hodnotu jako měnu v aplikaci, použijte vlastnost **fieldExtenededType**. Můžete použít vlastnost **numberOfDecimals** pro nastavení počtu zobrazených desetinných míst.</p> |
| 3           | Datum              | Formáty data jsou určeny nastavením **Formát data, času a čísla** uživatele, které je uvedeno pod **Předvolby jazyka a země / regionu** v poli **Možnosti uživatele**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Pokud není vlastnost **stringOptions** poskytnuta v objektu **TSTimesheetCustomField**, je uživateli poskytnuto pole s volným textem.

    Vlastnost **stringLength** lze použít k nastavení maximální délky řetězce, kterou mohou uživatelé zadat.

- Pokud je vlastnost **stringOptions** poskytnuta v objektu **TSTimesheetCustomField**, tyto prvky seznamu jsou jediné hodnoty, které mohou uživatelé vybrat pomocí tlačítek s možnostmi (přepínačů).

    V takovém případě může pole řetězce fungovat jako hodnota výčtu pro účely vstupu uživatele. Chcete-li uložit hodnotu do databáze jako výčet, ručně namapujte hodnotu řetězce zpět na hodnotu výčtu před uložením do databáze pomocí řetězce příkazů (viz „Použití řetězce příkazů ve třídě TSTimesheetEntryService k uložení záznamu časového výkazu z aplikace zpět do databáze" dále v tomto tématu).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Tuto vlastnost můžete použít k formátování skutečných hodnot jako měny. Tento přístup je použitelný pouze tehdy, když hodnota **fieldBaseType** **Reálné**.

- **TSCustomFieldExtendedType: Žádný** - Není použito žádné formátování.
- **TSCustomFieldExtendedType::Měna** - Formátujte hodnotu jako měnu.

    Pokud je aktivní formátování měny, lze pole **stringValue** použít pro předání kódu měny, který by měl být zobrazen v aplikaci. Hodnota je hodnota jen pro čtení.

    Pole **realValue** obsahuje peněžní částku, která by měla být uložena do databáze.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Tuto vlastnost můžete použít k určení, kde se má vlastní pole v aplikaci objevit.

- **TSCustomFieldSection::Záhlaví** - Pole se objeví v části **Zobrazit více podrobností** v aplikaci. Tato pole jsou vždy jen pro čtení.
- **TSCustomFieldSection::Řádek** - Pole se objeví za všemi integrovanými poli řádku v záznamech časového výkazu. Tato pole mohou být upravitelná nebo pouze pro čtení.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Tato vlastnost identifikuje pole, když jsou hodnoty, které aplikace poskytuje, uloženy zpět do databáze.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Tato vlastnost identifikuje pole, když jsou hodnoty, které aplikace poskytuje, uloženy zpět do databáze.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Nastavte tuto vlastnost na **Ano** k určení, že by uživatelé měli upravit pole v sekci zadávání časového výkazu . Nastavte vlastnost na **Ne**, aby bylo jen pro čtení.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Nastavte tuto vlastnost na **Ano** k určení, že by pole v sekci zadávání časového výkazu mělo být povinné.

### <a name="label-str"></a>label (str)

Tato vlastnost určuje štítek, který se zobrazuje vedle pole v aplikaci.

### <a name="stringoptions-list-of-strings"></a>stringOptions (seznam řetězců)

Tato vlastnost je použitelná pouze v případě, že je vlastnost **fieldBaseType** nastavena na **Řetězec**. Pokud je vlastnost **stringOptions** nastavená, hodnoty řetězců, které jsou k dispozici pro výběr pomocí přepínačů, jsou určeny řetězci v seznamu. Pokud nejsou k dispozici žádné řetězce, je povoleno zadávání volného textu do pole řetězce (příklad najdete v části „Použití řetězce příkazů ve třídě TSTimesheetEntryService k uložení záznamu časového výkazu z aplikace zpět do databáze“ dále v tomto tématu).

### <a name="stringlength-int"></a>stringLength (int)

Tato vlastnost určuje maximální délku pole řetězce. Je použitelná pouze v případě, že je vlastnost **fieldBaseType** nastavena na **Řetězec**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Tato vlastnost určuje počet desetinných míst, která se zobrazují pro skutečné pole. Je použitelná pouze v případě, že je vlastnost **fieldBaseType** nastavena na **Reálné**.

### <a name="ordersequence-int"></a>orderSequence (int)

Tato vlastnost řídí pořadí, ve kterém se vlastní pole zobrazují v aplikaci, když je zadáno více než jedno vlastní pole. Nejprve se zobrazí pole, která mají nižší čísla.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Pro pole typu **Booleovský** tato vlastnost předá booleovskou hodnotu pole mezi serverem a aplikací.

### <a name="guidvalue-guid"></a>guidValue (guid)

Pro pole typu **GUID** tato vlastnost předá hodnotu globálně jedinečný identifikátor (GUID) pole mezi serverem a aplikací.

### <a name="int64value-int64"></a>int64Value (int64)

Pro pole typu **int64** tato vlastnost předá hodnotu int64 pole mezi serverem a aplikací.

### <a name="intvalue-int"></a>intValue (int)

Pro pole typu **Int** tato vlastnost předá hodnotu Int pole mezi serverem a aplikací.

### <a name="realvalue-real"></a>realValue (real)

Pro pole typu **Reálné** tato vlastnost předá reálnou hodnotu pole mezi serverem a aplikací.

### <a name="stringvalue-str"></a>stringValue (str)

Pro pole typu **Řetězec** tato vlastnost předá hodnotu řetězec pole mezi serverem a aplikací. Používá se také pro pole typu **Reálný**, která jsou formátována jako měna. U těchto polí se vlastnost používá k předání kódu měny do aplikace.

### <a name="datevalue-date"></a>dateValue (date)

Pro pole typu **Datum** tato vlastnost předá datovou hodnotu pole mezi serverem a aplikací.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Zobrazení a uložení vlastního pole v sekci zadávání časového výkazu

Níže je snímek obrazovky z mobilní aplikace vytvoření záznamu časového výkazu. Zobrazuje integrovaná pole a vlastní pole v sekci „Zadání času“ s názvem „Testovací řetězec“ s již nastavenou hodnotou výčtu „Druhá možnost“.

![Otestujte vlastní pole řetězce v aplikaci](media/timesheet-entry.jpg)



Níže je snímek obrazovky z mobilní aplikace uživatele, který si vybral jednu z možností výčtu dostupných pro vlastní pole „Testovací řetězec“.  Dvě možnosti jsou „První možnost“ a „Druhá možnost“ zobrazené jako přepínače. Druhá možnost je aktuálně vybrána.

![Volitelná tlačítka (přepínače) pro vlastní pole Testovací řetězec](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Rozšiřte tabulku TSTimesheetLine tak, aby měla vlastní pole

V typických scénářích je pravděpodobné, že data pro vlastní pole v sekci zadávání časového výkazu budou uložena do tabulky TSTimesheetLine. Lze však použít jiné tabulky, pokud lze data načíst na základě poskytnutého záznamu TSTimesheetTrans nebo pokud nemá konkrétní kontext záznamu (například pokud je pole v parametrech projektu nastaveno jako jen pro čtení).

Všimněte si, že vlastní pole nemusí mít žádné záložní záznamy databáze. Mohou být dynamicky generovány na základě logiky X++. Tento přístup může být užitečný ve scénářích jen pro čtení (příklad dynamicky generovaných hodnot vlastního pole viz část „Použití řetězce příkazů ve třídě TSTimesheetDetails, metoda buildCustomFieldListForHeader k vyplnění podrobností časového výkazu“.)

Níže je snímek obrazovky ze stromu aplikačních objektů Visual Studio. Zobrazuje rozšíření tabulky TSTimesheetLine s polem TestLineString přidaným jako vlastní pole.

![Řádek řetězce](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Pomocí řetězce příkazů v metodě buildCustomFieldList třídy TSTimesheetSettings zobrazíte pole v části zadání časového výkazu

Tento kód řídí nastavení zobrazení pro pole v aplikaci. Například řídí typ pole, štítek, zda je pole povinné a v jaké části se pole zobrazuje.

Následující příklad ukazuje pole řetězce pro časové záznamy. Toto pole má dvě možnosti, **První možnost** a **Druhá možnost**, které jsou k dispozici prostřednictvím volitelných tlačítek (přepínačů). Pole v aplikaci je přidruženo k poli **TestLineString**, které je přidáno do tabulky TSTimesheetLine.

Všimněte si metody **TSTimesheetCustomField::newFromMetatdata()** ke zjednodušení inicializace vlastností vlastního pole: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** a **numberOfDecimals**. Tyto parametry můžete také nastavit ručně, jak chcete.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Pomocí řetězce příkazů v metodě buildCustomFieldListForEntry třídy TSTimesheetEntry zadejte hodnoty do záznamu časového výkazu

Metoda **buildCustomFieldListForEntry** se používá k zadávání hodnot na uložené řádky časového výkazu v mobilní aplikaci. Jako parametr vezme záznam TSTimesheetTrans. Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Pomocí řetězce příkazů ve třídě TSTimesheetEntryService uložíte záznam časového výkazu z aplikace zpět do databáze

Chcete-li uložit vlastní pole zpět do databáze v obvyklém použití, musíte rozšířit více metod:

- Metoda **timesheetLineNeedsUpdating** se používá k určení, zda byl záznam řádku změněn uživatelem v aplikaci a musí být uložen do databáze. Pokud výkon není problém, lze tuto metodu zjednodušit, aby se vždy vrátila hodnota **true**.
- Metody **populateTimesheetLineFromEntryDuringCreate** a **populateTimesheetLineFromEntryDuringUpdate** lze rozšířit tak, aby zadávaly hodnoty v databázovém záznamu TSTimesheetLine ze záznamu smlouvy TSTimesheetEntry, který je poskytnut. V následujícím příkladu si všimněte, jak se mapování mezi databázovým polem a vstupním polem provádí ručně pomocí kódu X++.
- Metodu **populateTimesheetWeekFromEntry** lze také rozšířit, pokud vlastní pole, které je namapováno na objekt **TSTimesheetEntry**, musí zapisovat zpět do databázové tabulky TSTimesheetLineweek.

> [!NOTE]
> Následující příklad uloží hodnotu **firstOption** nebo **secondOption**, kterou uživatel vybere pro databázi jako nezpracovanou hodnotu řetězce. Pokud je databázové pole pole typu **Výčet**, lze tyto hodnoty ručně namapovat na hodnotu výčtu a poté uložit do pole výčtu v databázové tabulce.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Zobrazení vlastního pole v sekci záhlaví časového výkazu

Níže je snímek obrazovky z mobilní aplikace uživatele, který prohlíží časový výkaz. V pravém horním rohu bylo vybráno tlačítko „Další informace“ pro zobrazení možnosti „Zobrazit další podrobnosti“.  

![Příkaz Zobrazit více podrobností](media/show-more.png)

Níže je snímek obrazovky z mobilní aplikace zobrazující část Více časového výkazu. Do sekce záhlaví časového výkazu bylo přidáno vlastní pole s názvem „Míra využití tohoto časového výkazu (vypočítané vlastní pole)“. Ve vlastním poli je nastavena hodnota jen pro čtení „0,667“.

![Sekce Další](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Rozšiřte tabulku TSTimesheetTable tak, aby měla vlastní pole

V typických scénářích je pravděpodobné, že data pro vlastní pole v sekci záhlaví budou vybrána z tabulky TSTimesheetHeader. Lze však použít jiné tabulky, pokud lze data načíst na základě poskytnutého záznamu TSTimesheetTable nebo pokud nemá konkrétní kontext záznamu (například pokud je pole v parametrech projektu nastaveno jako jen pro čtení).

Všimněte si, že vlastní pole nemusí mít žádné záložní záznamy databáze. Mohou být dynamicky generovány na základě logiky X++. Následující příklad ukazuje tento přístup.

Pole v sekci záhlaví jsou v aplikaci vždy jen pro čtení.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Pomocí řetězce příkazů v metodě buildCustomFieldList třídy TSTimesheetSettings zobrazíte pole v části záhlaví

Tento kód řídí nastavení zobrazení pro pole v aplikaci. Například řídí typ pole, štítek, zda je pole povinné a v jaké části se pole zobrazuje.

Následující příklad ukazuje vypočítanou hodnotu v sekci záhlaví v aplikaci.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Pomocí řetězce příkazů v metodě buildCustomFieldListForHeader třídy TSTimesheetDetails vyplňte detaily časového výkazu

Metoda **buildCustomFieldListForHeader** se používá k vyplnění podrobností v záhlaví časového výkazu v mobilní aplikaci. Jako parametr vezme záznam TSTimesheetTable. Pole z tohoto záznamu lze použít k vyplnění hodnoty vlastního pole v aplikaci. Následující příklad nenačte žádné hodnoty z databáze. Místo toho používá logiku X++ ke generování vypočítané hodnoty, která se poté zobrazí v aplikaci.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Další možnosti konfigurovatelnosti / rozšiřitelnosti

### <a name="adding-additional-validation-for-the-app"></a>Přidání dalšího ověření pro aplikaci

Existující logika funkce časového výkazu na úrovni databáze bude i nadále fungovat podle očekávání. Chcete-li přerušit dokončení operací ukládání nebo odeslání a zobrazit konkrétní chybovou zprávu, můžete do kódu přidat hodnotu **chyba zahození („zpráva pro uživatele“)** pomocí řetězce rozšíření příkazů. Tady jsou tři příklady užitečných rozšiřitelných metod:

- Pokud příkaz **validateWrite** v tabulce TSTimesheetLine vrací hodnotu **false**, během operace ukládání časového řádku se v mobilní aplikaci zobrazí chybová zpráva.
- Pokud příkaz **validateSubmit** v tabulce validateSubmit vrací hodnotu **false**, během odesílání časového výkazu do aplikace se uživateli zobrazí chybová zpráva.
- Logika, která vyplňuje pole (například **Vlastnost řádku**) během metody **vložit** v tabulce TSTimesheetLine bude stále spuštěna.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skrytí a označení předem připravených polí jako jen pro čtení prostřednictvím konfigurace

Z parametrů projektu můžete v mobilní aplikaci nastavit pole připravená k použití pouze ke čtení nebo skrytá. Nastavte možnosti v části **Mobilní časové rozvrhy** na kartě **Časový výkaz** stránky **Parametry řízení projektu a účetnictví**.

![Parametry projektu](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Změna aktivit, které jsou k dispozici pro výběr prostřednictvím rozšíření

Aktivity, které jsou k dispozici pro výběr projektu, se vyplňují prostřednictvím metod **getActivitiesForProject()** a **getActivityQuery()** ve třídě **TsTimesheetProjectService**. Pomocí řetězce příkazů můžete toto chování změnit tak, aby odpovídalo vašemu obchodnímu scénáři pro aktivity, které jsou k dispozici pro výběr pro konkrétní projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Zadání výchozí kategorie projektu do záznamů časového rozvrhu

K zadání výchozí kategorie projektu do záznamů časového výkazu dochází na třech úrovních. Pomocí řetězce příkazů můžete rozšířit chování na kterékoli nebo všech těchto úrovních a dosáhnout požadovaného chování. Používá se následující hierarchie:

1. Aplikace se pokusí vložit výchozí kategorii ze zdroje projektu. Tato výchozí kategorie je nastavena v metodách **getCurrentUserResource** a **getDelegatedResourcesForCurrentUser** ve třídě **TSTimesheetSettingsService**.
2. Pokud není výchozí kategorie poskytnuta na úrovni zdrojů projektu, aplikace se ji pokusí vytáhnout z aktivity projektu. Tato výchozí kategorie je nastavena v metodě **getActivitiesForProject** třídy **TSTimesheetProjectService**.
3. Pokud není výchozí kategorie poskytnuta na úrovni aktivity projektu, je výchozí kategorie převzata z parametrů projektu. Tato výchozí kategorie je nastavena v metodě **getProjectDetailsbyRule** třídy **TSTimesheetProjectService**.
