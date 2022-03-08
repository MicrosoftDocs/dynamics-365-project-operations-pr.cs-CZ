---
title: Správa více zákazníků v projektových nabídkách
description: Toto téma poskytuje informace o práci na nabídkách zahrnujících více zákazníků, kteří budou financovat projekt.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073634"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Správa více zákazníků v projektových nabídkách

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Projektové nabídky podporují scénář, kdy návrh zahrnuje více zákazníků, kteří budou obchod financovat. Karta **Souhrn** nabídky obsahuje pole **Potencionální zákazník**, které identifikuje primárního zákazníka obchodu. Další zákazníky pro obchod lze nastavit na kartě **Zákazníci** projektové nabídky.

Všichni zákazníci nabídky na kartě **Zákazníci** projektové nabídky jsou uvedeni jako výchozí zákazníci řádku nabídky na všech **nových** řádcích nabídek založených na projektu vytvořených pro nabídku. Žádné stávající řádky nabídek založených na projektu nezdědí nové záznamy zákazníků nabídky vytvořené po nich.

Zákazníky nabídky a zákazníky řádku nabídky lze přidávat, aktualizovat nebo odstraňovat kdykoli před získáním nabídky. Platný zákazník v nabídce musí být nastaven jako zákazník ve vlastnící společnosti nebo právnické osobě na stránce **Zákazníci**. Právní subjekty jsou zřízeny v modulu **Řízení projektů a účetnictví** aplikace Dynamics 365 Project Operations a jsou k dispozici jako společnosti v modulech **Prodeje a dodání projektu** aplikace Project Operations.

## <a name="concept-of-a-primary-customer"></a>Koncept primárního zákazníka

Zákazník uvedený na kartě **Souhrn** projektové nabídky jako potenciální zákazník je primárním zákazníkem nabídky. Pokud se pokusíte odstranit primárního zákazníka ze seznamu zákazníků v nabídce, zobrazí se chyba se zprávou, že záznam primárního zákazníka v nabídce nelze odstranit.

Primární zákazník by neměl být aktualizován ze seznamu zákazníků v nabídce. Primárního zákazníka však můžete ovlivnit změnou potenciálního zákazníka na kartě **Souhrn** nabídky. Když je toto pole aktualizováno na kartě **Souhrn nabídky**, nově vybraný potenciální zákazník je přidán jako nový zákazník nabídky s nastaveným příznakem **Primární**. Starý potenciální zákazník bude i nadále zákazníkem v nabídce.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka nabídky

Zákazník nabídky může být vytvořen, aktualizován nebo odstraněn na kartě **Zákazníci nabídky** na stránce **Nabídka**. Pole uvedená v následující tabulce se nacházejí v záznamu zákazníka nabídky patřícího do projektové nabídky.

| **Pole** | **Umístění** | **Relevance, účel a vedení** | **Dopad na následné složky** |
| --- | --- | --- | --- |
| Účet | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Vypíše seznam všech aktivních účtů. Po vytvoření záznamu je toto pole uzamčeno. Chcete-li jej aktualizovat, odstraňte záznam a znovu jej vytvořte. Pokud jste zaznamenali nějaké skutečnosti nebo pokud je záznam zákazníka nabídky primárním zákazníkem, budete moci záznam odstranit. | Po vytvoření řádku nabídky se zákazníci nabídky zkopírují k zákazníkům řádku nabídky. Po získání nabídky se také zákazníci nabídky zkopírují k zákazníkům projektové smlouvy. |
| Procento rozdělení fakturace | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Představuje procento z každé nevyfakturované prodejní transakce, která bude připsána tomuto zákazníkovi nabídky. | Zkopírováno do nově vytvořených řádků nabídek a do zákazníků projektové smlouvy. |
| Fakturační adresa – jméno kontaktu | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Toto je textové pole a mělo by se použít k identifikaci kontaktní osoby faktury pro tohoto zákazníka. Výchozí hodnoty jsou brány ze záznamu souvisejícího účtu | Zkopírováno do zákazníků projektové smlouvy po získání nabídky, a následně do pole Fakturační adresa – jméno kontaktu na faktuře, která je generována pro tohoto zákazníka. |
| Fakturační adresa – jméno | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Toto textové pole by se mělo použít k identifikaci kontaktní osoby faktury pro tohoto zákazníka. | Zkopírováno do zákazníků projektové smlouvy po získání nabídky, a následně do pole **Fakturační adresa – jméno kontaktu** na faktuře, která je generována pro tohoto zákazníka. |
| Platební podmínky | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Toto je sada možností s hodnotami, které jsou implicitně načteny ze záznamu souvisejícího účtu. | Zkopírováno do zákazníků projektové smlouvy po získání nabídky, a následně do pole **Fakturační adresa – jméno kontaktu** na faktuře, která je generována pro tohoto zákazníka. |
| Je zaokrouhlení | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Označuje, zda je tento zákazník výchozím zaokrouhlovacím zákazníkem pro tento obchod. | Zkopírováno do zákazníků projektové smlouvy při získání nabídky. |
| Vlastnící společnost | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Právnická osoba, kterou má tento zákazník nastavenu v modulu **Řízení projektů a účetnictví**. Toto pole je pouze ke čtení a je nastaveno na vlastnící společnost samotné nabídky. Seznam zákazníků, které chcete přidat do pole **Účet**, je již filtrován do seznamu z této vlastnické společnosti v modulu **Řízení projektů a účetnictví** aplikace Project Operations. | Vlastnická společnost odpovídá konceptu právnické osoby v modulu **Řízení projektů a účetnictví** aplikace Project Operations. Všechny náklady a výnosy plynoucí z tohoto projektu jsou účtovány v hlavní knize vlastnící společnosti, |
| Nepřekročitelný limit | Upravitelná mřížka na kartě **Zákazníci nabídky** a formuláře **Hlavní** a **Vytvořit** pro zákazníka nabídky. | Určuje, zda existuje sjednaný limit nebo strop celkové částky, která bude fakturována tomuto zákazníkovi za tuto zakázku. | Zkopírováno do zákazníků projektové smlouvy při získání nabídky. |

## <a name="editing-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace se dají upravit v prostředí in-line úprav v mřížce. Pokud součet procent rozdělení fakturace není 100%, dojde k chybě. Po aktualizaci procent rozdělení fakturace chybu odstraníte aktualizací stránky.

Můžete také zkusit vybrat možnost **Rovnoměrně distribuovat** v podřízené mřížce zákazníků nabídky. Tato akce přiděluje rozdělení fakturace všem zákazníkům nabídky. Pokud existuje zaokrouhlovací faktor, bude přidán k zaokrouhlovacímu zákazníkovi. Jeden ze zákazníků nabídky je vždy označen jako zaokrouhlující zákazník. To znamená, že záznam zákazníka nabídky má příznak **Zaokrouhlování** nastaven na **Ano**. Obvykle se jedná o primárního zákazníka nabídky, ale lze to změnit.