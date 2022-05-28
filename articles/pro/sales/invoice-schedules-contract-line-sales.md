---
title: Vytvoření plánů faktur na řádku smlouvy na základě projektu – omezené
description: Tohle téma poskytuje informace o vytváření rozpisů faktur a milníků.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: edacae144f5c4879d3cfdf9585281858d7312589
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581966"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Vytvoření plánů faktur na řádku smlouvy na základě projektu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Můžete připojit rozpis faktur na řádku smlouvy na základě projektu. Fakturace je povolena až po získání smlouvy na vytvoření smlouvy projektu. Rozpisy faktur umožňují automatické vytváření konceptů faktur pro řádek smlouvy na základě projektu. Pokud plánujete vždy vytvářet faktury ručně, můžete přeskočit vytváření plánů faktur na řádku smlouvy na základě projektu nebo na řádku smlouvy.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Vytvoření rozpisu faktury času a materiálu pro řádek smlouvy na základě projektu

Když je metodou fakturace pro řádek smlouvy na základě projektu čas a materiál, můžete vytvořit rozpis faktur na základě data. Chcete-li automaticky vygenerovat plán faktur na základě data, proveďte následující kroky.

1. Jděte na **Nastavení** > **Četnosti faktur** a nastavte četnost faktur.
2. Otevřete smlouvu projektu a na kartě **Souhrn** nastavte požadované datum dodání.
3. Otevřete řádek smlouvy času a materiálu, pro který chcete vytvořit rozpis faktury na základě data. 
4. Na kartě **Rozpis faktury** vyberte počáteční datum fakturace a četnost fakturace. 
5. V podmřížce vyberte **Generovat rozpis faktur**.

    Systém generuje rozpis faktury s následujícími informacemi o poli:

    - **Datum spuštění faktury** je nastaveno na datum na základě četnosti fakturace.
    - **Mezní datum transakce** je nastaveno na den před **Datem spuštění faktury**.
    - **Stav spuštění** je automaticky nastaven na **Nespuštěno**. Když je úloha automatického vytváření faktur spuštěna pro určité **Datum spuštění faktury**, aktualizuje toto pole buď na **Úspěšné spuštění**, nebo **Neúspěšné spuštění**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Vytvoření rozpisu faktury pevné ceny pro řádek smlouvy na základě projektu

Pokud má řádek smlouvy na základě projektu metodu fakturace s pevnou cenou, můžete vytvořit rozpis faktury na základě milníků. Pomocí následujících kroků můžete automaticky vygenerovat rozpis faktury na základě milníků pro pevnou sadu milníků, které se rovnoměrně rozdělí pro kalendářní období.

1. Jděte na **Nastavení** > **Četnosti faktur** a nastavte četnost faktur.
2. Otevřete smlouvu projektu a na kartě **Souhrn** nastavte požadované datum dodání.
3. Otevřete řádek smlouvy s pevnou cenou, na kterém potřebujete vytvořit plán milníků. 
4. Na kartě **Rozpis faktury (Milníky fakturace)** vyberte počáteční datum fakturace a četnost fakturace. 
5. V podmřížce vyberte **Generovat periodické milníky**.

    Systém generuje rozpis faktury s následujícími informacemi o milníku:

    - **Název milníku** je nastaven na datum, které je diktováno na základě četnosti fakturace.
    - **Datum milníku** je nastaveno na datum, které je diktováno na základě četnosti fakturace.
    - **Částka milníku** se vypočítá vydělením částky smlouvy na řádku smlouvy na základě projektu počtem milníků diktovaných četností, začátkem fakturace a požadovanými termíny dodání.
    - Pokud má řádek smlouvy hodnotu v poli **Odhadovaná částka daně**, toto pole je také přiděleno stejně všem milníkům během generování pravidelných milníků.

Milníky fakturace by se měly rovnat smluvní hodnotě řádku smlouvy na základě projektu. Pokud se nerovnají, dojde k chybě. Tuto chybu můžete opravit tak, že ověříte, že milníky fakturace sečtou smluvní hodnotu řádku buď vytvořením, úpravou nebo odstraněním milníků. Po provedení změn stránku obnovte.

### <a name="manually-create-milestones"></a>Ruční vytváření milníků

Milníky pevné ceny lze generovat ručně, pokud nejsou pravidelně rozděleny. Chcete-li vytvořit milník ručně, proveďte následující postup.

1. Otevřete řádek smlouvy s pevnou cenou, na kterém chcete vytvořit milník. 
2. Na kartě **Rozpis faktury** v podmřížce vyberte **+ Vytvořit nový milník řádku smlouvy**.
3. V formuláři **Vytvoření milníku** zadejte požadované informace na základě následující tabulky. 

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Název milníku | Vytvořit | Textové pole pro název milníku. | Toto pole je zahrnuto v milníku řádku smlouvy o projektu a na faktuře. |
| Projektový úkol | Vytvořit | Pokud je milník svázán s úkolem projektu, použijte tento odkaz k přidání vlastní logiky a nastavení stavu milníku na základě stavu úkolu. | Neexistuje žádný následný dopad tohoto odkazu na úkol. |
| Datum milníku | Vytvořit | Datum, kdy by měl proces automatického vytváření faktur hledat stav tohoto milníku, aby jej mohl zohlednit pro fakturaci. | To je zahrnuto v milníku řádku smlouvy o projektu a na faktuře. |
| Stav faktury | Vytvořit | Při vytvoření milníku je tento stav vždy nastaven na **Nepřipraveno k fakturaci** nebo **Nezahájeno**. | To je zahrnuto v milníku řádku smlouvy o projektu a na faktuře. |
| Částka řádku | Vytvořit | Částka nebo hodnota milníku, která bude zákazníkovi fakturována. | Toto pole je zahrnuto v milníku řádku smlouvy o projektu a na faktuře. |
| Daň | Vytvořit | Částka daně použitá u milníku. | To je zahrnuto v milníku řádku smlouvy o projektu a na faktuře. |

4. Zvolte **Uložit a zavřít**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]