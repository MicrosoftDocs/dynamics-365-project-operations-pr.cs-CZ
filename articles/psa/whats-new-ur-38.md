---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 38, V3
description: Toto téma obsahuje funkce a opravy, které jsou k dispozici ve Microsoft Dynamics 365 Project Service Automation vydání aktualizace 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598710"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci pro aplikaci Microsoft Dynamics 365 Project Service Automation. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Je kompatibilní s Dynamics 365 9.x. Chcete-li provést aktualizaci na toto vydání, navštivte stránku Centra pro správu online řešení Dynamics 365 a nainstalujte aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 38 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.59.117 a je obecně dostupná prostřednictvím vlastní aktualizace v prosinci 2021.

## <a name="update-release-38"></a>Aktualizace verze 38

### <a name="bug-fixes"></a>Opravy chyb

Byly vyřešeny následující problémy.

**Čas a výdaje**

- Dojde k výjimce, když délka protokolů sady schválení překročí 100 000 záznamů.
- Uživatelé nemají přístup k mřížce **Časový záznam** z hlavní stránky **Časový záznam**.
- Dialog **Import časového záznamu** nezobrazí žádný text, když nejsou žádné položky vhodné pro import.
- Uživatelé mohou vytvářet sady schválení, kde je pole **Cílový stav** nastaveno na **Neznámý**.

**Správa projektů**

- Průběhové křivky nejsou správně zobrazeny v přiřazení zdrojů pro čas UTC (+09:30) a UTC (+10:00), když začíná letní čas.
- Pole **Dodatečný sloupec** pro strukturovaný rozpis prací je v některých místních prostředích skryto.
- Ovládací prvek výběru data pro ovládací prvek kalendáře v mřížce **Projektový úkol** není správně lokalizován pro čínštinu.

**Prodej**

- Hodnoty **Plnění smlouvy** a **Skutečné náklady projektu** se neshodují, když rezervovatelné zdroje, které mají různé smluvní jednotky a měny, odešlou časové záznamy.
- Vlastní pracovní postup pro automatické potvrzování faktur selže, když jsou faktury importovány jako spravované řešení. Zobrazí se následující zpráva: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Neplatný stav faktury."
- Když je **Kořen** vybrán jako možnost sumarizace a projekt má odhady ze směsi tříd transakcí (například kombinace odhadů času, výdajů a materiálu), systém sumarizuje třídy transakcí jako jeden řádek poplatků.
- Ve scénářích, kdy je řádek výdajů přidaný před řádek smlouvy přidružen k projektu, není správná cena zadána jako výchozí hodnota v poli **Aktualizovat cenu**.
- U entit **Projekt** a **Úkol** nejsou povoleny záporné částky prodeje.
