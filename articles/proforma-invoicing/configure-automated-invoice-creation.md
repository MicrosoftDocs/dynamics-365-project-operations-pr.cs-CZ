---
title: Konfigurace automatického vytváření faktur
description: Tento článek poskytuje informace o tom, jak nakonfigurovat systém pro automatické generování faktur.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 273e00e7841c8a34e249e54a7d868034bc34a1f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920604"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurace automatického vytváření faktur

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Chcete-li nakonfigurovat automatické spuštění faktury v Dynamics 365 Project Operations, proveďte následující kroky.

1. Přejděte na **Nastavení** > **Dávkové úlohy**.
2. Vytvořte dávkovou úlohu a pojmenujte ji **Vytvořit faktury v Project Operations**. Název dávkové úlohy musí obsahovat slova „Vytvořit faktury”.
3. V poli **Typ úlohy** vyberte **Žádný**. Ve výchozím nastavení jsou možnosti **Frekvence denně** a **Je aktivní** nastaveny na **Ano**.
4. Vyberte **Spustit pracovní postup**. V dialogovém okně **Vyhledat záznam** se zobrazí tři pracovní postupy:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom vyberte **Přidat**.
6. V dalším dialogovém okně vyberte **OK**. Po pracovním postupu **Spánek** následuje pracovní postup **Zpracovat**.

  > [!NOTE]
  > Pracovní postup **ProcessRunner** můžete také vybrat v kroku 5. Když potom vyberete **OK**, bude pracovní postup **Zpracovat** následován pracovním postupem **Spánek**.

Pracovní postupy **ProcessRunCaller** a **ProcessRunner** vytvářejí faktury. **ProcessRunCaller** volá **ProcessRunner**. **ProcessRunner** je pracovní postup, který skutečně vytváří faktury. Prochází všemi řádky smluv, pro které musí být vytvořeny faktury, a vytváří faktury pro tyto řádky. Aby určil řádky smluv, pro které musí být vytvořeny faktury, vyhledává úloha data spuštění faktury pro řádky smluv. Jestliže řádky smluv, které patří k jedné smlouvě, mají stejné datum spuštění faktury, budou transakce sloučeny do jedné faktury, která má dva řádky faktury. Pokud neexistují žádné transakce pro vytvoření faktur, úloha přeskočí vytvoření faktury.

Proces **ProcessRunner** po svém dokončení volá proces **ProcessRunCaller**, poskytne čas ukončení a je zavřen. Proces **ProcessRunCaller** poté spustí časovač, který běží po dobu 24 hodin od zadaného času ukončení. Po doběhnutí časovače je **ProcessRunCaller** uzavřen.

Úloha dávkového zpracování pro vytváření faktur je opakující se úloha. Pokud je tento dávkový proces spuštěn vícekrát, vytvoří se více instancí této úlohy a způsobí chyby. Proto byste tento dávkový proces měli spustit pouze jednou a restartovat ho, pouze pokud přestane běžet.

> [!NOTE]
> Dávková fakturace běží pouze pro řádky projektové smlouvy, které jsou konfigurovány podle plánů faktur. Řáeke smlouvy s metodou fakturace s pevnou cenou musí mít nakonfigurované milníky. Řádek smlouvy o projektu s metodou fakturace času a materiálu bude vyžadovat sestavení časového rozvrhu faktur. Totéž platí pro řádek smlouvy založené na projektu.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]