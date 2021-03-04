---
title: model zabezpečení,
description: Toto téma obsahuje informace o modelu zabezpečení v Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642895"
---
# <a name="security-model"></a>Model zabezpečení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations obsahuje jedinečný model zabezpečení, který umožňuje obchodní model zabezpečení založený na rolích, kterým spolupracuje se skupinami Microsoft Office. 


## <a name="security-roles"></a>Role zabezpečení
Mezi funkce front-endu Project Operations patří následující role:

| Role                          | Popis                                                                                                                                                                 | Obor |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Správce postupů              | Podporuje vykazování napříč projekty.                                                                                                            | Obchodní jednotka              |
| Schvalovatel projektu              | Schvaluje časy a výdaje projektu.                                                                                                                              | Obchodní jednotka |
| Správce fakturace projektu | Vytváří návrh faktur.                                                                                                                                                 | Obchodní jednotka |
| Vedoucí projektu               | Vytvoří plán projektu a požaduje zdroje.                                                                                                                              | Obchodní jednotka |
| Projektový zdroj              | Členové týmu, kteří mohou rezervovat a nahlásit čas.                                                                                                          | Obchodní jednotka|
| Správce zdrojů              | Všechny funkce správy zdrojů, jako je plnění požadavků na zdroje a rezervací, oddělené pro podporu hybridní konfigurace projektový manažer + správce zdrojů a jediné centralizované role Správce zdrojů. | Obchodní jednotka |


Microsoft Project pro web zahrnuje následující role:

| Role           | Popis                                                                                                        | Obor  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Uživatel projektu   | Kolaborativní uživatel aplikace Project, který je schopen vytvářet vlastní projekty a prohlížet všechny s ním sdílené projekty. | Uživatelské   |
| Systém projektu | Role použitá pro kontext aplikace. Zákazníci by neměli tuto systémovou roli používat.                                    | Globální |

## <a name="security-enforcement"></a>Prosazování bezpečnosti
Akce, které se provádějí na úrovni projektu, se provádějí v kontextu přihlášeného uživatele. To znamená, že za účelem vytvoření, otevření nebo odstranění projektu musí uživatel mít přístup k projektu v CDS. Přístup v CDS může být udělen prostřednictvím kteréhokoli z možných mechanismů obsažených v platformě. Například když může uživatel s větším rozsahem přistupovat k projektu nebo pokud byla provedena explicitní akce sdílení projektu, která uživateli uděluje přístup.

Je důležité toto vzít do úvahy při vytváření projektů v Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderní skupinová spolupráce pomocí Project Operations
Project pro web a Project Operations podporují moderní skupiny pro spolupráci. Uživatelé přidaní do projektu prostřednictvím skupiny mohou upravovat plán projektu.

Project pro Web přidává uživatele do skupiny automaticky při přiřazení.

Skupiny umožňují společně pracovat na oprávněních projektu a podpůrných artefaktech spolupráce. Následující diagram zobrazuje události a změny stavu, ke kterým dochází během procesu přiřazování skupin.

Project Operations nevytváří skupinu prostřednictvím implicitní akce a dělá to pouze prostřednictvím explicitní akce prosazení skupin.

Hledání členů skupiny v dialogovém okně **Správa skupiny** je omezeno na členy, kteří jsou nastaveni jako součást skupiny zabezpečení prostředí. Další informace naleznete v části [Řízení přístupu uživatelů k prostředím: skupiny zabezpečení a licence](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Skupinový režim](./media/groupsmode.png)

1. Projekt je vytvářen a vlastněn vytvářejícím uživatelem.
2. Vlastník projektu je aktualizován na tým.
3. Tým vlastníka je mapován na zadanou nebo vytvořenou skupinu Office.
4. Původní vlastník projektu je přidán do skupiny Office.

## <a name="deployment-recommendation"></a>Doporučení pro nasazení
Během dalšího vývoje modelu skupinové spolupráce Office do něj bude přidána funkčnost, která poskytne podrobnější kontrolu v průběhu času. Zákazníkům, kteří dnes nasazují Project Operations, se doporučuje, aby se zaměřili na tradiční model zabezpečení Microsoft Dynamics 365.

Další informace najdete v tématu [Zabezpečení v rámci služby Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Zabezpečení v Project Operations a Microsoft Dynamics 365 Finance
Project Operations zahrnuje následující role:

- Vedoucí projektu
- Účetní projektu

Další informace o zabezpečení v aplikaci Finance najdete v tématu [Zabezpečení založené na rolích](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]