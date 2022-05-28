---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o uznání výnosů v Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 51c553ecf45452615cbcadce6386f32be427acaa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601424"
---
# <a name="revenue-recognition-overview"></a>Přehled uznání výnosů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

v Dynamics 365 Project Operations se zásady uznání výnosů liší podle vybrané metody fakturace pro projekt nebo část projektu. Toto téma obsahuje informace o uznání výnosů v Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Zaúčtování transakcí pomocí způsobu fakturace času a materiálu

- Uznávání nákladů a výnosů je propojeno. Transakční náklady a nevyfakturované prodeje se zaúčtují pomocí [Deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md).
- Profil nákladů a výnosů projektu určuje, zda se nevyfakturované prodejní transakce zaúčtují do hlavní knihy. Je-li vybráno **Časově rozlišené výnosy**, systém během účtování použije účty **Hodnota prodeje probíhající práce (WIP)** a **Časově rozlišené výnosy – hodnota prodeje**. Následuje příklad této metody.  

  | Typ transakce | Debet / kredit | Množství |
  | --- | --- | --- |
  | Hodnota prodeje probíhající práce | Debet | 100 |
  | Časově rozlišené výnosy – hodnota prodeje | Kredit | 100 |

- Výnosy jsou uznané při fakturaci. Systém používá úšet **Fakturované výnosy** během účtování. Následuje příklad této metody.  

  | Typ transakce | Debet / kredit | Množství |
  | --- | --- | --- |
  | Zůstatek zákazníka | Debet | 120 |
  | Splatná DPH | Kredit | 20 |
  | Fakturované výnosy | Kredit | 100 |

- Pokud byly výnosy časově rozlišeny při zaúčtování nevyfakturovaných prodejů, systém tyto nashromážděné výnosy při fakturaci stornuje.

  | Typ transakce | Debet / kredit | Množství |
  | --- | --- | --- |
  | Hodnota prodeje probíhající práce | Kredit | 100 |
  | Časově rozlišené výnosy – hodnota prodeje | Debet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Zaúčtování transakcí pomocí způsobu fakturace fixní ceny

- Uznávání nákladů a výnosů je samostatné. Transakční náklady se zaúčtují pomocí [Deníku integrace Project Operations](../project-accounting/project-operations-integration-journal.md). Nevyfakturované prodejní transakce se nevytvářejí.
- Výnosy lze uznat během fakturace, pokud má profil nákladů a výnosy projektu vobu **Zásada použitá pro výpočty dokončení projektu** nastavenou na **Žádné probíhající práce**. Tuto metodu používejte pouze pro krátkodobé jednoduché projekty.
- Výnosy lze uznat pomocí odhadů výnosů s fixní cenou, a to buď metodou **Dokončená smlouva** nebo **Uznání výnosů z procentuálního dokončení**.

## <a name="additional-resources"></a>Další materiály
[Článek Konfigurace účetnictví pro fakturovatelné projekty](../project-accounting/configure-accounting-billable-projects.md)

[Projekty odhadu výnosů pevné ceny](rev-rec-percentage-completion-method.md)

[Správa odhadů výnosů](rev-rec-completed-contract-method.md)

[Náklady na dokončení metod](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]