---
title: Opravené faktury – omezené
description: Toto téma poskytuje informace o opravených fakturách v aplikaci Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176423"
---
# <a name="corrected-invoices---lite"></a>Opravené faktury – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Potvrzenou fakturu za projekt lze opravit ke zpracování změn nebo kreditů podle dohody se zákazníkem a projektovým manažerem.

Chcete-li provést úpravy potvrzené faktury, otevřete potvrzenou fakturu a vyberte **Opravit tuto fakturu**. 

> [!NOTE]
> Tento výběr není k dispozici, dokud nebude potvrzena faktura projektu.

Z potvrzené faktury se vytvoří nový koncept faktury. Všechny podrobnosti řádku faktury z dříve potvrzené faktury se zkopírují do nového konceptu. Následuje několik klíčových bodů, které je třeba pochopit o podrobnostech řádku v nové opravené faktuře:

- Všechna množství se aktualizují na nulu. Aplikace předpokládá, že všechny fakturované položky jsou plně připsány. V případě potřeby můžete tato množství ručně aktualizovat, aby odrážela množství, které je fakturováno, a nikoli množství, které je připsáno. Na základě zadaného množství aplikace vypočítá připsané množství. Tato částka se promítne do skutečných hodnot, které se vytvářejí při potvrzení opravené faktury. Pokud provádíte změny v částce daně, musíte zadat správnou částku daně, nikoli částku daně, která je připisována.
- Dříve potvrzené řádky smlouvy na základě produktu se nekopírují. Zpracování oprav na projektové faktuře založené na produktu není podporováno.
- Opravy milníků jsou vždy zpracovány jako plné kredity.
- Částky záloh lze opravit, pokud byla zákazníkovi fakturována nesprávná částka.
- Odsouhlasení záloh lze opravit, pokud byla použita nesprávná částka k vyrovnání proti poplatkům na dříve potvrzené faktuře.

> [!IMPORTANT]
> Podrobnosti řádku faktury, které jsou opravami dalších již fakturovaných poplatků, mají pole **Oprava** nastavený na **Ano**. Faktury, které opravují podrobnosti řádku faktury, mají pole s názvem **Má opravy**, které je také nastaveno na **Ano**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Skutečné hodnoty vytvořené při potvrzení opravné faktury:

Níže jsou uvedeny skutečné hodnoty vytvořené aplikací při potvrzení opravy na základě operací provedených na konceptu opravné faktury před potvrzením.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrďte opravu fakturované zálohy.<strong></strong>
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
Skutečná hodnota storna fakturovaného prodeje je vytvořena pro částku v záloze, aby se stornoval původní fakturovaný prodej.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový fakturovaný skutečný prodej je vytvořen pro částku opraveného řádku faktury na základě zálohy.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný skutečný prodej se zápornou částkou opraveného řádku faktury na základě zálohy, který bude použit k odsouhlasení.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrzení opravy dříve odsouhlasené zálohy.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nevyfakturované prodejní storno zálohy, která byla vytvořena pro odsouhlasení. Tato částka je kladná a má zrušit zápornou hodnotu, která byla vytvořena při předchozím odsouhlasení.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Skutečné storno fakturovaného prodeje na částku na předchozí faktuře.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nový fakturovaný skutečný prodej pro částku opravené zálohy, který je použit na opravenou fakturu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nevyfakturovaný skutečný prodej se zápornou částkou z opraveného zbytku zálohy, který bude použit k odsouhlasení na pozdějších fakturách.
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
Milník faktura nebo stav fakturace na řádku smlouvy projektu je aktualizován na **Připraveno k fakturaci**.
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
Nepodporováno </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Kredity a opravy dříve fakturovaného řádku smlouvy na základě produktu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nepodporováno </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]