---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191532"
---
# <span data-ttu-id="d3dd8-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="d3dd8-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="d3dd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d3dd8-103">Creare un oggetto di override della regola gestita</span><span class="sxs-lookup"><span data-stu-id="d3dd8-103">Create managed rule override object</span></span>

## <span data-ttu-id="d3dd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3dd8-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3dd8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3dd8-105">DESCRIPTION</span></span>
<span data-ttu-id="d3dd8-106">Creare un oggetto PSAzureManagedRuleOverride per il gruppo di regole WAF gestito ignora la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="d3dd8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3dd8-107">EXAMPLES</span></span>

### <span data-ttu-id="d3dd8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3dd8-108">Example 1</span></span>
<span data-ttu-id="d3dd8-109">Creare un oggetto di override della regola gestita per la regola 942250 (che si trova nel gruppo SQLI).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="d3dd8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3dd8-110">PARAMETERS</span></span>

### <span data-ttu-id="d3dd8-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="d3dd8-111">-Action</span></span>
<span data-ttu-id="d3dd8-112">Azione di override</span><span class="sxs-lookup"><span data-stu-id="d3dd8-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3dd8-113">-DefaultProfile</span></span>
<span data-ttu-id="d3dd8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dd8-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="d3dd8-115">-Disabled</span></span>
<span data-ttu-id="d3dd8-116">Stato disabilitato</span><span class="sxs-lookup"><span data-stu-id="d3dd8-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dd8-117">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="d3dd8-117">-Exclusion</span></span>
<span data-ttu-id="d3dd8-118">Esclusione</span><span class="sxs-lookup"><span data-stu-id="d3dd8-118">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dd8-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="d3dd8-119">-RuleId</span></span>
<span data-ttu-id="d3dd8-120">ID regola</span><span class="sxs-lookup"><span data-stu-id="d3dd8-120">Rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3dd8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3dd8-121">CommonParameters</span></span>
<span data-ttu-id="d3dd8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3dd8-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3dd8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3dd8-124">INPUTS</span></span>

### <span data-ttu-id="d3dd8-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3dd8-125">None</span></span>

## <span data-ttu-id="d3dd8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3dd8-126">OUTPUTS</span></span>

### <span data-ttu-id="d3dd8-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d3dd8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="d3dd8-128">Note</span><span class="sxs-lookup"><span data-stu-id="d3dd8-128">NOTES</span></span>

## <span data-ttu-id="d3dd8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3dd8-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3dd8-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="d3dd8-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)