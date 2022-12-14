---
title: Konfigurace účtovatelných součástí na řádku projektové smlouvy
description: Tento článek poskytuje informace o tom, jak přidat účtovatelné komponenty do smluvních řádků v Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825556"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfigurace účtovatelných součástí na řádku projektové smlouvy

_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádek smlouvy na základě projektu má *zahrnuté* komponenty a *účtovatelné* komponenty.

Zahrnuté komponenty jsou komponenty, které podléhají:

  - Způsob fakturace a rozdělení zákazníků
  - Nepřekročitelné limity 
  - Nastavení frekvence faktur definované na řádku smlouvy na základě projektu

Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**. Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku smlouvy:

  - Účtovatelné
  - Neúčtovatelné

Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.

Účtovatelnost je definována na úkolech pro řádek smlouvy projektu a platí pro všechny třídy transakcí zahrnutých na řádku. Pokud je pole **Zahrnout úkoly** na řádku smlouvy prázdné nebo je nastaveno na **Celý projekt**, karta **Účtovatelné úlohy** nebude k dispozici.

Účtovatelnost definovaná pro role pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Čas**. Pokud je pole **Zahrnout čas** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné role** nebude k dispozici.

Účtovatelnost definovaná na kategoriích transakcí pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Výdaj**. Pokud je pole **Zahrnout výdaje** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné kategorie** nebude k dispozici.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného

Úkol projektu může být účtovatelný nebo neúčtovatelný na konkrétním řádku smlouvy, což umožňuje následující nastavení:

Pokud řádek smlouvy na základě projektu zahrnuje **Čas** a určitý úkol, **T1** je k němu přidruženo jako účtovatelné. Pokud existuje druhý řádek smlouvy, který zahrnuje **Výdaje**, můžete úkol T1 na řádku smlouvy asociovat jako neúčtovatelný. Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady jsou neúčtovatelné.

Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku smlouvy aktualizací pole **Typ fakturace** v podmřížce Úkoly řádku smlouvy. Alternativně můžete aktualizovat pole **Typ fakturace** v nastavení fakturace úkolu projektu, které zobrazuje řádky smluv přidružené k úkolu.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Nastavení role jako účtovatelné nebo neúčtovatelné

Role může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.

Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku smlouvy. Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné role**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné

Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.

Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku smlouvy na základě projektu. Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.

### <a name="resolve-chargeability"></a>Vyřešení účtovatelnosti

Vytvořený odhad nebo skutečná hodnota pro čas bude považována za účtovatelnou, pouze pokud:

   - **Čas** je uveden v řádku smlouvy.
   - **Role** je nakonfigurována jako účtovatelná na řádku smlouvy.
   - **Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku smlouvy.
 
 Pokud jsou tyto tři věci pravdivé, úkol je také nakonfigurován jako účtovatelný. 

Vytvořený odhad nebo skutečná hodnota pro výdaj bude považována za účtovatelnou, pouze pokud:

   - **Výdaj** je uveden v řádku smlouvy
   - **Kategorie transakce** je nakonfigurována jako účtovatelná na řádku smlouvy
   - **Zahrnuté úkoly** je nastaveno na **Vybraný úkol** na řádku smlouvy
  
 Pokud jsou tyto tři věci pravdivé, **úkol** je také nakonfigurován jako účtovatelný. 

Vytvořený odhad nebo skutečná hodnota pro materiál bude považována za účtovatelnou, pouze pokud:

   - **Materiály** je uvedeno v řádku smlouvy
   - **Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku smlouvy

Pokud jsou tyto dvě věci pravdivé, **úkol** je také nakonfigurován jako účtovatelný. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Zahrnuje čas</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Zahrnuje výdaj</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Zahrnuje materiály</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Zahrnuté úkoly</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Role</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategorie</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Úkol</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Dopad účtovatelnosti</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Účtovatelné</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Účtovatelné</strong>
                </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: <strong>účtovatelná</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Účtovatelné</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Účtovatelné</strong>
                </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: <strong>účtovatelná</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: Účtovatelné </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: účtovatelná </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </p>
                <p>
Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </p>
                <p>
Typ fakturace při skutečném materiálu: <strong>Neúčtovatelné</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: účtovatelná </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Účtovatelné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: Účtovatelné </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: účtovatelná </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Není k dispozici</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: účtovatelná </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="70" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: Účtovatelné </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: účtovatelná </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ano </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Není k dispozici</strong>
                </p>
                <p>
Typ fakturace na skutečnou hodnotu materiálu: účtovatelná </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="70" valign="top">
                <p>
Účtovatelné </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: Účtovatelné </p>
                <p>
Typ fakturace při skutečných výdajích: Účtovatelné </p>
                <p>
Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ano </p>
            </td>
            <td width="78" valign="top">
                <p>
Ano </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Celý projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neúčtovatelné</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nelze nastavit </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: <strong>Neúčtovatelná</strong>
                </p>
                <p>
Typ fakturace při skutečných výdajích: <strong>Neúčtovatelné</strong>
                </p>
                <p>
Typ fakturace při skutečném materiálu: <strong>Není k dispozici</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
