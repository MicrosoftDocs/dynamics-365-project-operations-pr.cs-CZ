---
title: Správa projektů a rezervací v kalendáři služeb Office 365
description: Postup správy projektů a rezervací v kalendáři Office 365
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cf51333179d2d972af84de7adb4b718b6e17d038
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598894"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Správa projektů a rezervací v kalendáři (Project Service)

> [!Note]
> ZASTARALÉ: Tato funkce jj již zastaralá a není více dostupná.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Pomocí kalendáře služeb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] můžete zobrazovat osobní schůzky, rezervace týkající se práce na projektu a přiřazení pracovních příkazů pro Field Service.  
  
 Díky tomu, že vše je k dispozici na jednom místě, můžete snadno naplánovat svůj den. Všechny vaše události, schůzky, rezervace a úkoly jsou dostupné ve vašem kalendáři služeb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Pokud používáte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], můžete také zadat osobní schůzky v zobrazení časového záznamu řešení Project Service. Díky tomu budou mít vedoucí projektů a správci zdrojů přehled o vaší dostupnosti pro projekty. Rovněž tím ušetříte čas, protože nemusíte zadávat informace o osobních schůzkách dvakrát. Můžete jednoduše importovat své osobní schůzky z kalendáře do zobrazení časového záznamu řešení Project Service.  
  
 Váš kalendář bude synchronizovat rezervace projektů a pracovních příkazů pro nadcházející čtyři týdny. Toto nastavení nelze změnit.  
  
 Synchronizace je podporována pouze jedním směrem, a to z aplikace PSA do kalendáře [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Můžete synchronizovat v obráceném pořadí. 
  
 Další informace o používání kalendáře služeb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] naleznete v části [Kalendář v aplikaci Outlook na webu pro podnikání](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Nastavení  
 Dříve než budete moci zobrazovat a spravovat vaše rezervace v kalendáři služeb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], musíte nastavit několik věcí.  
  
- Budete muset mít přihlašovací údaje globálního správce [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] nebo správce systému .  
  
- Správce bude muset nakonfigurovat profil e-mailového serveru a každý uživatel bude muset nakonfigurovat svou poštovní schránku. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Nastavení zpracování e-mailů prostřednictvím synchronizace na straně serveru](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Zapnutí synchronizace pro organizaci (úloha správce)  
  
1.  V hlavní nabídce klikněte na **Nastavení** > **Správa**.  
  
2.  Klikněte na **Nastavení systému**.  
  
3.  Klikněte na kartu **Synchronizace**.  
  
4.  V položce **Vyberte, jestli chcete povolit synchronizaci rezervace zdrojů s** zaškrtněte **Synchronizovat rezervaci zdrojů s aplikací Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Zapnutí synchronizace pro váš uživatelský profil (úkol uživatele)  
  
1.  Klikněte na tlačítko **Nastavení** v pravém horním rohu obrazovky.  
  
2.  Klikněte na položku **Možnosti**.  
  
3.  Klikněte na kartu **Synchronizace**.  
  
4.  V položce **Synchronizace rezervace zdrojů s aplikací Outlook** zaškrtněte **Synchronizovat rezervaci zdrojů s aplikací Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importování vašich osobních schůzek (úkol uživatele)  
 Můžete importovat své osobní schůzky z kalendáře do zobrazení časového záznamu řešení Project Service Automation.  
  
1. Otevřete kalendář služeb [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] a klikněte na tlačítko **Importovat data**.  
  
2. V obrazovce Filtry vyberte **Schůzky z Exchange** a klikněte na tlačítko **Použít**.  
  
3. Systém převede schůzky do zobrazení časového záznamu jako navrhované položky z aktuálního týdne. Chcete-li přidat další položky pro další týden, klikněte na tlačítko **Předchozí** nebo **Další**.  
  
4. Vyberte schůzku, kterou chcete přidat do zobrazení časového záznamu řešení Project Service Automation.  
  
5. V místní nabídce **Časový záznam** vyberte příslušné možnosti pro převod schůzky do zobrazení časového záznamu řešení Project Service Automation.  
  
6. Klikněte na **Uložit**.  
  
### <a name="see-also"></a>Viz také  
 [Příručka – Čas, výdaje a spolupráce](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
