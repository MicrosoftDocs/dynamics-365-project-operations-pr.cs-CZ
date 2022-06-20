---
title: Vytváření a potvrzení deníků oprav
description: Tento článek poskytuje informace o vytváření a potvrzování deníku oprav.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928056"
---
# <a name="create-and-confirm-correction-journals"></a>Vytváření a potvrzení deníků oprav

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Občas může být nesprávně zadán čas nebo výdaj. Konzultant může například vybrat nesprávné datum při vytváření časového záznamu nebo může vybrat nesprávný projekt, když zadává výdaj. Pokud konzultant nemůže aktualizovat odeslané záznamy, může back-end správce přímo opravit skutečné hodnoty pro projekt.

## <a name="correct-approved-time-entries"></a>Oprava schválených časových údajů     

Chcete-li opravit jeden nebo více časových záznamů pro projekt, proveďte následující kroky.

1. V oblasti **Prodej** vyberte **Transakce** a poté vyberte **Schválený čas**. 

2. V seznamu **Schválený čas** vyhledejte a vyberte jeden nebo více schválených časových záznamů, které chcete opravit. Pomocí filtru můžete vyhledat související položky. Můžete například filtrovat ID projektu a vybrat všechny schválené časové záznamy s tímto ID projektu.

3. Zvolte **Opravit položky**. Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava času**. Vybrané položky se přidají do deníku. 

4. Na stránce **Nový deník** zadejte **Popis** pro svůj deník oprav a poté vyberte kartu **Opravy časových záznamů**.  

5. V části **Nové hodnoty pro časové záznamy** aktualizujte pole správnými informacemi podle potřeby. Například můžete změnit přiřazený projekt nebo rezervovatelný zdroj.

6. Vyberte **Náhled**. V dialogovém okně vyberte **OK**. Na kartě **Řádky deníku** můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným časovým záznamům, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny. Pokud je třeba provést další opravy, opakujte kroky 5 a 6. 

    > [!NOTE]
    > Všechny opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro časové záznamy**.

7. Pokud se opravy objeví podle očekávání, vyberte **Potvrdit**. V dialogovém okně vyberte **OK**.

8. Vraťte se do části **Prodej**, vyberte **Projekty** a poté otevřete projekt, pro který jste právě aktualizovali časové záznamy. 

9. Na stránce **Projekty** na kartě **Skutečné hodnoty** zobrazte provedené změny. 

    > [!NOTE]
    > Pokud není karta **Skutečné hodnoty** viditelná, vyberte **Související** > **Skutečné hodnoty**.  

10. V seznamu **Přidružené zobrazení skutečností** můžete vidět, že původní časové záznamy, které byly stornovány, jsou stále uvedeny, stejně jako odpovídající opravené časové záznamy. 

 
## <a name="correct-approved-expense-entries"></a>Oprava schválených záznamů výdajů

Chcete-li opravit jeden nebo více záznamů výdajů, proveďte následující kroky. 

1. V části **Prodej** v levém navigačním podokně pod možností **Transakce** vyberte **Schválené výdaje**.

2. V seznamu **Schválené výdaje** vyberte projekt, který chcete opravit, a poté vyberte **Opravit položky**. Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava výdajů**. 

3. Na stránce **Nový deník** zadejte **Popis** pro opravu a na kartě **Oprava výdajů** v části **Nové hodnoty nákladů** vyberte datová pole, která chcete opravit pro vybrané řádky výdajů. Například můžete přiřadit výdaje jinému **projektu**, nebo opravit **Kategorie výdajů**, **Datum výdaje**, nebo **Rezervovatelný zdroj**.

4. Vyberte **Náhled**. V dialogovém okně vyberte **OK**. 

5. Na kartě **Řádky deníku** ověřte opravy. Můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným záznamům výdajů, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny.

6. Pokud opravené hodnoty odpovídají očekávání, vyberte **Potvrdit**. V dialogovém okně vyberte **OK**. Pokud se hodnoty nezobrazují podle očekávání, vyberte **Zrušit** a vraťte se do seznamu **Schválené výdaje**. Opakujte kroky 2 až 5. 

7. Po potvrzení deníku oprav se vraťte k projektu nebo projektům, které jste aktualizovali, abyste viděli své změny.

8. Na stránce projektu na kartě **Skutečné hodnoty** zkontrolujte seznam **Přidružené zobrazení skutečných hodnot**. Jsou uvedeny původní záznamy a opravené záznamy.


## <a name="correct-approved-material-usage-logs"></a>Oprava protokolů schváleného použití materiálu

Chcete-li opravit jeden nebo více záznamů v protokolu použití materiálu, proveďte následující kroky.

1. V oblasti **Prodej** v levém navigačním podokně v sekci **Transakce** vyberte **Skutečné hodnoty**.

2. V seznamu **Skutečné hodnoty** pomocí sloupcových filtrů vyberte třídu transakcí **Materiál**, takže jsou zobrazeny pouze skutečné hodnoty materiálů. K dalšímu omezení zobrazených skutečných hodnot použijte filtry dalších sloupců. Poté, co najdete požadovanou sadu skutečných hodnot, vyberte skutečné hodnoty a poté vyberte **Opravit položky**. Automaticky se vytvoří nový deník oprav a je přiřazen typ **Oprava materiálu**.

3. Na stránce **Nový deník** v poli **Popis** zadejte popis opravy. Poté na kartě **Oprava materiálu** v sekci **Nové hodnoty pro materiály** vyberte datová pole, která chcete u vybraných materiálových řádků opravit. Můžete například přiřadit materiál k jinému projektu nebo opravit produkt, datum materiálu nebo subdodávku.

4. Vyberte **Náhled**. Poté v dialogovém okně vyberte **OK**.

5. Na kartě **Řádky deníku** ověřte provedené opravy. Můžete zobrazit seznam původních skutečných hodnot, které souvisejí s vybranými stornovanými položkami materiálu a opravenými odpovídajícími řádky, které byly vytvořeny.

6. Pokud opravené hodnoty odpovídají očekávání, vyberte **Potvrdit**. Poté v dialogovém okně vyberte **OK**. Pokud hodnoty nejsou podle očekávání, příkazem **Zrušit** se vraťte do seznamu **Skutečné hodnoty**. Pak opakujte kroky 2 až 5.

7. Po potvrzení deníku oprav se vraťte k projektu nebo projektům, které jste aktualizovali, abyste viděli své změny.

8. Na stránce projektu na kartě **Skutečné hodnoty** zkontrolujte seznam **Přidružené zobrazení skutečných hodnot**. Jsou uvedeny původní záznamy a opravené záznamy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
