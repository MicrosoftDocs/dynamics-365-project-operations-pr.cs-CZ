---
title: Zakoupení neskladovaných materiálů pomocí nevyřízené faktury dodavatele
description: Tento téma vysvětluje, jak zaznamenat nevyřízené faktury dodavatele.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009028"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Zakoupení neskladovaných materiálů pomocí nevyřízené faktury dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Když společnost pro projekt pořizuje neskladované materiály, lze náklady okamžitě zaznamenat oproti projektu. 

Například Contoso Robotics USA provádí projekt obnovy zařízení a potřebuje softwarové licence. Tyto licence jsou zakoupeny od dodavatele třetí strany.  Pomocí Dynamics 365 Finance účetní odpovědný za účty zaznamená dokument nevyřízené faktury dodavatele a přiřadí náklady na licenci přímo proti projektu obnovy zařízení. 

> [!IMPORTANT]
> Než použijete funkce popsané v tomto tématu, zkontrolujte a použijte požadované konfigurace. Další informace viz [Povolené neskladovaných materiálů a nevyřízených faktury dodavatele](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Zaúčtování nevyřízené faktury dodavatele související s projektem 

Nevyřízené faktury dodavatele lze zaznamenat na stránce **Nevyřízené faktury dodavatele** (**Závazky** > **Faktury** > **Nevyřízené faktury dodavatele**). Chcete-li zaúčtovat nevyřízenou fakturu dodavatele související s projektem, postupujte takto:

1. Přejděte na **Závazky** > **Faktury** a vyberte **Nový**. 
2. V poli **Účet faktury** vyberte dodavatele a v poli **Číslo** zadejte identifikaci faktury dodavatele.
3. Přidejte řádek na fakturu dodavatele a do pole **Číslo položky** vyberte skladovou položku zakoupenou od dodavatele. 

    > [!NOTE]
    > Řádky faktury dodavatele založené na kategorii nákupu nelze proti projektu zaznamenat. 
    
5. Přidejte zakoupené množství. Systém naplní jednotkovou cenu na základě konfigurace ceny zboží, které není skladem. 
6. Ověřte celkovou částku a další požadované podrobnosti na řádku.
7. Na řádku podrobnosti na kartě **Projekt** vyberte ID projektu, do kterého bude tato položka zaznamenána.
8. Volitelně vyberte číslo aktivity a aktualizujte kategorii projektu a vlastnost řádku.
9. Zaúčtujte nevyřízenou fakturu dodavatele. Když je faktura zaúčtována, systém zaznamená:
    
    - Částka zůstatku dodavatele.
    - Částka DPH.
    - Náklady na projekt se zaznamenají na účet integrace nákupu.
    - Skutečná transakce projektu v Dataverse. Tato transakce je dále zpracovávána pomocí [deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md). Zaúčtováním tohoto deníku se částka přesune z účtu integrace nákupu do účtu nákladů projektu.
