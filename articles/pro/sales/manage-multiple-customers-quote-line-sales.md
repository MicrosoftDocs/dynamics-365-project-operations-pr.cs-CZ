---
title: Správa více zákazníků v řádcích nabídek založených na projektu
description: Toto téma popisuje správu více zákazníků v řádcích nabídek založených na projektu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6a509fcf8d1fa11b4ce1ba1493d9c3cc64b4f22f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073681"
---
# <a name="managing-multiple-customers-on-project-based-quote-lines"></a>Správa více zákazníků v řádcích nabídek založených na projektu

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Řádky nabídek založených na projektu podporují scénáře, kde každý řádek nabídky obsahuje seznam zákazníků, kteří za ni platí. Tento seznam zákazníků v řádku nabídky založené na projektu může být stejný jako seznam zákazníků v nabídce. Můžete také změnit seznam zákazníků, aby se lišili. Po získání projektové nabídky se seznam zákazníků na řádku nabídky založené na projektu zkopíruje do odpovídající řádky smlouvy založené na projektu, aby bylo možné vytvořit konečnou projektovou smlouvu. Zákazníci v nabídce založené na projektu jsou zkopírováni do projektové smlouvy.

Když fakturujete konečnou projektovou smlouvu, seznam zákazníků na řádku smlouvy založené na projektu má přednost před seznamem v projektové smlouvě. Seznam zákazníků v projektové smlouvě se používá pouze pro výchozí hodnoty nových řádků projektové smlouvy.

Všichni zákazníci nabídky na kartě **Zákazníci** projektové nabídky jsou uvedeni jako výchozí zákazníci řádku nabídky na všech nových řádcích nabídek založených na projektu vytvořených pro projektovou nabídku. Žádné stávající řádky nabídek založených na projektu nezdědí nové záznamy zákazníků nabídky vytvořené po nich.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka řádku nabídky

Zákazníka řádku nabídky můžete vytvořit, aktualizovat nebo odstranit na kartě **Zákazníci řádku nabídky** na stránce **Řádek nabídky založené na projektu**. Když přidáte nového zákazníka do řádku nabídky založené na projektu, zákazník se také přidá do celkové nabídky jako zákazník nabídky, s výchozím procentem rozdělení fakturace na celkovou nabídku 0%. Procentuální rozdělení fakturace na celkové nabídce je zkopírováno do nových řádků nabídky a do konečné projektové smlouvy. Když však fakturujete ze smlouvy, použije se procento rozdělení fakturace na úrovni řádku nabídky, nikoli procento rozdělení fakturace na celkové úrovni smlouvy. 

V následující tabulce jsou uvedena pole v záznamu zákazníka řádku nabídky patřícího do řádku nabídky založené na projektu.

| Pole | Místo | Popis a rady | Dopad na následné složky |
| --- | --- | --- | --- |
| **Obchodní vztah** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky** , hlavní formulář a formuláře pro rychlé vytvoření zákazníka řádku nabídky. | Vypíše seznam všech aktivních účtů. Po vytvoření záznamu je toto pole uzamčeno. Pokud potřebujete pole aktualizovat, smažte a znovu vytvořte záznam. Pokud jste zaznamenali nějaké skutečnosti, nemůžete záznam smazat. | Když vyberete účet z hlavního seznamu účtů, který chcete přidat, přidá se při jeho uložení zákazník řádku nabídky také jako zákazník nabídky. Po získání nabídky se zákazníci řádku nabídky zkopírují k zákazníkům řádku projektové smlouvy. |
| **Procento rozdělení fakturace** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky** , hlavní formulář a formuláře pro rychlé vytvoření zákazníka řádku nabídky. | Představuje procento z každé nevyfakturované prodejní transakce, která bude připsána tomuto zákazníkovi řádku nabídky. | Zkopírováno do zákazníků řádků projektové smlouvy. |
| **Nepřekročitelný limit** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky** , hlavní formulář a formuláře pro rychlé vytvoření zákazníka řádku nabídky. | Určuje, zda existuje sjednaný limit nebo strop celkové částky, která bude fakturována tomuto zákazníkovi za tento řádek nabídky. | Zkopírováno do zákazníků řádku projektové smlouvy při získání nabídky. |
| **Je zaokrouhlení** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky** , hlavní formulář a formuláře pro rychlé vytvoření zákazníka řádku nabídky. | Udává, zda je tento zákazník výchozím zaokrouhlovacím zákazníkem pro tento řádek nabídky založené na projektu. | Zkopírováno do zákazníků projektové smlouvy při získání nabídky. |

## <a name="edit-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace se dají upravit v řádku. Pokud součet procent rozdělení fakturace není 100%, dojde k chybě. Po úpravě procent rozdělení fakturace chybu odstraníte aktualizací stránky řádku nabídky.

Pomocí akce rovnoměrného rozložení na podřízené mřížce zákazníků řádku nabídky přidělte rozdělení fakturace všem zákazníkům řádku nabídky. Pokud existuje zaokrouhlovací faktor, bude přidán k zaokrouhlovacímu zákazníkovi. Jeden ze zákazníků řádku nabídky je vždy označen jako zaokrouhlovací zákazník, což znamená, že v záznamu zákazníka řádku nabídky je příznak zaokrouhlování nastaven na **Ano**. 
