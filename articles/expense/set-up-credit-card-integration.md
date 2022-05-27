---
title: Nastavení integrace kreditní karty
description: Tento téma vysvětluje, jak pracovat s transakcemi kreditních karet, které souvisejí s výdaji.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c9d993f1999b0be24794bbe828afa8eb74744e9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577045"
---
# <a name="set-up-credit-card-integration"></a>Nastavení integrace kreditní karty

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Transakce kreditních karet související s výdaji lze nastavit tak, aby se automaticky importovaly podle opakujícího se plánu. Alternativně lze transakce podle potřeby importovat ručně. Transakce kreditní kartou se importují prostřednictvím datové entity transakcí kreditní kartou.

## <a name="import-credit-card-transactions"></a>Import transakcí kreditní kartou

Chcete-li importovat transakce kreditní kartou, postupujte takto:

1. Na stránce **Transakce kreditní kartou** vyberte **Importovat transakce**. Pokud otevíráte správu dat poprvé, musí systém aktualizovat seznam datových entit, než budete moci pokračovat.
2. V poli **Název** zadejte jedinečný popis úlohy importu.
3. V poli **Formát zdrojových dat** vyberte formát souboru k importu, který obsahuje transakce kreditní kartou.
4. Vyberte **Odeslat** a poté vyhledejte a vyberte soubor, který chcete importovat.
5. Po odeslání souboru ověřte mapování souboru transakcí kreditní karty a sloupců datové entity transakce kreditní karty výběrem odkazu na dlaždici **Zobrazit mapu**. Pokud existují chyby mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo **Podrobnosti mapování**.
6. Chcete-li automatizovat transakce kreditní kartou, vyberte **Vytvořit opakující se datovou úlohu**. Poté můžete nastavit opakování, které definuje, jak často se mají transakce kreditní kartou importovat. Jakmile budete hotovi, zvolte **OK**.
7. Chcete-li nyní importovat vybraný soubor, vyberte **Importovat**.
8. Pokud se během importu vyskytnou chyby, můžete si prohlédnout protokol provádění nebo pracovní data, ve kterých najdete chyby, které musíte opravit, abyste zajistili úspěšný import.

> [!NOTE]
> Pokud potřebujete importovat více než jeden formát souboru, musíte pro každý typ formátu vytvořit samostatné úlohy importu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Změna přiřazení transakcí kreditní kartou pro ukončené zaměstnance

Po ukončení záznamu zaměstnance je účet zaměstnance služby Active Directory Domain Services (AD DS) deaktivován. Mohou však existovat aktivní transakce kreditních karet, které je třeba stále proplatit a uhradit. Na stránce **Transakce kreditní kartou** můžete znovu přiřadit zaměstnance u jakékoli transakce kreditní kartou, kde byl přidružený zaměstnanec ukončen.

Vyberte jednu nebo více transakcí kreditní kartou a poté vyberte **Znovu přiřadit transakce**. Poté můžete vybrat dalšího zaměstnance, kterému chcete přiřadit transakce kreditní kartou. Poté, co byly transakce s kreditními kartami znovu přiřazeny, mohou být vybrány pro výkazy výdajů a zaplaceny obvyklým postupem pro refundaci výkazu výdajů.

## <a name="delete-credit-card-transactions"></a>Odstranění transakcí kreditní kartou 

Někdy po importu transakcí kreditní kartou může být nutné některé transakce odstranit. Může to být způsobeno tím, že transakce jsou duplicitní nebo protože data nejsou přesná. Správci mohou použít funkci **„Odstranění transakcí kreditní kartou“** k výběru a odstranění transakcí kreditní karty, které **nejsou připojeny** k sestavě výdajů. 

1. Přejděte do nabídky **Pravidelné úkoly** > **Odstranit transakce kreditní kartou**.
2. Vyberte **Filtr** a zadejte informace identifikující záznamy, které mají být odstraněny.
3. Výběrem tlačítka **OK** záznamy odstraníte. 

## <a name="storing-credit-card-numbers"></a>Ukládání čísel platebních karet

Pro uložení čísel kreditních karet jsou k dispozici tři možnosti. Čísla kreditních karet jsou uložena na stránce **Parametry správy výdajů**.

- **Zabránit zadání čísla karty** – Čísla kreditních karet se neukládají.
- **Hash čísla karty (uložit poslední 4 číslice)** – Poslední čtyři číslice čísel kreditních karet jsou uloženy v šifrovaném formátu.
- **Uložit čísla karet** – Čísla kreditních karet jsou uložena v nešifrovaném formátu. Tato možnost není v souladu se standardem zabezpečení dat (DSS) odvětví platebních karet (PCI). Aby organizace dodržovala předpisy PCI DSS, měli by správci organizací rozhodnout buď čísla kreditních karet neukládat, nebo ukládat jen hashe čísel.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
