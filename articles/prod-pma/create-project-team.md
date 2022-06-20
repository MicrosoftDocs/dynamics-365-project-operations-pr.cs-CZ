---
title: Vytvoření projektového týmu
description: Tento článek obsahuje informace, jak vytvořit a spravovat projektové týmy.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927320"
---
# <a name="create-a-project-team"></a>Vytvoření projektového týmu

[!include [banner](../includes/banner.md)]

Chce-li použít role, které byly předtím nastaveny v projektu, musí projektový manažer přidružit role k projektu. Projektu lze přiřadit více rolí. Aby nedocházelo k nejasnostem, jsou tyto role během rezervace automaticky označeny. Například pokud projektový manažer vyžaduje tři softwarové inženýry, jsou automaticky generovány tři role softwarového inženýra, které jsou označeny štítky **softwarový inženýr 1**, **softwarový inženýr 2** a **softwarový inženýr 3**. Pokud již byly charakteristiky rolí nastaveny pro roli, použijí se jako filtr během hledání zdrojů. Podle potřeby lze přidat další charakteristiky k dalšímu upřesnění vyhledávání.

Nastavení zobrazení lze také přizpůsobit tak, aby poskytovalo lepší přehled o dostupnosti zdrojů. K dispozici jsou možnosti zobrazení hodinové, denní, týdenní, měsíční, čtvrtletní a roční dostupnosti. K dispozici je také možnost zobrazit dostupnou a zbývající kapacitu zdrojů. Tato možnost je užitečná pro správu času, když odhadujete dostupný čas pro aktivity nebo dostupnost zdrojů.

Projektový manažer může vybrat roli na stránce a poté, pokud existuje dostupný zdroj vyhovující požadavku, vybere rezervaci prostředku, aby naplnil roli. Všimněte si, že zdroje nemusí být rezervovány v tomto okamžiku ve fázi plánování. Když vytvoříte strukturovaný rozpis prací, můžete role nahradit personálními zdroji pro projekt. Pokud jsou role nahrazeny personálními zdroji ve strukturovaném rozpisu prací, nastavení prostředků automaticky aktualizuje seznam a plánování projektového týmu.

[![Seznam projektového týmu, který zahrnuje role i skutečné zdroje.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektový manažer má různé možnosti rezervace zdroje pro projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadat hodiny**. Tyto možnosti rezervace lze kdykoli zrušit, pokud se změní přiřazení zdrojů. Podporovány jsou dva typy rezervací:

- **Závazná rezervace** – Rezervace zdroje byla schválena a potvrzena pro práci na zakázce po stanovenou dobu.
- **Předběžná rezervace** – Rezervace zdrojů byly pro práci na zakázce po stanovenou dobu nastaveny předběžně.

Následující procedura vysvětluje, jak vytvořit projektový tým:

## <a name="create-a-project-team"></a>Vytvoření projektového týmu

1. Na stránce se seznamem **Všechny projekty** vyberte projekt a poté vyberte možnost **Upravit**.
2. Na kartě **Projektový tým a plánování** zadejte v poli **Naplánovat koncové datum** datum zahájení plánu plus jeden měsíc. Pokud je například datum zahájení plánu 24. června 2017 (24. 6. 2017), zadejte **24. 7. 2017**.
3. Vyberte **Přidat**.
4. V podokně **Přidat role do projektu** vyberte v poli **Role** hodnotu **Vyšší projektový manažer**.
5. Vyberte **Požadované kompetence**.
6. Na stránce **Vyberte charakteristiky** jsou ve výchozím nastavení vybrány charakteristiky, které jste předtím nastavili pro roli Vyšší projektový manažer. Vyberte **OK**.
7. Na stránce **Přidat role do projektu** zadejte v poli **Počet zdrojů** číslo **1**.
8. V poli **Zdroj** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence. Vyberte položku **Daniel Goldschmidt** a potom vyberte **Vytvořit**.
9. Na stránce **Projekt** vyberte příkaz **Přidat**.
10. V podokně **Přidat role do projektu** vyberte v poli **Role** hodnotu **Člen týmu**. V poli **Počet zdrojů** zadejte **5**.
11. Vyberte **Vytvořit**.
12. Na stránce **Projekty** vyberte **Splnit prostředek**.

## <a name="monitor-project-teams"></a>Monitorování projektových týmů
1. Na stránce **Všechny projekty** vyberte odkaz **ID projektu** pro projekt **Fáze 2 upgradu XYZ**.
2. Na kartě **Projektový tým a plánování** ověřte, zda jsou projektové zdroje v seznamu správné.


[!INCLUDE[footer-include](../includes/footer-banner.md)]