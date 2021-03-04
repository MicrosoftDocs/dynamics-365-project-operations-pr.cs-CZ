---
title: Mobilní pracovní prostor správy výdajů
description: Toto téma obsahuje informace o pracovním prostoru mobilní správy výdajů. Tento pracovní prostor umožňuje uživatelům zaznamenat a odeslat účtenku, aby ji mohli později připojit k výkazu výdajů. Uživatelé mohou také rychle vytvořit řádek výdajů pomocí přiložené účtenky a vytvářet a spravovat své výkazy výdajů.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b6d577861a6ebfae55b64a8a06143256e0f1ff40
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960464"
---
# <a name="expense-management-mobile-workspace"></a>Mobilní pracovní prostor správy výdajů

Toto téma obsahuje informace o pracovním prostoru mobilní **správy výdajů**. Tento pracovní prostor umožňuje uživatelům zaznamenat a odeslat účtenku, aby ji mohli později připojit k výkazu výdajů. Uživatelé mohou také rychle vytvořit řádek výdajů pomocí přiložené účtenky a vytvářet a spravovat své výkazy výdajů. Schvalovatelé mohou dále používat mobilní pracovní prostor **Správa výdajů** k zobrazení výkazů výdajů, které jsou jim přiřazeny, a tyto výkazy výdajů buď schválit, nebo odmítnout.


Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Dynamics 365 Unified Ops.


## <a name="overview"></a>Přehled

Mnoho organizací vyžaduje, aby zaměstnanec žádající náhradu výdajů připojil k výkazu výdajů souvisejících se zaměstnáním nebo s cestou kopii účtenky. Mobilní pracovní prostor **Správa výdajů** umožňuje uživatelům rychle vytvářet nové řádky výdajů na mobilním zařízení podle vlastního výběru pomocí přiložené fotografie účtenky. Uživatelé mohou také pořídit fotografii účtenky a později ji připojit k výkazu výdajů. Zaměstnanci mohou také vytvářet a spravovat své výkazy výdajů a poté je odesílat ke schválení a úhradě pomocí svého mobilního zařízení.


Konkrétně mobilní pracovní prostor **Správa výdajů** umožňuje uživatelům provádět tyto úkoly:

- Vyfoťte účtenku a nahrajte ji do Dynamics 365 Finance. Tuto fotografii pak můžete připojit k sestavě výdajů později.
- Nahrát soubor jako zaznamenanou účtenku. Tento soubor pak můžete připojit k sestavě výdajů později.
- Vytvořit nový řádek výdajů pomocí přiložené účtenky. Poté můžete položku řádku přidat do výkazu výdajů později a odeslat ji ke schválení a náhradě.

Můžete také použít tyto funkce:

- Vytvořit nový výkaz výdajů.
- Připojit transakce kreditní kartou a další dříve vytvořené výdaje k výkazu výdajů.
- Vytvořit nové výdaje pro výkaz výdajů.
- Připojit účtenku k jakémukoliv výdaji pro výkaz výdajů buď pořízením fotografie účtenky, nebo nahráním souboru jako zaznamenané účtenky.
- V závislosti na zásadách výdajů společnosti přidat k výdajům seznam hostů.
- V závislosti na zásadách výdajů společnosti rozepsat výdaje.
- Odeslat výkaz výdajů ke schválení a úhradě.
- Schválit nebo zamítnout výkazy výdajů, pro které jste přiřazeným schvalovatelem.

## <a name="prerequisites"></a>Požadavky
Předpoklady se liší podle verze, která byla nasazena pro vaši organizaci.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Předpoklady, pokud používáte Dynamics 365 Finance 
Pokud byl pro vaši organizaci nasazen Finance, musí správce systému publikovat mobilní pracovní prostor **Správa výdajů**. Pokyny viz [Publikujte mobilní pracovní prostory](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

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
<td>Implementujte KB 4019015.</td>
<td>Správce systému</td>
<td>KB 4019015 je aktualizace X++ nebo opravná oprava metadat, která obsahuje mobilní pracovní prostor <strong>Správa výdajů</strong>. Chcete-li implementovat KB 4019015, musí váš správce systému postupovat podle těchto kroků.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Stáhněte si opravu hotfix metadat z Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Vytvořte nasaditelný balíček</a>, který obsahuje modely <strong>ApplicationSuite</strong> a <strong>ExpenseMobile</strong> a poté nahrajte nasaditelný balíček do LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Použijte nasaditelný balíček</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publikujte mobilní pracovní prostor <strong>Správa výdajů</strong>.</td>
<td>Správce systému</td>
<td>Pro pokyny viz <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publikujte mobilní pracovní prostor</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Stažení a instalace mobilní aplikace Dynamics 365 for Operations
Stáhněte si a nainstalujte mobilní aplikaci Dynamics 365 Unified Ops:

- [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pro iPhony](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace
1. Otevřete mobilní aplikaci na svém mobilním zařízení.
2. Zadejte vaši Dynamics 365 URL.
4. Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte vaše pověření.
5. Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud váš správce systému publikuje nový pracovní prostor později, budete muset aktualizovat seznam mobilních pracovních prostorů.


[![Aktualizace stažením](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zaznamenání účtenky pomocí mobilního pracovního prostoru správy výdajů

1. Na svém mobilním zařízení otevřete pracovní prostor **Správa výdajů**.
2. Vyberte **Zaznamenat účtenku**.
3. Vyberte **Pořídit fotografii** nebo **Zvolit obrázek**.
4. Postupujte podle jednoho z těchto kroků:

    - Pokud jste vybrali **Pořídit fotografii**, postupujte podle těchto kroků:

        1. Jste přesměrováni na fotoaparát na vašem mobilním zařízení, abyste mohli pořídit fotografii účtenky. Po dokončení fotografování vyberte **OK** pro přijetí fotografie.
        2. Volitelné: Zadejte název fotografie a jakékoliv poznámky.

    - Pokud jste vybrali **Zvolit fotografii**, postupujte podle těchto kroků:

        1. V seznamu vyberte obrázek.
        2. Volitelné: Zadejte název obrázku a jakékoliv poznámky.

5. Vyberte **Hotovo**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Rychle zadejte výdaje pomocí mobilního pracovního prostoru správy výdajů
1. Na svém mobilním zařízení otevřete pracovní prostor **Správa výdajů**.
2. Vyberte **Rychlé zadání výdaje**.
3. Vyberte kategorii výdaje. Uvidíte seznam kategorií výdajů, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud vaše kategorie není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle kategorie výdaje nebo přepněte na vyhledávání podle typu výdaje.
4. Zadejte datum transakce výdaje.
5. Volitelné: Pro výdaj zadejte obchodníka.
6. Zadejte částku výdaje.
7. Vyberte měnu výdaje. Uvidíte seznam kódů měn, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 400 měn, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud vaše měna není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle měny nebo přepněte na vyhledávání podle názvu kategorie.
8. Vyberte **Pořídit fotografii** nebo **Zvolit obrázek**.
9. Postupujte podle jednoho z těchto kroků:

    - Pokud jste zvolili **Pořídit fotografii**, budete přesměrováni na fotoaparát na vašem mobilním zařízení, abyste mohli pořídit fotografii účtenky. Po dokončení fotografování vyberte **OK** pro přijetí fotografie.
    - Pokud jste vybrali **Zvolit obrázek**, vyberte obrázek v seznamu.

10. Vyberte **Hotovo**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Schválení výkazu výdajů pomocí mobilního pracovního prostoru Správa výdajů (pokud používáte aktualizaci z července 2017)
1. Na svém mobilním zařízení otevřete pracovní prostor **Správa výdajů**.
2. **Schválení výdajů** zobrazuje počet výkazů výdajů, které jsou vám přiřazeny ke schválení. Číslo se aktualizuje přibližně každých 30 minut. Vyberte **Schválení výdajů**.

    Zobrazí se výkazy výdajů, které jsou vám přiřazeny ke schválení.
    
3. Vyberte výkaz výdajů a zobrazte podrobnosti výdajů.
4. Vyberte výdaj a zobrazte jeho podrobnosti. Informace, které se zobrazují u výdajů, zahrnují veškeré podrobnosti o účtence, hostech a položkách.
5. Zpět na stránce **Výkaz výdajů** vyberte schválení nebo odmítnutí výkazu výdajů.
6. Zadejte jakékoli komentáře k akci schválení.
7. Vyberte **Hotovo**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Vytvoření nového výkazu výdajů a jeho odeslání ke schválení pomocí mobilního pracovního prostoru Správa výdajů (pokud používáte aktualizaci z července 2017)
1. Na svém mobilním zařízení otevřete pracovní prostor **Správa výdajů**.
2. Vyberte **Zadání výdaje**.
3. Vyberte **Nový výkaz**, nebo vyberte v seznamu existující výkaz výdajů.
4. U nových výkazů výdajů zadejte účel a veškeré další dostupné informace. Tyto informace se liší v závislosti na tom, jakým způsobem je pro vaši společnost nakonfigurována správa výdajů.
5. Vyberte **Hotovo**.
6. Chcete-li přidat stávající výdaje, například transakce kreditní kartou, do výkazu výdajů, vyberte **Připojit**.
7. Vyberte jeden nebo více výdajů v seznamu.
8. Vyberte **Hotovo**.
9. Chcete-li do výkazu výdajů přidat nový výdaj, vyberte **Nový výdaj**.
10. Vyberte kategorii výdaje. Uvidíte seznam kategorií výdajů, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud vaše kategorie není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle kategorie výdaje nebo přepněte na vyhledávání podle typu výdaje.
11. Volitelné: Pro výdaj zadejte obchodníka.
12. Zadejte datum transakce výdaje.
13. Zadejte částku výdaje.
14. Vyberte měnu výdaje. Uvidíte seznam kódů měn, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 400 měn, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud vaše měna není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle měny nebo přepněte na vyhledávání podle názvu kategorie.
15. Vyberte **Hotovo**.
16. Chcete-li k výdaji přidat další podrobnosti, vyberte **Přidat další podrobnosti**. Pole, která jsou k dispozici, závisí na konfiguraci správy výdajů pro vaši společnost.
17. Pokud zásady společnosti vyžadují účtenku pro výdaj, vyberte **Účtenky** a potom postupujte podle těchto kroků:

    1. Vyberte **Zaznamenat účtenku** nebo **Připojit účetenku**.
    2. Postupujte podle jednoho z těchto kroků:

        - Pokud jste vybrali **Zaznamenat účtenku**, postupujte podle těchto kroků:

            1. Vyberte **Pořídit fotografii** nebo **Zvolit obrázek**.
            2. Postupujte podle jednoho z těchto kroků:

                - Pokud jste vybrali **Pořídit fotografii**, postupujte podle těchto kroků:

                    1. Jste přesměrováni na fotoaparát na vašem mobilním zařízení, abyste mohli pořídit fotografii účtenky. Po dokončení fotografování vyberte **OK** pro přijetí fotografie.
                    2. Volitelné: Zadejte název fotografie a jakékoliv poznámky.

                - Pokud jste vybrali **Zvolit fotografii**, postupujte podle těchto kroků:

                    1. V seznamu vyberte obrázek.
                    2. Volitelné: Zadejte název obrázku a jakékoliv poznámky.

            3.  Vyberte **Hotovo**.

        - Pokud jste vybrali **Připojit účtenku**, postupujte podle těchto kroků:

            1.  V seznamu vyberte jeden nebo více obrázků.
            2.  Vyberte **Hotovo**.

    3. Vyberte tlačítko **Zpět** pro návrat k podrobnostem výdajů.

18. Pokud zásady společnosti vyžadují hosty pro výdaj, vyberte **Hosté** a potom postupujte podle těchto kroků:

    1. Vyberte **Host**, **Předchozí hosté** nebo **Spolupracovníci**.
    2. Postupujte podle jednoho z těchto kroků:

        - Pokud jste vybrali **Host**, postupujte podle těchto kroků:

            1. Zadejte jméno hosta.
            2. Volitelné: Zadejte organizaci anebo zemi hosta.
            3. Volitelné: Zadejte pracovní pozici hosta.
            4. Vyberte **Hotovo**.

        - Pokud jste vybrali **Předchozí hosté**, postupujte podle těchto kroků:

            1. V seznamu vyberte jedno nebo více předchozích hostů. Zobrazí se seznam předchozích hostů, které jste přidali do předchozích výkazů výdajů načtených do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud váš předchozí host není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle názvu nebo přepněte na vyhledávání podle organizace, země nebo pracovní pozice.
            2. Vyberte **Hotovo**.

        - Pokud jste vybrali **Spolupracovníci**, postupujte podle těchto kroků:

            1. V seznamu vyberte jednoho nebo více spolupracovníků. Uvidíte seznam spolupracovníků, kteří jsou načteni do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud váš spolupracovník není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle názvu nebo přepněte na vyhledávání podle společnosti nebo pracovní pozice.
            2. Vyberte **Hotovo**.

    3. Vyberte tlačítko **Zpět** pro návrat k podrobnostem výdajů.

19. Pokud zásady společnosti vyžadují rozpis výdaje, vyberte **Rozepsat** a potom postupujte podle těchto kroků:

    1. Vyberte první datum, které chcete rozepsat.
    2. Vyberte **Přidat rozepsání**.
    3. Vyberte dílčí kategorii pro rozepsání výdaje. Uvidíte seznam dílčích kategorií výdajů, které jsou načteny do vaší aplikace pro offline použití. Ve výchozím nastavení je načteno 50 položek, ale vývojář může toto číslo změnit. Další informace naleznou vývojáři v části [Mobilní platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Pokud vaše dílčí kategorie není v seznamu, vyberte **Vyhledat** pro online hledání. Hledejte podle názvu dílčí kategorie výdajů.
    4. Zadejte částku transakce pro rozepsání.
    5. Pokud je to nutné, upravte datum transakce.
    6. Vyberte **Hotovo**.
    7. Opakujte předchozí kroky, dokud nedokončíte přidávání všech položek pro vybrané datum.
    8. Pro další dny můžete vybrat **Kopírovat do dalšího dne** a zkopírovat položky do dalšího dne. Alternativně můžete vybrat datum pro rozpis a potom přidat položky jako u prvního data.
    9. Po dokončení rozpisu výdajů vyberte tlačítko **Zpět** pro návrat k podrobnostem výdajů.

20. Vyberte tlačítko **Zpět** pro návrat na stránku **Výkaz výdajů**.
21. Opakujte předchozí kroky, dokud nedokončíte přidávání všech výdajů.
22. Vyberte položku **Odeslat**.
23. Zadejte jakékoli komentáře pro schvalovatele.
24. Vyberte **Hotovo**.
