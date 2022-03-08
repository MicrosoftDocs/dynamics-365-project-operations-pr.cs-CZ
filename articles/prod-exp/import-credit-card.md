---
title: Import a údržba transakcí kreditní kartou
description: Toto téma vysvětluje, jak importovat a udržovat transakce kreditních karet související s výdaji. Tyto transakce lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu, nebo je lze podle potřeby ručně importovat.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995843"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Import a údržba transakcí kreditní kartou

Transakce kreditních karet související s výdaji lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu. Alternativně lze transakce podle potřeby importovat ručně. Transakce kreditní kartou se importují prostřednictvím datové entity transakce kreditní kartou.

Další informace o datových entitách najdete v tématu [Datové entity ](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Import transakcí kreditní kartou

1. Na stránce **Transakce kreditní kartou** vyberte **Importovat transakce**. Pokud otevíráte správu dat poprvé, musí systém aktualizovat seznam datových entit, než budete moci pokračovat.
2. Do pole **Název** zadejte jedinečný popis úlohy importu.
3. V poli **Formát zdrojových dat** vyberte formát souboru k importu, který obsahuje transakce kreditní kartou.
4. Vyberte **Odeslat** a poté vyhledejte a vyberte soubor, který chcete importovat.
5. Po odeslání souboru ověřte mapování souboru transakcí kreditní karty a sloupců datové entity transakce kreditní karty výběrem odkazu na dlaždici **Zobrazit mapu**. Pokud existují chyby mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo **Podrobnosti mapování**.
6. Chcete-li automatizovat transakce kreditní kartou, vyberte **Vytvořit opakující se datovou úlohu**. Poté můžete nastavit opakování, které definuje, jak často se mají transakce kreditní kartou importovat. Jakmile budete hotovi, zvolte **OK**.
7. Chcete-li nyní importovat vybraný soubor, vyberte **Importovat**.
8. Pokud se během importu vyskytnou chyby, můžete si prohlédnout protokol provádění nebo pracovní data a zobrazit chyby, které musíte opravit, abyste mohli zaručit úspěšný import.

> [!NOTE]
> Pokud musíte importovat více než jeden formát souboru, musíte vytvořit samostatné úlohy importu pro každý typ formátu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Změna přiřazení transakcí kreditní kartou pro ukončené zaměstnance

Po ukončení záznamu zaměstnance je účet zaměstnance služby Active Directory Domain Services (AD DS) deaktivován. Mohou však existovat aktivní transakce kreditních karet, které je třeba stále proplatit a uhradit. Ze stránky **Transakce kreditní kartou** můžete zaměstnanci znovu přiřadit jakékoli transakce kreditní kartou, kde byl přidružený zaměstnanec ukončen.

Vyberte jednu nebo více transakcí kreditní kartou a poté vyberte **Znovu přiřadit transakce**. Poté můžete vybrat dalšího zaměstnance, kterému chcete přiřadit transakce kreditní kartou. Poté, co byly transakce s kreditními kartami znovu přiřazeny, mohou být vybrány pro výkazy výdajů a zaplaceny obvyklým postupem pro refundaci výkazu výdajů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]