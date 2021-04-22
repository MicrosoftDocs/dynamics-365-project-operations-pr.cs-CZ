---
title: Nabídky - klíčové koncepty
description: Tento téma poskytuje informace o projektových a prodejních nabídkách dostupných v Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 488c57527e6cc153093014438453001170f311dc
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663677"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepty jedinečné pro nabídky na základě projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Dynamics 365 Project Operations existují dva typy nabídek, projektové nabídky a prodejní nabídky. Tyto dva typy nabídek se liší následujícími způsoby:

- **Mřížky pro položky řádku**: V prodejní nabídce je k dispozici pouze jedna mřížka pro řádkové položky. Na projektové nabídce existují dvě mřížky pro položky řádku. Jedna mřížka je pro řádky projektu a druhá pro řádky produktu.
- **Aktivace a revize**: Prodejní nabídky podporují aktivaci a revize. Tyto procesy nejsou v nabídce projektu podporovány.
- **Připojené objednávky**: K prodejní nabídce můžete připojit více objednávek. K projektové nabídce lze připojit pouze jednu projektovou smlouvu.
- **Získání nabídky**: Když získáte prodejní nabídku, související příležitost může zůstat otevřená. Po získání projektové nabídky je související příležitost uzavřena.
- **Pole a koncepty**: Prodejní nabídka neobsahuje některá pole a koncepty, které jsou součástí projektové nabídky. Mezi tato pole patří **Smluvní jednotka**, **Manažer obchodních vztahů** a **Fakturační adresa – jméno kontaktu**.  
- **Typ**: Prodejní nabídky a projektové nabídky jsou také identifikovány pomocí pole **Typ** založeného na sadě možností. U prodejní nabídky má toto pole hodnotu **Na základě zboží**. U projektové nabídky má hodnotu **Na základě práce**.

Toto téma se zaměřuje na podrobnosti projektových nabídek.

Projektová nabídka v Project Operations může obsahovat více položek řádků nebo řádků nabídky. Projektová nabídka obsahuje ve skutečnosti dvě mřížky pro řádkové položky. Jedna mřížka je pro řádky založené na projektech, které umožňují detailní odhady. Druhá mřížka je pro řádky založené na produktech, které používají jednoduchou jednotkovou cenu a přístup založený na množství.

- **Založené na projektech** Hodnota nabídky je určena poté, co odhadnete, kolik práce je potřeba. Pomocí projektu a plánu projektu můžete odhadnout základní práci, přímo jako podrobnosti řádku pod každým řádkem nabídky, nebo na základě zcela nových odhadů. Řádky nabídky založené na projektu se nacházejí pouze v nabídkách založených na projektech, které jsou vytvářeny pomocí Project Operations. Tento typ řádku poptávky je přizpůsobený formulář řádků nezahrnutých do nabídky, které jsou k dispozici v Microsoft Dynamics 365 Sales.

- **Založené na produktu**: Hodnota nabídky je určena na základě množství prodaných jednotek a jednotkové prodejní ceny. Produkt na řádku založeném na produktu může pocházet z katalogu produktů v prodeji nebo se může jednat o produkt, který definujete. Tento typ řádku nabídky je také k dispozici pro nabídky založené na projektech, které jsou vytvářeny pomocí Project Operations.

Částka v nabídce je součtem řádků založených na produktu a řádků založených na projektu.

> [!NOTE]
> V Project Operations nejsou vyžadovány nabídky a řádky nabídky. Proces projektu můžete zahájit pomocí projektové smlouvy (prodaného projektu). Příležitost je však vždy vyžadována, bez ohledu na to, zda začnete pomocí nabídky nebo projektové smlouvy.

## <a name="project-based-quote-lines"></a>Řádky nabídky založené na projektu

Řádek nabídky založený na projektu v Project Operations obsahuje následující metody fakturace:

- Čas a materiál
- Pevná cena

### <a name="time-and-material"></a>Čas a materiál

Metoda fakturace času a materiálu je založena na spotřebě. Když vyberete tuto metodu fakturace, zákazníkovi je vystavena faktura, když projekt vyvolá náklady. Faktury se vytvářejí periodicky na základě data. V průběhu prodejního procesu poskytuje hodnota nabídky časových a materiálových komponent pouze odhad konečných nákladů pro zákazníka. Dodavatel se nezavazuje k dokončení projektu v přesně uvedené hodnotě nabídky. Časové a materiálové komponenty zvyšují riziko zákazníka. Zákazníci mohou chtít vyjednat další klauzule o nepřekročení, aby minimalizovali své riziko. Project Operations nepodporuje nastavení klauzulí o nepřekročení.

### <a name="fixed-price"></a>Pevná cena

U metody fakturace pomocí pevné ceny se dodavatel zavazuje k dodání projektu s pevnými náklady pro zákazníka. Zákazníkovi je fakturována hodnota nabídky řádku nabídky s pevnou cenou bez ohledu na náklady, které dodavateli v souvislosti s dodáním tohoto řádku nabídky vznikly. Hodnota řádku nabídky s pevnou cenou je fakturována jedním z následujících způsobů: 

- Jako paušální částka na začátku nebo na konci projektu nebo při dosažení milníku projektu. 
- Při frekvenci stejných splátek v pevné hodnotě na základě data na řádku nabídky. Tyto splátky se nazývají periodické milníky.
- Ve splátkách, které mají peněžní hodnotu, která je v souladu s pokrokem práce nebo konkrétními milníky, kterých je v projektu dosaženo. V tomto případě se může hodnota každé splátky lišit, ale všechny musí být přidány k pevné hodnotě na řádku nabídky.

Project Operations podporuje všechny tři typy rozpisů faktur pro řádky nabídek s pevnou cenou.

## <a name="transaction-classification"></a>Klasifikace transakce

Profesionální servisní organizace svým zákazníkům obvykle předkládají nabídky a faktury podle klasifikace nákladů. Náklady jsou reprezentovány následujícími klasifikacemi transakcí:

- **Čas**: Tato klasifikace představuje náklady na práci nebo čas lidských zdrojů na projekt.
- **Výdaje**: Tato klasifikace představuje všechny ostatní druhy výdajů na projekt. Protože výdaje mohou být široce klasifikovány, většina organizací vytváří podkategorie, jako jsou cestování, pronájem aut, hotel nebo kancelářské potřeby.
- **Poplatek**: Tato klasifikace představuje různé režijní náklady, pokuty a další položky, které jsou účtovány zákazníkovi. 
- **Daň**: Tato klasifikace představuje částky daně, které uživatelé přidávají při zadávání výdajů.
- **Materiálové transakce**: Tato klasifikace představuje skutečné hodnoty z produktových řádků na potvrzené projektové faktuře.
- **Milník**: Tato klasifikace je používána logikou pro fakturaci s pevnou cenou.

Ke každému řádku nabídky lze přidružit jednu nebo více těchto klasifikací transakcí. Po získání nabídky je mapování mezi klasifikací transakce a řádkem poptávky převedeno na řádek smlouvy.
  
Nabídka může například obsahovat následující dva řádky nabídky: 

- Konzultační práce, která používá metodu fakturace času a materiálu, kdy jsou použitelné klasifikace transakcí času a poplatků. Například všechny transakce času a poplatků pro ukázkový projekt **Implementace Dynamics AX** jsou zákazníkovi fakturovány na základě času a použitých materiálů. 
- Související cestovní výdaje, které používají metodu fakturace pevné ceny. Například všechny cestovní výdaje pro ukázkový projekt **Implementace Dynamics AX** jsou fakturovány s pevnou peněžní hodnotou.

> [!NOTE]
> Kombinace klasifikací projektu a transakce **Čas**, **Výdaje** a **Poplatek**, které jsou přidruženy k řádku nabídky nebo řádku smlouvy, musí být jedinečné. Pokud je stejná kombinace projektu a třídy transakce přidružena k více než jednomu řádku smlouvy nebo řádku nabídky, Project Operations nebude pracovat správně.

## <a name="billing-types"></a>Typy fakturace

Pole **Typ fakturace** definuje koncept účtovatelnosti. Jedná se o sadu možností s následujícími možnými hodnotami:

- **Účtovatelné**: Náklady, které narůstají podle této role/kategorie, jsou přímé náklady, které řídí spuštění projektu, a zákazník za tuto práci zaplatí. Platbu lze spravovat jako dohodu o čase a materiálu nebo o pevné ceně. Zaměstnanec, který tento čas stráví, však dostane odpovídající kredit za své fakturovatelné využití.
- **Neúčtovatelné**: Náklady, které narůstají podle této role/kategorie, jsou považovány za přímé náklady, které řídí spuštění projektu, přestože zákazník tento fakt nepozná a za tuto práci nezaplatí. Zaměstnanci, který tento čas stráví, za něj nebude připsán kredit s fakturovatelným využitím.
- **Neplacené**: Náklady, které narůstají podle této role/kategorie, jsou považovány za přímé náklady, které řídí spuštění projektu, a zákazník tento fakt zjistí. Zaměstnanci, který tento čas stráví, za něj bude připsán kredit pro fakturovatelné využití. Tyto náklady však nejsou účtovány zákazníkovi.
- **Není k dispozici**: Pomocí této možnosti jsou sledovány náklady vynaložené na interní projekty, které nevyžadují sledování výnosů.

## <a name="invoice-schedule"></a>Rozpis faktury

Rozpis faktury je posloupnost kalendářních dat, kdy dojde k fakturaci projektu. Rozpis faktury můžete volitelně vytvořit na řádku nabídky. Každý řádek nabídky může obsahovat vlastní rozpis faktury. Chcete-li vytvořit rozpis faktury, musíte zadat následující hodnoty atributů:

- Počáteční datum fakturace 
- Datum dodání, které představuje koncové datum fakturace v projektu.
- Četnost faktury

Tyto tři hodnoty atributů se používají ke generování nezávazné sady dat pro stanovení fakturace.

## <a name="invoice-frequency"></a>Četnost faktur

Četnost faktury je entita, která uchovává hodnoty atributů, které pomáhají vyjádřit četnost vytváření faktury. Následující atributy vyjadřují nebo definují entitu četnosti faktur:

- **Období**: Jsou podporována měsíční, čtrnáctidenní a týdenní období. 
- **Počet spuštění za období**: Pro týdenní a čtrnáctidenní období můžete definovat pouze jedno spuštění za období. Pro měsíční období můžete definovat mezi jedním a čtyřmi spuštěními za období. 
- **Dny spuštění**: Dny, kdy by měla být spouštěna fakturace. Tento atribut můžete nakonfigurovat dvěma způsoby:
  - **Pracovní dny**: Můžete například určit, že fakturace bude spouštěna každé pondělí nebo každé druhé pondělí. Zákazníci, kteří musí nastavit spuštění fakturace v pracovní den, mohou upřednostnit tento typ konfigurace. 
  - **Kalendářní dny**: Můžete například určit, že fakturace bude spouštěna sedmý a dvacátý první den každého měsíce. Některé organizace mohou upřednostňovat tento typ konfigurace, protože pomáhá zaručit, že fakturace bude každý měsíc spuštěna podle pevně stanoveného plánu.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Rozpis faktury pro řádek nabídky s pevnou cenou

Pro řádek nabídky s pevnou cenou můžete použít mřížku **Rozpis faktury** k vytvoření fakturačních milníků, které se rovnají hodnotě řádku nabídky.

- Chcete-li vytvořit fakturační milníky, které jsou rovnoměrně rozděleny, vyberte četnost faktury, zadejte na řádku nabídky počáteční datum fakturace a vyberte **Požadované datum dokončení** pro nabídku v části **Souhrn** v záhlaví nabídky. Chcete-li vytvořit rovnoměrně rozdělené milníky na základě vybrané četnosti faktury, vyberte poté **Vygenerovat pravidelné milníky**. 
- Chcete-li vytvořit jednorázový fakturační milník, vytvořte milník a poté jako částku milníku zadejte hodnotu řádku nabídky.
- Chcete-li vytvořit fakturační milníky založené na konkrétních úkolech v projektovém plánu, vytvořte milník a namapujte ho na prvek plánu projektu v uživatelském rozhraní fakturačního milníku.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
