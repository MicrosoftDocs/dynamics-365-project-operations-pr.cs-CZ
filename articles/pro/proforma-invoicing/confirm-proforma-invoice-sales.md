---
title: Potvrzení proforma faktury – omezené
description: Toto téma poskytuje informace o tom, jak potvrzovat proforma faktury v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176513"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Potvrzení proforma faktury – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Po potvrzení proforma faktury se stav projektové faktury aktualizuje na **Potvrzeno**. Když je faktura potvrzena, stane se pouze pro čtení. Do budoucna bude možné fakturu opravit, pouze pokud dojde k opravám nebo kreditům zahájeným zákazníkem nebo pokud je faktura označena jako zaplacená.

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
Nevyfakturovaný skutečný prodej se zápornou částkou zálohy, která má být použita k odsouhlasení.
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
Nový nevyfakturovaný skutečný prodej, který je neúčtovatelný za zbývající hodiny a částku po odečtení korigovaných čísel na upraveném detailu řádku faktury, zrušení skutečného prodeje a ekvivalentní fakturovaný skutečný prodej.
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
Fakturovaný skutečný prodej pro množství a částku při původním schválení výdaje </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Fakturace řádku smlouvy založené na produktu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturovaný skutečný prodej na řádek produktu s množstvím a částkou pocházejícím z řádku smlouvy na základě produktu.
                </p>
            </td>
        </tr>
    </tbody>
</table>
