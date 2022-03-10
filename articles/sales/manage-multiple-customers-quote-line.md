---
title: Správa více zákazníků v řádcích nabídek založených na projektu
description: Toto téma poskytuje informace o tom, jak provádět správu více zákazníků v řádcích nabídek založených na projektu.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf3d10cc4a742f7247586d09f5b209cbfdbbd790bdf97e09da06d9db583e61a5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992018"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Správa více zákazníků v řádcích nabídek založených na projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádky nabídek založených na projektu podporují scénáře, kde každý řádek nabídky obsahuje seznam zákazníků, kteří za ni platí. Tento seznam zákazníků v řádku nabídky založené na projektu může být stejný jako seznam zákazníků v nabídce. Můžete také změnit seznam zákazníků, aby se lišili. Chcete-li vytvořit konečnou projektovou smlouvu po získání projektové nabídky, seznam zákazníků na řádku nabídky založené na projektu se zkopíruje do odpovídající řádky smlouvy založené na projektu. Zákazníci v nabídce založené na projektu jsou zkopírováni do projektové smlouvy.

Když fakturujete konečnou projektovou smlouvu, seznam zákazníků na řádku smlouvy založené na projektu má přednost před seznamem v projektové smlouvě. Seznam zákazníků v projektové smlouvě se používá pouze pro výchozí hodnoty nových řádků projektové smlouvy.

Všichni zákazníci nabídky na kartě **Zákazníci** projektové nabídky jsou uvedeni jako výchozí zákazníci řádku nabídky na všech nových řádcích nabídek založených na projektu vytvořených pro projektovou nabídku. Žádné stávající řádky nabídek založených na projektu nezdědí nové záznamy zákazníků nabídky vytvořené po nich.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Vytvoření, aktualizace nebo odstranění záznamu zákazníka řádku nabídky

Zákazníka řádku nabídky můžete vytvořit, aktualizovat nebo odstranit na kartě **Zákazníci řádku nabídky** na stránce **Řádek nabídky založené na projektu**. Když přidáte nového zákazníka do řádku nabídky založené na projektu, zákazník se také přidá do celkové nabídky jako zákazník nabídky, s výchozím procentem rozdělení fakturace na celkovou nabídku 0%. Procentuální rozdělení fakturace na celkové nabídce je zkopírováno do nových řádků nabídky a do konečné projektové smlouvy. Když však fakturujete ze smlouvy, použije se procento rozdělení fakturace na úrovni řádku nabídky, nikoli procento rozdělení fakturace na celkové úrovni smlouvy. 

V následující tabulce jsou uvedena pole v záznamu zákazníka řádku nabídky patřícího do řádku nabídky založené na projektu.

| Pole | Místo | Popis a rady | Dopad na následné složky |
| --- | --- | --- | --- |
| **Obchodní vztah** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky**, hlavní formulář a formulář pro rychlé vytvoření zákazníka řádku nabídky. | Vypíše seznam všech aktivních účtů. Po vytvoření záznamu je toto pole uzamčeno. Pokud potřebujete pole aktualizovat, smažte a znovu vytvořte záznam. Pokud jste zaznamenali nějaké skutečnosti, nemůžete záznam smazat. | Když vyberete účet z hlavního seznamu účtů, který chcete přidat, přidá se jako zákazník nabídky také zákazník na řádku nabídky. Po získání nabídky se zákazníci řádku nabídky zkopírují k zákazníkům řádku projektové smlouvy. |
| **Procento rozdělení fakturace** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky**, hlavní formulář a formulář pro rychlé vytvoření zákazníka řádku nabídky. | Představuje procento z každé nevyfakturované prodejní transakce, která bude připsána tomuto zákazníkovi řádku nabídky. | Zkopírováno do zákazníků řádků projektové smlouvy. |
| **Nepřekročitelný limit** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky**, hlavní formulář a formulář pro rychlé vytvoření zákazníka řádku nabídky. | Určuje, zda existuje sjednaný limit nebo strop celkové částky, která bude fakturována tomuto zákazníkovi za tento řádek nabídky. | Zkopírováno do zákazníků řádku projektové smlouvy při získání nabídky. |
| **Vlastnící společnost** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky**, hlavní formulář a formulář pro rychlé vytvoření zákazníka řádku nabídky, | Právnická osoba, ve které je tento zákazník nastaven v modulu **Řízení projektů a účetnictví**. Toto pole je pouze ke čtení a je nastaveno na vlastnící společnost samotné nabídky. Seznam zákazníků, které chcete přidat do pole **Účet**, je již filtrován do seznamu z vlastnické společnosti v modulu **Řízení projektů a účetnictví** aplikace Project Operations. | Vlastnící společnost odpovídá pojmu právnická osoba. Všechny náklady a výnosy plynoucí z tohoto projektu jsou účtovány v hlavní knize vlastnící společnosti. |
| **Je zaokrouhlení** | Upravitelná mřížka na kartě **Zákazníci řádku nabídky**, hlavní formulář a formulář pro rychlé vytvoření zákazníka řádku nabídky. | Udává, zda je tento zákazník výchozím zaokrouhlovacím zákazníkem pro tento řádek nabídky založené na projektu. | Zkopírováno do zákazníků projektové smlouvy při získání nabídky. |

## <a name="edit-billing-split-percentages"></a>Úprava procentuálních rozdělení fakturace

Procenta rozdělení fakturace se dají upravit v řádku. Pokud součet procent rozdělení fakturace není 100%, dojde k chybě. Po úpravě procent rozdělení fakturace chybu odstraníte aktualizací stránky řádku nabídky.

Pomocí akce rovnoměrného rozložení na podřízené mřížce zákazníků řádku nabídky přidělte rozdělení fakturace všem zákazníkům řádku nabídky. Pokud existuje zaokrouhlovací faktor, bude přidán k zaokrouhlovacímu zákazníkovi. Jeden ze zákazníků řádku nabídky je vždy označen jako zaokrouhlovací zákazník, což znamená, že v záznamu zákazníka řádku nabídky je příznak zaokrouhlování nastaven na **Ano**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]