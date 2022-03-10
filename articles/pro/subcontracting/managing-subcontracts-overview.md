---
title: Správa subdodávek ve službě Project Operations
description: Toto téma poskytuje přehled procesu správy komplexních subdodávek v Microsoft.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323588"
---
# <a name="subcontract-management-in-project-operations"></a>Správa subdodávek ve službě Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma poskytuje přehled procesu správy komplexních subdodávek v projektových organizacích. Subdodávky pro služby se obvykle řídí tokem obchodního procesu, který je uveden v následujícím diagramu.

![Tok subdodavatelských procesů](../media/SubcontractingProcessFlow.png)

Následující seznam obsahuje podrobný popis procesu subdodávky.

1. Projektový manažer vytvoří subdodávku s dodavatelem. Pro subdodávku se standardně používají ceníky, které jsou připojeny k záznamu dodavatele. Účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**.
2. Projektový manažer může všechny nákupy rozdělit do řádkových položek na subdodávku. Řádky subdodávky mohou být na čas, výdaje nebo produkty. Třída transakce každého řádku subdodávky určuje, k čemu daný řádek slouží.
3. Správce obchodního vztahu prodejce a správce projektu mohou iterovat subdodávku. Cenu lze upravit v nákupních cenících, které jsou přiřazeny k subdodávce.
4. Pokud je v tomto okamžiku nebo později v procesu řádek subdodávky na čas, správce účtu dodavatele přidruží kontakty dodavatele ke každému řádku subdodávky. Toto sdružení poskytuje informace projektovému manažerovi, který pracuje na subdodávce. Když je dodavatelský kontakt spojen s řádkem subdodávky, systém automaticky vytvoří rezervovatelný zdroj z kontaktu, pokud rezervovatelný zdroj již neexistuje.
5. Způsob účtování na každém řádku subdodávky může být **Pevná cena** nebo **Čas a materiál**. U řádků subdodávek s pevnou cenou můžete nastavit plán faktur na základě milníků.
6.  Poté, co je subdodávka nastavena a vyjednávání je dokončeno, je potvrzeno. Potvrzené subdodávky nelze upravovat, ale pokud dojde ke změnám, lze subdodávku „znovu otevřít pro úpravy“. Nastaví se stav z **Potvrzeno** zpět na **Návrh** a vyjednávání lze znovu otevřít. 
7.  Při vytváření generického člena týmu v projektu může být člen týmu přidružen k řádku subdodávky. To naznačuje potřebu obsazení generického člena týmu kapacitou subdodavatele.
8.  Pojmenovaní členové týmu mohou být buď vytvořeni přímo v projektu, nebo vytvořeni rezervací využitím zkušeností s plánováním zdrojů. Pokud je pojmenovaný člen projektového týmu smluvním pracovníkem, je možné jej přiřadit k řádku subdodávky. Tím se vyčerpá dostupná kapacita na řádku subdodávky.
9.  Zdroje subdodavatele mohou protokolovat čas, výdaje a využití materiálu v projektech a úkolech projektu a potom je odeslat ke schválení. U zaměstnanců je to podobné. Při záznamu času může smluvní pracovník vybrat konkrétní subdodávku a řádek subdodávky.
10. Při schvalování se budou v čase schválení subdodavateli zaznamenávat skutečné náklady projektu na základě kupní ceny smluvního pracovníka nebo role, kterou na projektu vykonával.
11. Faktury dodavatele a řádkové položky faktury dodavatele lze v systému zaznamenat za práci provedenou zdroji dodavatele nebo za produkty dodané dodavatelem. Řádky faktury dodavatele musejí být specifické pro projekt a pro čas třídy transakcí, náklady, produkt/materiál, milník nebo poplatek. Volitelně mohou řádky faktury dodavatele odkazovat na řádek subdodávky.
12. Systém automaticky přiřadí k faktuře dodavatele všechny skutečné náklady, které odpovídají řádku subdodávky a projektu. To usnadní třícestný proces shody a proces ověření.
13. Vedoucí projektu potom může zkontrolovat automaticky přiřazené skutečné údaje o projektu, odebrat nebo přidat další skutečné náklady projektu a dokončit proces ověření.
14. Dokončení procesu ověření na všech řádcích označí fakturu dodavatele jako **Připraveno k platbě**. V této fázi lze fakturu a řádky dodavatele převést do systému účetnictví nebo závazků za účelem zpracování platby dodavateli. Dříve zaznamenané náklady projektu budou stornovány a skutečné náklady z řádku faktury dodavatele budou zaznamenány do projektu.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Množstevní řádky subdodávky a pracovní řádky subdodávky

Řádek subdodávky může být množství nebo pracovní. 

Když je řádek subdodávky **množstevní** kupované množství zakoupené na řádku subdodávky na čas, náklady nebo materiál lze použít na jakýkoli projekt.

Když je řádek subdodávky **pracovní**, řádek subdodávky se mapuje na soubor prací reprezentovaný uzlem v plánu projektu. Hodnota řádku subdodávky je součtem všech komponent, které jsou nutné k provedení souboru prací. Jsou modelovány jako podrobnosti řádku subdodávky a může se jednat o kolekci času, nákladů nebo materiálů. V případě řádku subdodávky na základě práce je řádek subdodávky také vyhrazen pro jeden projekt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

