---
title: Nastavení rolí v šablonách strukturovaného rozpisu prací
description: Toto téma poskytuje informace o nastavení informací o rolích v šablonách strukturovaného rozpisu prací.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997593"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Nastavení rolí v šablonách strukturovaného rozpisu prací

[!include [banner](../includes/banner.md)]

Projektoví manažeři mohou nastavit šablony strukturovaného rozpisu prací, které mohou použít při vytváření strukturovaného rozpisu prací pro nové projekty. Projektoví manažeři mohou při vytváření šablony přidávat role. Pomocí následujícího postupu přiřadíte roli šabloně strukturovaného rozpisu prací.

1. Vyberte položku nabídky **Řízení projektů a účetnictví** > **Nastavení** > **Projekty** > **Šablony strukturovaného rozpisu prací**.
2. Vyberte položku **Detaily** pro vybranou šablonu strukturovaného rozpisu prací.
3. Vyberte úkol v seznamu a poté v poli **Role** vyberte roli, kterou chcete k úkolu přiřadit.

## <a name="work-with-a-wbs"></a>Práce se strukturovaným rozpisem prací

Můžete vytvořit nový strukturovaný rozpis prací nebo můžete zkopírovat rozpis z existující šablony strukturovaného rozpisu prací. Projektový manažer může snadno spravovat zdroje přiřazením rolí k novým úkolům ve strukturovaném rozpisu prací. Role lze vyměnit buď po získání zdroje, nebo po identifikaci potvrzeného zdroje pro práci na úkolu. Tato flexibilita umožňuje projektovým manažerům provádět následující úkoly:

- Určit počet zdrojů, které jsou vyžadovány pro pracovní balíčky strukturovaného rozpisu prací.
- Odhadovat projektové náklady.
- Určit předběžný rozpočet.
- Odhadnout trvání aktivity na základě rolí a zdrojů.
- Vypracovat některé plány správy projektů na základě dostupných informací o projektu.

Do strukturovaného rozpisu prací byly přidány další možnosti pro lepší využití funkce zajišťování zdrojů.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnost</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přiřazení zdrojů</td>
<td>Zobrazit přiřazené zdroje, datumy, počet hodin a typ rezervace pro úkoly na strukturovaném rozpisu prací.</td>
</tr>
<tr class="even">
<td>Automaticky vygenerovat tým</td>
<td>Automaticky přidávat plánované prostředky pomocí rolí, které jsou přidruženy k úkolu. Aplikace Finance automaticky navrhne plánované zdroje pomocí multikriteriální rozhodovací analýzy založené na rolích. Po nastavení rolí a úsilí (v hodinách) pro úkoly ve WBS a po uvolnění struktury vyberte příkaz <strong>Automaticky generovat tým</strong>. Požadovaný počet plánovaných zdrojů je přidán do strukturovaného rozpisu prací a na kartu <strong>Plánování projektu a týmu</strong>.</td>
</tr>
<tr class="odd">
<td>Zdroj (rozevírací seznam)</td>
<td>Na stránce <strong>Spustit přiřazení prostředku</strong> můžete vybrat zdroje pro závaznou nebo předběžnou rezervaci na základě zadané doby trvání. Můžete upravit nastavení zobrazení, abyste viděli a nastavili dobu trvání aktivit zdrojů. Zdroje můžete vybrat a přiřadit na úrovni pracovního balíčku pomocí následujících možností:
<ul>
<li><strong>Přijmout</strong> – Potvrďte změny zdroje, který je přiřazen k úkolu.</li>
<li><strong>Zrušit</strong> – Zrušte změny zdroje, který je přiřazen k úkolu.</li>
<li><strong>Přiřadit automaticky</strong> – Dostupný personální zdroj, který má odpovídající roli, je automaticky vybrán a přiřazen k vybranému úkolu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stránce **Všechny projekty** vyberte projekt **Fáze 2 upgradu XYZ**.
2. Vyberte položku nabídky **Plán** > **Aktivity** > **Strukturovaný rozpis prací**.
3. Výběrem možnosti **Nový** přidáte do strukturovaného rozpisu prací následující aktivity první úrovně:

    - Spouštěcí
    - Plánování
    - Spouštění
    - Monitorování a řízení
    - Uzavřeno

4. Nastavte data a úsilí (v hodinách), jak je znázorněno na následujícím obrázku.

    [![Nastavení dat a úsilí](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vyberte řádek úlohy **Spouštěcí** a poté v poli **Role** vyberte **Vyšší projektový manažer**.
6. Vyberte **Publikovat**.
7. Na stejném řádku vyberte v poli **Zdroj** položku **Daniel Goldschmidt** a potom vyberte **Přijmout**.
8. Vyberte řádek úlohy **Plánování** a poté v poli **Role** vyberte položku **Obchodní analytik**.
9. Vyberte příkaz **Publikovat** a potom vyberte **Automaticky generovat tým**.
10. V okně se zprávou, které se objeví, vyberte **Ano**.
11. V poli **Zdroj** ověřte, zda je v něm hodnota **Obchodní analytik 1**.
12. Pro zdroj **Obchodní analytik 1** otevřete vyhledávání a vyberte možnost **Spustit přiřazení zdrojů**. Poté vyberte pracovníka pro úkol.
13. Vyberte možnost **Předběžně přiřadit** &gt; **Plná kapacita**.

    > [!NOTE] 
    > Neobdržíte varování, že zadaný zdroj je nyní 2, protože počet zdrojů zůstává 1.

14. Na stránce **Strukturovaný rozpis prací** ověřte přiřazení zdrojů ve strukturovaném rozpisu prací a poté vyberte příkaz **Uložit**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]