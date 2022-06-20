---
title: Integrace duálního zápisu Project Operations
description: Tento článek poskytuje přehled integrace duálního zápisu Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927964"
---
# <a name="project-operations-dual-write-integration-overview"></a>Přehled integrace duálního zápisu Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Project Operations používá [možnosti duálního zápisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) k synchronizaci dat napříč Microsoft Dataverse a Dynamics 365 Finance.

Následující obrázek ukazuje, jak jsou data synchronizována jako součást této integrace mezi Dataverse a Finance.

![Přehled toků dat Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations na Dataverse poskytuje moderní uživatelské rozhraní (UI) a snadnou rozšiřitelnost bez kódování / s malým množstvím kódování pomocí funkcí Power Platform. Projektoví manažeři, Resource manageři, členové projektového týmu a další personální pracovníci komunikující se zákazníky vykonávají své činnosti v Project Operations na Dataverse.

Project Operations ve Finance poskytuje podporu projektového účetnictví a rozpoznávání výnosů. Project Operations se připojuje k finančnímu rámci ve Finance pro výpočet DPH, směnných kurzů, vykazování finančních dimenzí a další. Účetní projektu pracuje většinou ve Finance.

Integrace Project Operations se skládá z následující integrace komponent:


- [Nastavení Project Operations a integrace dat konfigurace](resource-dual-write-setup-integration.md) 
- [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md)
- [Projektové faktury](resource-dual-write-project-invoice.md)
- [Řízení výdajů](resource-dual-write-expense.md)
- [Faktura dodavatele](resource-dual-write-vendor-invoice.md)
