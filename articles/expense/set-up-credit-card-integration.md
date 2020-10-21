---
title: Nastavení integrace kreditní karty
description: Toto téma vysvětluje, jak importovat a udržovat transakce kreditních karet související s výdaji.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896813"
---
# <a name="set-up-credit-card-integration"></a>Nastavení integrace kreditní karty

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Transakce kreditních karet související s výdaji lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu. Alternativně lze transakce podle potřeby importovat ručně. Transakce kreditní kartou se importují prostřednictvím datové entity transakce kreditní kartou.

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
