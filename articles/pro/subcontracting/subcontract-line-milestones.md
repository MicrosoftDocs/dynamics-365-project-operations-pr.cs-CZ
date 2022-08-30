---
title: Milníky řádku subdodávky
description: Tento článek vysvětluje, jak vytvořit a udržovat plán faktur založený na milnících pro subdodávku s dodavatelem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2fe26f5ba3c7bbc689c83a2ba67d444a09a264d5
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261785"
---
# <a name="subcontract-line-milestones"></a>Milníky řádku subdodávky

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

    | Pole | Popis |Funkční dopad|
    | --- | --- |----------------------|
    | Název milníku | Název milníku. |Toto se zobrazí jako první sloupec ve všech vyhledáváních podle milníků řádků subdodávek. Řádek faktury dodavatele, který je vytvořen na základě tohoto milníku, bude také používat název milníku řádku subdodávky jako výchozí název řádku faktury dodavatele.|
    | Popis | Popis milníku. |Řádek faktury dodavatele, který je vytvořen na základě tohoto milníku, bude také používat popis milníku řádku subdodávky jako výchozí popis řádku faktury dodavatele.|
    | Datum milníku | Datum, kdy by měl proces automatického vytváření faktur hledat stav tohoto milníku, aby bylo možné jej zohlednit při fakturaci.| Tato hodnota bude použita jako výchozí datum řádku faktury dodavatele při fakturaci pro tento řádek subdodávky. |
    | Výše | Částka nebo hodnota milníku, která bude zákazníkovi fakturována. |Tato hodnota je použita jako výchozí částka na řádku faktury dodavatele při fakturaci pro tento řádek subdodávky. |
    | Daň | Částka daně použitá u milníku.| Tato hodnota je použita jako výchozí částka daně na řádku faktury dodavatele při fakturaci pro tento řádek subdodávky. |
    | Částka po zdanění | Toto pole je jen pro čtení a počítá se jako částka + daň.|Tato hodnota je použita jako výchozí na řádku faktury dodavatele při fakturaci pro tento řádek subdodávky. |
    | Stav faktury | Při vytváření milníku je tento stav vždy nastaven na **Není připraveno k fakturaci**.|  Když je stav **Připraveno k fakturaci**, vytvoření faktury dodavatele zahrnuje tento milník na faktuře dodavatele. |

5. Zvolte **Uložit a zavřít**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
