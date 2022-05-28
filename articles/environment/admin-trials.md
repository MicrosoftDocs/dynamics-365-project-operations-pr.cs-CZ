---
title: Registrace ke zkušební verzi Project Operations
description: Toto téma obsahuje informace o tom, jak nasadit zkušební verzi projektu Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: a0c2532370c99cfe75b54da42c329f5b244a47e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584266"
---
# <a name="sign-up-for-project-operations-trials"></a>Registrace ke zkušební verzi Project Operations 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení – od obchodu po proforma fakturaci a Project Operations pro scénáře založené na skladovém materiálu / výrobě_ 



Toto téma vysvětluje, jak se přihlásit k odběru zkušební nabídky partnera a jak nasadit prostředí Dynamics 365 Project Operations.

S novou zkušební verzí Project Operations můžete automaticky nasadit kterýkoli ze tří podporovaných scénářů nasazení po vyplnění dotazníku, který doporučuje nejlepší přístup k nasazení. Toto téma obsahuje následující informace:

- Jak uplatnit svou zkušební nabídku.
- Jak zahájit zajišťování.
- Jak konfigurovat duální zápis.
- Další informace o Project Operations. 

Následující tabulka obsahuje podrobnosti o nové zkušební nabídce.

| **Položka nabídky**               | **Podrobnosti**                                  |
|------------------------------|----------------------------------------------|
| Typ nabídky                   | Tento typ nabídky je potenciální zákazník správce, takže je nutno uplatnit správce klienta. |
| Použití nabídky                    | Jedenkrát na klienta                          |
| Trvání nabídky               | 30 kalendářních dní                             |
| Uplatnění na klienta       | 0                                            |
| Přípona                    | 1 prodloužení, 30 kalendářních dní               |
| Počet zkušebních prostředí | 3                                            |


## <a name="admin-trial-details"></a>Podrobnosti o zkušební verzi správce
Následující tabulka uvádí podrobnosti o zkušební verzi a způsob jejich použití pro každý typ nasazení.

| **Položka**                      | **Lite**                                     | **Neskladové materiály** | **Skladové materiály** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Údaje o instalaci jsou k dispozici           | Ano                                          | Ano                       | Ano (USSI)            |
| Transakční data            | No                                           | No                        | No                    |
| Čas zřizování v minutách  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Požadavky
Pro nasazení zkušební verze Dynamics 365 Project Operations jsou nutné následující předpoklady.

- Zaregistrujete se na [Dynamics 365 Project Operations - Zkušební ukázka](https://www.aka.ms/try-po).
- Uživatel, který nasadí zkušební ukázku, musí mít práva globálního správce klienta Azure.

> [!IMPORTANT]
> Tuto úlohu musí provést jen jedna osoba v organizaci, správca klientu. Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Zkušební ukázka 

Než začnete, přihlaste se do prohlížeče pomocí uživatelského pracovního účtu v klientu, kde chcete zobrazit zkušební ukázku Project Operations.

1. Uplatněte první kód nabídky **Dynamics 365 Project Operations (CRM) - Zkušební ukázka** vložením do adresy URL prohlížeče.

    ![Uplatnění nabídky](./media/16RedeemFirstOfferNew.png)

2. Objednávku potvrďte.

    ![Potvrďte objednávku](./media/17ConfirmOrderNew.png)

  Uvidíte, že nabídka potvrzení byla úspěšně uplatněna.

   ![Potvrzení](./media/18OrderConfirmationNew.png)

  Budete přesměrováni do [centra pro správu Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Dotazník a zřizování

1.  Přejděte do [centra pro správu Power Platform](https://admin.powerplatform.com/projectoperationstrial) a vyplňte dotazník.  
2.  Zkontrolujte doporučený typ nasazení a vyberte **Spustit instalaci** zahájit zajišťování.
3.  Zkontrolujte podmínky a ujednání a potom vyberte **Spustit**.

   Po spuštění zřizování budete přesměrováni na seznam prostředí v centru pro správu Power Platform. Zatímco zřizování probíhá, stav vašeho prostředí je **Příprava instance**.
 
  Když je zřizování dokončeno, stav vašeho prostředí je **Připraveno**. Zřizování prostředí zahrnuje nasazení ukázkových dat.
 
4.  Vyberte příslušnou adresu URL aplikace Microsoft Dataverse a adresy URL finančních a provozních aplikací k ověření nasazení.

## <a name="configuring-dual-write"></a>Jak konfigurovat duální zápis.
- Chcete-li konfigurovat role zabezpečení pro duální zápis, pročtěte si článek [Aktualizace nastavení zabezpečení u Project Operations v Dataverse](resource-provision-new-environment.md).
- Chcete-li konfigurovat mapy duálního zápisu, pročtěte si článek [Spuštění mapování duálního zápisu Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Přiřazení licencí

Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.

1. Přejděte do [centra pro správu Microsoft 365](https://portal.office.com/) a přiřaďte licence vašim uživatelům.

   ![Domovská stránka centra pro správu](./media/14AdminPortal.png)

2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.

   ![Přiřazení licencí](./media/15AssignLicenses.png)

3. Ověřte, že byla vybrána licence zkušební ukázka **Dynamics 365 Project Operations** a vyberte **Uložit změny**.

## <a name="additional-resources"></a>Další materiály

Následující zdroje poskytují užitečné pokyny na začátku vaší práce s Project Operations:

- [Řada videa - Přehled Project Operations, obsahuje materiály pro hlubší porozumění a plán nasazení](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Určení typu nasazení](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Nejčastější dotazy

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Co když potřebuji ALM nebo ELM pro mé prostředí finančních a provozních aplikací?

- Pro partnery, kteří vyžadují úplné možnosti správy životního cyklu prostředí. Projdete si novou nabídku pro partnery [Žádost o licenci Partner Sandbox](https://experience.dynamics.com/requestlicense). 
- Pro partnery, kteří hledají další informace o právech na interní užívání. Viz [Výhody cloudových a softwarových práv pro interní použití (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Mohu si zkušební dobu prodloužit na více než 30 dní?
Chcete-li si zkušební verzi prodloužit, proveďte následující kroky.

1. V **centru pro správu Microsoft 365** přejděte na **Fakturace** > **Vaše produkty**.
2. Vyberte **Dynamics 365 Project Operations (CE) - Zkušební ukázka (CE)**.
3. V části **Datum spotřeby**, vyberte **Prodloužit datum**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Mohu upgradovat z nasazení Lite na scénáře založené na zdrojích/položkách, které nejsou na skladě?
V současné době neexistuje podpora pro upgrade prostředí z verze Lite na nasazení založené zdrojích/položkách, které nejsou na skladě.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Mohu získat přístup k LCS (Lifecycle Services) pro svá finanční prostředí?  
Č. U těchto zkušebních verzí je nasazení řešeno pomocí Centra pro správu Power Platform. Přístup do finančního prostředí je omezen.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Mohu si zkušební verzi nainstalovat do stávajícího prostředí?
Pokud máte existující prostředí, bude vám povoleno nainstalovat nasazení Lite na stávající prodej prostředí Dataverse z Centra pro správu Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
