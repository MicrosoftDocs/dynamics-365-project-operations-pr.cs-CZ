---
title: Správa více zákazníků na řádcích projektové smlouvy
description: Tento článek poskytuje informace o správě více zákazníků v řádcích smluv na základě projektu.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec8457fd32a5c215bbc2056b02b2ab3527c4ab1f
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825932"
---
# <a name="manage-multiple-customers-on-project-contract-lines"></a>Správa více zákazníků na řádcích projektové smlouvy

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Řádky smlouvy na základě projektu mohou zahrnovat seznam zákazníků, kteří jsou odpovědní za platbu. Tento seznam zákazníků na řádku smlouvy na základě projektu může být stejný jako seznam zákazníků na smlouvě, ale není to nutné. Když vyhrajete nabídku projektu a vytvoříte projektovou smlouvu, seznam zákazníků na řádku nabídky se zkopíruje na odpovídající řádek smlouvy. Zákazníci v nabídce jsou zkopírováni do smlouvy.

Když je projektová smlouva fakturována, seznam zákazníků na řádku smlouvy na základě projektu má přednost před seznamem zákazníků na smlouvě. Seznam zákazníků ve smlouvě o projektu se používá pouze pro výchozí nové řádky smlouvy.

Všichni smluvní zákazníci na kartě **Zákazníci** projektové smlouvy se automaticky stanou zákazníky na řádku smlouvy na všech nových řádcích smlouvy vytvořených pro projektovou smlouvu. Žádné stávající řádky smlouvy nezdědí nové záznamy zákazníků smlouvy vytvořené po nich.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka na řádku smlouvy

Můžete vytvořit, aktualizovat nebo odstranit zákazníka na řádku smlouvy z karty Zákazníci na řádku smlouvy na stránce Řádka smlouvy na základě projektu. Když je na řádku smlouvy na základě projektu přidán nový zákazník, přidá se také na celkovou smlouvu jako smluvní zákazník s výchozím procentem rozdělení fakturace na nula procent. Procentuální rozdělení fakturace na celkové smlouvě se zkopíruje do nových řádků smlouvy a do případné projektové smlouvy. Při fakturaci ze smlouvy se ale používá procentuální rozdělení fakturace na úrovni řádku smlouvy, nikoli procentuální rozdělení fakturace na úrovni celkové smlouvy.

Níže jsou pole v záznamu zákazníka na řádku **smlouvy** pro řádek smlouvy na základě projektu, na která byste měli pamatovat při práci:

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| **Obchodní vztah** | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Všechny aktivní obchodní vztahy. Po vytvoření záznamu je toto pole uzamčeno. Chcete-li pole aktualizovat, odstraňte záznam a vytvořte nový záznam. Pokud jste zaznamenali nějaké skutečné hodnoty, nemůžete záznam smazat. Pro tento obchodní vztah však můžete procento rozdělení fakturace označit jako nula. Když je záznam označen jako nula, budou ovlivněny všechny budoucí skutečné náklady a výnosy, které jsou tomuto zákazníkovi přiřazeny nebo rozděleny. | Když vyberete obchodní vztah z hlavního seznamu obchodních vztahů a přidáte jej a uložíte, zákazník na řádku smlouvy se také přidá jako zákazník smlouvy. Zákazníci na řádku smlouvy se použijí, když jsou generovány faktury. |
| **Procento rozdělení fakturace** | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Toto pole představuje procento každé nefakturované prodejní transakce, která bude připsána tomuto zákazníkovi na řádku smlouvy. | Zákazníci na řádku smlouvy a procenta rozdělení fakturace se používají při vytváření skutečných hodnot po schválení a při generování faktury. |
| **Nepřekročitelný limit** | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Určuje, zda existuje sjednaný limit nebo strop celkové částky na řádku smlouvy, která bude tomuto zákazníkovi fakturována. | Nepřekročitelný limit pro zákazníka na řádku smlouvy se používá při vytváření skutečných hodnot a generování faktur. |
| **Je zaokrouhlení** | Upravitelná mřížka na kartě **Zákazníci smlouvy** a ve **hlavním** formuláři a formuláři pro **rychlé vytvoření** pro zákazníka na řádku smlouvy. | Toto pole označuje, zda je tento zákazník výchozím zákazníkem pro zaokrouhlování pro tento řádek smlouvy na základě projektu. | Když generujete skutečnou hodnotu podle procenta rozdělení fakturace, mohou existovat určité rozdíly při zaokrouhlování. Tomuto zákazníkovi se v tomto případě připisují rozdíly v zaokrouhlování. |

## <a name="edit-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace lze upravit v mřížce. Pokud procentuální rozdělení fakturace nedosáhne 100 procent, dojde k chybě. Po úpravě procentuálního rozdělení fakturace aktualizujte stránku, abyste chybu opravili.

Můžete také vybrat **Rovnoměrně rozdělit** v podmřížce zákazníka na řádku smlouvy. Tato akce rovnoměrně rozdělí fakturaci všem zákazníkům na řádku smlouvy. Pokud existuje nějaký faktor zaokrouhlování, bude přidán k zákazníkovi pro zaokrouhlování. Jeden zákazník na řádku smlouvy je vždy označen jako zákazník pro **Zaokrouhlování** s příznakem **Zaokrouhlování** nastaveným na **Ano**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
