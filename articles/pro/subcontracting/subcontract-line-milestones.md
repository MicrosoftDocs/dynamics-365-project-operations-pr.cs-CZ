---
title: Milníky řádku subdodávky
description: Toto téma vysvětluje, jak vytvořit a udržovat plán faktur na základě milníků pro subdodávku s dodavatelem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323768"
---
# <a name="subcontract-line-milestones"></a>Milníky řádku subdodávky

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations řádek subdodávky s metodou fakturace s pevnou cenou může určit plán fakturace založený na milníku dodavatele.

Milníky pro fakturaci dodavatelů lze generovat automaticky pomocí nastavené frekvence nebo je můžete vytvořit ručně.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatické vytvoření plánu faktur založené na milníku pro řádek subdodávky

Chcete-li automaticky vygenerovat plán faktur založený na milníku pro pevnou sadu rovnoměrně rozdělených milníků, proveďte následující kroky.

1. Přejděte na **Nastavení** > **Frekvence faktur** a nastavte frekvenci faktur pro řádky subdodávky.
2. Otevřete stránku **Subdodávky**, otevřete subdodávku, se kterou chcete pracovat, a potom otevřete řádek subdodávky s pevnou cenou, pro kterou se chystáte vytvořit plán milníků.
3. Na kartě **Mezníky řádku subdodávky** vyberte **Generovat periodické milníky**.
4. V dialogovém okně zadejte nebo vyberte časové období, počet milníků a četnost faktur. Můžete vybrat datum zahájení nebo počet milníků a četnost faktur nebo datum zahájení nebo můžete zvolit koncové datum a frekvenci faktur. Nelze vybrat koncové datum a počet milníků.
Pomocí těchto informací systém generuje milníky a záznamy, které jsou zobrazeny v mřížce **Milníky**.

   - **Název milníku** - Název milníku je nastaven na datum milníku na základě četnosti faktur.
   - **Datum milníku** - Datum na základě četnosti faktur.
   - **Částka milníku** - Vypočítá se tak, že se částka mezisoučtu na řádku subdodávky vydělí počtem milníků.

Pokud má řádek subdodávky hodnotu v poli **Odhadovaná částka daně**, je tato hodnota přidána ke každému milníku stejnoměrně při generování periodických milníků.

Součet částek milníků na řádku subdodávky se musí rovnat částce na řádku subdodávky. Pokud se nerovnají, dojde k chybě. Chybu můžete opravit a ověřit, že se celkový milník rovná hodnotě řádku subdodávky vytvořením, úpravou nebo odstraněním částek milníků a daňových částek. Po provedení změn uložte a obnovte stránku, abyste zajistili, že již nebudou žádné chyby.

## <a name="manually-create-subcontract-line-milestones"></a>Formulář pro rychlé vytvoření milníku řádku subdodávky

Milníky s pevnou cenou na řádku subdodávky lze generovat ručně, pokud nejsou pravidelně rozděleny. Chcete-li vytvořit milník řádku subdodávky postupujte podle následujících kroků.

1. V navigačním podokně vyberte **Subdodávky** a otevřete subdodávku, na které chcete pracovat.
2. Otevřete řádek subdodávky s pevnou cenou, pro kterou chcete vytvořit milník.
3. Na kartě **Milníky řádku subdodávky** na dílčí mřížce vyberte **+ nový milník řádku subdodávky**.
4. Na stránce **Nový milník řádku subdodávky** zadejte požadované informace na základě následující tabulky.

    | Pole | Popis |
    | --- | --- |
    | Název milníku | Název milníku. |
    | Popis | Popis milníku.  |
    | Datum milníku | Datum, kdy by měl proces automatického vytváření faktur hledat stav tohoto milníku, aby bylo možné jej zohlednit při fakturaci. Tato hodnota je zahrnuta v řádku faktury dodavatele při fakturaci této subdodávky. |
    | Výše | Částka nebo hodnota milníku, která bude zákazníkovi fakturována. Tato hodnota je zahrnuta v řádku faktury dodavatele při fakturaci této subdodávky. |
    | Daň | Částka daně použitá u milníku. Tato hodnota je zahrnuta v řádku faktury dodavatele při fakturaci této subdodávky. |
    | Částka po zdanění | Toto pole pouze pro čtení se počítá jako částka + daň. Tato hodnota je zahrnuta v řádku faktury dodavatele při fakturaci této subdodávky. |
    | Stav faktury | Při vytváření milníku je tento stav vždy nastaven na **Není připraveno k fakturaci**.  Když je stav **Připraveno k fakturaci**, vytvoření faktury dodavatele zahrnuje tento milník na faktuře dodavatele. |

5. Zvolte **Uložit a zavřít**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
