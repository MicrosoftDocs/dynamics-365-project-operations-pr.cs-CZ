---
title: Správa více zákazníků v projektových smlouvách
description: Toto téma poskytuje informace o správě několika zákazníků na projektových smlouvách.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dda8bc58c00082a9ef3835ea293003c63013983f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277960"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Správa více zákazníků v projektových smlouvách

Toto téma poskytuje informace o správě několika zákazníků na projektových smlouvách. Můžete použít projektovou smlouvu, když je pro financování obchodu potřeba smluvní dohoda pro více zákazníků. Na stránce **Projektová smlouva** karta **Souhrn** obsahuje informace o primárním zákazníkovi obchodu. Na kartu **Zákazníci** lze přidat další zákazníky, kteří se obchodu účastní.

Všichni smluvní zákazníci na kartě **Zákazníci** projektové smlouvy se automaticky stanou zákazníky na řádku smlouvy na všech nových řádcích smlouvy založené na projektu vytvořených pro projektovou smlouvu. Žádné stávající řádky smlouvy na základě projektu nezdědí nové záznamy zákazníky kontraktů, kteří jsou vytvořeni později.

Smluvní zákazníky a zákazníky na řádku smlouvy lze přidávat, aktualizovat nebo odstranit kdykoli před získáním smlouvy. Zákazník na projektové smlouvě musí být nastaven jako zákazník ve společnosti, která je vlastníkem, nebo právnická osoba na stránce **Zákazníci**. Právní subjekty jsou zřízeny v modulu **Řízení projektů a účetnictví** v Dynamics 365 Project Operations a jsou k dispozici jako společnosti v modulech **Prodeje projektu** a **Doručení** Project Operations.

## <a name="primary-customers"></a>Primární zákazníci

Potenciální zákazník na kartě **Souhrn** projektové smlouvy je primárním zákazníkem smlouvy. Primárního zákazníka nelze aktualizovat ze seznamu smluvních zákazníků. Při pokusu o odstranění primárního zákazníka ze seznamu zákazníků ve smlouvě se zobrazí chybová zpráva, že záznam primárního zákazníka ve smlouvě nelze odstranit. Místo toho změňte zákazníka v poli **Potenciální zákazník** na kartě **Souhrn** projektové smlouvy. Když je toto pole aktualizováno, nový zákazník je přidán jakožto nový smluvní zákazník s příznakem **Primární** nastaveným na **Ano**. Předchozí primární zákazník je stále zákazníkem na základě smlouvy, již však není primárním zákazníkem.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka smlouvy

Smluvní zákazník může být vytvořen, aktualizován nebo odstraněn z kary **Projektoví zákazníci** na stránce **Smlouva**. Následující pole jsou na kartě uvedeni v záznamu smluvního zákazníka projektové smlouvy.

| **Pole** | **Umístění** | **Popis** | 
| --- | --- | --- | 
| Účet | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Vypíše seznam všech aktivních účtů. Po vytvoření záznamu je toto pole uzamčeno. Chcete-li aktualizovat záznam, musíte jej odstrait a znovu vytvořit. Pokud jste zaznamenali nějaké skutečné hodnoty, nebo pokud je záznam smluvního zákazníka primárním zákazníkem, nemůžete záznam odstranit. Smluvní zákazníci se při vytvoření řádku smlouvy zkopírují jako zákazníci na řádku smlouvy. |
| Procento rozdělení fakturace | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Představuje procento každé nefakturované prodejní transakce, která je připsána tomuto smluvnímu zákazníkovi. Když jsou vytvořeny nové řádky smlouvy projektu, procentuální rozdělení fakturace se zkopíruje do nových vytvořených řádků smlouvy a zákazníkům řádků smlouvy projektu. |
| Fakturační adresa – jméno kontaktu | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Toto textové pole by se mělo použít k identifikaci kontaktní osoby pro fakturu pro zákazníka. Výchozí hodnoty jsou získány ze souvisejícího záznamu obchodního vztahu. Jméno konktaktní osoby je zkopírováno do pole **Fakturační adresa – název smlouvy** na faktuře, která je generována pro tohoto zákazníka. |
| Fakturační adresa – jméno | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Toto textové pole použijte k identifikaci kontaktní osoby pro fakturu pro zákazníka. Výchozí hodnoty jsou získány ze souvisejícího záznamu obchodního vztahu. Jméno je zkopírováno do pole **Fakturační adresa – název smlouvy** na faktuře, která je generována pro tohoto zákazníka. |
| Platební podmínky | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Výchozí hodnoty jsou získány ze souvisejícího záznamu obchodního vztahu. Podmínky jsou zkopírovány do pole **Fakturační adresa – název smlouvy** na faktuře, která je generována pro tohoto zákazníka. |
| Vlastnící společnost | Upravitelná mřížka na kartě **Zákazníci projektové smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka projektu. | Právnická osoba, ve které je zákazník nastaven v modulu **Řízení projektů a účetnictví**. Toto pole je jen pro čtení a je nastaveno na společnost projektové smlouvy.</br>Seznam zákazníků, které chcete přidat do pole **Účet**, je již filtrován do seznamu z vlastnické společnosti v modulu **Řízení projektů a účetnictví** aplikace Project Operations. Vlastnická společnost se rovná právnické osobě v modulu **Řízení projektů a účetnictví** v Project Operations. Všechny náklady a výnosy plynoucí z tohoto projektu jsou účtovány v hlavní knize vlastnící společnosti. |
| Je zaokrouhlení | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Označuje, zda je zákazník výchozím zaokrouhlovacím zákazníkem obchodu. Na projektové smlouvě může být pouze jeden zákazník pro zaokrouhlování. Když rozdělení nákladů a nefakturovaných prodejů pro množství způsobí rozdíly v zaokrouhlení, použije se tento rozdíl na skutečnou hodnotu, která je mapována na tohoto zákazníka. |
| Nepřekročitelný limit | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro smluvního zákazníka. | Určuje, zda existuje sjednaný limit nebo strop celkové částky na řádku smlouvy, která bude v tomto případě fakturována zákazníkovi. Nepřekročitelný limit nastavený na úrovni smluvního zákazníka je vyhodnocen na základě nefakturovaných skutečných hodnot prodeje, které odkazují na tohoto smluvního zákazníka. |

## <a name="edit-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace lze upravit v mřížce. Pokud procentuální rozdělení fakturace nedosáhne 100 procent, dojde k chybě. Po úpravě procentuálního rozdělení fakturace aktualizujte stránku **Projektová smlouva**, abyste chybu opravili.

Můžete také vybrat **Rovnoměrně rozdělit** v podmřížce projektových smluvních zákazníků. Rozdělená fakturace se přiděluje rovnoměrně všem zákazníkům v projektové smlouvě. Pokud existuje nějaký faktor zaokrouhlování, bude přidán k zákazníkovi pro zaokrouhlování. Jeden ze smluvních zákazníků má vždy příznak **Zaokrouhlování** nastaven na **Ano**. Tento zákazník je zákazníkem zaokrouhlování. Zákazník zaokrouhlování je obvykle také primárním zákazníkem smlouvy, ale není to nutné.


[!INCLUDE[footer-include](../includes/footer-banner.md)]