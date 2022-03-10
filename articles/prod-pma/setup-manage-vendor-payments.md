---
title: Nastavení a používání plateb dodavatelů zaplacených po uhrazení platby
description: Toto téma vysvětluje, jak vytvořit podmínky zaplacení po zaplacení (pay-when-paid; PWP), abyste mohli uvolnit částečné platby dodavateli na základě plateb od zákazníka.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 9976dadf57f1c84bf3f295ff3c8359c16e4849a3bf887f8bd33e46a04e2a5952
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008848"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Nastavení a používání plateb dodavatelů zaplacených po uhrazení platby

[!include [banner](../includes/banner.md)]

Když schválíte dodavatele, aby pracoval jako subdodavatel, možná budete chtít zadržet platbu pro něj, dokud vám zákazník za projekt nezaplatí. Tento scénář se dá realizovat tak, že nastavíte podmínky zaplacení po zaplacení (PWP) při nastavování nákupní objednávky (PO) u dodavatele.

Když například zákazník zaplatí částku na projektové faktuře, můžete uvolnit část nebo celou částku na faktuře dodavatele. Stačí nastavit podmínky PWP, které určují, že dodavateli bude zaplaceno poté, co od zákazníka obdržíte procento související platby. Pokud obdržíte částečnou platbu od zákazníka, můžete ručně uvolnit některé související faktury dodavatele k platbě.

Následující příklad popisuje proces, při kterém se používají termíny PWP.

## <a name="example"></a>Příklad

Vaše organizace souhlasí s tím, že zákazníkovi poskytne 100 počítačů s nainstalovaným softwarem za cenu 150,00 USD za počítač. Vy si poté najmete dodavatele, který vám poskytne počítače s nainstalovaným softwarem. Podle smlouvy musí zákazník schválit kvalitu počítačů, než zaplatí vaší organizaci. Zásadou vaší organizace je zadržet platby dodavatelům, dokud vám zákazník nezaplatí. Proto jste nastavili projekt tak, aby měl PWP procento s hodnotou 100 procent.

Dodavatel vám pošle 100 počítačů, které mají nainstalovaný software, spolu s fakturou na 10 000,00 USD. Protože jsou v projektu nastaveny podmínky PWP, neplatíte prodejci hned po obdržení počítačů. Místo toho odešlete počítače zákazníkovi spolu s fakturou na 15 000,00 USD. Zákazník zkontroluje počítače a schválí celou částku projektové faktury.

Poté, co od zákazníka obdržíte úplnou platbu, zaplatíte dodavateli 10 000,00, tedy celou částku faktury dodavatele.

## <a name="set-up-pwp-terms-for-a-project"></a>Nastavení podmínek PWP pro projekt

Když nastavujete podmínky PWP pro projekt, musíte určit minimální částku (jako procento), kterou vám musí zákazník zaplatit za projekt, než vy zaplatíte dodavateli. Mezní hodnota částky se automaticky vypočítá z faktur zákazníka pro daný projekt. Při nastavení prahového procenta pro podmínky PWP postupujte takto.

1. Přejděte do části **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty**.
2. Najděte a otevřete projekt, u kterého chcete nastavit podmínky PWP.
3. Na pevné záložce **Smlouvy s dodavatelem** vyberte položku **Přidat řádek**.
3. V poli **Kód účtu** vyberte jednu z následujících možností:

    - **Tabulka** – Podmínky PWP platí pro jednoho dodavatele.
    - **Skupina** – Podmínky PWP platí pro všechny dodavatele ve skupině dodavatelů.
    - **Vše** – Podmínky PWP platí pro všechny dodavatele.

4. Pokud jste v předchozím kroku vybrali možnost **Tabulka** nebo **Skupina**, vyberte v poli **Dodavatel nebo skupina dodavatelů** vyberte dodavatele nebo skupinu dodavatelů, na které se vztahují podmínky PWP. Pokud jste vybrali v předchozím kroku možnost **Vše**, není možné pole **Dodavatel nebo skupina dodavatelů** upravit.
5. Pokud jsou pro dodavatele v projektu nastaveny podmínky zadržení, vyberte v poli **Podmínky zádržného dodavatele** ID pravidla pro podmínky zadržení.
6. V poli **Procento prahu PWP** zadejte prahové procento pro projekt. Procento, které pro projekt zadáte, definuje minimální částku, kterou vám musí zákazník zaplatit, než vy zaplatíte dodavateli.

## <a name="create-a-po-that-has-pwp-terms"></a>Vytvoření NO, která má podmínky PWP

Když zaúčtujete fakturu od dodavatele, na kterého se vztahují podmínky PWP, zobrazí se tyto podmínky na řádcích nákupní objednávky. Chcete-li vytvořit nákupní objednávku, která obsahuje podmínky PWP, postupujte takto.

1. Přejděte do nabídky **Nákup a zajišťování zdrojů** \> **Nákupní objednávky** \> **Všechny nákupní objednávky**.
2. V podokně akcí vyberte **Nová**. Pak v dialogovém okně **Vytvořit nákupní objednávku** zadejte požadované informace a vyberte **OK**.

    Případně otevřete existující nákupní objednávku na stránce seznamu **Všechny nákupní objednávky**.

4. Na stránce **Nákupní objednávka** zkontrolujte na pevné záložce **Řádky nákupní objednávky** podrobnosti o řádku nákupní objednávky pro dodavatele. Možnost **Zaplatit po uhrazení platby** je automaticky vybrána a hodnota v poli **Procento prahu PWP** se automaticky zkopíruje z pole **Procento prahu PWP** na stránce **Projekty**.
6. Pokud nechcete v řádku nákupní objednávky pro dodavatele použít podmínky PWP, zrušte zaškrtnutí možnosti **Zaplatit po uhrazení platby**. V tomto případě bude pole **Procento prahu PWP** pro řádek NO resetováno na 0 (nula).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizujte platbu od zákazníka a zaplaťte prodejci

Když dodavatel dokončí svou práci na projektu a pošle vám fakturu, musíte zkontrolovat stav projektu a faktury zákazníka, abyste zjistili, zda byly u projektu splněny podmínky PWP. Pokud byly splněny podmínky PWP pro dodavatele, můžete na základě plateb zákazníka za projekt určit, které řádky na faktuře dodavatele zaplatíte. Pokud se rozhodnete zaplatit prodejci, přestože podmínky PWP nebyly splněny, můžete podmínky PWP přepsat na stránce **Faktura dodavatele se zaplacením po uhrazení platby**.

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Dotazy a sestavy** \> **Dotazy na zádržné** \> **Faktura dodavatele se zaplacením po uhrazení platby**.
2. Na stránce **Faktury dodavatele se zaplacením po uhrazení platby** zadejte do vyhledávacího pole hodnoty a vyhledejte fakturu dodavatele, kterou chcete zkontrolovat. Poté vyberte možnost **Hledat**.
3. Na pevné záložce **Řádky faktury dodavatele** vyberte řádky, které chcete změnit.
4. Pokud jsou podmínky **Zaplatit po uhrazení platby** pro řádek faktury splněny, vyberte možnost **Uvolnit platbu dodavatele**. Možnost **Zaplatit po uhrazení platby** se vypne a hodnota pole **Připraveno k platbě** se změní na **Ano**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]