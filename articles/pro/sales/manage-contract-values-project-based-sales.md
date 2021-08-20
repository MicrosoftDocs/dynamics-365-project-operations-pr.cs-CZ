---
title: Přehled řádků smlouvy založené na projektu
description: Tohle téma poskytuje informace o práci s řádky smlouvy na základě projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999038"
---
# <a name="project-based-contract-lines-overview"></a>Přehled řádků smlouvy založené na projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řádky smlouvy na základě projektu v Dynamics 365 Project Operations jsou navrženy tak, aby obsahovaly odhad a řešení fakturace pro konkrétní součásti projektové práce na aktivitě. Struktura řádku smlouvy na základě projektu je rozšířena pro odhady projektu a scénáře fakturace o následující koncepty:

- Způsob fakturace
- Projekt a mapování úkolů
- Zahrnuté třídy transakcí
- Nepřekročitelný limit
- Nastavení účtovatelnosti
- Odhady pomocí podrobností řádku smlouvy
- Zákazníci řádku smlouvy

Následující tabulka obsahuje pole na kartě **Obecné** pro řádky smlouvy založené na projektu, které pomáhají připravit základ pro podrobný odhad a řešení fakturace pro projektovou práci.

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| **Jméno** | Název řádku smlouvy. Tento název označuje diskrétní složku smlouvy, která se odhaduje. U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídající hodnoty řádku nabídky na základě projektu. | Tento název je zkopírován do řádku faktury projektu, který je vytvořen z tohoto řádku smlouvy při vytváření faktury. |
| **Způsob fakturace** | U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídajícího pole na řádku nabídky. Toto je sada možností, která představuje dva hlavní smluvní modely podporované v Project Operations:</br>- **Pevná cena**</br>- **Čas a materiál** | Na základě způsobu fakturace odkazované řádky smlouvy bude zpracována samotná transakce. Pokud má řádka smlouvy odkazovaná skutečnou hodnotou metodu fakturace času a materiálu, vytvoří se záznamy skutečných nákladů a nefakturovaného prodeje. Pokud má řádek smlouvy, na který odkazuje skutečná hodnota, způsob fakturace s pevnou cenou, vytvoří se pouze skutečné náklady. |
| **Project** | Toto pole použijte k identifikaci projektu, který bude použit k provedení práce na této aktivitě. | Tato hodnota bude použita ve spojení se **Zahrnutými úkoly** a **Zahrnutými třídami transakcí** k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty. |
| **Zahrnuté úkoly** | Označuje, zda tento řádek smlouvy zahrnuje všechny projektové úkoly pro vybraný projekt nebo pouze podmnožinu úkolů. Jedná se o sadu možností s následujícími možnými hodnotami:</br>- **Všechny projektové úkoly**</br>- **Pouze vybrané úkoly projektu**. Prázdná hodnota v tomto poli se rovná výběru **Všechny projektové úkoly**. | Pokud je vybrána možnost **Pouze vybrané úkoly**, můžete vybrat konkrétní úkoly a přidružit je k tomuto řádku smlouvy na kartě **Nastavení účtování úkolů** na stránce **Projekt**. Tato hodnota se použije v souvislosti s poli **Projekt** a **Zahrnuté třídy transakcí** ke čtení odkazu na řádek smlouvy v záznamu skutečného nebo odhadovaného řádku. |
| **Zahrnout čas** | Hodnota **Ano**/**Ne** označuje, zda budou do na tomto řádku smlouvy zahrnuty časové transakce nebo náklady práce na vybraném projektu. Hodnota **Ne** označuje, že časové transakce nebo mzdové náklady nebudou zahrnuty do tohoto řádku smlouvy. Hodnota **Ano**, znamená že ano. | Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty. |
| **Zahrnout výdaj** | Hodnota **Ano**/**Ne** označuje, zda budou do tohoto řádku smlouvy zahrnuty náklady výdajů na vybraném projektu. Hodnota **Ne** označuje, že výdajové náklady nebudou zahrnuty do tohoto řádku smlouvy. Hodnota **Ano**, znamená že ano. | Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty. |
| **Zahrnout materiály** | Hodnota **Ano**/**Ne** označuje, zda budou do tohoto řádku smlouvy zahrnuty náklady materiálu na vybraném projektu. Hodnota **Ne** označuje, že nebudou do řádku smlouvy zahrnuty náklady na materiál. Hodnota **Ano**, znamená že ano. | Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty. |
| **Zahrnout poplatek** | Hodnota **Ano**/**Ne** označuje, zda budou do tohoto řádku smlouvy zahrnuty poplatky na vybraném projektu. Hodnota **Ne** označuje, že poplatky nebudou zahrnuty do tohoto řádku smlouvy. Hodnota **Ano**, znamená že ano. | Tato hodnota se používá ve spojení s projektem k vyřešení odkazu na řádek smlouvy na záznamu řádku skutečné nebo odhadované hodnoty. |
| **Nasmlouvaná částka** | Na řádku smlouvy s pevnou cenou je tato částka dohodnutá hodnota, která bude zákazníkovi fakturována za všechny součásti práce přidružené k tomuto řádku smlouvy. Na řádku smlouvy času a materiálu je tato částka odhadnutá hodnota, co bude zákazníkovi fakturováno za všechny součásti práce přidružené k tomuto řádku smlouvy. U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídajícího pole na řádku nabídky. Pokud má řádek smlouvy na základě projektu podrobnosti, je toto pole uzamčeno pro úpravy a shrnuto z částky v podrobnostech řádku smlouvy. | Pokud řádek smlouvy obsahuje podrobnosti, lze tuto hodnotu upravit změnou částek v podrobnostech řádku. Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování částky před daní z milníků periodické fakturace. |
| **Odhad daně** | Uživatel může toto pole upravit a zadat odhadovanou částku daně na řádku smlouvy. Pokud má řádek smlouvy na základě projektu podrobnosti, je toto pole uzamčeno pro úpravy a shrnuto z částky daně v podrobnostech řádku smlouvy. | Pokud řádek smlouvy obsahuje podrobnosti, lze tuto hodnotu upravit změnou částek daně v podrobnostech řádku. Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování daně z milníků periodické fakturace. |
| **Nasmlouvaná částka včetně daně** | Řádka smlouvy s částkou včetně daně Toto pole je jen pro čtení a počítá se jako **Nasmlouvaná částka + daň**. | Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování milníků periodické fakturace. |
| **Nepřekročitelný limit** | Uživatel může toto pole upravit a je k dispozici pouze na řádcích smlouvy založené na projektu se způsobem fakturace nastaveným na čas a materiál. | Uživatel může toto pole upravit. Když skutečná hodnota času a materiálu odkazuje na tento řádek smlouvy pro čas a materiál, skutečná částka je vyhodnocena vůči nepřekročitelnému limitu na tomto řádku smlouvy. Toto vyhodnocení je dokončeno po započítání již utracených a potvrzených částek. |
| **Rozpočet zákazníka** | Toto pole je upravitelné a je zkopírováno z odpovídajícího pole na řádku nabídky, pokud byla smlouva vytvořena z nabídky. | Toto pole slouží pouze pro informaci a nemá žádný následný význam. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravidla ověření pro možnosti na kartě Obecné pro řádky smlouvy založené na projektu

Pravidlo 1: Pokud je pole **Zahrnuté úkoly** prázdné nebo nastavené na **Všechny projektové úkoly**, všechny projektové úkoly jsou zahrnuty na řádku smlouvy.

Pravidlo 2: Když je pole **Zahrnuté úkoly** prázdné nebo explicitně nastaveno na **Všechny projektové úkoly**, projekt a určitou třídu transakcí lze zahrnout pouze do jedné řádky smlouvy na základě projektu.

Pravidlo 3: Když je pole **Zahrnuté úkoly** nastaveno na **Pouze vybrané projektové úkoly**, projekt a určitou třídu transakcí lze zahrnout pouze do více řádek smlouvy na základě projektu.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Smlouva</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Řádek smlouvy</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Zahrnuté úkoly</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zahrnout čas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zahrnout výdaj</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Zahrnout materiály</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Zahrnout</strong>
                </p>
                <p>
                    <strong>Poplatek</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Platné / Neplatné</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Důvod</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 2. Čas, náklady, materiály a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 i ŘN2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 2. Čas, materiály a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 i ŘN2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Čas, materiály a poplatky za projekt P1 jsou zahrnuty na ŘN1.
                </p>
                <ul>
                    <li>
Výdaje v projektu P1 jsou zahrnuty na řádku ŘS2.
                    </li>
                </ul>
                <p>
Žádné překrývání toho, co je zahrnuto na každém řádku smlouvy, a proto je zadání platné.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 2 </p>
                <p>
Č1 zahrnuje čas, materiály, výdaje a poplatky za podmnožinu úkolů v projektu P1.
                </p>
                <p>
ŘN2 zahrnuje čas, materiály, výdaje a poplatky za celý projekt P1, a proto se překrývá s tím, co je zahrnuto v S1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Podle pravidla č. 3 </p>
                <p>
Č1 zahrnuje čas, výdaje, materiály, výdaje a poplatky za podmnožinu úkolů v projektu P1.
                </p>
                <p>
ŘN2 zahrnuje čas, výdaje, materiály a poplatky za podmnožinu úkolů v projektu P1.
                </p>
                <p>
Jediná další validace je kolem podmnožiny úkolů na ŘN1, která se liší od podmnožiny úkolů na ŘN2, aby se zajistilo, že nedojde k překrývání. Toto provádí systém, když jsou přidruženy úkoly.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
S1 </p>
            </td>
            <td width="65" valign="top">
                <p>
ŘS2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
