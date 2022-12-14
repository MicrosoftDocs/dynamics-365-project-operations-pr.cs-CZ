---
title: Správa více zákazníků v projektových smlouvách
description: Tento článek poskytuje informace o správě více zákazníků v řádcích projektových smluv.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 001c3c822a5d1cef6bd85164ef5e63e81719dafb
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824522"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Správa více zákazníků v projektových smlouvách

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Projektové smlouvy v Dynamics 365 Project Operations podporují situace, kdy smluvní smlouva zahrnuje více zákazníků, kteří financují obchod. Karta **Souhrn** na stránce **Projektová smlouva** obsahuje pole **Zákazník**. Toto pole identifikuje primárního zákazníka obchodu. Další zákazníky pro obchod lze nastavit na kartě **Zákazníci** na stránce **Projektová smlouva**.

Všichni smluvní zákazníci uvedení na projektové smlouvě se automaticky stanou zákazníky na všech nových řádcích smlouvy na základě projektu vytvořených pro projektovou smlouvu. Stávající řádky smlouvy na základě projektu nezdědí nové zákazníky kontraktů při vytváření nových záznamů.

Řádky smlouvy na základě produktu jsou automaticky přidruženy k primárnímu zákazníkovi.

Smluvní zákazníci a zákazníci na řádku smlouvy lze přidávat, aktualizovat nebo odstranit kdykoli před získáním smlouvy.

## <a name="primary-customer"></a>Primární zákazník

Zákazník uvedený na kartě **Souhrn** projektové smlouvy, protože potenciální zákazník je primárním zákazníkem smlouvy. Při pokusu o odstranění primárního zákazníka ze seznamu zákazníků ve smlouvě se zobrazí chybová zpráva, že záznam primárního zákazníka ve smlouvě nelze odstranit.

Primárního zákazníka nelze aktualizovat ze seznamu smluvních zákazníků. Místo toho změňte potenciálního zákazníka na kartě **Souhrn** smlouvy. Když je toto pole aktualizováno na stránce **Souhrn smlouvy**, nový zákazník je přidán přidá jako nový smluvní zákazník s nastaveným příznakem **Primární**. Předchozí primární zákazník bude i nadále zákazníkem smlouvy.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka smlouvy

Smluvní zákazník může být vytvořen, aktualizován nebo odstraněn z kary **Zákazníci** na stránce **Projektová smlouva**. Pole v následující tabulce jsou v záznamu zákazníka projektové smlouvy a měli byste je mít na paměti, když se smlouvou pracujete.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| **Obchodní vztah** | Mřížku lze upravit na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Vypíše seznam všech aktivních účtů. Po vytvoření záznamu je toto pole uzamčeno. Chcete-li aktualizovat obchodní vztah, odstraňte záznam a znovu jej vytvořte. Pokud jste zaznamenali nějaké skutečné hodnoty, nebo pokud je záznam smluvního zákazníka primárním zákazníkem, nemůžete záznam odstranit. | Smluvní zákazníci se při vytvoření řádku smlouvy zkopírují jako zákazníci na řádku smlouvy. |
| **Procento rozdělení fakturace** | Mřížku lze upravit na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Představuje procento každé nefakturované prodejní transakce, která je připsána tomuto smluvnímu zákazníkovi. | Zkopírováno na nové řádky smlouvy a do zákazníků na řádcích projektové smlouvy na nových řádcích projektové smlouvy. |
| **Fakturační adresa – jméno kontaktu** | Mřížku lze upravit na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Toto textové pole by se mělo použít k identifikaci kontaktní osoby faktury pro tohoto zákazníka. Toto pole získá hodnotu ze souvisejícího záznamu obchodního vztahu. | Zkopírováno do pole **Fakturační adresa – název smlouvy** na faktuře, která je generována pro tohoto zákazníka. |
| **Fakturační adresa – jméno** | Mřížku lze upravit na kartě **Smluvní zákazníci** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro smluvního zákazníka. | Toto textové pole by se mělo použít k identifikaci kontaktní osoby faktury pro tohoto zákazníka. Toto pole získá hodnotu ze souvisejícího záznamu obchodního vztahu. | Zkopírováno do pole **Fakturační adresa – název smlouvy** na faktuře, která je generována pro tohoto zákazníka. |
| **Platební podmínky** | Mřížku lze upravit na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Hodnoty jsou získány ze souvisejícího záznamu obchodního vztahu. | Zkopírováno do pole **Fakturační adresa – název smlouvy** na faktuře, která je generována pro tohoto zákazníka. |
| **Je zaokrouhlení** | Mřížku lze upravit na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Označuje, zda je tento zákazník výchozím zaokrouhlovacím zákazníkem pro tento obchod. Na projektové smlouvě může být pouze jeden zákazník pro zaokrouhlování. | Když rozdělení nákladů a nefakturovaných prodejů pro množství způsobí rozdíly v zaokrouhlení, použije se tento rozdíl na skutečnou hodnotu, která je mapována na tohoto zákazníka. |
| **Nepřekročitelný limit** | Mřížku lze upravit na kartě **Smluvní zákazníci** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro smluvního zákazníka. | Určuje, zda existuje sjednaný limit nebo strop celkové částky na řádku smlouvy, která bude v tomto případě fakturována zákazníkovi. | **Nepřekročitelný limit** nastavený na úrovni smluvního zákazníka bude vyhodnocen pomocí **Nefakturovaných skutečných hodnot prodeje**, které odkazují na tohoto smluvního zákazníka. |

## <a name="edit-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace lze upravit v prostředí pro úpravu mřížky na řádku. Pokud procentuální rozdělení fakturace nedosáhne 100 procent, dojde k chybě. Po úpravě procentuálního rozdělení fakturace aktualizujte stránku, abyste se chyby zbavili.

Můžete také vybrat **Rovnoměrně rozdělit** v podmřížce **Smluvní zákazníci**, abyste rozdělení fakturace rovnoměrně přidělili všem smluvním zákazníkům. Pokud existuje faktor zaokrouhlování, bude přidán k zákazníkovi pro zaokrouhlování. Jeden ze smluvních zákazníků je vždy označen jako zákazník **zaokrouhlování**, což znamená, že záznam smluvního zákazníka má příznak zaokrouhlování nastaven na **Ano**. Obvykle se jedná o primárního zákazníka smlouvy, ale lze jej také změnit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
