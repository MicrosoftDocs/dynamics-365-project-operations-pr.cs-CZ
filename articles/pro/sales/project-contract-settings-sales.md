---
title: Nastavení projektové smlouvy – omezené
description: Tento článek poskytuje informace o polích, která ovlivňují řádky smlouvy, a informace o smlouvě, které jsou shrnuty za všechny řádkové položky.
author: rumant
ms.date: 03/08/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6123cbc028cf49cc198173697969f415b0789256
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917062"
---
# <a name="header-details-for-project-contracts"></a>Podrobnosti záhlaví pro projektové smlouvy

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek poskytuje informace o polích, která se vztahují na celou projektovou smlouvu, včetně nastavení, která ovlivňují všechny řádky smlouvy. Zahrnuty jsou také informace o smlouvě, které jsou shrnuty za všechny řádkové položky za účelem zvýšení KPI projektové smlouvy.

V následující tabulce jsou uvedena pole na kontraktu projektu, která jsou jedinečná pro Dynamics 365 Project Operations nebo mají některé důležité změny v chování z prodejních objednávek v Dynamics 365 Sales.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Typ | Karta **Souhrn** (skrytá) | Toto pole sady možností obsahuje následující možnosti:</br>- **Na základě práce** (k dispozici pouze v případě, že je nainstalována aplikace Project Operations)</br>- **Na základě zboží** (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Sales)</br>- **Na základě servisní údržby** (k dispozici, když je nainstalována služba Dynamics 365 Field Service) | V Project Operations je hodnota tohoto pole implicitně nastavena na hodnotu **Na základě práce** a klasifikuje smlouvu jako založenou na projektu. Smlouva by měla být založená na projektu, aby povolila všechna rozšíření a funkce specifické pro projekt. |
| Potenciální zákazník | Karta **Souhrn** | Odkaz na záznam společnosti nebo účtu zákazníka. Když je smlouva vytvořena z nabídky, zkopíruje se toto pole z odpovídajícího pole záznamu nabídky. | Měna v projektové smlouvě má výchozí hodnotu na základě měny zákazníka. Toto však lze změnit před uložením smlouvy. |
| Manažer obchodních vztahů | Karta **Souhrn** | Jméno manažera obchodních vztahů pro tento obchod. Když je smlouva vytvořena z nabídky, zkopíruje se toto pole z odpovídajícího pole záznamu nabídky. | Manažer obchodních vztahů je zodpovědný za řízení vztahu se zákazníkem až do dokončení projektu. Výchozí hodnoty smluvní jednotky u projektové smlouvy jsou nastaveny na základě záznamu rezervovatelného zdroje svázaného s manažerem obchodních vztahů. |
| Smluvní jednotka | Karta **Souhrn** | Organizační jednotka, která je odpovědná za realizaci projektů asociovaných s touto smlouvou. Když je smlouva vytvořena z nabídky, zkopíruje se toto pole z odpovídajícího pole záznamu nabídky. | Smluvní jednotka je divize společnosti, která realizuje projekty. Každá smluvní jednotka má měnu a tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během projektu. |
| Ceník produktů | Karta **Souhrn** | Tento ceník se používá pro určení výchozích cen v řádcích smluv založených na produktu. Rozevírací seznam možností pro toto pole zobrazuje seznam ceníků, kde měna ceníku odpovídá měně smlouvy. Když je smlouva vytvořena z nabídky, zkopíruje se toto pole z odpovídajícího pole záznamu nabídky. Toto pole v projektové smlouvě má výchozí hodnotu načtenou ze záznamu účtu, ale lze ji změnit. | Toto pole nijak neovlivňuje další proces. |
| Měna | Karta **Souhrn** | Měna použitá k nahlášení hodnoty tohoto obchodu a měna, ve které bude zákazníkovi fakturováno. Když je smlouva vytvořena z nabídky, zkopíruje se toto pole z odpovídajícího pole záznamu nabídky. Toto pole v projektové smlouvě má výchozí hodnotu načtenou ze záznamu účtu, ale lze ji změnit. | Po uložení smlouvy již toto pole nelze upravovat. Toto pole se používá k určení výchozích hodnot ceníků produktů a projektů ve smlouvě. Měna použitá ve smlouvě se musí shodovat s měnou ceníku. |
| Nepřekročitelný limit | Karta **Souhrn** | Toto pole označuje vyjednanou horní mez konečné hodnoty, se kterou zákazník u tohoto obchodu souhlasil. | Horní mez se vyhodnocuje během provádění a je použitelná ve všech řádkových položkách a projektech přidružených k tomuto obchodu. |
| Požadované datum dodávky | Karta **Souhrn** | Když je smlouva vytvořena z projektové nabídky, zkopíruje se toto pole z odpovídajícího pole záznamu projektové nabídky. | Toto datum se používá jako konečné datum pro generování rozpisů faktur. |

Na kartě **Plnění smlouvy** projektové smlouvy jsou k dispozici následující KPI. 

>[!NOTE]
>Všechny částky na kartě **Plnění smlouvy** jsou vyjádřeny ve výchozí měně prostředí.

| Pole | Umístění | Description |
| --- | --- | --- |
| Hodnota smlouvy | Souhrnná smlouva | Celková hodnota projektové smlouvy.|
| Fakturovaná částka | Souhrnná smlouva | Součet částek na všech fakturách uplatněných vůči této smlouvě.|
| Vzniklé náklady | Souhrnná smlouva | Součet všech skutečných nákladů zaznamenaných u všech projektů, které jsou mapovány na smlouvu. |
| Hrubá marže | Souhrnná smlouva | Fakturovaná částka - Náklady vzniklé do data / Fakturovaná částka |
| Očekávaná marže | Souhrnná smlouva | (Hodnota smlouvy - Odhadované náklady) / Hodnota smlouvy Odhadované náklady = součet všech odhadovaných nákladů u všech projektů mapovaných na smlouvu.|
| Hodnota smlouvy | Řádky založené na projektech | Hodnota řádku smlouvy. |
| Fakturovaná částka | Řádky založené na projektech | U řádku smlouvy s pevnou cenou: Součet částek všech skutečných milníků fakturovaných prodejů oproti tomuto řádku smlouvy na různých fakturách vytvořených pro tuto smlouvu. U řádku smlouvy o čase a materiálu: Součet částek všech skutečných účtovatelných fakturovaných prodejů oproti tomuto řádku smlouvy na různých fakturách vytvořených pro tuto smlouvu. |
| Vzniklé náklady | Řádky založené na projektech | Součet všech skutečných nákladů zaznamenaných u všech projektů, které jsou mapovány na řádek smlouvy. |
| Hrubá marže | Řádky založené na projektech | (Fakturovaná částka - Náklady vzniklé do data) / Fakturovaná částka |
| Očekávaná marže | Řádky založené na projektech | (Částka řádku smlouvy v základní měně - Odhadované náklady pro řádek smlouvy v základní měně) / Částka řádku smlouvy v základní měně |
| Vzniklé náklady | Detail řádku založeného na projektu | Čas: Součet částek skutečných časových nákladů zaznamenaných pro tuto roli v projektu, která je mapována na řádek smlouvy. Výdaje: Součet částek všech skutečných výdajových nákladů zaznamenaných pro tuto kategorii v projektu, která je mapována na řádek smlouvy. |
| Zaznamenané množství | Detail řádku založeného na projektu | Čas: Množství skutečných časových nákladů pro roli v projektu, která je mapována na tento řádek smlouvy. Výdaje: Všechna množství pro tuto kategorii výdajů u skutečných výdajových nákladů projektu, která je mapována na tento řádek smlouvy. |
| Fakturovaná částka | Detail řádku založeného na projektu | U řádku smlouvy s pevnou cenou je toto pole ponecháno na úrovni podrobností prázdné a zobrazuje se pouze na úrovni řádku smlouvy. U řádku smlouvy o čase a materiálu jsou výpočty dokončeny na úrovni podrobností. Podrobnosti zobrazují součet částky na všech řádcích fakturovaných výnosů oproti tomuto řádku smlouvy, které jsou účtovatelné. |
| Fakturované množství | Detail řádku založeného na projektu | U řádku smlouvy s pevnou cenou je toto pole ponecháno na úrovni podrobností prázdné a zobrazuje se pouze na úrovni řádku smlouvy. U řádku smlouvy o čase a materiálu jsou výpočty dokončeny na úrovni podrobností pro čas a výdaje. Čas: Součet hodin na všech řádcích fakturovaných výnosů pro tuto roli oproti tomuto řádku smlouvy, které jsou účtovatelné. Výdaje: Všechna množství pro tuto kategorii výdajů u skutečných výdajových nákladů projektu, která je mapována na tento řádek smlouvy. |
| Hodnota smlouvy | Řádky založené na produktech | Hodnota řádku smlouvy tohoto řádku smlouvy založeného na produktu. |
| Fakturovaná částka | Řádky založené na produktech | Součet částek na všech řádcích faktur oproti tomuto řádku smlouvy založenému na produktu v různých fakturách, které jsou vytvořeny pro tuto smlouvu. |
| Vzniklé náklady | Řádky založené na produktech | Součet všech skutečných nákladů zaznamenaných pro řádek smlouvy založený na produktu. |
| Hrubá marže | Řádky založené na projektech | Fakturovaná částka - Náklady vzniklé do data / Fakturovaná částka |
| Očekávaná marže | Řádky založené na produktech | (Hodnota řádku smlouvy - Odhadované náklady na řádek smlouvy) / Hodnota řádku smlouvy |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
