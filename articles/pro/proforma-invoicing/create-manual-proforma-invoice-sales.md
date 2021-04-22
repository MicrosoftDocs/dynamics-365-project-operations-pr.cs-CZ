---
title: Projektové proforma faktury
description: Tento téma poskytuje informace o projektových proforma fakturách v Project Operations.
author: rumant
manager: Annbe
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d08e2b0422a991aa4c98ae5d1e0f60aa0eb9daa6
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867168"
---
# <a name="proforma-project-pnvoices"></a>Projektové proforma faktury

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Projektová proforma fakturace je užitečná, protože projektovým manažerům poskytuje druhou úroveň schválení před tím, než vytvoří faktury pro zákazníky. První úroveň schválení je dokončena schválením časových, výdajových a materiálových záznamů, které odešlou členové projektového týmu.

Dynamics 365 Project Operations Lite Deployment není navrženo pro generování faktur pro zákazníky. Následující seznam ukazuje, proč nelze faktury generovat:

- Neobsahuje daňové informace.
- Nelze převést jiné měny na fakturační měnu.
- Nelze správně formátovat faktury pro tisk.

Místo toho můžete k vytvoření zákaznických faktur, které používají informace v generovaných návrzích faktur, použít finanční nebo účetní systém.

## <a name="creating-project-invoices"></a>Vytvoření projektových faktur

Projektové faktury lze vytvářet jednotlivě nebo hromadně. Můžete je vytvořit ručně nebo je lze nakonfigurovat tak, aby byly generovány v automatických spuštěních.

### <a name="manually-create-project-invoices"></a>Ruční vytvoření projektových faktur 

Na stránce se seznamem **Projektové smlouvy** můžete vytvořit projektové faktury samostatně pro každou projektovou smlouvu nebo můžete faktury vytvořit hromadně pro více projektových smluv.

   - K vytvoření faktury pro konkrétní projektovou smlouvu na stránce se seznamem **Projektové smlouvy** otevřete projektovou smlouvu pak vyberte **Vytvořit fakturu**.

   Je vygenerována faktura pro všechny transakce vybrané projektové smlouvy, které mají stav **Připraveno k fakturaci**. Tyto transakce zahrnují čas, výdaje, materiály, milníky, řádky kontraktů na základě produktů a další nevyfakturované řádky prodejního deníku, které mohly být potvrzeny.

Hromadné vytváření faktur:

1. Na stránce se seznamem **Projektových smluv** vyberte jednu nebo více projektových smluv, pro které chcete vytvořit fakturu, a pak vyberte **Vytvořit projektové faktury**.
2. Zobrazí se zpráva s upozorněním, že před vytvořením faktur může dojít k prodlevě. Tento proces je také zobrazen. Výběrem **OK** zavřete dialogové okno.

   Je vygenerována faktura pro všechny transakce na řádku smlouvy, které mají stav **Připraveno k fakturaci**. Tyto transakce zahrnují čas, výdaje, materiály, milníky, řádky kontraktů na základě produktů a další nevyfakturované řádky prodejního deníku, které mohly být potvrzeny.

3. Chcete-li zobrazit generované faktury, přejděte do **Prodej** \> **Fakturace** \> **Faktury**. Pro každou projektovou smlouvu se zobrazí jedna faktura.

### <a name="set-up-automated-creation-of-project-invoices"></a>Nastavení automatického vytváření projektových faktur 

Chcete-li nakonfigurovat spuštění automatické fakturace, postupujte následujícím způsobem.

1. Přejděte na **Nastavení** \> **Dávkové úlohy**.
2. Vytvořte dávkovou úlohu a pojmenujte ji **Vytvořit faktury v Project Operations**. Název dávkové úlohy musí obsahovat termín „Vytvořit faktury”.
3. V poli **Typ úlohy** vyberte **Žádný**. Ve výchozím nastavení jsou možnosti **Frekvence denně** a **Je aktivní** nastaveny na **Ano**.
4. Vyberte **Spustit pracovní postup**. V dialogovém okně **Vyhledat záznam** se zobrazí následující pracovní postupy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom vyberte **Přidat**.
6. V dalším dialogovém okně vyberte **OK**. Po pracovním postupu **Spánek** následuje pracovní postup **Zpracovat**.

    Pracovní postup **ProcessRunner** můžete také vybrat v kroku 5. Když potom vyberete **OK**, bude pracovní postup **Zpracovat** následován pracovním postupem **Spánek**.

Pracovní postupy **ProcessRunCaller** a **ProcessRunner** vytvářejí faktury. **ProcessRunCaller** volá **ProcessRunner**. **ProcessRunner** je pracovní postup, který vytváří faktury. Tento pracovní postup prochází všemi řádky smluv, pro které musí být vytvořeny faktury, a vytváří faktury. Aby určil řádky smluv, pro které musí být vytvořeny faktury, vyhledává pracovní postup data spuštění faktury pro řádky smluv. Jestliže řádky smluv, které patří k jedné smlouvě, mají stejné datum spuštění faktury, budou transakce sloučeny do jedné faktury, která má dva řádky faktury. Pokud neexistují žádné transakce pro vytvoření faktur, nejsou vytvořeny žádné faktury.

Proces **ProcessRunner** po svém dokončení volá proces **ProcessRunCaller**, poskytne čas ukončení a je zavřen. Proces **ProcessRunCaller** poté spustí časovač, který běží po dobu 24 hodin od zadaného času ukončení. Po doběhnutí časovače je **ProcessRunCaller** uzavřen.

Úloha dávkového zpracování pro vytváření faktur je opakující se úloha. Pokud je tento dávkový proces spuštěn vícekrát, vytvoří se více instancí této úlohy a může to způsobit chyby. K obejití tohoto problému spusťte tento dávkový proces pouze jednou a restartujte ho, pouze pokud přestane běžet.

> [!NOTE]
> Dávková fakturace běží pouze pro řádky projektové smlouvy, které jsou konfigurovány podle plánů faktur. Řáeke smlouvy s metodou fakturace s pevnou cenou musí mít nakonfigurované milníky. Řádek smlouvy o projektu s metodou fakturace času a materiálu bude vyžadovat sestavení časového rozvrhu faktur. Totéž platí pro řádek smlouvy založené na projektu.      
 
### <a name="edit-a-draft-invoice"></a>Úprava konceptu faktury

Když vytváříte koncept projektové faktury, jsou všechny nefakturované prodejní transakce, které byly vytvořeny při schválení časových a výdajových záznamů, načteny do faktury. Dokud je faktura stále ve fázi konceptu, můžete provést následující úpravy:

- Odstranit nebo upravit podrobnosti řádku faktury.
- Upravit a přizpůsobit množství a typ fakturace.
- Přímo přidat čas, náklady, materiály a poplatky jako transakce na faktuře. Tuto funkci můžete použít v případě, že je řádek faktury namapován na řádek smlouvy, který umožňuje tyto třídy transakcí.

Chcete-li fakturu potvrdit, vyberte **Potvrdit**. Tato akce představuje jednosměrnou akci. Když vyberete **Potvrdit**, faktura se nastaví jen pro čtení a vytvoří se skutečné fakturované hodnoty z každé podrobnosti řádku faktury pro každý řádek faktury. Pokud podrobnosti řádku faktury odkazují na nefakturovanou skutečnou hodnotu prodeje, stornuje se nefakturovaná skutečná hodnota prodeje. Jakýkoli detail řádku faktury, který byl vytvořen ze záznamu o čase, výdaji nebo použití materiálu, bude odkazovat na skutečný nevyfakturovaný prodej. Systémy integrace hlavní knihy mohou pomocí tohoto storna stornovat nedokončenou práci projektu (WIP) pro účetní účely.

### <a name="correct-a-confirmed-invoice"></a>Oprava potvrzené faktury

Potvrzené faktury lze upravovat. Když opravíte potvrzenou fakturu, vytvoří se nový koncept opravné faktury. Protože se předpokládá, že chcete zrušit všechny transakce a množství z původní faktury, obsahuje tato opravná faktura všechny transakce z původní faktury a všechna množství na ní jsou nula.

Pokud transakce nevyžadují opravu, můžete je odebrat z konceptu opravné faktury. Pokud chcete zrušit nebo vrátit pouze částečné množství, můžete upravit pole **Množství** v podrobnostech řádku. Pokud otevřete podrobnosti řádku faktury, uvidíte původní množství faktury. Potom můžete upravit aktuální množství faktury tak, aby bylo menší nebo větší než původní množství faktury.

Po potvrzení opravné faktury se původní skutečná hodnota fakturovaného prodeje stornuje a vytvoří se nová skutečná hodnota fakturovaného prodeje. Pokud bylo množství sníženo, rozdíl způsobí, že bude vytvořena nová skutečná hodnota nefakturovaného prodeje. Pokud byl například původní fakturovaný prodej na 8 hodin a opravné podrobnosti řádku faktury obsahují snížené množství 6 hodin, stornují se původní vyfakturované prodejní řádky a vytvoří dvě nové skutečné hodnoty:

- Fakturovaná skutečná hodnota prodeje pro 6 hodin.
- Skutečná hodnota nefakturovaného prodeje pro zbývající dvě hodiny. Tato transakce může být fakturována později nebo označena jako neúčtovatelná, v závislosti na jednáních se zákazníkem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
