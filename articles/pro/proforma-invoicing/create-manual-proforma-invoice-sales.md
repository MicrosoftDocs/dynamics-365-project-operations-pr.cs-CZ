---
title: Vytvoření manuální proforma faktury – omezené
description: Toto téma poskytuje informace o o vytváření manuálních proforma faktur v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764495"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Vytvoření manuální proforma faktury – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations lze proforma faktury podle potřeby vytvářet ručně. Proforma fakturu můžete ručně vytvořit na stránce seznamu **Projektové smlouvy** ze seznamu nebo ze stránky s podrobnostmi **Projektová smlouva**.

##  <a name="project-contracts-list-page"></a>Stránka se seznamem Projektové smlouvy

Na stránce se seznamem **Projektové smlouvy** vyberte jednu nebo více projektových smluv a vytvořte faktury pro všechny vybrané záznamy.

Systém zkontroluje, která z vybraných projektových smluv má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem. Z těchto smluv systém vytvoří koncepty proforma faktur. Pokud má projektová smlouva více zákazníků, může být vytvořena jedna faktura na zákazníka a více faktur na projektovou smlouvu.

Všechny vytvořené faktury projektu jsou k dispozici na stránce **Faktura** v části **Fakturace** oblasti **Prodej**.

## <a name="project-contract-details-page"></a>Stránka s podrobnostmi projektových smluv

Pro forma fakturu lze také vytvořit na stránce s podrobnostmi **Smlouva o projektu**. Systém ověří, že projektová smlouva má nevyřízené položky **Připraveno k fakturaci** datované před dnešním datem. Z těchto smluv systém vytváří návrhy proforma faktur na základě počtu zákazníků na každém řádku smlouvy.

Když je vytvořena jedna proforma faktura, otevře se stránka **Faktura**. Pokud je pro danou projektovou smlouvu vytvořeno více faktur, otevře se stránka seznamu **Faktury** se seznamem, kde se zobrazí všechny vytvořené faktury.
