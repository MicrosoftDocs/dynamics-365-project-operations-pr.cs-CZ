---
title: Potvrzení proforma faktury
description: Tento téma poskytuje informace o potvrzení proforma faktury.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073625"
---
# <a name="confirm-a-proforma-invoice"></a>Potvrzení proforma faktury

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**. Když je faktura potvrzena, stane se pouze pro čtení. Do budoucna bude možné fakturu opravit, pouze pokud dojde k opravám nebo kreditům zahájeným zákazníkem nebo pokud je označena jako zaplacená.

V následující tabulce jsou uvedeny skutečné hodnoty vytvořené systémem. Tyto skutečné hodnoty se vytvoří, když se na faktuře konceptu projektu provedou určité operace, než se potvrdí.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scénář</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Skutečné hodnoty vytvořené při potvrzení</strong>
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
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající hodiny a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného nevyfakturovaného prodeje a ekvivalentní fakturovaný skutečný prodej.
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
