---
title: Vytvoření a použití podmínek zadržení plateb dodavatele
description: Tento téma poskytuje informace o tom, jak nastavit a udržovat podmínky zadržení pro platby dodavatele.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3961d18fcd53381ad43a1d3e598ac61652ba9843
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685094"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Vytvoření a použití podmínek zadržení plateb dodavatele

[!include [banner](../includes/banner.md)] 

Nastavení podmínek zadržení plateb dodavatele pro projekt je užitečné, když chce vaše organizace zadržet část plateb provedených prodejci. Například když chcete pozdržet platbu prodejci, dokud dodané produkty nesplní vaše očekávání. Podmínky pro zadržení plateb dodavatele lze určit při sjednávání smlouvy s dodavatelem.

## <a name="create-vendor-payment-retention-terms"></a>Vytvoření podmínek zadržení plateb dodavatele

Můžete zadat procento platby dodavatele za zadržení a procento dříve zadržených částek, které mají být uvolněny. Částky jsou automaticky zadržovány na fakturách dodavatelů, dokud smlouva nedosáhne zadaného stavu dokončení. Jakmile nastavíte podmínky zadržení, můžete je použít na jakýkoli projekt pro daného dodavatele.

Pomocí následujících kroků můžete nastavit a udržovat podmínky zadržení plateb dodavatele. 

1. Přejděte do **Řízení projektů a účetnictví** > **Zadržení** > **Podmínky zadržení plateb dodavatele**.
2. Vyberte možnost **Nový** a přidejte novou podmínku zadržení pro dodavatele. Hodnota **ID pravidla** pro novou podmínku je automaticky zadána. 
3. Zadejte krátký popis do pole **Popis** pole a na rychlé kartě **Podmínky** vyberte **Přidat řádek** pro zadání hodnot podmínek pro následující:

   - **Procento dodaných jednotek**: Zadejte procento dokončení pro danou podmínku. Částky jsou automaticky zadržovány na fakturách dodavatelů, dokud fáze dokončení projektu neodpovídá zadanému procentu. Například pokud zadáte 50,00, částky budou zadrženy, dokud nebude projekt dokončen na 50 procent.
   - **Procento k zadržení**: Zadejte procento z částky faktury dodavatele, která se má zadržet. Například pokud zadáte 10,00, pak se 10 procent částky na faktuře dodavatele zadrží, dokud projekt nedosáhne procenta dokončení stanoveného v poli **Procento dodaných jednotek**.
   - **Procento k uvolnění**: Vyberte **Přidat řádek** k zadání procenta všech dříve zadržených částek, které mají být uvolněny pro vybranou úroveň dokončení projektu.

> [!NOTE]
> Pokud máte více než jeden milník pro různé úrovně dokončení projektu, zadejte pro každé pravidlo zadržení samostatný řádek podmínek zadržení pro dodavatele. Každý řádek může specifikovat jiné procento zadržení a jiné procento uvolnění pro každou určenou úroveň dokončení projektu.

Jakmile vytvoříte podmínky zadržení pro dodavatele, můžete je použít na projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Použití podmínek zadržení pro dodavatele na projekt

1. Přejděte do nabídky **Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty** a otevřete projekt na stránce seznamu projektů.
2. Na pevné záložce **Smlouvy s dodavatelem** vyberte položku **Přidat řádek**.
3. V poli **Kód účtu** vyberte jednu z následujících možností: 

   - **Tabulka**: Podmínky zadržení pro dodavatele platí pro jednoho dodavatele.
   - **Skupina**: Podmínky zadržení pro dodavatele platí pro všechny dodavatele ve skupině dodavatelů.
   - **Vše**: Podmínky zadržení pro dodavatele platí pro všechny dodavatele.

4. V poli **Dodavatel / skupina dodavatelů** vyberte dodavatele nebo skupinu dodavatelů, na které se vztahují podmínky zadržení pro dodavatele. Pokud jste vybrali **Všechno** v předchozím kroku, toto pole není k dispozici.
5. V poli **Podmínky zadržení pro dodavatele** vyberte podmínky zadržení, které jste vytvořili v předchozím postupu.
6. Pokud má projekt pro dodavatele nastaveny také podmínky zaplacení po uhrazení (PWP), zadejte prahovou hodnotu pro projekt do pole **Procento prahové hodnoty PWP**.

Podmínky zadržení pro dodavatele se také zobrazují na nákupních objednávkách, které pro dodavatele vytvoříte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]