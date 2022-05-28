---
title: Nastavení zádržného dodavatele
description: Toto téma vysvětluje, jak nastavit zádržné dodavatele.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583696"
---
# <a name="set-up-vendor-retention"></a>Nastavení zádržného dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma vysvětluje, jak nastavit zádržné dodavatele.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Nastavení účtu zádržného dodavatele v hlavní knize

1. V Dynamics 365 Finance přejděte do části **Hlavní kniha** > **Nastavení zaúčtování** > **Účty pro automatické transakce**.
2. Přidejte nový řádek.
3. V poli **Typ zapčtování** vyberte **Zádržné dodavatele**.
4. Vyberte hlavní účet pro zaúčtování zádržného dodavatele.

## <a name="create-vendor-retention-terms"></a>Vytvoření podmínek zádržného dodavatele

Na stránce **Podmínky zádržného dodavatele** pro nastavení a správu podmínek zadržení plateb dodavatelům. Zadejte procento zadržené platby dodavateli a procento dříve zadržené částky, kterou chcete uvolnit. Částky jsou automaticky zadržovány na fakturách dodavatelů, dokud smlouva nedosáhne zadaného stavu dokončení. Po nastavení podmínek zádržného dodavatele je můžete použít na jakýkoli projekt, na kterém dodavatel pracuje.

1. V modulu Finance Přejděte na **Řízení projektů a účetnictví** > **Nastavení** > **Zadržení** > **Podmínky zadržení plateb dodavateli**.
2. Vyberte možnost **Nový** a přidejte novou podmínku zadržení pro dodavatele. Hodnota v poli **ID pravidla** pro novou podmínku se automaticky zadá. 
3. V poli **Popis** zadejte popisný název nové podmínky.
4. Na kartě **Podmínky** volbou **Přidat řádek** zadejte podmínku zádržného dodavatele.
5. V poli **Procento dodaných jednotek** zadejte procento dokončení pro dané pravidlo. Na faktuře dodavatele se částka automaticky zachová, dokud není fáze dokončení projektu rovna zadanému procentu. Například pokud zadáte 50,00, částky budou zadrženy, dokud nebude projekt dokončen na 50 procent.
6. V poli **Procento k zadržení** zadejte procento zadržené částky faktury dodavatele. Například pokud do tohoto pole zadáte hodnotu 10,00, 10 procent z částky na fakturách dodavatele na zůstane zadrženo, dokud projekt nedosáhne procenta dokončení vybraného v poli **Procento dodaných jednotek**.
7. V poli **Procento k uvolnění** zadejte procento libovolné dříve zadržené částky, kterou chcete vydat po dosažení vybrané úrovně dokončení projektu.

> [!NOTE]
> Pokud máte více než jeden milník pro různé úrovně dokončení projektu, zadejte samostatný řádek s podmínkami zádržného dodavatele pro každé pravidlo zadržení. Každý řádek můžete představovat jiné procento zádržného a uvolnění pro každou uvedenou úroveň dokončení projektu.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Nastavení smlouvy dodavatele pro projekt

Nastavte podmínky zádržného dodavatele, které se vztahují na projekt. Podmínky zadržení pro dodavatele se také zobrazují na nákupních objednávkách, které pro dodavatele vytvoříte.

1. V modulu Finance přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty**. 
2. Vyberte projekt a v podokně akcí vyberte **Skupina projektu** > **Smlouvy s dodavatelem**.
3. Na stránce **Smlouvy s dodavatelem** přidejte nový řádek.
4. V poli **Kód účtu** vyberte jednu z následujících možností:
   - **Tabulka**: Podmínky zadržení pro dodavatele platí pro jednoho dodavatele.
   - **Skupina**: Podmínky zadržení pro dodavatele platí pro všechny dodavatele ve skupině dodavatelů.
   - **Vše**: Podmínky zadržení pro dodavatele platí pro všechny dodavatele.
5. V poli **Dodavatel / skupina dodavatelů** vyberte dodavatele nebo skupinu dodavatelů, na které se vztahují podmínky zádržného pro dodavatele. Pokud jste vybrali **Vše** v předchozím kroku, toto pole není k dispozici.
6. V poli **Podmínky zádržného dodavatele** vyberte ID pravidla podmínky zádržného, které se mají použít u tohoto dodavatele.

