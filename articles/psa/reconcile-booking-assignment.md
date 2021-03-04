---
title: Spárování rezervací a přiřazení
description: Toto téma poskytuje informace o skutečných hodnotách.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147915"
---
# <a name="reconcile-bookings-and-assignments"></a>Spárování rezervací a přiřazení

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektové rezervace a projektová přiřazení členů projektového týmu jsou volně spárovány. Zdroj tedy může mít přiřazení úkolů, která neodpovídají rezervacím a rezervace, které neodpovídají přiřazením úkolů. V ideálním případě by měly být projektové rezervace a přiřazení zarovnány, aby zdroje měly potvrzenou kapacitu k provádění přiřazení úkolů. Skutečnost je však taková, že může dojít k rezervaci na základě dostupnosti a časování úkolů se může změnit, protože projekt pokračuje v životním cyklu. Proto volné spárování umožňuje flexibilitu.

Z důvodu volného spárování rezervací projektů a přiřazení úkolů je v entitě Projekt zahrnuta karta **Vyrovnání**. Tato karta pomáhá projektovým manažerům vyrovnat rezervace členů týmu a jejich přiřazení pro daný projektový tým.

Karta **Vyrovnání** zobrazuje pro každého pojmenovaného člena týmu rezervace a přiřazení až k úrovni jednotlivých přiřazení úkolů. Zobrazuje hodiny v buňkách představují časová období od měsíců po dny.

V poli **Časové měřítko** můžete vybrat **Měsíc**, **Týden** nebo **Den**. Ve výchozím nastavení je vybrán **Týden**. Výchozí hodnotu však můžete změnit tak, že vyberete tlačítko **Nastavení**. Při otevření karty **Vyrovnání**, se zobrazí aktuální datum, ale pro přesun dopředu nebo dozadu v čase můžete použít ovládací prvek kalendáře. Pokud má projekt datum zahájení, které je v budoucnosti, karta toto datum zobrazí při svém otevření. Ovládací prvek kalendáře také obsahuje možnosti, které umožňují přesun data zahájení a ukončení projektu.

Chcete-li zobrazit podrobnosti o rezervacích tohoto zdroje, můžete u jednotlivých zdrojů použít ovládací prvky pro rozbalení. Přiřazení jednotlivých zdrojů můžete také rozbalit na úroveň jednotlivého úkolu.

V dolní části karty **Vyrovnání** je zobrazen celkový čistý součet projektu a tato karta také obsahuje sloupec celkem. Pro každý zdroj je na kartě vypočten rozdíl mezi rezervacemi člena týmu pro projekt a shrnutím přiřazení tohoto člena týmu. V ideálním případě by tento rozdíl měl být 0 (nula). Jinými slovy, mezi rezervacemi a přiřazeními zdroje by neměl být žádný rozdíl. Jakékoli rozdíly jsou označeny barvou a stínováním pro volání dvou podmínek:

- **Nedostatečná rezervace** – k nedostatečné rezervaci dochází tehdy, když zdroj obsahuje více přiřazení, než zezervací. Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit.
- **Nadbytečné rezervace** – k nadbytečným rezervacím dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům. Tento stav může být přijatelný, pokud byl například tento zdroj rezervován před přiřazením úkolu. V jiných případech však není plánováno přiřazení zdroje k úkolům. V těchto případech by měl projektový manažer zvážit zrušení rezervací zdroje, aby bylo možné použít kapacitu pro jiný projekt.

> [!NOTE]
> Legenda těchto stavů může být skryta, aby bylo možné ponechat více místa pro mřížku. V tomto případě můžete nastavit aby se legenda zobrazovala tak, že vyberete tlačítko **Nastavení**.

V některých případech, kdy je pole **Časové měřítko** nastaveno na úroveň, která je vyšší než **Den**, mohou být rozdíly vypočteny jako 0 (nula). Například na úrovni **Měsíc** může být čistý rozdíl pro zdroj roven 0 (nule), což označuje, že se rezervace rovnají přiřazením. Pokud se však podíváte na úroveň **Týden**, můžete se setkat s tím, že v prvním týdnu měsíce jsou přiřazení ve výši 0 (nula) hodin a rezervace 40 hodin a ve druhém týdnu jsou přiřazení 40 hodin a rezervace 0 (nula) hodin. Ačkoli se celkové rezervace a přiřazení pro daný měsíc rovnají, liší se po týdnech.

Když se podíváte na vyšší úrovně, karta **Vyrovnání** zobrazuje indikátor buňky, který vás upozorní, že se na nižších úrovních vyskytují rozdíly. Například na následujícím obrázku je v buňce zobrazen indikátor buňky pro měsíc říjen 2018 pro zdroj pojmenovaný Libuše Horáčková. Proto je vidět, že i když jsou rezervace a přiřazení zdroje stejné, tak při agregaci na úrovni **Měsíc** se na nižších úrovních neshodují.

![Neodpovídající rezervace a přiřazení na měsíční úrovni](media/reconcile-assignments-01.JPG)

Dvojitým kliknutím buňku přibližte na další nižší úroveň a zobrazíte rozdíl. Pokud například dvakrát kliknete na rozdíl říjen 2018 pro Libuši Horáčkovou, přejdete na podrobnější úroveň **Týden**. Poté můžete zjistit, že zdroj má rezervace na 16 hodin, ale žádná přiřazení v prvních dvou týdnech v říjnu a 16 hodin přiřazení, ale žádnou rezervaci ve třetím říjnovém týdnu.

![Neodpovídající rezervace a přiřazení na týdenní úrovni](media/reconcile-assignments-02.JPG)

Kliknutím pravým tlačítkem myši na buňku pro oddálení další vyšší úrovně. Indikátor buňky můžete také vypnout výběrem tlačítka **Nastavení**. 

Můžete také použít tlačítka **Předchozí** a **Další** nad mřížkou a procházet všemi rozdíly v projektu. Chcete-li tato tlačítka používat, je nutné nejprve vybrat zdroj. Vyberte **Další** pro přechod na další rozdíl mezi rezervacemi a přiřazeními pro daný zdroj. Chcete-li přejít zpět na předchozí graf, vyberte tlačítko **Předchozí**.

Pokud máte přiřazení úkolů pro zdroj bez přiřazení, můžete nyní vybrat souhrnné nedostatečné rezervace a kliknout na možnost **Prodloužit rezervaci**. Poté můžete zobrazit rezervaci, která je požadována pro vyřešení nedostatku zdroje. Můžete také zobrazit rezervace zdroje na aktuálním projektu a dalších projektech. Chcete-li vytvořit rezervaci pro zdroj, vyberte **OK**, rezervaci zdroje bez ohledu na aktuální dostupnost. Projektový manažer nebo správce prostředku pak může pomocí Plánovací vývěsky spravovat situace, ve kterých je zdroj přerezervovaný nad svoji kapacitu, protože jejich rezervace byla prodloužena.

## <a name="managing-with-time-zones"></a>Správa pomocí časových pásem
Pro zajištění přesných a předvídatelných výsledků při používání funkce Prodloužit rezervaci musejí být splněny dva klíčové předpoklady:  

- Uživatel musí nakonfigurovat časové pásmo svého zařízení tak, aby odpovídalo časovému pásmu definovanému v nastavení personalizace vašeho systému.
 
  ![Nastavení časového pásma v systému Windows 10](media/reconcile-assignments-03.png)

  ![Nastavení časového pásma v nastavení personalizace](media/reconcile-assignments-04.png)
 
- Rezervovatelný zdroj musí mít alespoň jednu minutu pracovní doby, která se překrývá s průběhovými křivkami, které slouží k definování požadovaného rozšíření. Následující příklad ukazuje zdroje kontroly s pracovní dobou, která spadá mezi 9:00 a 19:00. 

  ![Porovnání průběhových křivek zdroje](media/reconcile-assignments-05.png)

Následující tabulka znázorňuje:

- Šablonu kalendáře projektu.
- Zdroj A: Tento zdroj má stejný kalendář a je ve stejném časovém pásmu jako projekt. Čas zahájení rezervace bude 9:00.
- Zdroje B: Tento zdroj je umístěn v jiném časovém pásmu než projekt, a proto začíná v 7:00 v jejich časovém pásmu. Rezervace však začnou v 9:00, protože to je nejčasnější počáteční čas průběhové křivky přiřazení.
- Zdroje C a D: Zdroje jsou také umístěny v různých časových pásmech, lišících se od sebe navzájem i od projektu a jejich rezervace nezačínají dříve, než jejich příslušné dostupné časy zahájení.

|Entita  |Kalendář  |
|-|-|
|Šablona kalendáře projektu   | ![kalendář projektu](media/reconcile-assignments-06.png) |
|Zdroj A  | ![Kalendář zdroje A](media/reconcile-assignments-06.png) |
|Zdroj B  |  ![Kalendář zdroje B](media/reconcile-assignments-07.png) |
|Zdroj C  |  ![Kalendář zdroje C](media/reconcile-assignments-08.png) |
|Zdroj D  | ![Kalendář zdroje D](media/reconcile-assignments-09.png)  |
 
Když přejdete do zobrazení odsouhlasení, zobrazí se přiřazení zdrojů a související rezervační nedostatky.
 ![Zobrazení odsouhlasení před rozšířením](media/reconcile-assignments-10.png)

Po spuštění funkce Prodloužit rezervaci u každého zdroje jsou rezervace pro každý zdroj úspěšně rozšířeny. Důvodem je to, že pracovní doba každého zdroje se překrývala s průběhovými křivkami nedostatku.
 ![Zobrazení odsouhlasení po prodloužení rezervace](media/reconcile-assignments-11.png) 

Bližší pohled na podrobnosti rezervace však ukazuje rozdíly v době zahájení rezervace. Rezervace nezačnou dříve, než je počáteční čas průběhové křivky přiřazení a než je k dispozici počáteční čas zdroje.
 ![Nové rezervace zdrojů na plánovací vývěsce](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]