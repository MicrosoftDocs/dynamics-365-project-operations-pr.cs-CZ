---
title: Potvrzení proforma faktury založené na projektu
description: Tento téma poskytuje informace o tom, jak potvrdit projektovou proforma fakturu.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867122"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Potvrzení proforma faktury založené na projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**. Když je faktura potvrzena, stane se pouze pro čtení. Do budoucna bude možné fakturu opravit pouze v případě, že dojde k opravám nebo kreditům zahájeným zákazníkem.

V následující tabulce jsou uvedeny skutečné hodnoty vytvořené systémem. Tyto skutečné hodnoty se vytvoří, když se na faktuře konceptu projektu provedou určité operace, než se potvrdí.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scénář</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace záloh </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej typu <strong>Záloha</strong> je vytvořen pro částku v záloze.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutečný nevyfakturovaný prodej se zápornou částkou zálohy nebo platby předem, která má být použita k odsouhlasení.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Po úplném odsouhlasení zálohy na fakturu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení. Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej na částku na této faktuře.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Po částečném odsouhlasení zálohy na fakturu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení. Tato částka je kladná, protože má zrušit zápornou hodnotu, která byla vytvořen při fakturaci zálohy.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej na částku na této faktuře.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Záporný nevyfakturovaný skutečný prodej zbývající zálohy, která má být použita k odsouhlasení na budoucích fakturách.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace časové transakce bez jakýchkoli úprav konceptu faktury.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej pro hodiny a částku při původním schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturace časové transakce, která byla upravena, aby se snížilo množství.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který nelze účtovat za zbývající hodiny a částku po odečtení opravených údajů v údajích upraveného řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace časové transakce, která byla upravena, aby se zvýšilo množství.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro hodiny a částku při původním schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace transakce výdaje bez jakýchkoli úprav konceptu faktury.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej pro množství a částku při původním schválení výdaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturace transakce výdaje, která byla upravena, aby se snížilo množství.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace transakce výdaje, která byla upravena, aby se zvýšilo množství.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro množství a částku při původním schválení výdaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace významné transakce bez jakýchkoli úprav konceptu faktury.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované vrácení prodeje a množství a částky na původním schválení použití materiálu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Vyfakturovaný skutečný prodej a množství a částky na původním schválení použití materiálu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturace materiálové transakce, která byla upravena, aby se snížilo množství.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované vrácení prodeje a množství a částky na původním schválení času.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající množství a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace materiálové transakce, která byla upravena, aby se zvýšilo množství.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované vrácení prodeje a množství a částky na původním schválení použití materiálu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace poplatku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované storno prodeje pro částku poplatku na původním řádku deníku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej pro množství a částku na původním řádku deníku poplatku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturace milníku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Skutečně fakturovaný prodej pro část milníku v původním milníku na řádku smlouvy o projektu.
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
