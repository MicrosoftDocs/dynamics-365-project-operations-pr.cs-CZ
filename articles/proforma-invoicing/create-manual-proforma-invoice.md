---
title: Vytvoření manuální proforma faktury
description: Toto téma poskytuje informace o vytvoření proforma faktury.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d3c84664f1b0701db17f0c05654e0c99bb6c640
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128050"
---
# <a name="create-a-manual-proforma-invoice"></a>Vytvoření manuální proforma faktury

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Fakturace poskytuje projektovým manažerům druhou úroveň schválení před tím, než vytvoří faktury pro zákazníky. První úroveň schválení je dokončena schválením časových a výdajových záznamů, které odešlou členové projektového týmu.

Řešení Dynamics 365 Project Operations není navrženo pro generování zákaznických faktur, a to z následujících důvodů:

- Neobsahuje daňové informace.
- Neumí pomocí správně nakonfigurovaných směnných kurzů převést jiné měny na fakturační měnu.
- Neumí správně formátovat faktury, aby je bylo možné vytisknout.

Místo toho můžete k vytvoření zákaznických faktur, které používají informace vygenerované z návrhů faktu, použít finanční nebo účetní systém.

## <a name="creating-project-invoices"></a>Vytvoření projektových faktur

Projektové faktury lze vytvářet jednotlivě nebo hromadně. Můžete je vytvořit ručně nebo je lze nakonfigurovat tak, aby byly generovány v automatických spuštěních.

### <a name="manually-create-project-invoices"></a>Ruční vytvoření projektových faktur 

Ze stránky se seznamem **Projektové smlouvy** můžete vytvořit projektové faktury samostatně pro každou projektovou smlouvu nebo můžete faktury vytvořit hromadně pro více projektových smluv.

Chcete-li vytvořit fakturu pro konkrétní projektovou smlouvu, postupujte podle tohoto kroku.

- Na stránce se seznamem **Projektových smluv** otevřete projektovou smlouvu a pak vyberte **Vytvořit fakturu**.

    Je vygenerována faktura pro všechny transakce vybrané projektové smlouvy, které mají stav **Připraveno k fakturaci**. Tyto transakce zahrnují čas, výdaje, milníky a řádky smlouvy založené na produktu.

Chcete-li vytvořit faktury hromadně, postupujte následovně.

1. Na stránce se seznamem **Projektových smluv** vyberte jednu nebo více projektových smluv, pro které musíte vytvořit fakturu, a pak vyberte **Vytvořit projektové faktury**.

    Zobrazí se zpráva s upozorněním, že před vytvořením faktur může dojít k prodlevě. Tento proces je také zobrazen.

2. Výběrem **OK** zavřete dialogové okno.

    Je vygenerována faktura pro všechny transakce na řádku smlouvy, které mají stav **Připraveno k fakturaci**. Tyto transakce zahrnují čas, výdaje, milníky a řádky smlouvy založené na produktu.

3. Chcete-li zobrazit generované faktury, přejděte do **Prodej** \> **Fakturace** \> **Faktury**. Pro každou projektovou smlouvu se zobrazí jedna faktura.

### <a name="set-up-automated-creation-of-project-invoices"></a>Nastavení automatického vytváření projektových faktur 

Chcete-li nakonfigurovat spuštění automatické fakturace, postupujte následujícím způsobem.

1. Přejděte na **Nastavení** \> **Dávkové úlohy**.
2. Vytvořte dávkovou úlohu a pojmenujte ji **Vytvořit faktury v Project Operations**. Název dávkové úlohy musí obsahovat termín „Vytvořit faktury”.
3. V poli **Typ úlohy** vyberte **Žádný**. Ve výchozím nastavení jsou možnosti **Frekvence denně** a **Je aktivní** nastaveny na **Ano**.
4. Vyberte **Spustit pracovní postup**. V dialogovém okně **Vyhledat záznam** se zobrazí tři pracovní postupy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom vyberte **Přidat**.
6. V dalším dialogovém okně vyberte **OK**. Po pracovním postupu **Spánek** následuje pracovní postup **Zpracovat**.

    Pracovní postup **ProcessRunner** můžete také vybrat v kroku 5. Když potom vyberete **OK**, bude pracovní postup **Zpracovat** následován pracovním postupem **Spánek**.

Pracovní postupy **ProcessRunCaller** a **ProcessRunner** vytvářejí faktury. **ProcessRunCaller** volá **ProcessRunner**. **ProcessRunner** je pracovní postup, který skutečně vytváří faktury. Prochází všemi řádky smluv, pro které musí být vytvořeny faktury, a vytváří faktury pro tyto řádky. Aby určil řádky smluv, pro které musí být vytvořeny faktury, vyhledává úloha data spuštění faktury pro řádky smluv. Jestliže řádky smluv, které patří k jedné smlouvě, mají stejné datum spuštění faktury, budou transakce sloučeny do jedné faktury, která má dva řádky faktury. Pokud neexistují žádné transakce pro vytvoření faktur, úloha přeskočí vytvoření faktury.

Proces **ProcessRunner** po svém dokončení volá proces **ProcessRunCaller**, poskytne čas ukončení a je zavřen. Proces **ProcessRunCaller** poté spustí časovač, který běží po dobu 24 hodin od zadaného času ukončení. Po doběhnutí časovače je **ProcessRunCaller** uzavřen.

Úloha dávkového zpracování pro vytváření faktur je opakující se úloha. Pokud je tento dávkový proces spuštěn vícekrát, vytvoří se více instancí této úlohy a způsobí chyby. Proto byste tento dávkový proces měli spustit pouze jednou a restartovat ho, pouze pokud přestane běžet.

> [!NOTE]
> Dávková fakturace běží pouze pro řádky projektové smlouvy, které jsou konfigurovány podle plánů faktur. Řáeke smlouvy s metodou fakturace s pevnou cenou musí mít nakonfigurované milníky. Řádek smlouvy o projektu s metodou fakturace času a materiálu bude vyžadovat sestavení časového rozvrhu faktur. Totéž platí pro řádek smlouvy založené na projektu.      
 
### <a name="edit-a-draft-invoice"></a>Úprava konceptu faktury

Když vytváříte koncept projektové faktury, jsou všechny nefakturované prodejní transakce, které byly vytvořeny při schválení časových a výdajových záznamů, načteny do faktury. Dokud je faktura stále ve fázi konceptu, můžete provést následující úpravy:

- Odstranit nebo upravit podrobnosti řádku faktury.
- Upravit a přizpůsobit množství a typ fakturace.
- Přímo přidat čas, náklady a poplatky jako transakce na faktuře. Tuto funkci můžete použít v případě, že je řádek faktury namapován na řádek smlouvy, který umožňuje tyto třídy transakcí.

Chcete-li fakturu potvrdit, vyberte **Potvrdit**. Akce Potvrdit představuje jednosměrnou akci. Když vyberete **Potvrdit**, systém nastaví fakturu jen pro čtení a vytvoří skutečné fakturované hodnoty z každé podrobnosti řádku faktury pro každý řádek faktury. Pokud podrobnosti řádku faktury odkazují na nefakturovanou skutečnou hodnotu prodeje, tak systém také stornuje nefakturovanou skutečnou hodnotu prodeje. (Všechny podrobnosti řádku faktury vytvořené z časových nebo výdajových záznamů budou odkazovat na nefakturovanou skutečnou hodnotu prodeje.) Systémy integrace hlavní knihy mohou toto storno použít ke zrušení probíhající práce (WIP) pro účetní účely.

### <a name="correct-a-confirmed-invoice"></a>Oprava potvrzené faktury

Potvrzené faktury lze upravovat (opravovat). Když opravíte potvrzenou fakturu, vytvoří se nový koncept opravné faktury. Protože se předpokládá, že chcete zrušit všechny transakce a množství z původní faktury, obsahuje tato opravná faktura všechny transakce z původní faktury a všechna množství na ní jsou 0 (nula).

Pokud transakce nevyžadují opravu, můžete je odebrat z konceptu opravné faktury. Pokud chcete zrušit nebo vrátit pouze částečné množství, můžete upravit pole **Množství** v podrobnostech řádku. Pokud otevřete podrobnosti řádku faktury, uvidíte původní množství faktury. Potom můžete upravit aktuální množství faktury tak, aby bylo menší nebo větší než původní množství faktury.

Po potvrzení opravné faktury se původní skutečná hodnota fakturovaného prodeje stornuje a vytvoří se nová skutečná hodnota fakturovaného prodeje. Pokud bylo množství sníženo, rozdíl způsobí, že bude vytvořena i nová skutečná hodnota nefakturovaného prodeje. Pokud byl například původní fakturovaný prodej na 8 hodin a opravné podrobnosti řádku faktury obsahují snížené množství 6 hodin, stornují se původní vyfakturované prodejní řádky a vytvoří dvě nové skutečné hodnoty:

- Fakturovaná skutečná hodnota prodeje pro 6 hodin.
- Skutečná hodnota nefakturovaného prodeje pro zbývající dvě hodiny. Tato transakce může být buď fakturována později, nebo označena jako neúčtovatelná, v závislosti na jednáních se zákazníkem.
