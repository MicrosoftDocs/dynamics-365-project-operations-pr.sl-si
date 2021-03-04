---
title: Vključevanje polj po meri za mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet v sistemih iOS in Android
description: Ta tema ponuja skupne vzorce za uporabo razširitev za vključevanje polj po meri.
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
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084810"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Vključevanje polj po meri za mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet v sistemih iOS in Android

[!include [banner](../includes/banner.md)]

Ta tema ponuja skupne vzorce za uporabo razširitev za vključevanje polj po meri. Zajete so naslednje teme:

- Različne vrste podatkov, ki jih podpira ogrodje polja po meri
- Prikaz polj samo za branje ali polj, ki jih je mogoče urejati, v vnosih časovnega lista in shranjevanje vrednosti, ki jih vnese uporabnik, nazaj v zbirko podatkov
- Prikaz polj samo za branje v glavi časovnega lista
- Vključevanje druge poslovne logike po meri za vnos privzetih vrednosti v polja in dodatno preverjanje veljavnosti

## <a name="audience"></a>Občinstvo

Ta tema je namenjena razvijalcem, ki vključujejo svoja polja po meri v mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet, ki je na voljo za Apple iOS in Google Android. Predpostavlja se, da bralci poznajo razvoj X++ in funkcije časovnega lista projekta.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Pogodba o podatkih – razred TSTimesheetCustomField X++

Razred **TSTimesheetCustomField** je razred pogodbe o podatkih X++, ki predstavlja informacije o polju po meri za funkcije časovnega lista. Seznami predmetov polja po meri se posredujejo v pogodbo o podatkih TSTimesheetDetails in TSTimesheetEntry za prikaz polj po meri v mobilni aplikaciji.

- **TSTimesheetDetails** – pogodba o glavi časovnega lista.
- **TSTimesheetEntry** – pogodba o transakciji časovnega lista. Skupine teh predmetov, ki imajo enake informacije o projektu in vrednost **timesheetLineRecId** , predstavljajo vrstico.

### <a name="fieldbasetype-types"></a>fieldBaseType (vrste)

Lastnost **FieldBaseType** v predmetu **TsTimesheetCustom** določa vrsto polja, ki se prikaže v aplikaciji. Podprte so spodnje vrednosti **Vrste**.

| Vrednost »Vrste« | Vrsta              | Opombe |
|-------------|-------------------|-------|
| 0           | Niz (in oštevilčenje) | Polje se prikaže kot besedilno polje. |
| 1           | Celo število           | Vrednost je prikazana kot število brez decimalnih mest. |
| 2           | Dejanska vrednost              | Vrednost je prikazana kot število z decimalnimi mesti.<p>Če želite v aplikaciji prikazati dejansko vrednost kot valuto, uporabite lastnost **fieldExtensedType**. Uporabite lahko lastnost **numberOfDecimals** in nastavite število prikazanih decimalnih mest.</p> |
| 3           | Datum              | Oblike zapisa datuma določa uporabnikova nastavitev **Oblika zapisa datuma, časa in številk** , ki je navedena pod možnostjo **Nastavitev jezika in države/regije** v razdelku **Uporabniške možnosti**. |
| 4           | Logična vrednost           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Če lastnost **stringOptions** ni na voljo v predmetu **TSTimesheetCustomField** , je uporabniku na voljo polje s prostim besedilom.

    Lastnost **stringLength** lahko uporabite za nastavitev največje dolžine niza, ki jo lahko vnesejo uporabniki.

- Če je lastnost **stringOptions** na voljo v predmetu **TSTimesheetCustomField** , so ti elementi seznama edine vrednosti, ki jih lahko uporabniki izberejo z uporabo izbirnih gumbov.

    V tem primeru lahko polje niza deluje kot vrednost oštevilčenja za vnos uporabnika. Če želite shraniti vrednost v zbirko podatkov kot oštevilčenje, ročno preslikajte vrednost niza nazaj na vrednost oštevilčenja, preden jo shranite v zbirko podatkov z uporabo niza ukazov (za primer glejte razdelek »Uporaba niza ukazov v razredu TSTimesheetEntryService za shranjevanje vnosa v časovnem listu iz aplikacije nazaj v zbirko podatkov« v nadaljevanju te teme).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

To lastnost lahko uporabite za oblikovanje dejanskih vrednosti kot valute. Ta pristop se uporablja le, če je vrednost **fieldBaseType** vrste **Dejanska vrednost**.

- **TSCustomFieldExtendedType:None** – oblikovanje ni uporabljeno.
- **TSCustomFieldExtendedType::Currency** – vrednost je oblikovana kot valuta.

    Ko je oblikovanje valute dejavno, lahko uporabite polje **stringValue** za posredovanje kode valute, ki jo želite prikazati v aplikaciji. Vrednost je vrednost samo za branje.

    Polje **realValue** vsebuje denarni znesek, ki ga je treba shraniti v zbirko podatkov.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

S to lastnostjo lahko določite, kje v aplikaciji naj se prikaže polje po meri.

- **TSCustomFieldSection::Header** – polje bo prikazano v razdelku **Prikaži več podrobnosti** v aplikaciji. Ta polja so vedno samo za branje.
- **TSCustomFieldSection::Line** – polje se bo prikazalo za vsemi vnaprej pripravljenimi polji vrstice v vnosih časovnega lista. Ta polja so lahko polja, ki jih je mogoče urejati, ali polja samo za branje.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ta lastnost prepozna polje, ko se vrednosti, navedene v aplikaciji, shranijo nazaj v zbirko podatkov.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ta lastnost prepozna polje, ko se vrednosti, navedene v aplikaciji, shranijo nazaj v zbirko podatkov.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Nastavite to lastnost na **Da** , če želite, da uporabniki lahko urejajo polje v razdelku za vnos v časovni list. Nastavite lastnost na **Ne** , če želite, da je polje samo za branje.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Nastavite to lastnost na **Da** , če želite, da je polje v razdelku za vnos v časovni list obvezno.

### <a name="label-str"></a>label (str)

Ta lastnost določa oznako, ki je prikazana poleg polja v aplikaciji.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Ta lastnost se uporablja samo, če je lastnost **fieldBaseType** nastavljena na vrsto **Niz**. Če je nastavljena lastnost **stringOptions** , so vrednosti nizov, ki so na voljo za izbiro z izbirnimi gumbi, določene z nizi na seznamu. Če ni nizov, je dovoljen vnos prostega besedila v polje niza (za primer glejte razdelek »Uporaba niza ukazov v razredu TSTimesheetEntryService za shranjevanje vnosa v časovnem listu iz aplikacije nazaj v zbirko podatkov« v nadaljevanju te teme).

### <a name="stringlength-int"></a>stringLength (int)

Ta lastnost določa največjo dolžino polja niza. Uporablja se samo, če je lastnost **fieldBaseType** nastavljena na vrsto **Niz**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ta lastnost določa število decimalnih mest, ki so prikazana za dejansko polje. Uporablja se samo, če je lastnost **fieldBaseType** nastavljena na vrsto **Dejanska vrednost**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ta lastnost upravlja vrstni red prikaza polj po meri v aplikaciji, če je določeno več kot eno polje po meri. Najprej so prikazana polja z nižjimi številkami.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Pri poljih vrste **Logična vrednost** ta lastnost posreduje logično vrednost polja med strežnikom in aplikacijo.

### <a name="guidvalue-guid"></a>guidValue (guid)

Pri poljih vrste **GUID** ta lastnost posreduje vrednost globalnega enoličnega identifikatorja (GUID) za polje med strežnikom in aplikacijo.

### <a name="int64value-int64"></a>int64Value (int64)

Pri poljih vrste **Int64** ta lastnost posreduje vrednost »int64« polja med strežnikom in aplikacijo.

### <a name="intvalue-int"></a>intValue (int)

Pri poljih vrste **Int** ta lastnost posreduje vrednost »int« polja med strežnikom in aplikacijo.

### <a name="realvalue-real"></a>realValue (real)

Pri poljih vrste **Dejanska vrednost** ta lastnost posreduje dejansko vrednost polja med strežnikom in aplikacijo.

### <a name="stringvalue-str"></a>stringValue (str)

Pri poljih vrste **Niz** ta lastnost posreduje vrednost niza za polje med strežnikom in aplikacijo. Uporablja se tudi za polja vrste **Dejanska vrednost** , ki so oblikovana kot valuta. Pri teh poljih se lastnost uporablja za posredovanje kode valute v aplikacijo.

### <a name="datevalue-date"></a>dateValue (date)

Pri poljih vrste **Datum** ta lastnost posreduje vrednost datuma za polje med strežnikom in aplikacijo.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Prikaz in shranjevanje polja po meri v razdelku za vnos v časovni list

Spodaj je posnetek zaslona iz mobilne aplikacije, ki prikazuje ustvarjanje vnosa v časovni list. Prikazuje vnaprej pripravljena polja in polje po meri v razdelku »Časovni vnos«, imenovano »Preizkusni niz«, z že nastavljeno vrednostjo oštevilčenja »Druga možnost«.

![Polje po meri »Preizkusni niz« v aplikaciji](media/timesheet-entry.jpg)



Spodaj je posnetek zaslona iz mobilne aplikacije uporabnika, ki izbere eno od možnosti oštevilčevanja, ki je na voljo za polje po meri »Preizkusni niz«.  Možnosti, prikazani kot izbirna gumba, sta »Prva možnost« in »Druga možnost«. Trenutno je izbrana druga možnost.

![Izbirna gumba za polje po meri »Preizkusni niz«](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Razširitev tabele TSTimesheetLine, tako da ima polje po meri

Običajno so podatki za polje po meri v razdelku za vnos v časovni list shranjeni v tabelo TSTimesheetLine. Vendar lahko uporabite druge tabele, če je podatke mogoče pridobiti na podlagi zapisa TSTimesheetTrans, ki je na voljo, ali če ni določenega konteksta zapisa (če je na primer polje v parametrih projekta nastavljeno kot samo za branje).

Upoštevajte, da polja po meri ne potrebujejo rezervnih zapisov zbirke podatkov. Lahko so dinamično ustvarjeni na podlagi logike X++. Ta pristop je lahko uporaben v primerih samo za branje (za primer dinamično ustvarjenih vrednosti polja po meri glejte razdelek »Uporaba niza ukazov v razredu TSTimesheetDetails, metodi buildCustomFieldListForHeader za vnašanje podrobnosti časovnega lista«).

Spodaj je posnetek zaslona drevesa predmetov aplikacije iz aplikacije Visual Studio. Prikazuje razširitev tabele TSTimesheetLine s poljem TestLineString, ki je dodano kot polje po meri.

![Niz vrstice](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Uporaba niza ukazov v metodi buildCustomFieldList razreda TSTimesheetSettings za prikaz polja v razdelku za vnos v časovni list

Ta koda upravlja nastavitve prikaza za polje v aplikaciji. Upravlja na primer vrsto polja, oznako, ali je polje obvezno in v katerem razdelku se polje prikaže.

Spodnji primer prikazuje polje niza v časovnem vnosu. To polje ima dve možnosti, **Prva možnost** in **Druga možnost** , ki sta na voljo prek izbirnih gumbov. Polje v aplikaciji je povezano s poljem **TestLineString** , ki je dodano v tabelo TSTimesheetLine.

Oglejte si uporabo metode **TSTimesheetCustomField::newFromMetatdata()** za enostavnejšo inicializacijo lastnosti polja po meri: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** in **numberOfDecimals**. Te parametre lahko nastavite tudi ročno, če želite.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Uporaba niza ukazov v metodi buildCustomFieldListForEntry razreda TSTimesheetEntry za vnos vrednosti v vnosu v časovni list

Metoda **buildCustomFieldListForEntry** se uporablja za vnos vrednosti v vrsticah shranjenega časovnega lista v mobilni aplikaciji. Kot parameter je potreben zapis TSTimesheetTrans. Polja iz tega zapisa lahko uporabite za vnos vrednosti polja po meri v aplikaciji.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Uporaba niza ukazov v razredu TSTimesheetEntryService za shranjevanje vnosa v časovni list iz aplikacije nazaj v zbirko podatkov

Če želite polje po meri shraniti nazaj v zbirko podatkov pri običajni uporabi, morate razširiti več metod:

- Metoda **timesheetLineNeedsUpdating** se uporablja za ugotavljanje, ali je uporabnik v aplikaciji spremenil zapis vrstice in ga je treba shraniti v zbirko podatkov. Če učinkovitost delovanja ni zaskrbljujoča, lahko to metodo poenostavite, tako da vedno vrne vrednost **true**.
- Metodi **populateTimesheetLineFromEntryDuringCreate** in **populateTimesheetLineFromEntryDuringUpdate** lahko razširite tako, da vnesejo vrednosti v zapis zbirke podatkov TSTimesheetLine iz zapisa pogodbe o podatkih TSTimesheetEntry, ki je na voljo. V spodnjem primeru si oglejte, kako se preslikava med poljem zbirke podatkov in poljem za vnos ročno izvede prek kode X++.
- Metoda **populateTimesheetWeekFromEntry** se lahko razširi tudi, če je za polje po meri, ki je preslikano v predmet **TSTimesheetEntry** , potrebno povratno zapisovanje v tabelo zbirke podatkov TSTimesheetLineweek.

> [!NOTE]
> V spodnjem primeru je vrednost **firstOption** ali **secondOption** , ki jo izbere uporabnik, shranjena v zbirko podatkov kot neobdelana vrednost niza. Če je polje zbirke podatkov polje vrste **Oštevilčevanje** , lahko te vrednosti ročno preslikate v vrednost oštevilčevanja in nato shranite v polje oštevilčevanja v tabeli zbirke podatkov.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Prikaz polja po meri v razdelku glave časovnega lista

Spodaj je posnetek zaslona iz mobilne aplikacije, ki prikazuje časovni list. V zgornjem desnem kotu je bil izbran gumb »Več informacij« za prikaz možnosti »Prikaži več podrobnosti«.  

![Ukaz »Prikaži več podrobnosti«](media/show-more.png)

Spodaj je posnetek zaslona iz mobilne aplikacije, ki prikazuje razdelek »Več« na časovnem listu. Polje po meri, imenovano »Stopnja izkoristka tega časovnega lista (izračunano polje po meri)«, je bilo dodano v odsek glave časovnega lista. V polju po meri je nastavljena vrednost samo za branje »0,667«.

![Razdelek »Več«](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Razširitev tabele TSTimesheetTable, tako da ima polje po meri

Običajno so podatki za polje po meri v odseku glave pridobljeni iz tabele TSTimesheetHeader. Vendar lahko uporabite druge tabele, če je podatke mogoče pridobiti na podlagi zapisa TSTimesheetTable, ki je na voljo, ali če ni določenega konteksta zapisa (če je na primer polje v parametrih projekta nastavljeno kot samo za branje).

Upoštevajte, da polja po meri ne potrebujejo rezervnih zapisov zbirke podatkov. Lahko so dinamično ustvarjeni na podlagi logike X++. Naslednji primer prikazuje ta pristop.

Polja v odseku glave so v aplikaciji vedno samo za branje.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Uporaba niza ukazov v metodi buildCustomFieldList razreda TSTimesheetSettings za prikaz polja v odseku glave

Ta koda upravlja nastavitve prikaza za polje v aplikaciji. Upravlja na primer vrsto polja, oznako, ali je polje obvezno in v katerem razdelku se polje prikaže.

Naslednji primer prikazuje izračunano vrednost v odseku glave v aplikaciji.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Uporaba niza ukazov v metodi buildCustomFieldListForHeader razreda TSTimesheetDetails za vnos podrobnosti časovnega lista

Metoda **buildCustomFieldListForHeader** se uporablja za vnos podrobnosti glave časovnega lista v mobilni aplikaciji. Kot parameter je potreben zapis TSTimesheetTable. Polja iz tega zapisa lahko uporabite za vnos vrednosti polja po meri v aplikaciji. Naslednji primer ne prebere nobene vrednosti iz zbirke podatkov. Namesto tega uporablja logiko X++ za ustvarjanje izračunane vrednosti, ki je nato prikazana v aplikaciji.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Druge možnosti konfiguracije/razširljivosti

### <a name="adding-additional-validation-for-the-app"></a>Dodajanje dodatnega preverjanja veljavnosti za aplikacijo

Obstoječa logika za funkcije časovnega lista na ravni zbirke podatkov bo še vedno delovala po pričakovanjih. Če želite prekiniti dokončanje operacij shranjevanja ali pošiljanja in prikazati določeno sporočilo o napaki, lahko prek razširitve z nizom ukazov v kodo dodate **throw error("message to user")**. Tukaj so trije primeri uporabnih razširljivih metod:

- Če metoda **validateWrite** v tabeli TSTimesheetLine vrne vrednost **false** med operacijo shranjevanja za vrstico časovnega lista, se v mobilni aplikaciji prikaže sporočilo o napaki.
- Če metoda **validateSubmit** v tabeli TSTimesheetTable vrne vrednost **false** med pošiljanjem časovnega lista v aplikaciji, se uporabniku prikaže sporočilo o napaki.
- Logika, ki izpolni polja (na primer **Lastnost vrstice** ) med metodo **insert** v tabeli TSTimesheetLine, se bo še vedno izvajala.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skrivanje in označevanje vnaprej pripravljenih polj kot samo za branje prek konfiguracije

Iz parametrov projekta lahko v mobilni aplikaciji označite vnaprej pripravljena polja samo za branje ali jih skrijete. Nastavite možnosti v razdelku **Mobilni časovni listi** na zavihku **Časovni list** na strani **Vodenje projektov in računovodski parametri**.

![Projektni parametri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Spreminjanje dejavnosti, ki so na voljo za izbiro prek razširitev

Dejavnosti, ki so na voljo za izbiro projekta, so vnesene prek metod **getActivitiesForProject()** in **getActivityQuery()** v razredu **TsTimesheetProjectService**. Z nizom ukazov lahko to delovanje spremenite tako, da se ujema z vašim poslovnim scenarijem za dejavnosti, ki so na voljo za izbiro za določen projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Vnos privzete kategorije projekta v vnosih v časovni list

Vnos privzete kategorije projekta v vnosih v časovni list poteka na treh ravneh. Z nizom ukazov lahko razširite delovanje na posamezni ravni ali na vseh ravneh, da dosežete želeno delovanje. Uporablja se naslednja hierarhija:

1. Aplikacija poskuša pridobiti privzeto kategorijo iz vira projekta. Ta privzeta kategorija je nastavljena v metodah **getCurrentUserResource** in **getDelegatedResourcesForCurrentUser** v razredu **TSTimesheetSettingsService**.
2. Če privzeta kategorija ni na voljo na ravni vira projekta, jo aplikacija poskuša pridobiti iz dejavnosti projekta. Ta privzeta kategorija je nastavljena v metodi **getActivitiesForProject** v razredu **TSTimesheetProjectService**.
3. Če privzeta kategorija ni na voljo na ravni dejavnosti projekta, se pridobi iz parametrov projekta. Ta privzeta kategorija je nastavljena v metodi **getProjectDetailsbyRule** v razredu **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]