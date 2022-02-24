---
title: Správa více zákazníků na řádcích smlouvy na základě projektu
description: Tohle téma poskytuje informace o práci s řádky smluv a smlouvami, které obsahují více zákazníků.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 71081775ab45167bc1bff1979f7856a2a2a91385
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181894"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Správa více zákazníků na řádcích smlouvy na základě projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řádky smlouvy na základě projektu mohou zahrnovat seznam zákazníků, kteří jsou odpovědní za platbu. Tento seznam zákazníků na řádku smlouvy na základě projektu může být stejný jako seznam zákazníků na smlouvě, ale není to nutné. Když vyhrajete nabídku projektu a vytvoříte projektovou smlouvu, seznam zákazníků na řádku nabídky se zkopíruje na odpovídající řádek smlouvy. Zákazníci v nabídce jsou zkopírováni do smlouvy.

Když je projektová smlouva fakturována, seznam zákazníků na řádku smlouvy na základě projektu má přednost před seznamem zákazníků na smlouvě. Seznam zákazníků ve smlouvě o projektu se používá pouze pro výchozí nové řádky smlouvy.

Všichni smluvní zákazníci na kartě **Zákazníci** projektové smlouvy se automaticky stanou zákazníky na řádku smlouvy na všech nových řádcích smlouvy vytvořených pro projektovou smlouvu. Žádné stávající řádky smlouvy nezdědí nové záznamy zákazníků smlouvy vytvořené po nich.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka na řádku smlouvy

Můžete vytvořit, aktualizovat nebo odstranit zákazníka na řádku smlouvy z karty **Zákazníci na řádku smlouvy** na stránce **Řádka smlouvy na základě projektu**. Když je na řádku smlouvy na základě projektu přidán nový zákazník, přidá se také na celkovou smlouvu jako smluvní zákazník s výchozím procentem rozdělení fakturace na nula procent. Procentuální rozdělení fakturace na celkové smlouvě se zkopíruje do nových řádků smlouvy a do případné projektové smlouvy. Při fakturaci ze smlouvy se ale používá procentuální rozdělení fakturace na úrovni řádku smlouvy, nikoli procentuální rozdělení fakturace na úrovni celkové smlouvy. 

Níže jsou pole v záznamu zákazníka na řádku smlouvy pro řádek smlouvy na základě projektu, na která byste měli pamatovat při práci:

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Účet | Upravitelná mřížka na kartě **Zákazníci na řádku smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro zákazníka na řádku smlouvy | Všechny aktivní obchodní vztahy. Po vytvoření záznamu je toto pole uzamčeno. Chcete-li pole aktualizovat, odstraňte záznam a vytvořte nový záznam. Pokud jste zaznamenali nějaké skutečné hodnoty, nemůžete záznam smazat. Pro tento obchodní vztah však můžete procento rozdělení fakturace označit jako nula. Když je záznam označen jako nula, budou ovlivněny všechny budoucí skutečné náklady a výnosy, které jsou tomuto zákazníkovi přiřazeny nebo rozděleny. | Když vyberete obchodní vztah z hlavního seznamu obchodních vztahů a přidáte jej a uložíte, zákazník na řádku smlouvy se také přidá jako zákazník smlouvy. Zákazníci na řádku smlouvy se použijí, když jsou generovány faktury. |
| Procento rozdělení fakturace | Upravitelná mřížka na kartě **Zákazníci na řádku smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro zákazníka na řádku smlouvy | Toto pole představuje procento každé nefakturované prodejní transakce, která bude připsána tomuto zákazníkovi na řádku smlouvy. | Zákazníci na řádku smlouvy a procenta rozdělení fakturace se používají při vytváření skutečných hodnot po schválení a při generování faktury. |
| Nepřekročitelný limit | Upravitelná mřížka na kartě **Zákazníci na řádku smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro zákazníka na řádku smlouvy | Určuje, zda existuje sjednaný limit nebo strop celkové částky na řádku smlouvy, která bude tomuto zákazníkovi fakturována. | Nepřekročitelný limit pro zákazníka na řádku smlouvy se používá při vytváření skutečných hodnot a generování faktur. |
| Vlastnící společnost | Upravitelná mřížka na kartě **Zákazníci na řádku nabídky** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro zákazníka na řádku nabídky | Právní subjekt, ve kterém je tento zákazník zřízen. Toto pole je jen pro čtení a je nastaveno na společnost, která vlastní nabídku. Seznam zákazníků, které chcete přidat do pole **Obchodní vztah**, je již filtrován v seznamu od této vlastnící společnosti. | Pojem vlastnící společnost se rovná pojmu právnické osoby. Všechny náklady a výnosy plynoucí z tohoto projektu jsou účtovány v hlavní knize vlastnící společnosti. |
| Je zaokrouhlení | Upravitelná mřížka na kartě **Zákazníci na řádku smlouvy** a ve hlavním formuláři a formuláři pro rychlé vytvoření pro zákazníka na řádku smlouvy | Toto pole označuje, zda je tento zákazník výchozím zákazníkem pro zaokrouhlování pro tento řádek smlouvy na základě projektu. | Když generujete skutečnou hodnotu podle procenta rozdělení fakturace, mohou existovat určité rozdíly při zaokrouhlování. Tomuto zákazníkovi se v tomto případě připisují rozdíly v zaokrouhlování. |

## <a name="edit-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace lze upravit v mřížce. Pokud procentuální rozdělení fakturace nedosáhne 100 procent, dojde k chybě. Po úpravě procentuálního rozdělení fakturace aktualizujte stránku, abyste chybu opravili.

Můžete také zkusit vybrat **Rovnoměrně rozdělit** v podmřížce zákazníka na řádku smlouvy. Tato akce rovnoměrně rozdělí fakturaci všem zákazníkům na řádku smlouvy. Pokud existuje nějaký faktor zaokrouhlování, bude přidán k zákazníkovi pro zaokrouhlování. Jeden zákazník na řádku smlouvy je vždy označen jako zákazník pro **Zaokrouhlování** s příznakem **Zaokrouhlování** nastaveným na **Ano**.
