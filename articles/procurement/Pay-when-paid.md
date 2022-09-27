---
title: Platby dodavatelů typu „Zaplatit po uhrazení platby“
description: Toto téma vysvětluje, jak použít scénář „Zaplatit po uhrazení platby“ (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525330"
---
# <a name="pay-when-paid-vendor-payments"></a>Platby dodavatelů typu „Zaplatit po uhrazení platby“

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma vysvětluje, jak použít scénář „Zaplatit po uhrazení platby“ (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Vytvoření nákupní objednávky, která má podmínky PWP

Když zaúčtujete fakturu od dodavatele, na kterého se vztahují podmínky PWP, zobrazí se tyto podmínky na řádcích nákupní objednávky. Chcete-li vytvořit nákupní objednávku, která obsahuje podmínky PWP, postupujte takto.

1. V Microsoft Dynamics 365 Finance postupujte podle jednoho z těchto kroků:

    - Přejděte do nabídky **Nákup a zajišťování zdrojů** \> **Nákupní objednávky** \> **Všechny nákupní objednávky**. V podokně akcí vyberte **Nová**. V dialogovém okně **Vytvoření nákupní objednávky** vyberte dodavatele, pro kterého jsou v projektu nastaveny podmínky PWP, zadejte další požadované informace a poté vyberte **OK**.
    - Přejděte do části **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty**. V podokně akcí na kartě **Správa** vyberte **Úloha položky**. Vyberte nákupní objednávku. Vyberte dodavatele, pro kterého jsou v projektu nastaveny podmínky PWP, a poté vyberte **OK**.

2. Na stránce **Nákupní objednávka** na záložce s náhledem **Řádky nákupní objednávky** volbou **Přidat řádek** vytvořte řádek nákupní objednávky.
3. Vyberte číslo položky nebo kategorii nákupu a zadejte další požadované údaje. Zkontrolujte podrobnosti řádku objednávky pro dodavatele.

    Možnost **Zaplatit po uhrazení platby** je automaticky vybrána a hodnota v poli **Procento prahu PWP** se automaticky zkopíruje z pole **Procento prahu PWP** na stránce **Projekty**.

4. Pokud nechcete v řádku nákupní objednávky pro dodavatele použít podmínky PWP, zrušte zaškrtnutí možnosti **Zaplatit po uhrazení platby**. V tomto případě bude pole **Procento prahu PWP** pro řádek NO resetováno na **0** (nula).
5. Na stránce **Nákupní objednávka** v podokně Akce na kartě **Nákup** klikněte na tlačítko **Potvrdit**. Nákupní objednávka se potvrdí.
6. V podokně akcí na kartě **Faktura** vyberte **Fakturu**, čímž vygenerujete fakturu pro nákupní objednávku.

## <a name="create-a-project-invoice-proposal"></a>Vytvoření návrhu faktury projektu

Návrhy faktur projektu slouží k vytvoření faktur projektu pro zákazníka. Ve scénáři PWP jsou platby dodavatele závislé na platbách zákazníků podle nastavení PWP. Existují však možnosti, které vám umožní uvolnit platby bez plateb zákazníka dle potřeby. Chcete-li vytvořit fakturu projektu pro zákazníka, postupujte následovně.

1. V aplikacích pro zapojení zákazníků přejděte na **Projekt** \> **Projekty** a vyberte projekt.
2. Na kartě **Skutečné hodnoty** vyberte skutečný řádek, který je vygenerován nákupní objednávkou, který má typ transakce **Nefakturovaný prodej**. Poté vyberte **Připraveno pro fakturu**.
3. Jděte na **Prodej** \> **Prodej** \> **Projektová smlouva** a vyberte projektovou smlouvu.
4. V podokně Akce volbou **Faktura** vygenerujte fakturu zákazníka.
5. V části Finance přejděte na **Řízení projektů a účetnictví** \> **Periodické** \> **Importovat z pracovní tabulky** a volbou **OK** vygenerujte deník integrace Project Operations.
6. Jděte na **Řízení projektů a účetnictví** \> **Projektové faktury** \> **Návrh faktury projektu** a volbou **Zaúčtovat** zaúčtujte návrhu faktury, který byl vygenerován pro projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizujte platbu od zákazníka a zaplaťte prodejci

Když dodavatel dokončí svou práci na projektu a pošle vám fakturu, musíte zkontrolovat stav projektu a faktury zákazníka, abyste zjistili, zda byly u projektu splněny podmínky PWP. Pokud byly splněny podmínky PWP pro dodavatele, můžete na základě plateb zákazníka za projekt určit, které řádky na faktuře dodavatele zaplatíte. Pokud se rozhodnete zaplatit prodejci, přestože podmínky PWP nebyly splněny, můžete podmínky PWP přepsat na stránce **Faktura dodavatele se zaplacením po uhrazení platby**.

1. V části Finance přejděte na **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty** a vyberte projekt.
2. V podokně akcí vyberte **Řízení** a poté volbou **Faktury dodavatele** zobrazte všechny faktury dodavatele, které byly pro projekt vygenerovány.
3. Na stránce **Faktury dodavatele se zaplacením po uhrazení platby** zadejte do vyhledávacího pole hodnoty a vyhledejte fakturu dodavatele, kterou chcete zkontrolovat. Poté vyberte možnost **Hledat**.
4. Volbou **Zaplatit po uhrazení platby** zobrazíte pouze faktury PWP.
5. Na záložce s náhledem **Řádky faktury dodavatele** vyberte řádky, které chcete uvolnit pro platbu.
6. Vyberte **Uvolnit platbu dodavatele**. Možnost **Zaplatit po uhrazení platby** se vypne a hodnota pole **Připraveno k platbě** se změní na **Ano**.
