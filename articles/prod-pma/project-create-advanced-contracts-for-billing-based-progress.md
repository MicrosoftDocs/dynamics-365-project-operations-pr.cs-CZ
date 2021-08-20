---
title: Vytváření rozšířených smluv pro fakturaci na základě pokroku
description: Toto téma vysvětluje, jak vytvořit projektové smlouvy, abyste mohli generovat faktury pro zákazníky na základě procenta z dokončené práce.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 661e8aa0be70e9c8aadcb3a3d9dd6d39d1bcb2fd55d198b3c9af19fc2d0ae9d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000973"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Vytváření rozšířených smluv pro fakturaci na základě pokroku
[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit projektové smlouvy, abyste mohli vytvářet faktury pro zákazníky na základě procenta z dokončené práce. Částky faktury se automaticky počítají pro rozpočtové kategorie práce, které jste pro projekt nastavili. Časování faktur je nastaveno při sjednávání projektové smlouvy se zákazníkem.

Pomocí postupů v tomto tématu můžete nastavit smlouvu, přidružený projekt a pravidla fakturace, která počítají částky faktur pro rozpočtové kategorie práce, které jste pro projekt nastavili.

Poté, co vytvoříte smlouvu a projekt, můžete nastavit podrobnosti projektu. Můžete například definovat aktivity a přiřadit pracovníky k projektu.

## <a name="example"></a>Příklad

Vaše organizace je firma zabývající se vývojem softwaru. Souhlasíte s vytvořením balíčku mzdového účetnictví pro zákazníka s celkovou částkou 20 000 amerických dolarů (USD). Vaše organizace se zavazuje fakturovat zákazníkovi, jakmile dokončíte konkrétní procento projektu. Pro práci nastavíte následující projektové kategorie, abyste je mohli použít v procesu fakturace:

- Poradenství
- Návrh
- Instalace

Nastavíte také pravidla fakturace, která automaticky vypočítají částky faktury pro procento projektové práce dokončené v každé kategorii.

Manažer rozpočtu vytvoří rozpočet pro kategorie projektů. Množství dokončené práce se automaticky vypočítá jako procento skutečné práce ve srovnání s částkami rozpočtu.

## <a name="prerequisites"></a>Požadavky

Před vytvořením projektu, který používá pravidla fakturace, musíte nastavit číselné řady pro pravidla fakturace a deník poplatků, který se používá k zaúčtování fakturace průběhu.

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.
2. Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Číselné řady** nastavte číselnou posloupnost, kterou chcete použít při vytváření pravidel fakturace.
3. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Deníky** \> **Poplatek**.
4. Na stránce **Deník poplatků** vyberte **Nový** a zadejte název deníku.

## <a name="create-a-contract-for-progress-billings"></a>Vytvoření smlouvy pro fakturaci průběhu

Tento postup využijte k vytvoření projektové smlouvy pro projekt s pevnou cenou. Projektovou fakturu vytvoříte, když práce dokončená na projektu dosáhne stanoveného procenta.

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Projektové smlouvy**.
2. Na stránce **Projektové smlouvy** vyberte **Nové**.
3. V dialogovém okně **Nová projektová smlouva** nastavte následující pole:

    - **Jméno**
    - **Typ financování**
    - **Zdroj financování**
    - **Prodejní měna** – Ve výchozím nastavení se tato měna používá ve fakturách zákazníků spojených s projektovou smlouvou. Prodejní měnu však můžete na konkrétní faktuře zákazníka změnit.

4. Vyberte **OK**. Informace se zkopírují do záhlaví stránky **Projektové smlouvy**.
5. Na stránce **Projektové smlouvy** vyplňte zbývající požadované informace o projektu.

## <a name="create-a-project-for-progress-billings"></a>Vytvoření projektu pro fakturaci průběhu

Tento postup využijte k vytvoření projektu a všech dílčích projektů, které jsou spojeny s projektovou smlouvou.

1. Přejděte do části **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty**.
2. Na stránce **Všechny projekty** vyberte příkaz **Nový**.
3. V dialogovém okně **Nový projekt** vyberte v poli **Typ projektu** hodnotu **Čas a materiál**.
4. Vyberte skupinu projektu. Skupina projektu definuje informace o účtování pro projekty, které jsou skupině přiřazeny.
5. Vyberte příkaz **Vytvořit projekt**.
6. Po vytvoření projektu nastavte fázi projektu na **Probíhá**.

## <a name="create-a-budget-for-a-project"></a>Vytvoření rozpočtu pro projekt

Rozpočtové kategorie se používají k automatickému výpočtu částek faktury pro procento práce dokončené v každé kategorii. Pomocí následujícího postupu vytvořte rozpočtové kategorie pro odhadované náklady.

1. Přejděte do části **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty**.
2. Na stránce **Všechny projekty** vyberte a otevřete požadovaný projekt.
3. Na stránce **Projekty** v podokně akcí na kartě **Plán** vyberte ve skupině **Rozpočet** hodnotu **Rozpočet projektu**.
4. Na stránce **Rozpočet projektu** zadejte odhadované náklady pro každou kategorii v projektu.

## <a name="create-billing-rules-for-progress-billings"></a>Vytvořte pravidla fakturace pro fakturaci průběhu

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Projektové smlouvy**.
2. Na stránce **Projektové smlouvy** vyberte a otevřete projektovou smlouvu.
3. Na stránce projektové smlouvy vyberte na pevné záložce **Pravidla fakturace** příkaz **Přidat**.
4. Na stránce **Pravidlo fakturace** vyberte v poli **Typ řádku** hodnotu **Průběh**.
5. Na pevné záložce **Podrobnosti řádku pravidla účtování** v poli **Hodnota smlouvy** zadejte celkovou hodnotu smlouvy.
6. V poli **Kategorie** vyberte kategorii, do které chcete zaúčtovat transakci poplatku.
7. V poli **Projekt** vyberte projekt, který používá toto fakturační pravidlo.
8. Volitelné: Přiřaďte pravidlo fakturace k dalším projektům. Na pevné záložce **Projekt** v části **Dostupné projekty** vyberte projekt a poté kliknutím na tlačítko se šipkou doprava přidejte projekt do části **Vybrané projekty**.
9. Volitelné: Vypočítejte procentní částku, kterou zákazník zadrží z plateb na faktuře. Na pevné záložce **Podmínky zadržení platby** vyberte zdroj financování a poté v poli **Procento zádržného** zadejte procento zádržného.
10. Opakováním těchto kroků vytvoříte další fakturační pravidla pro projektovou smlouvu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]