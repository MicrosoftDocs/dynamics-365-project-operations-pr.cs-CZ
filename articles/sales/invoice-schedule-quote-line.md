---
title: Plány faktur na řácích nabídky založené na projektu
description: Tento téma poskytuje informace o vytváření harmonogramů faktur a milníků pro řádky nabídek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 506de5217de48814d6b8f03a10c7c8648c575198
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278275"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Plány faktur na řácích nabídky založené na projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řádek nabídky založený na projektu umožňuje vyjádřit plán faktur. To je během fáze nabídky volitelné, protože aplikace nepodporuje fakturaci projektu, když je vázán na řádek nabídky. Fakturace je povolena až po získání nabídky. Jediným následným dopadem vytvoření plánu faktur během fáze nabídky je, že tento plán faktur je zkopírován do řádku smlouvy na základě projektu. Pokud během fáze nabídky nevytvoříte plán faktur, budete to moci provést na řádku smlouvy založené na projektu.

Celkově je účelem plánů faktur umožnit automatické vytváření návrhů faktur pro řádek smlouvy založené na projektu. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Vytvořte harmonogram faktury za čas a materiál pro řádek nabídky založené na projektu

Když je metodou fakturace pro řádek nabídky na základě projektu Čas a materiál, systém vygeneruje plán faktur na základě data. Chcete-li automaticky vygenerovat plán faktur na základě data, proveďte následující kroky.

1. Přejděte na **Nastavení** > **Frekvence faktur** a nastavte frekvenci faktur.
2. Na stránce **Nabídky** otevřete nabídku projektu a na kartě **Souhrn** nastavte požadované datum dodání.
3. Otevřete řádek nabídky času a materiálu, pro který potřebujete vytvořit harmonogram faktur na základě data. 
4. Na kartě **Časový plán faktur** vyberte hodnoty v polích **Zahájení fakturace** a **Frekvence faktur**. 
5. V podmřížce vyberte **Generovat rozpis faktur**.
6. Aplikace generuje plán faktur s poli **Datum spuštění faktury**, **Mezní datum transakce** a **Stav spuštění** následujícím způsobem:

    - **Datum spuštění faktury** je nastaveno na datum, které je určeno na základě frekvence fakturace.
    - **Mezní datum transakce** je nastaven na den před **Datem spuštění faktury**.
    - **Stav spuštění** je automaticky nastaven na **Nespuštěno**. Když je úloha automatického vytváření faktur spuštěna pro určité datum spuštění faktury, aktualizuje toto pole buď na **Spuštění úspěšné** nebo **Spuštění selhalo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Vytvořte harmonogram faktury za fixní cenu pro řádek nabídky založené na projektu

Když má řádek nabídky na základě projektu metodu fakturace **Ficní**, systém vytvoří plán faktur na základě milníků. Dokončením následujících kroků automaticky vygenerujete tento plán pro fixní sadu milníků, které jsou rovnoměrně rozloženy pro kalendářní období.

1. Přejděte na **Nastavení** > **Frekvence faktur** a nastavte frekvenci faktur.
2. Na stránce **Nabídky** otevřete nabídku projektu a na kartě **Souhrn** nastavte požadované datum dodání.
3. Otevřete řádek nabídky fixní ceny, pro který potřebujete vytvořit milníkový plán. 
4. Na kartě **Časový plán faktur** vyberte hodnoty v polích **Zahájení fakturace** a **Frekvence faktur**. 
5. V podmřížce vyberte **Generovat periodické milníky**.
6. Aplikace generuje plán faktur s názvem milníku, datem a částkou.

    - Název milníku je nastaven na datum, které je určeno na základě frekvence fakturace.
    - Datum milníku je nastaven na datum, které je určeno na základě frekvence fakturace.
    - Částka milníku se vypočítá vydělením částky nabídky na řádku nabídky na základě projektu počtem milníků, jak je diktováno frekvencí a začátkem fakturace a požadovanými termíny dodání.
    - Pokud má řádek nabídky odhadovanou částku daně, je tato hodnota při generování pravidelných milníků rozdělena mezi každý milník rovnoměrně.

### <a name="manually-create-milestones"></a>Ruční vytváření milníků

Milníky fixní ceny lze také generovat ručně, pokud nejsou pravidelně rozděleny. Postup ručního vytváření milníků:

Otevřete řádek nabídky fixní ceny, pro který potřebujete vytvořit milník. Na kartě **Rozpis faktury** vyberte **+ Vytvořit nový milník řádku nabídky** a zadejte požadované informace na základě následující tabulky.

| **Pole** | **Umístění** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- | --- |
| Název milníku | Vytvořit | Název milníku. | To je přeneseno na milník řádku smlouvy projektu a na fakturu |
| Projektový úkol | Vytvořit | Pokud je milník svázán s úkolem projektu, můžete pomocí tohoto odkazu přidat vlastní logiku nastavavení stavu milníku na základě stavu úlohy. | Aplikace nemá žádný následný dopad tohoto odkazu na úkol. |
| Datum milníku | Vytvořit | Nastavte datum, kdy by měl proces automatického vytváření faktur hledat stav tohoto milníku, aby jej mohl zohlednit pro fakturaci. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Stav faktury | Vytvořit | Když je vytvořen milník, je tento stav vždy nastaven na **Není připraveno na fakturaci**. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Částka řádku | Vytvořit | Částka nebo hodnota milníku, která bude zákazníkovi fakturována. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |
| Daň | Vytvořit | Výše daně, která bude použita k milníku. | To je přeneseno na milník řádku smlouvy projektu a na fakturu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]