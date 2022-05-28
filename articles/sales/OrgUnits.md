---
title: Organizační jednotky
description: Toto téma popisuje koncept organizačních jednotek a vysvětluje, jak vytvořit a udržovat organizační jednotky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581368"
---
# <a name="organizational-units-overview"></a>Přehled organizačních jednotek

V aplikaci Microsoft Dynamics 365 Project Operations je *organizační jednotka* je zřetelnou skupinou nebo divizí ve společnosti, která se věnuje poskytování profesionálních služeb, která využívá fakturovatelné zdroje s nákladovými sazbami.

U společností profesionálních služeb, které využívají technické zdroje v různých praktických oblastech nebo obchodních oborech, se náklady na vyplnění role mohou lišit v závislosti na oblasti praxe nebo obchodním oboru, kde je role vyplněna. V tomto scénáři koncepce organizačních jednotek pomáhá poskytnutím způsobu seskupování sady fakturovatelných rolí v divizi společnosti, která má pro tyto role odlišnou strukturu nákladů.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Pojetí organizačních jednotek v Project Operations

V aplikaci Project Operations obsahuje organizační jednotka specifickou měnu a specifické ceníky.

Měna organizační jednotky je primární měnou, která se používá ke sledování nákladů.

Ke každé organizační jednotce může být připojen jeden nebo více nákladových ceníků. Project Operations klade následující omezení na ceníky, které lze připojit k organizační jednotce:

- Ceníky musejí být v měně organizační jednotky.
- Ceníky musí být nákladovými ceníky.

Kromě toho entita Zdroj zahrnuje atribut organizační jednotky. Každý zdroj lze přiřadit jedné organizační jednotce.

### <a name="roles-of-organizational-units"></a>Role organizačních jednotek

Organizační jednotka hraje v Project Operations dvě role:

- **Smluvní jednotka** – organizační jednotka, která zastupuje skupinu nebo divizi společnosti, která je primárně zodpovědná za získání prodeje a řízení dodávky práce a služeb zákazníkovi. Smluvní jednotka je identifikována pomocí pole **Smluvní jednotka** v části hlavičky stránek **Příležitost**, **Nabídka**, **Projektová smlouva** a **Projekt**.
- **Jednotka zdroje** – organizační jednotka, k níž zdroj náleží nebo je přiřazen. Tato organizační jednotka může poskytnout své zdroje pro některé role v prohlášeních o práci (SOWs) a projektech vlastněných smluvní jednotkou.

![Smluvní jednotky a financování jednotek.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Často kladené dotazy k organizačním jednotkám

Zde naleznete některé nejčastější dotazy týkající se organizačních jednotek.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Jak je entita Organizační jednotky v Project Operations spojena s entitou Organizace, která již v aplikaci Dynamics 365 existuje?

Entita Organizace v Dynamics 365 představuje název globální instance Dynamics 365. Tento název je obvykle název globálního podniku.

Entita Organizační jednotka představuje skupinu nebo divizi v globálním podniku. Tato skupina nebo divize obsahuje sadu rolí a nákladový ceník pro tyto role a tyto role a ceník se liší od rolí a ceníku jiných skupin nebo divizí v podniku.

Při instalaci Project Operations je vytvořena výchozí organizační jednotka založená na organizaci. Všechny existující zdroje jsou přiřazeny k výchozí organizační jednotce. Pokud se do aplikace Dynamics 365 importují noví uživatelé nebo zdroje služby Active Directory, proces importu uživatele je přiřadí k výchozí organizační jednotce v Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Jak se liší entita organizační jednotky od entity obchodní jednotky?

V aplikaci Dynamics 365 je entita organizační jednotky bezpečnostní konstrukt. Přidružení uživatele k organizační jednotce určuje entity a záznamy entit, ke kterým má uživatel přístup. Určuje také oprávnění (Vytvořit, Číst, Zapsat, Odstranit, Připojit, Připojit k, Přiřadit nebo Sdílet), která má uživatel pro tyto záznamy entit.

Entita Organizační jednotka představuje skupinu společnosti nebo divizi, které mají odlišné nákladové sazby pro zaměstnance, kteří jsou k ní přiřazeni. Přiřazení zdroje k organizační jednotce určuje náklady zdroje na zapojení projektu.

Pokud implementujete aplikaci Dynamics 365, optimalizujte bezpečnostní autorizaci pro hierarchii organizačních jednotek a přiřazení uživatelů k organizačním jednotkám. Přiřaďte všechny uživatele, kteří obvykle musí přistupovat ke stejné sadě záznamů, ke stejné organizační jednotce. Organizační jednotka nemá žádný vliv na bezpečnostní autorizaci nebo přístup.

**Příklad, který ukazuje jeden potenciální rozdíl v modelování organizačních jednotek a obchodních jednotek**

Contoso, Ltd. má prosperující technologické postupy společnosti Microsoft. Kamil a Gabriela jsou oba vývojáři C\#, ale Gabriela je ve Spojených státech, kdežto Kamil je v Indii. Většina zapojení projektů vyžaduje zdroje od společností Contoso India a Contoso US a Kamil a Gabriela vyžadují stejnou úroveň bezpečnostního přístupu k projektům v této praktické oblasti. Náklady vývojářů ze společnosti Contoso India se však výrazně liší od nákladů vývojářů ze společnosti Contoso US.

Zde je optimální způsob navržení tohoto scénáře pomocí aplikace Dynamics 365 a Project Operations.

1. Vytvořte technologický postup společnosti Microsoft jako je např. organizační jednotka a přidružte k ní Kamila a Gabrielu. Tímto způsobem můžete pomoci zaručit, že oba zaměstnanci mají stejnou úroveň bezpečnostního přístupu k jakýmkoli projektům v dané oblasti. Oba budou moci kontrolovat průběh a vykazovat čas, výdaje, využití materiálu a aktualizace úkolů.
2. Vytvořte dvě organizační jednotky, které pomohou zaručit, že náklady na projekt budou správně zohledněny.
3. Přidružte uživatele Gabriela ke společnosti Contoso US a uživatele Kamil ke společnosti Contoso India.
4. Přiřaďte oběma organizačním jednotkám příslušné nákladové ceníky. Tímto způsobem pomůžete zaručit, že náklady zaznamenané v projektu pro uživatele Kamil a Gabriela přesně odrážejí rozdíl nákladů mezi společnostmi Contoso US a Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Souvisejí v aplikaci Dynamics 365 organizační jednotky s prodejními oblastmi?

Mezi prodejními oblastmi a organizačními jednotkami neexistuje žádné přidružení nebo vztah. Prodejní oblast je typicky zeměpisná oblast, ve které dochází k prodeji. Ke každé prodejní oblasti lze přidružit prodejní ceník.

Organizační jednotka je interní skupina nebo divize ve společnosti, která sleduje náklady na sadu rolí, které prodává jiným divizím nebo externím zákazníkům.

**Příklad, který ukazuje jeden potenciální rozdíl v modelování organizačních jednotek a prodejních oblastí**

Společnost Contoso, Ltd. má dvě vývojová centra: Contoso US a Contoso India. Náklady na zdroje se mezi těmito dvěma vývojovými centry značně liší. Společnost Contoso prodává své IT služby na mnoha mezinárodních trzích, jako jsou Latinská Amerika, Severní Amerika, Asie a Tichomoří, západní Evropa a Střední Východ. Fakturační sazby za stejné projektové role se mohou na těchto trzích značně lišit. Společnosti Contoso US a Contoso India by měly být nastaveny jako organizační jednotky a každá organizační jednotka by měla mít vlastní nákladový ceník. Asie a Tichomoří, Latinská Amerika, Severní Amerika, západní Evropa a Střední Východ by měly být nastaveny jako prodejní oblasti a každá prodejní oblast by měla mít vlastní prodejní ceník.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Proč existuje omezení pro přidružení ceníků k organizačním jednotkám?

Prodejní ceny jsou obvykle jedinečné pro zeměpisné oblasti nebo trhy, kde se služby prodávají. Interní divize společnosti obvykle nemají vlastní prodejní ceny pro stejný typ služeb. Interní divize však mají různé náklady na prodané zboží (COGS), v závislosti na dovednostech lidí, které zaměstnávají, a na pracovních podmínkách regionu, v němž působí. Vzhledem k tomu, že organizační jednotky jsou modelovány jako vnitřní divize společnosti, mohou mít pouze nákladové ceníky.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Proč nelze přidružit prodejní ceníky k organizačním jednotkám?

V Project Operations mohou prodejní ceníky přidruženy k zákazníkům a prodejním oblastem. Transakční entity, jako jsou Příležitost, Nabídka, Projektová smlouva a Projekt, používají prodejní ceníky, které jsou připojeny k zákaznickému obchodnímu vztahu nebo k prodejní oblasti za účelem určení fakturačních sazeb a potenciálního výnosu z účasti na projektu.

Nákladové ceníky jsou přidruženy k organizačním jednotkám. Transakční entity, jako jsou Příležitost, Nabídka, Projektová smlouva a Projekt, používají nákladové ceníky, které jsou připojeny ke smluvní jednotce za účelem určení nákladů na účast na projektu.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Jsou organizační jednotky v Project Operations hierarchické?

Č. V aktuální vydané verzi Project Operations nejsou organizační jednotky hierarchické. Proto nemůžete provádět následující úkoly:

- Konfigurovat vzor pro zadávání výchozích nákladových cen, které procházejí hierarchií.
- Vykazovat výnosy nebo náklady shrnuté na různých úrovních hierarchie organizační jednotky.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Jsme velká nadnárodní firma, která má komplexní, víceúrovňovou hierarchii nákladových středisek, divizí a fakturačních kanceláří. Jak můžeme nejlépe využít koncept organizačních jednotek v aktuální verzi Project Operations?

Pokud máte složitou hierarchii nákladových středisek, divizí, fakturačních kanceláří atd., nastavte uzly typu list této hierarchie jako samostatné organizační jednotky.

Následující příklad ukazuje typickou hierarchii.

**Contoso India**

- Postupy pro SAP

    - Techničtí poradci
    - Funkcionální poradci

- Technologické postupy společnosti Microsoft

    - Techničtí poradci
    - Funkcionální poradci

**Contoso US**

- Postupy pro SAP

    - Techničtí poradci
    - Funkcionální poradci

- Technologické postupy společnosti Microsoft

    - Techničtí poradci
    - Funkcionální poradci

Pokud se vaše hierarchie podobá tomuto příkladu, musíte ji nastavit jako prostý seznam, jak je znázorněno zde:

- Contoso India – Postup pro SAP – Techničtí poradci
- Contoso India – Postup pro SAP – Funkcionální poradci
- Contoso India – Technologické postupy společnosti Microsoft – Funkcionální poradci
- Contoso India – Technologické postupy společnosti Microsoft – Funkcionální poradci
- Contoso US – Postup pro SAP – Techničtí poradci
- Contoso US – Postup pro SAP – Funkcionální poradci
- Contoso US – Technologické postupy společnosti Microsoft – Techničtí poradci
- Contoso US – Technologické postupy společnosti Microsoft – Funkcionální poradci

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Jsme malá společnost poskytující profesionální služby, která pracuje jako jediná divize. Jak můžeme nejlépe využít koncept organizačních jednotek v aktuální verzi Project Operations?

Pokud vaše společnost pracuje jako jedna jednotka, která má jeden nákladový ceník, nemusíte nastavovat žádné organizační jednotky. Během instalace Project Operations se vytvoří jedna výchozí organizační jednotka, která má stejný název jako organizace. Ve výchozím nastavení jsou všichni uživatelé přiřazeni k této organizační jednotce. Kdykoli systém vyžaduje, aby byla vybrána organizační jednotka, je tato organizační jednotka ve výchozím nastavení vybrána.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Pokud je projekt vytvořen z nabídky nebo řádku projektové smlouvy, výchozí smluvní jednotka pochází z nabídky nebo projektové smlouvy. Jaká je výchozí smluvní jednotka, pokud je projekt vytvořen před prodejními entitami, jako jsou například nabídka nebo projektová smlouva?

Pokud je projekt vytvořen samostatně, je výchozí smluvní jednotka projektu založena na uživateli, který jej vytvořil. Tento uživatel je také výchozím projektovým manažerem. Pokud je projekt namapován na prodejní entitu, jako je například nabídka nebo projektová smlouva, je smluvní jednotka v projektu založena na prodejní entitě. V takovém případě mohou být odhady projektu přepočítány, protože nákladový ceník se používá k výpočtu změn odhadu nákladů při změně smluvní jednotky. Prodejní ceník se používá k výpočtu odhadů prodeje, které budou změněny, aby byly synchronizovány s projektovým ceníkem nabídky.

Pole **Smluvní jednotka** a **Měna** projektu jsou uzamčeny pro úpravy, protože musí být synchronizovány s hodnotami prodejní entity (nabídka nebo projektová smlouva), na kterou je projekt namapován.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Vytváření a udržování organizačních jednotek v Project Operations

Chcete-li vytvořit organizační jednotku v Project Operations, postupujte takto.

1. Přejděte do nabídky **Nastavení \> Organizační jednotky**.
2. Vyberte **Nové**.
3. V oblasti **Obecné** zadejte název organizační jednotky do pole **Název**. Poté nastavte další pole podle potřeby.
4. Zvolte **Uložit** a vytvořte záznam, abyste mohli pokračovat v jeho úpravách.
5. V části **Ceníky nákladů** výběrem značky plus (**+**) přidejte ceník. Zde můžete přidat pouze ceníky s kontextem **Náklady**.
6. V poli **Název** vyberte tlačítko **Hledat** a vyberte ceník, který chcete zpřístupnit této organizační jednotce. Podle potřeby přidejte další ceníky.
7. Po dokončení přidávání ceníků vyberte ikonu **Uložit** v pravém dolním rohu stránky.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
