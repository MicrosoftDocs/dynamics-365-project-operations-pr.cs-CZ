---
title: Vytvoření plánu faktur na řádku smlouvy na základě projektu
description: Tento téma poskytuje informace o vytváření harmonogramů faktur a milníků pro řádky smlouvy.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 23378b51c8324a60918ad494e7f659dbbc94e2a8
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074012"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Vytvoření plánu faktur na řádku smlouvy na základě projektu 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Můžete vytvářet plán faktur na řádku smlouvy na základě projektu. Fakturace je povolena až poté, co je získána smlouva a vytváříte smlouvu o projektu. Rozpis faktur umožňuje automatické vytváření konceptů faktur za řádek smlouvy na základě projektu. Pokud však faktury vytváříte pouze ručně, můžete přeskočit vytváření plánů faktur na řádcích smlouvy.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Vytvořte harmonogram faktury za čas a materiál pro řádek smlouvy.

Když je metodou fakturace pro řádek smlouvy na základě projektu čas a materiál, můžete vytvořit rozpis faktur na základě data. Chcete-li automaticky vygenerovat plán faktur na základě data, proveďte následující kroky.

1. Přejděte na **Nastavení** > **Frekvence faktur** a nastavte frekvenci faktur.
2. Přejděte na záznam smlouvy o projektu a na kartě **Shrnutí** v poli **Požadované datum dodání** vyberte datum.
3. Otevřete řádek smlouvy **Čas a materiál** , pro který potřebujete vytvořit rozpis faktur na základě data. 
4. Na kartě **Rozpis faktur** vyberte datum zahájení fakturace a frekvence faktur.
5. V podmřížce vyberte **Generovat rozpis faktur**. Rozpis faktur se vygeneruje s poli **Datum spuštění faktury** , **Mezní datum transakce** a **Stav spuštění** následujícím způsobem:

    - **Datum spuštění faktury** : Toto datum je určeno na základě frekvence fakturace.
    - **Mezní datum transakce** Den před datem spuštění faktury.
    - **Stav spuštění** : Automaticky nastaveno na **Nespuštěno**. Když je úloha automatického vytváření faktur spuštěna pro určité datum spuštění faktury, aktualizuje toto pole buď na **Spuštění úspěšné** , nebo **Spuštění selhalo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Vytvořte harmonogram faktury za fixní cenu pro řádek smlouvy

Když má řádek smlouvy fixní metodu fakturace, můžete vytvořit plán faktur na základě milníků. 

> [!NOTE]
> Milníky nelze vytvořit na řádku smlouvy, pokud na řádek smlouvy není namapován žádný projekt.

Provedením následujících kroků automaticky vygenerujete rozpis faktur na základě milníků pro fixní sadu milníků, které jsou rovnoměrně rozloženy pro kalendářní období.

1. Přejděte na **Nastavení** > **Frekvence faktur** a nastavte frekvenci faktur.
2. Přejděte na záznam smlouvy o projektu a na kartě **Shrnutí** v poli **Požadované datum dodání** vyberte datum.
3. Otevřete řádek smlouvy **Fixní cena** , pro který vytváříte milníkový plán. Na kartě **Milníky faktur** vyberte datum zahájení fakturace a frekvence faktur. 
4. V podmřížce vyberte **Generovat periodické milníky**. Rozpis faktur je generován pomocí polí **Název milníku** , **Datum milníku** a **Částka milníku** nastavených následovně:

    - **Název milníku** : Toto datum je určeno na základě frekvence fakturace.
    - **Datum milníku** : Toto datum je určeno na základě frekvence fakturace.
    - **Částka milníku** : Tato částka se vypočítá vydělením částky smlouvy na řádku smlouvy počtem milníků, jak je diktováno frekvencí a začátkem fakturace a požadovanými termíny dodání.

    Pokud má řádek smlouvy hodnotu v poli **Odhadovaná částka daně** , toto pole je také při generování periodických milníků rovnoměrně přiděleno každému milníku.

Milníky fakturace by se měly rovnat smluvní hodnotě řádku smlouvy. Pokud ne, zobrazí se chyba na stránce **Řádek smlouvy**. Chybu můžete opravit ověřením, že milníky fakturace dají v součtu smluvní hodnotu řádku vytvořením, úpravou nebo odstraněním milníků. Po provedení změn obnovte stránku, abyste chybu odstranili.

### <a name="manually-create-milestones"></a>Ruční vytváření milníků

Milníky fixní ceny můžete také generovat ručně, pokud nejsou pravidelně rozděleny. Pomocí následujících kroků ručně vytvoříte milník.

1. Otevřete řádek smlouvy s pevnou cenou, pro kterou vytváříte milník, a na kartě **Rozpis faktur** vyberte **+ Vytvořit nový milník řádku smlouvy**. 
2. Na stránce **Vytvoření milníku** zadejte požadované informace na základě následující tabulky.

| Pole | Místo | Relevance, účel a vedení | Dopad na následné složky |
| --- | --- | --- | --- |
| Název milníku | Vytvořit | Textové pole pro název milníku. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Projektový úkol | Vytvořit | Pokud je milník svázán s úkolem projektu, můžete pomocí tohoto odkazu přidat vlastní logiku nastavení stavu milníku na základě stavu úlohy. | Aplikace nemá žádný následný dopad tohoto odkazu na úkol. |
| Datum milníku | Vytvořit | Nastavte datum, kdy by měl proces automatického vytváření faktur hledat stav tohoto milníku, aby jej mohl zohlednit pro fakturaci. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Stav faktury | Vytvořit | Když je vytvořen milník, je tento stav vždy nastaven na **Není připraveno na fakturaci** nebo **Není uloženo**. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Částka řádku | Vytvořit | Částka nebo hodnota milníku, která bude zákazníkovi fakturována. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Daň | Vytvořit | Částka daně použitá u milníku. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |

3. Zvolte **Uložit a zavřít**.
