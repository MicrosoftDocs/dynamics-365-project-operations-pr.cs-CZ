---
title: Potvrzení proforma faktury projektu
description: Tento téma poskytuje informace o potvrzování projektových proforma faktur v Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004118"
---
# <a name="confirm-a-proforma-project-invoice"></a>Potvrzení proforma faktury projektu 

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
