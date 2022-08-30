---
title: Synchronizace stavu projektu, která brání úpravám uzavřených projektů
description: Tento článek vysvětluje, jak synchronizovat stav projektu, abyste zabránili úpravám neaktivních nebo uzavřených projektů.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348005"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synchronizace stavu projektu, která brání úpravám uzavřených projektů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

## <a name="scenario"></a>Scénář

Společnost Contoso zahájila ostrý provoz se scénáři Microsoft Dynamics 365 Project Operations založenými na zdrojích/položkách, které nejsou na skladě. V rámci běžných obchodních aktivit mohou být projekty dokončeny nebo pozastaveny. Projekt můžete deaktivovat, abyste zajistili, že nebudou generovány žádné výdaje ani faktury.

## <a name="solution"></a>Řešení

### <a name="prerequisites"></a>Předpoklady

-   Musí být nainstalována aplikace Microsoft Dynamics 365 Finance 10.0.29 nebo novější.
-   Mapu dvojího zápisu 1.0.0.3 pro Projects V2 (msdyn\_projects) musíte nainstalovat nebo ručně konfigurovat podle dále uvedeného popisu.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Vytvoření aktualizované verze mapy duálního zápisu Projects V2 integrace s Project Operations

Chcete-li aktualizovat mapování duálního zápisu Projects V2 v Project Operations:

1. Přejděte do pracovního prostoru **Správa dat** a vyberte **Duální zápis**.
2. Vyberte dlaždici **Duální zápis**.
3. Ve sloupci **Mapování tabulky** vyhledejte a vyberte entitu **Project V2 (msdyn\_projects)** a poté vyberte Zastavit.
4. Výběrem názvu mapy otevřete mapu a poté vyberte **[Žádný]**.
5. V dialogovém okně Vybrat sloupec vyberte **statecode \[Stav projektu\]** a poté vyberte OK. Počet hodnot v seznamu omezíte zápisem **state** v hodnotě filtru.
6.  Vyberte položku **Přidat nebo upravit transformaci** ve sloupci **typ mapy**, chcete-li transformaci upravit.
7.  V seznamu **Typ transformace** vyberte **ValueMap**.
8.  Vyberte položku **Přidat mapování hodnoty** a poté přidejte následující **Klíče** a **Hodnoty**:

   Key       | Hodnota 
   ----------|-------
   InProcess | 0     
   dokončené | 0     

![Snímek obrazovky zobrazující mapování duálního zápisu](media/projectstage-dw-mapping.png)

9. Vyberte **Uložit**.
10. V horní části stránky **Duální zápis > Projects V2 (msdyn_projects)** vyberte **Uložit jako**.
11. V podokně **Přidat tabulku** v poli **Vydavatel** vyberte **Výchozí vydavatel CDS**.
12. Nastavte pole **Verze** na 1.0.0.3.
13. Zadejte **Popis** a poté vyberte **Uložit**.
14. V horní části stránky **Duální zápis > Projects V2 (msdyn_projects)** vyberte **Spustit** a poté vyberte **Ano**, pokud budete požádáni o potvrzení před spuštěním. 

### <a name="close-a-newly-completed-project"></a>Zavření nově dokončeného projektu

Aplikace Dynamics 365 Finance používá pole **fáze projektu** pro rozlišení projektů **ve zpracování** a projektů **dokončených**. **Dokončené** projekty nemohou vynakládat výdaje ani být fakturovány zákazníkům.

1. Otevřete projekt, který chcete deaktivovat.
2. V pásu karet vyberte **Deaktivovat**.

> [!NOTE]
> Projekt můžete buď deaktivovat, nebo zavřít, protože oba se budou v kontextu Finance chovat stejně.

3. Ve Finance otevřete stránku **Seznam všech projektů**.
4. Potvrďte, že se deaktivovaný projekt nezobrazuje v seznamu.
5. Ve filtru **Zobrazit projekty** nad seznamem změňte hodnotu z **Aktivní** na **Vše**.
6. Nyní uvidíte deaktivovaný projekt.

Pokud se pokusíte zaznamenat čas nebo výdaje k tomuto projektu ve Finance, neměli byste mít možnost projekt vybrat. Pokud ručně zadáte číslo projektu ve výdaji, zobrazí se zpráva s hlášením „Dokončený projekt neumožňuje záznam do projektu“. Fakturace a další fakturační funkce by měly být deaktivovány, protože budou v kontextu uzavřeného projektu.

