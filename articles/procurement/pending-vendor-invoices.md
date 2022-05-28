---
title: Nákup neskladových materiálů nebo kategorií zásobování pomocí nevyřízené faktury dodavatele
description: Tento téma vysvětluje, jak zaznamenat nevyřízené faktury dodavatele.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612649"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nákup neskladových materiálů nebo kategorií zásobování pomocí nevyřízené faktury dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Protože společnost pořizuje neskladové materiály nebo kategorie zásobování pro projekt, lze náklady okamžitě zaúčtovat proti projektu. 

Společnost Contoso Robotics USA například provádí projekt obnovy vybavení a potřebuje softwarové licence. Tyto licence jsou zakoupeny od dodavatele třetí strany.  V aplikaci Dynamics 365 Finance zaznamená úředník závazků nevyřízený doklad faktury dodavatele a přiřadí náklady na licenci přímo k projektu obnovy zařízení. 

> [!IMPORTANT]
> Než použijete funkce popsané v tomto tématu, zkontrolujte a použijte požadované konfigurace. Více informací viz téma [Povolení neskladovaných materiálů a nevyřízených faktur dodavatele](configure-materials-nonstocked.md) a [Používání kategorií zásobování s projektovými nákupními objednávkami a nevyřízenými fakturami dodavatele](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Zaúčtování nevyřízené faktury dodavatele související s projektem 

Nevyřízené faktury dodavatele lze zaznamenat na stránce **Nevyřízené faktury dodavatele** (**Závazky** > **Faktury** > **Nevyřízené faktury dodavatele**). Chcete-li zaúčtovat nevyřízenou fakturu dodavatele související s projektem, postupujte takto:

1. Přejděte na **Závazky** > **Faktury** a vyberte **Nová**. 
1. V poli **Fakturační účet** vyberte dodavatele a poté v poli **Číslo** zadejte identifikaci faktury dodavatele.
1. Přidejte řádek do faktury dodavatele a poté v poli **Číslo položky** vyberte neskladovanou položku, která byla zakoupena od dodavatele. Případně v poli **Kategorie zásobování** vyberte kategorii zásobování, která byla zakoupena od dodavatele.   
1. Přidejte zakoupené množství. Systém vyplní jednotkovou cenu na základě konfigurace ceny neskladované položky. 
1. Ověřte celkovou částku a další požadované podrobnosti na řádku.
1. V detailech řádku na kartě **Projekt** vyberte ID projektu, do kterého bude tato položka zaznamenána.
1. Volitelné: Vyberte číslo aktivity a aktualizujte kategorii projektu a vlastnost čáry.
1. Zaúčtujte nevyřízenou fakturu dodavatele. Při zaúčtování faktury systém zaznamená následující informace:
    
    - Částka zůstatku dodavatele.
    - Částka DPH.
    - Náklady na projekt se zaznamenají na účet integrace nákupu.
    - Transakce skutečných nákladů projektu v Dataverse.  Tato transakce je dále zpracovávána pomocí [deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md). Zaúčtováním tohoto deníku se částka přesune z účtu integrace nákupu do účtu nákladů projektu. 
    - Nákupy, které jsou fakturovány zákazníkovi projektu pomocí metody fakturování času a materiálu. Kromě toho jsou pro nákupy v Dataverse vytvořeny nefakturované prodejní transakce. Ceník produktu v Dataverse se používá pro prodejní ceny a částky pro nefakturované prodejní transakce.
