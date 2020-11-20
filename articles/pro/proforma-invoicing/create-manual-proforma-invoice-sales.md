---
title: Vytvoření manuální proforma faktury – omezené
description: Toto téma poskytuje informace o o vytváření manuálních proforma faktur v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176378"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Vytvoření manuální proforma faktury – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations lze proforma faktury vytvářet ručně podle potřeby. Proforma fakturu můžete ručně vytvořit na stránce seznamu **Projektové smlouvy** ze seznamu nebo ze stránky s podrobnostmi **Projektová smlouva**.

##  <a name="project-contracts-list-page"></a>Stránka se seznamem Projektové smlouvy

Na stránce se seznamem **Projektové smlouvy** vyberte jednu nebo více projektových smluv a vytvořte faktury pro všechny vybrané záznamy.

Systém zkontroluje, která z vybraných projektových smluv má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem. Z těchto smluv systém vytvoří koncepty proforma faktur. Pokud má projektová smlouva více zákazníků, může být vytvořena jedna faktura na zákazníka a více faktur na projektovou smlouvu.

Všechny vytvořené faktury projektu jsou k dispozici na stránce **Faktura** v části **Fakturace** oblasti **Prodej**.

## <a name="project-contract-details-page"></a>Stránka s podrobnostmi projektových smluv

Proforma fakturu lze také vytvořit na stránce s podrobnostmi **Smlouva o projektu**, kde se vytváří faktura za konkrétní smlouvu o projektu. Systém zkontroluje, že projektová smlouva má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem. Z těchto smluv systém vytváří návrhy proforma faktur na základě počtu zákazníků na každém řádku smlouvy.

Když je vytvořena jedna proforma faktura, otevře se stránka **Faktura**. Pokud je pro danou projektovou smlouvu vytvořeno více faktur, se otevře stránka se seznamem **Faktury**, kde se zobrazí všechny vytvořené faktury.
