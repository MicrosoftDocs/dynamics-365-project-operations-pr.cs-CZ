---
title: Důležité koncepce
description: Toto téma poskytuje informace o důležitých koncepcích správy zdrojů v Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 3a0305ab35a28348798f9d9c7452b3bee75412e4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601240"
---
# <a name="key-concepts"></a>Důležité koncepce

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Následující tabulka definuje klíčové koncepce, které se používají v aplikaci Dynamics 365 Project Service Automation.

| Koncepce                    | Definice |
|----------------------------|------------|
| Člen projektového týmu        | Člen projektového týmu může být jako součást projektového týmu pojmenovaným zdrojem, který má rezervace, pojmenovaným zdrojem, který nemá rezervace nebo obecným zdrojem. Obecné zdroje nemají rezervace, jsou pro projekt místní a nemají omezení kapacity v rámci projektů. |
| Obecný zdroj projektu   | Zástupný symbol zdroje, který umožňuje vytvořit tým a personálního obsazení plánu projektu, aniž by bylo nutné znát pojmenovaný zdroj. Kalendář projektu se používá jako kalendář obecného zdroje. Obecné zdroje mohou být přidány do projektového týmu a přiřazeny k úkolům. |
| Rezervované hodiny               | Hodiny zdroje jsou pro projekt závazně zarezervovány, aby pomohly zaručit dokončení práce na projektu. Zarezervované hodiny jsou spotřebovány z celkové kapacity zdroje. Rezervace jsou pouze proti pojmenovaným zdrojům, nikoli proti obecným zdrojům. |
| Přiřazené hodiny             | Hodiny zdroje jsou přiřazeny k úkolům v plánu projektu. Přiřazení mohou být buď proti pojmenovaným zdrojům, nebo obecným zdrojům. Přiřazení mohou být nezávislá na rezervacích. |
| Požadované hodiny             | Požadovaná kapacita, která ale není dosud splněna pomocí pojmenovaného zdroje. Požadované hodiny jsou relevantní pouze pro obecné členy týmu, kteří obsahují vygenerované požadavky na zdroje. |
| Poptávka                     | Aktuální a příchozí pracovní vytížení. V Project Service Automation je poptávka zobrazena jako požadavky na zdroje nebo žádosti o zdroje. |
| Požadavek na zdroj       | Entita, která slouží k zachycení požadovaných hodin, počátečního a koncového data, dovedností, zeměpisné oblasti a dalších cenových dimenzí pro požadované zdroje. Požadavky na zdroje jsou generovány buď od členů projektového týmu nebo jsou vytvořeny jednotlivě. |
| Žádost o zdroj           | Entita, která se používá jako obálka k přenosu požadavku na zdroj, který musí správce zdroje splnit. |
| Výchozí role zdroje      | Role, pod kterou je zdroj seskupen pro výpočet využití. Předpokládá se, že zdroj má požadované dovednosti pro roli a splní cílové využití pro tuto roli. |
| Organizační jednotka zdroje | Organizační jednotka, ke které je zdroj přiřazený. |
| Průběhová křivka                    | Hodiny úkolu, požadavku nebo přiřazení, které jsou rozděleny do denního rozdělení. Například pětidenní, 40hodinový úkol může být rozdělen na osm hodin denně za pět dní. |
| Zobrazení Vyrovnání        | Zobrazení, ve kterém jsou zobrazeny rezervace a přiřazení pro jednotlivé členy projektového týmu. Toto zobrazení umožňuje projektovému manažerovi vyhledat jakýkoli nesoulad mezi rezervacemi a přiřazeními a provést nápravné opatření, pokud k nějakému nesouladu dojde. |
| Pracovní doba                 | Entita, která slouží k identifikaci kapacity zdroje a pracovní a nepracovní doby. Tato entita je také označována jako kalendář zdroje. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
