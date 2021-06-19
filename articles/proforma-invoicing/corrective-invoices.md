---
title: Opravné faktury založené na projektu
description: Tento téma poskytuje informace o tom, jak vytvořit a potvrdit opravné faktury založené na projektu v Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012263"
---
# <a name="corrective-project-based-invoices"></a>Opravné faktury založené na projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Potvrzenou fakturu za projekt lze opravit ke zpracování změn nebo kreditů podle dohody se zákazníkem a projektovým manažerem.

Chcete-li provést úpravy potvrzené faktury, otevřete potvrzenou fakturu a vyberte **Opravit tuto fakturu**. 

> [!NOTE]
> Tento výběr není k dispozici, dokud není potvrzena faktura projektu nebo faktura založená na projektu obsahuje zálohy nebo zadržovací prostředky nebo odsouhlasení záloh nebo zadržovacích prostředků.

Z potvrzené faktury se vytvoří nový koncept faktury. Všechny podrobnosti řádku faktury z dříve potvrzené faktury se zkopírují do nového konceptu. Následuje několik klíčových bodů, které je třeba pochopit o podrobnostech řádku v nové opravené faktuře:

- Všechna množství se aktualizují na nulu. Dynamics 365 Project Operations předpokládá, že všechny fakturované položky jsou plně připsány. V případě potřeby můžete tato množství ručně aktualizovat, aby odrážela množství, které je fakturováno, a nikoli množství, které je připsáno. Na základě zadaného množství aplikace vypočítá připsané množství. Tato částka se promítne do skutečných hodnot, které se vytvářejí při potvrzení opravené faktury. Pokud provádíte změny v částce daně, musíte zadat správnou částku daně, nikoli částku daně, která je připisována.
- Opravy milníků jsou vždy zpracovány jako plné kredity.


> [!IMPORTANT]
> Údaje řádku faktury, které jsou opravami dalších již fakturovaných poplatků, mají pole **Oprava** nastaveno na **Ano**. Faktury, které mají opravené údaje řádku faktury, mají pole **Má opravy** nastaveno na **Ano**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Skutečné hodnoty vytvořené při potvrzení opravné faktury

V následující tabulce jsou uvedeny skutečné hodnoty, které jsou vytvořeny při potvrzení opravné faktury.

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
Fakturace celého kreditu dříve fakturované časové transakce.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro hodiny a částku na původním detailu řádku faktury pro čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový skutečný nevyfakturovaný prodej pro hodiny a částku na původním detailu řádku faktury pro čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturace částečného kreditu u časové transakce.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro hodiny a fakturovanou částku na původním detailu řádku faktury pro čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za hodiny a částku na upraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající hodiny a částku po odečtení opravených údajů v detailu řádku faktury.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace celého kreditu dříve fakturované transakce výdaje.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro výdaj.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro výdaj.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturace částečného kreditu dříve fakturované transakce výdaje.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro výdaj.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající množství a částku po odečtení opravených údajů v detailu řádku faktury.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace celého kreditu dříve fakturované transakce materiálu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované vrácení prodeje a množství a částky údajích původního řádku faktury pro materiál.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nová neyfakturovaná skutečná hodnota prodeje a množství a částky údajích původního řádku faktury pro materiál.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturace částečného kreditu u materiálové transakce.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované vrácení prodeje a množství a fakturované částky údajích původního řádku faktury pro materiál.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku v údaji upraveného řádku faktury, jeho zrušení a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutečný nový nevyfakturovaný prodej, který je účtovatelný za zbývající množství a částku po odečtení opravených údajů v detailu řádku faktury.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace celého kreditu dříve fakturované transakce poplatku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro množství a částku na původním detailu řádku faktury pro poplatek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej pro množství a částku na původním detailu řádku faktury pro poplatek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturace částečného kreditu dříve fakturované transakce poplatku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro množství a fakturovanou částku na původním detailu řádku faktury pro poplatek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový nevyfakturovaný skutečný prodej, který je účtovatelný za množství a částku na upraveném opraveném detailu řádku faktury, jeho storno a ekvivalentní fakturovaný skutečný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturace celého kreditu dříve fakturovaného milníku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Vyfakturované storno prodeje pro částku na původním detailu řádku faktury pro milník.
                </p>
                <p>
Stav faktury milníku je aktualizován z <b>Zákaznická faktura zaúčtována</b> na <b>Připraveno k fakturaci</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturace částečného kreditu dříve fakturovaného milníku.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tento scénář není podporován.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
