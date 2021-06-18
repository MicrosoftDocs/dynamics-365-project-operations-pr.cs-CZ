---
title: Denní diety
description: Tento téma poskytuje informace o pravidlech pro denní diety, které se používají ve správě výdajů.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995253"
---
# <a name="per-diems"></a>Denní diety

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Denní dieta je příspěvek vyplácený pracovníkovi, který cestuje za prací. Ve správě výdajů můžete vytvořit pravidla pro denní diety určené pro různé cestovní situace. Sazby denních diet mohou být založeny na ročním období, místě cesty nebo na obou kritériích. Když vytvoříte pravidlo denní diety, můžete určit, že určité procento sazby diety bude zadrženo, pokud pracovník obdrží bezplatné jídlo nebo služby. Můžete také nastavit minimální a maximální počet hodin, které musí cesta pracovníka trvat, aby byla sazba denní diety použita.

## <a name="configuration"></a>Konfigurace 

1. Chcete-li přidat místa vyplácení denních diet, přejděte na nabídku **Nastavit** > **Výpočty a kódy** > **Umístění denních diet**.
2. Pro každé z výše přidaných umístění vyberte sazbu denní diety a měnu, která je platná mezi konkrétním počátečním a konečným datem pro hotel, stravování a další výdaje. Sazby a měny diet se konfigurují v nabídce **Nastavit** > **Výpočty a kódy** > **Denní diety**.
3. Na stránce **Umístění denních diet** konfigurujte úrovně sazeb denních diet. Úrovně sazeb denních diet vám umožňují definovat procentuální rozdělení denního příspěvku na hotel, stravu a další výdaje. 
4. Chcete-li určit procentuální snížení sazby pro snídani, oběd nebo večeři, aktualizujte pole na stránce **Parametry správy výdajů** na kartě **Denní diety**. 
    
## <a name="submit-expenses-using-per-diem"></a>Odesílání výdajů na denní diety
Chcete-li odeslat výdaje s využitím denních diet, použijte při vytváření sestavy výdajů kategorie výdajů **Denní diety**. Zadejte hodnoty **Denní diety od data**, **Denní diety do data** a **Umístění denních diet**. Částka bude vypočítána na základě sazeb denních diet pro vybrané místo a redukce diety za jídlo bude vypočítána na základě úrovní sazeb denních diet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]