---
title: Přehled fakturovacího procesu
description: Tento článek poskytuje přehled procesu fakturace v Project Operations u scénářů založených na zdrojích/položkách, které nejsou na skladě.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923088"
---
# <a name="invoicing-process-overview"></a>Přehled fakturovacího procesu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Project Operations pro scénáře se zdroji bez skladových materiálů nabízí komplexní funkce přizpůsobené tak, aby vyhovovaly potřebám projektového manažera i účetního. Pro proces fakturace projektový manažer spravuje nevyřízené položky fakturace projektu a účetní vytváří kompatibilní a přesný dokument faktury orientované na zákazníka.

![Vývojový diagram fakturace.](./media/invoicing-flow.png)

Řádek smlouvy projektu definuje metodu fakturace pro související transakce projektu. Když projektový manažer schválí časové a nákladové transakce, systém zaznamená transakce do entity **Skutečné hodnoty projektu** a odešle informace do modulu **Řízení projektů a účetnictví** v Dynamics 365 Finance. Účetní projektu poté zkontroluje a zaúčtuje záznamy pomocí [deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md). Tento deník obsahuje důležité účetní údaje pro skutečná data projektu, jako je fakturace, skupina daně z prodeje, skupina daně z prodeje fakturační položky a finanční dimenze.

Projektový manažer může zkontrolovat nevyfakturované prodejní transakce pomocí metody fakturace času a materiálu v [Nevyřízených fakturacích času a materiálu](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) a fakturace pevné ceny v [Milnících pevné ceny](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Tato zobrazení umožňují filtrovat a vybrat transakce, které je třeba zahrnout do příštího fakturačního cyklu, a poté je označit jako **Připraveno k fakturaci**.

Můžete [ručně vytvořit proforma fakturu](../proforma-invoicing/create-manual-proforma-invoice.md) nebo použít [periodický proces](../proforma-invoicing/configure-automated-invoice-creation.md). Projektový manažer může [upravit návrh pro forma faktury](../proforma-invoicing/manage-proforma-invoice.md) podle potřeby a poté ho potvrdit.

Potvrzená pro forma faktura je odeslána do modulu **Řízení projektů a účetnictví** ve Finance. Účetní projektu naformátuje a aktualizuje návrh faktury projektu a poté zaúčtuje a vytiskne dokument. Zaúčtované faktury projektu se zaznamenávají v hlavní knize i v podřízených knihách zákazníka a projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]