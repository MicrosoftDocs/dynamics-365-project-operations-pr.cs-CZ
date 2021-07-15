---
title: Konfigurace neskladovaných materiálů a nevyřízené faktury dodavatele
description: Tento téma vysvětluje, jak povolit neskladované materiály a nevyřízené faktury dodavatele.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 41191384c688c3b77d08a0e7990ddf0d9a48545c
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293039"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurace neskladovaných materiálů a nevyřízené faktury dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

## <a name="minimum-version-requirement"></a>Minimální požadovaná verze

Používání neskladovaných materiálů a nevyřízené faktury dodavatele pro scénáře Dynamics 365 Project Operations založené na položkách, které nejsou na skladě / na zdrojích, vyžadují následující verze:

Řešení Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 nebo vyšší
- Řešení orchestrace aplikací pro duální zápis – 2.2.2.23 nebo vyšší

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) nebo vyšší. Ujistěte se, že je vaše prostředí Finance aktuální a všechny aktualizace kvality jsou použity, aby splňovaly minimální požadavky na verzi.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Spusťte mapy duálního zápisu pro skladové materiály a integraci faktur dodavatele

Tato část poskytuje informace o konkrétních mapách požadovaných pro neskladované materiály a faktury dodavatele. Ověřte, zda jsou nezbytné mapy uvedené v tématu [Zřízení nového prostředí](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) spuštěné ve vašem prostředí.

1. Přejděte na Lifecycle Services (LCS), přejděte na svůj projekt LCS a přejděte na stránku **Podrobnosti o prostředí**.
2. V části **Informace o prostředí Common Data Service** vyberte **Odkaz na CDS pro aplikace**. Poté, co vyberete odkaz, budete přesměrováni na seznam entit v mapováních.
3. Ujistěte se, že jsou spuštěny následující mapy. Pokud neběží, spusťte je a nezapomeňte zahrnout všechny související tabulkové mapové.

    - Odlišné produkty vydané CDS (produkty)
    - Dodavatelé v2 (msdyn_vendors)
    - Tabulka Project Operations pro odhady materiálu (msdyn_estimatelines)
    - Entita exportu faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoices)
    - Entita exportu řádku faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoicelines)
    - Skutečné hodnoty integrace Project Operations (msdyn_actuals). Ujistěte se, že používáte verzi mapy 1.0.0.14 nebo vyšší. Aktivní verzi mapy můžete vidět ve sloupci **Verze** na stránce **Duální zápis**. Novou verzi mapy můžete aktivovat výběrem **Verze tabulky mapy** a poté uložením vybrané verze.

Pokud používáte standardní demo data, možná budete muset zastavit a restartovat následující mapy entit s počáteční synchronizací:
  - Platební dny CDS V2 (msdyn_paymentdays)
  - Časový plán plateb (msdyn_paymentschedules)
  - Platební podmínky (msdyn_paymentterms)
  - Skupiny dodavatelů (msdyn_vendorgroups)
  - Jednotky (uom)

> [!NOTE]
> Počáteční synchronizace pro skupiny a jednotky dodavatelů může selhat u několika záznamů ve stávající ukázkové datové sadě. Selhání můžete ignorovat, protože vám nebudou bránit v používání ukázkových dat s Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurace předpokladů v Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivujte pracovní postup a vytvářejte účty založené na entitě dodavatele

Řešení orchestrace duálního zápisu poskytuje [hlavní integraci dodavatelů](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Jako předpoklad pro tuto funkci musí být data dodavatele vytvořena v entitě **Účty**. Aktivujte proces pracovního postupu šablony a vytvořte dodavatele v tabulce **Účty**, jak je popsáno v [přepínání mezi návrhy prodejců](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Nastavení produktů, které mají být vytvořeny jako aktivní

Neskladované materiály musí být nakonfigurovány jako **Vydané produkty** ve Finance. Řešení orchestrace duálního zápisu poskytuje připravenou [integraci vydaných produktů do produktového katalogu Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Ve výchozím nastavení jsou produkty z Finance synchronizovány do Dataverse ve stavu konceptu. Chcete-li produkt synchronizovat do aktivního stavu, aby jej bylo možné přímo použít v dokumentech o použití materiálu nebo nevyřízených fakturách dodavatele, přejděte na **Systém** > **Správa** > **Správa systému** > **Nastavení systému** a na kartě **Prodej** nastavte **Vytvářet produkty v aktivním stavu** na **Ano**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurace předpokladů ve Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Aktivace klíče funkce pro nevyřízené faktury dodavatele

Chcete-li povolit funkčnost přidání podrobností projektu na řádky faktury čekající na dodavatele, proveďte následující kroky.

1. Ve Finance přejděte na pracovní prostor **Správa funkcí**.
2. V seznamu funkcí vyhledejte **Aktivovat nevyřízené faktury dodavatele v Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě**, a vyberte **Aktivovat**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definice skupin kategorií a kategorií projektů pro položky

Nakonfigurujte alespoň jednu skupinu kategorií pro typ transakce **Položka** a alespoň jednu kategorie projektu využívající tuto skupinu. Další informace viz [Konfigurace kategorií projektu](../project-accounting/configure-project-categories.md#category-groups).

Zkontrolujte profily nákladů a výnosů projektu a nakonfigurujte nastavení účtování hlavní knihy pro transakce položek. Další informace viz [Konfigurace účtování pro fakturovatelné projekty](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Nastavení produktu nezahrnutého do katalogu

V Project Operations můžete zaznamenávat odhady materiálu a využití pro katalogové produkty, které jsou konfigurovány ve vydaném katalogu produktů, a pro produkty pro zápis. Používání produktů pro zápis vyžaduje jeden vydaný produkt, který je pro tento účel nakonfigurován ve službě Finance. Chcete-li nakonfigurovat produkt pro zápis, proveďte následující kroky. Opakujte tyto kroky v každé právnické osobě, která používá Project Operations pro scénáře prostředků / zdrojů, které nejsou na skladě.

1. Ve Finance přejděte na **Správa informací o produktu** > **Produkty** > **Vydané produkty** a vyberte **Nový**.
2. V poli **Typ produktu** vyberte **Položka** a v **Podtyp produktu** vyberte **Produkt**.
3. Zadejte číslo produktu (WRITEIN) a název produktu (produkt pro zápis).
4. Vyberte skupinu modelů položek. Ujistěte se, že vybraná skupina modelů položek má pole **Inventarizační zásady skladového produktu** nastaveno na **False**.
5. Vyberte hodnoty v polích **Skupina položek**, **Skupina dimenzí úložiště** a **Sledování skupiny dimenzí**. Použijte **Dimenze úložiště** pouze pro **Web** a v poli **Sledování dimenzí** vyberte **Žádné**.
6. Vyberte hodnoty v poli **Inventarizační jednotka**, **Nákupní jednotka** a **Prodejní jednotka** a poté uložte provedené změny.
7. Na kartě **Plán** nastavte výchozí nastavení pořadí a na kartě **Sklad** nastavte výchozí místo a sklad.
8. Přejděte na **Řízení projektů a účetnictví** > **Nastavit** > **Parametry řízení projektu a účetnictví** a otevřete **Project Operations na Dynamics 365 Dataverse**. 
9. Na kartě **Materiály** v poli **Produkt pro zápis** vyberte produkt, který jste vytvořili.
10. Ve prostředí Dataverse, v mapě webu otevřete entitu **Produkty** a najděte záznam produktu pro zápis. 
11. Otevřete podrobnosti záznamu a nastavte stav produktu na **Vyřazený**. Tento stav produktu brání komukoli v náhodném použití tohoto záznamu přímo v odhadech materiálu a dokumentech o použití.

### <a name="set-up-a-procurement-integration-account"></a>Nastavení účtu integrace nákupu

Účet integrace nákupu se používá jako zúčtovací účet při zaúčtování nevyřízené faktury dodavatele s řádky přiřazenými k projektu.

Když systém zaúčtuje nevyřízenou fakturu dodavatele, použije se tento účet pro částku nákladů projektu. Fakturační údaje dodavatele jsou zpracovány v Dataverse a vytvoří se odpovídající skutečná hodnota projektu. Informace ze skutečné hodnoty projektu se přidají do deníku integrace Project Operations. Když zaúčtujete deník integrace, částka se vymaže z účtu integrace nákupu a zaznamená se do nákladů projektu.

1. Chcete-li nastavit účet integrace zásobování, přejděte na **Řízení projektů a účetnictví** > **Nastavit** > **Parametry řízení projektu a účetnictví** a otevřete **Project Operations na Dynamics 365 Dataverse**. 
2. Vyberte kartu **Materiály** a vyberte hodnotu v poli **Účet integrace nákupu**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Nastavte výchozí hodnoty kategorie projektu pro položku

1. Ve Finance přejděte na **Řízení projektů a účetnictví** > **Nastavit** > **Parametry řízení projektu a účetnictví** a otevřete **Project Operations na Dynamics 365 Dataverse**. 
2. Na kartě **Výchozí hodnoty kategorie projektu** v poli **Položka** vyberte hodnotu. Tato kategorie projektu se používá pro významné transakce, pokud kategorie projektu nebyla nastavena v záznamu skutečných hodnot projektu.
