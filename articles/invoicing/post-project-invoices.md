---
title: Přehled fakturovacího procesu
description: Toto téma obsahuje přehled procesu fakturace v Project Operations pro scénáře se zdroji bez skladových materiálů.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369008"
---
# <a name="invoicing-process-overview"></a>Přehled fakturovacího procesu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Project Operations pro scénáře se zdroji bez skladových materiálů nabízí komplexní funkce přizpůsobené tak, aby vyhovovaly potřebám projektového manažera i účetního. Pro proces fakturace projektový manažer spravuje nevyřízené položky fakturace projektu a účetní vytváří kompatibilní a přesný dokument faktury orientované na zákazníka.

![Vývojový diagram fakturace](./media/invoicing-flow.png)

Řádek smlouvy projektu definuje metodu fakturace pro související transakce projektu. Když projektový manažer schválí časové a výdajové transakce, systém zaznamená transakce do entity **Skutečné hodnoty projektu** a odešle informace do modulu **Řízení projektů a účetnictví** v Dynamics 365 Finance. Účetní projektu poté zkontroluje a zaúčtuje záznamy pomocí [deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md). Tento deník obsahuje důležité účetní údaje pro skutečná data projektu, jako je fakturace, skupina daně z prodeje, skupina daně z prodeje fakturační položky a finanční dimenze.

Projektový manažer může zkontrolovat nevyfakturované prodejní transakce pomocí metody fakturace času a materiálu v [Nevyřízených fakturacích času a materiálu](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) a fakturace pevné ceny v [Milnících pevné ceny](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Tato zobrazení umožňují filtrovat a vybrat transakce, které je třeba zahrnout do příštího fakturačního cyklu, a poté je označit jako **Připraveno k fakturaci**.

Můžete [ručně vytvořit proforma fakturu](../proforma-invoicing/create-manual-proforma-invoice.md) nebo použít [periodický proces](../proforma-invoicing/configure-automated-invoice-creation.md). Projektový manažer může [upravit návrh pro forma faktury](../proforma-invoicing/manage-proforma-invoice.md) podle potřeby a poté ho potvrdit.

Potvrzená pro forma faktura je odeslána do modulu **Řízení projektů a účetnictví** ve Finance. Účetní projektu naformátuje a aktualizuje návrh faktury projektu a poté zaúčtuje a vytiskne dokument. Zaúčtované faktury projektu se zaznamenávají v hlavní knize i v podřízených knihách zákazníka a projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]