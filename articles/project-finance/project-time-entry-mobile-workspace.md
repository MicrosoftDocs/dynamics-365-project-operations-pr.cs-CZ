---
title: Mobilní pracovní prostor zadání času projektu
description: Toto téma obsahuje informace o Zadání času projektu na mobilních pracovních prostorech. Tento pracovní prostor umožňuje uživatelům vstoupit a ušetřit čas proti projektu pomocí mobilního zařízení.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750347"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilní pracovní prostor zadání času projektu

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o **Zadání času projektu** na mobilních pracovních prostorech. Tento pracovní prostor umožňuje uživatelům vstoupit a ušetřit čas proti projektu pomocí mobilního zařízení.

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Dynamics 365 Unified Ops. 

## <a name="overview"></a>Přehled
Jako součást své každodenní práce jsou prostředky projektu často na místě nebo na cestách. Mobilní pracovní prostor **Zadání času projektu** umožňuje uživatelům zadat svůj zúčtovatelný nebo nezúčtovatelný čas proti projektu na mobilním zařízení podle vlastního výběru. Proto mohou prostředky projektu zaznamenávat časové údaje kdykoli a kdekoli. Mohou také zobrazit časové záznamy, které již byly zaznamenány. 

Konkrétně v **Zadání času projektu** mobilním pracovní prostoru mohou uživatelé provádět tyto úkoly:

-   U libovolného vybraného data zadejte počet hodin, které jste strávili konkrétním úkolem.
-   Hledejte podle názvu projektu nebo zákazníka, abyste našli projekt, pro který chcete zadat čas.
-   Určete kategorii a aktivitu za čas, který jste strávili.
-   Zaznamenejte čas jako zúčtovatelný nebo nezúčtovatelný pro projekt.
-   Můžete zadat jakékoli externí nebo interní komentáře.

## <a name="prerequisites"></a>Požadavky
Předpoklady se liší podle verze Microsoft Dynamics 365, která byla nasazena pro vaši organizaci.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Předpoklady, pokud používáte Dynamics 365 Finance
Pokud byl pro vaši organizaci nasazen Finance, musí správce systému publikovat mobilní pracovní prostor **Zadání času projektu**. Pokyny viz [Publikujte mobilní pracovní prostor](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Předpoklady, pokud používáte verzi 1611 s aktualizací platformy 3 nebo novější
Pokud byla pro vaši organizaci nasazena verze 1611 s aktualizací platformy 3 nebo novější, musí správce systému splnit následující předpoklady. 

<table>
<thead>
<tr class="header">
<th>Požadavek</th>
<th>Role</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementujte KB 4018050.</td>
<td>Správce systému</td>
<td>KB 4018050 je aktualizace X++ nebo opravná oprava metadat, která obsahuje mobilní pracovní prostor <strong>Zadání času projektu</strong>. Chcete-li implementovat KB 4018050, musí váš správce systému postupovat podle těchto kroků.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stáhněte si opravu hotfix metadat z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje <strong>ApplicationSuite</strong> a <strong>ProjectMobile</strong> modely a poté nahrajte nasaditelný balíček do LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použijte nasaditelný balíček</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publikujte mobilní pracovní prostor <strong>Zadání času projektu</strong>.</td>
<td>Správce systému</td>
<td>Pro pokyny viz <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikujte mobilní pracovní prostor</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stažení a instalace mobilní aplikace

Stažení a instalace mobilní aplikace Finance and Operations:

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro iPhony](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace
1.  Otevřete mobilní aplikaci na svém mobilním zařízení.
2.  Zadejte vaši Dynamics 365 URL.
3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte vaše pověření.
4.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud váš správce systému publikuje nový pracovní prostor později, budete muset aktualizovat seznam mobilních pracovních prostorů.

[![Aktualizace stažením](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Zadejte čas pomocí mobilního pracovního prostoru Zadání času projektu
1.  Na svém mobilním zařízení vyberte ikonu pracovního prostoru **Zadání času projektu**.
2.  Vyberte **Čas projektu** Jsou zobrazena kalendářní data aktuálního týdne.
3.  Pro vybrané datum vyberte **Akce** &gt; **Nový záznam**.
4.  Zadejte počet hodin, které chcete zaznamenat.
5.  Vyberte hodnotu projekt pro časový záznam. Seznam zobrazuje projekty, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznete v článku [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Pokud váš projekt není v seznamu, vyberte **Vyhledat**. Hledání podle názvu nebo přepnutí na vyhledávání podle názvu projektu nebo zákazníka.
7.  Vyberte kategorii. Seznam zobrazuje kategorie, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznete v článku [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Pokud váše kategorie není v seznamu, vyberte **Vyhledat**. Hledat podle kategorie nebo přepnout na vyhledávání podle názvu kategorie.
9.  Vyberte některou aktivitu. Seznam zobrazuje aktivity, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznete v článku [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Pokud váše aktivity nejsou v seznamu, vyberte **Vyhledat**. Hledejte podle čísla aktivity nebo přepněte na hledání podle účelu.

11. Vyberte vlastnost řádek.
12. Volitelné: Zadejte jakékoli externí a interní komentáře.
13. Vyberte **Hotovo**.
