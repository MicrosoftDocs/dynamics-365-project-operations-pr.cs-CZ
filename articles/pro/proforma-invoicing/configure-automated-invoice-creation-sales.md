---
title: Nastavení automatického vytváření faktur
description: Tento téma poskytuje informace o nastavení a konfiguraci automatického vytváření proforma faktur.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d212f2279b28d900e75d45386e343f95b8e825e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004163"
---
# <a name="set-up-automatic-invoice-creation"></a>Nastavení automatického vytváření faktur 
 
_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

V Dynamics 365 Project Operations můžete konfigurovat automatické vytváření faktur. Systém vytvoří koncept proforma faktury na základě rozpisu faktury pro každou projektovou smlouvu a řádek smlouvy. Rozpisy faktur jsou konfigurovány na úrovni řádku smlouvy. Každý řádek ve smlouvě může mít odlišný rozpis faktury nebo stejný rozpis faktury může být obsažen v každém řádku smlouvy.

Když vytvoříte fakturu, systém vždy vytvoří alespoň jednu fakturu na projektovou smlouvu. V některých případech může být vytvořeno více faktur. Například pokud má smlouva více zákazníků, bude vytvořen stejný počet faktur jako počet zákazníků, kteří mají fakturovatelné transakce k fakturaci na danou smlouvu projektu.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Pochopení, jak jsou transakce zahrnuty na faktuře 

Někdy každý řádek smlouvy na základě projektu určuje samostatný rozpis faktur. Například implementační služby pro smlouvu Adatum mají následující řádky smlouvy:

- Prototypová práce, která je pevná cena se dvěma ručně vytvořenými milníky.
- Implementační práce, která zahrnuje čas a bude účtována každé dva týdny v pondělí.
- Vzniklé výdaje, které je třeba účtovat měsíčně první pondělí každého měsíce.

Rozpisy faktur definované u každé z těchto dvou řádkových položek vypadají jako v následující tabulce:

| Řádek smlouvy | Datum spuštění faktury | Mezní datum transakce | Datum milníku | Částka milníku |
| --- | --- | --- | --- | --- |
| Prototypová práce | Pondělí 5. října | - | Pondělí 5. října | 5000 USD |
| - | Úterý 3. listopadu | - | Úterý 3. listopadu | 12,000 USD |
| Implementační práce | Pondělí 5. října | Neděle 4. října | - | - |
| - | Pondělí 19. října | Neděle 18. října | - | - |
| - | Pondělí 2. listopadu | Neděle 1. listopadu | - | - |
| - | Pondělí 16. listopadu | Neděle 15. listopadu | - | - |
| Vzniklé výdaje | Pondělí 5. října | Neděle 4. října | - | - |
| - | Pondělí 2. listopadu | Neděle 1. listopadu | - | - |

V tomto příkladu, když je automatická fakturace spuštěna:

- **4. října nebo jakékoli dřívější datum**: Pro tuto smlouvu není generována žádná faktura, protože tabulka **Rozpis faktury** pro každý z těchto řádků smlouvy neobsahuje neděli 4. října jako datum spuštění faktury.
- **Pondělí 5. října**: Jedna faktura je generována pro:

    - Prototypová práce zahrnující milník, pokud je označen jako **Připraveno k fakturaci**.
    - Implementační práce, která zahrnuje všechny časové transakce vytvořené před datem uzavření transakce v neděli 4. října, která je označena jako **Připravena k fakturaci**.
    - Vzniklé výdaje, které zahrnují všechny výdajové transakce vytvořené před datem uzavření transakce v neděli 4. října, která je označena jako **Připravena k fakturaci**.
  
- **6. října nebo jakékoli datum před 19. říjnem**: Pro tuto smlouvu není generována žádná faktura, protože tabulka **Rozpis faktury** pro každý z těchto řádků smlouvy neobsahuje 6. října ani žádné datum před 19. říjnem jako datum spuštění faktury.
- **Pondělí 19. října**: Jedna faktura je vygenerována pro implementační práci, která zahrnuje všechny časové transakce vytvořené před datem uzavření transakce v neděli 18. října, která je označena jako **Připravena k fakturaci**.
- **Pondělí 2. listopadu**: Jedna faktura je generována pro:

    - Implementační práce, která zahrnuje všechny časové transakce vytvořené před datem uzavření transakce v neděli 1. listopadu, která je označena jako **Připravena k fakturaci**.
    - Vzniklé výdaje, které zahrnují všechny výdajové transakce vytvořené před datem uzavření transakce v neděli 1. listopadu, která je označena jako **Připravena k fakturaci**.

- **Úterý 3. listopadu**: Za prototypovou práci je vygenerována jedna faktura, která obsahuje milník pro 12 000 USD, pokud je označena jako **Připraveno k fakturaci**.

## <a name="configure-automatic-invoicing"></a>Konfigurovat automatické fakturování

Chcete-li nakonfigurovat spuštění automatické fakturace, postupujte následovně.

1. V nabídce **Project Operations** jděte do **Nastavení** > **Nastavení opakované fakturace**.
2. Vytvořte dávkovou úlohu a pojmenujte ji **rVytvořit faktury v Project Operations**. Název dávkové úlohy musí obsahovat slova „Vytvořit faktury”.
3. V poli **Typ úlohy** vyberte **Žádný**. Ve výchozím nastavení jsou pole **Frekvence denně** a **Je aktivní** nastaveny na **Ano**.
4. Vyberte **Spustit pracovní postup**. V dialogovém okně **Vyhledat záznam** se zobrazí tři pracovní postupy:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom vyberte **Přidat**.
6. V dalším dialogovém okně vyberte **OK**. Po pracovním postupu **Spánek** následuje pracovní postup **Zpracovat**. 

> [!NOTE]
> Pracovní postup **ProcessRunner** můžete také vybrat v kroku 5. Když potom vyberete **OK**, bude pracovní postup **Zpracovat** následován pracovním postupem **Spánek**.

Pracovní postupy **ProcessRunCaller** a **ProcessRunner** vytvářejí faktury. **ProcessRunCaller** volá **ProcessRunner**. **ProcessRunner** je pracovní postup, který skutečně vytváří faktury. Pracovní postup prochází všemi řádky smluv, pro které musí být vytvořeny faktury, a vytváří faktury pro tyto řádky. Aby určil řádky smluv, pro které musí být vytvořeny faktury, vyhledává úloha data spuštění faktury pro řádky smluv. Jestliže řádky smluv, které patří k jedné smlouvě, mají stejné datum spuštění faktury, budou transakce sloučeny do jedné faktury, která má dva řádky faktury. Pokud neexistují žádné transakce pro vytvoření faktur, úloha přeskočí vytvoření faktury.

Proces **ProcessRunner** po svém dokončení volá proces **ProcessRunCaller**, poskytne čas ukončení a je zavřen. Proces **ProcessRunCaller** poté spustí časovač, který běží po dobu 24 hodin od zadaného času ukončení. Po doběhnutí časovače je **ProcessRunCaller** uzavřen.

Úloha dávkového zpracování pro vytváření faktur je opakující se úloha. Pokud je tento dávkový proces spuštěn vícekrát, vytvoří se více instancí této úlohy a způsobí chyby. Proto byste tento dávkový proces měli spustit pouze jednou a restartovat ho, pouze pokud přestane běžet.

> [!NOTE]
> Dávková fakturace v Project Operations běží pouze pro řádky projektové smlouvy, které jsou konfigurovány podle plánů faktur. Řáeke smlouvy s metodou fakturace s pevnou cenou musí mít nakonfigurované milníky. Řádek smlouvy o projektu s metodou fakturace času a materiálu bude vyžadovat sestavení časového rozvrhu faktur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
