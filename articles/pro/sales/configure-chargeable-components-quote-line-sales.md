---
title: Konfigurace účtovatelných součásti řádku nabídky
description: Tento článek poskytuje informace o nastavení účtovatelných a neúčtovatelných komponent na řádku projektové nabídky.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4829055f429546c7911a05a765bc28ae085afa1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930034"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurace účtovatelných součásti řádku nabídky 

_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádek nabídky na základě projektu má koncept *zahrnutých* komponent a *účtovatelných* komponent.

Zahrnuté součásti podléhají:

  - Způsob fakturace a rozdělení zákazníků
  - Nepřekročitelné limity 
  - Nastavení frekvence faktur definované na řádku nabídky na základě projektu

Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**. Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku nabídky:

  - Účtovatelné
  - Neúčtovatelné

Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.

Účtovatelnost je definována na úkolech pro řádek nabídky a platí pro všechny třídy transakcí zahrnutých na řádku. Pokud je pole **Zahrnout úkoly** nastaveno na **Celý projekt** nebo ponecháno prázdné, karta **Účtovatelné úlohy** není k dispozici.

Účtovatelnost definovaná pro role pro řádek nabídky se vztahuje pouze na třídu transakcí **Čas**. Pokud je pole **Zahrnout čas** na řádku nabídky projektu nastaveno na **Ne**, karta **Účtovatelné role** není k dispozici.

Účtovatelnost definovaná na kategoriích transakcí pro řádek nabídky se vztahuje pouze na třídu transakcí **Výdaj**. Pokud je pole **Zahrnout výdaje** na řádku nabídky projektu nastaveno na **Ne**, karta **Účtovatelné kategorie** není k dispozici.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného

Úkol projektu může být účtovatelný nebo neúčtovatelný v kontextu konkrétního řádku nabídky podle projektu, což umožňuje následující nastavení.

Pokud řádek nabídky na základě projektu zahrnuje **Čas** a úkol **T1**, úkol je přidružen k řádku nabídky jako účtovatelný. Pokud existuje druhý řádek nabídky , který zahrnuje **Výdaje**, můžete úkol **T1** na řádku nabídky asociovat jako neúčtovatelný. Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady zaznamenané na úkolu jsou neúčtovatelné.

Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku nabídky založeného na projektu aktualizací pole **Typ fakturace** v podmřížce **Úkoly řádku nabídky**. Alternativně můžete aktualizovat typ fakturace pro projektový úkol v poli **Typ fakturace** v podmřížce v nastavení fakturace úkolu projektu, které zobrazuje řádky nabídek přidružené k úkolu.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Nastavení role jako účtovatelné nebo neúčtovatelné

Role může být účtovatelná nebo neúčtovatelná v kontextu konkrétního řádku nabídky založeného na projektu.

Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku nabídky aktualizací pole **Typ fakturace** v podmřížce **Účtovatelné role**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné

Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku nabídky.

Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku nabídky aktualizací pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.

### <a name="resolve-chargeability"></a>Vyřešení účtovatelnosti
Vytvořený odhad nebo skutečná hodnota pro čas bude považována za účtovatelnou, pouze pokud:

   - **Čas** je uveden v řádku nabídky.
   - **Role** je nakonfigurována jako účtovatelná na řádku nabídky.
   - **Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku nabídky. 

Pokud jsou tyto tři věci pravdivé, **Úkol** je také nakonfigurován jako účtovatelný. 

Vytvořený odhad nebo skutečná hodnota pro výdaj bude považována za účtovatelnou, pouze pokud: 

   - **Výdaj** je uveden v řádku nabídky.
   - **Kategorie transakce** je nakonfigurována jako účtovatelná na řádku nabídky.
   - **Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku nabídky.

Pokud jsou tyto tři věci pravdivé, **Úkol** je také nakonfigurován jako účtovatelný. 

Vytvořený odhad nebo skutečná hodnota pro materiál bude považována za účtovatelnou, pouze pokud:

   - **Materiály** je uvedeno v řádku nabídky.
   - **Zahrnuté úkoly** je nastaveno na **Vybrané úkoly** na řádku nabídky.

Pokud jsou tyto dvě věci pravdivé, **Úkol** je také nakonfigurován jako účtovatelný. 


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
Skutečná fakturace na čas: Účtovatelné </p>
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
Účtovatelné </p>
            </td>
            <td width="350" valign="top">
                <p>
Skutečná fakturace na čas: Účtovatelné </p>
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
