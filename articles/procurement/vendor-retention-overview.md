---
title: Přehled zádržného dodavatele
description: Toto téma poskytuje přehled o možnostech zádržného dodavatele.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588452"
---
# <a name="vendor-retention-overview"></a>Přehled zádržného dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Vaše organizace může chtít zadržet část plateb dodavatelům, kteří pracují na projektech pro vaši organizaci. Například než zaplatíte prodejci, možná budete chtít zajistit, aby položky a služby, které poskytoval, splňovaly vaše očekávání.

Když vyjednáváte nákupy pro projekty s dodavateli, můžete určit podmínky zádržného dodavatele, které obsahují procento nebo částku, která má být zadržena. Když dodavatel dodává položky a služby, odečtete zadané procento nebo částku zádržného z vaší platby dodavateli. Když je projekt dokončen nebo dosáhne přechodné fáze, jak je uvedeno ve smlouvě s dodavatelem, uvolníte zadrženou částku a vytvoříte platbu dodavatele.

## <a name="vendor-retention-example"></a>Příklad zádržného dodavatele

Následující příklad ukazuje, jak je zadrženo procento z částky faktury dodavatele na základě procenta dokončení projektu.

Společnost Contoso Robotics USA uzavřela smlouvu s prodejcem Fabrikam na provedení 100 hodin školení pro projekt obnovy vybavení. Celková hodnota smlouvy je 30 000 USD s dohodnutou kupní cenou 300 USD za hodinu.

Školení bude probíhat ve třech fázích s následujícím rozvrhem:

- Fáze 1: 50 hodin, neboli 50 procent projektu
- Fáze 2: 30 hodin, neboli 80 procent projektu celkem
- Fáze 3: 20 hodin, neboli 100 procent projektu

Následující tabulka uvádí podmínky zádržného.

| **Procento dodaných jednotek** | **Procenta, která se mají zadržet** | **Procenta, která se mají uvolnit** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Výsledkem transakcí jsou následující částky:

- Fáze 1:
  - Dlužná částka je 50 x 300 nebo 15 000.
  - 20 procent z částky, neboli 3 000, je zadrženo a bude uvolněno v pozdější fázi.
  - Částka, která je zaplacena prodejci, je 12 000.
- Fáze 2:
  - Dlužná částka je 30 x 300 nebo 9 000.
  - Zadrží se 10 procent z částky, neboli 900.
  - Je uvolněno 10 procent z 3 000, které byly zadrženy ve fázi 1, nebo 300.
  - Částka, která je zaplacena prodejci, je 8 400. Tato částka je 9 000 mínus 900 zadržených plus 300, která byla uvolněna z fáze zadržení 1.
- Fáze 3:
  - Dlužná částka je 20 x 300 nebo 6 000.
  - Žádná částka není zadržena.
  - Částka, která je uvolněna, je 3 600. Toto množství se skládá z 3 000, které byly zadrženy ve fázi 1, mínus 300 z fáze 1, která byla uvolněna ve fázi 2, plus 900, která byla zadržena ve fázi 2.
  - Částka, která je zaplacena prodejci, je 9 600. Tato částka se skládá ze zadržené částky 3 600 plus 6 000 za dokončení fáze 3.

Celková částka zaplacená prodejci po dokončení tří fází je 30 000, což je celková částka objednávky (15 000 + 9 000 + 6 000).
