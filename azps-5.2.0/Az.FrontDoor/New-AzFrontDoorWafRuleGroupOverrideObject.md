---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332248"
---
# <span data-ttu-id="8fad3-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="8fad3-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="8fad3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fad3-102">SYNOPSIS</span></span>
<span data-ttu-id="8fad3-103">Creare un oggetto RuleGroupOverride per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="8fad3-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="8fad3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fad3-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fad3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fad3-105">DESCRIPTION</span></span>
<span data-ttu-id="8fad3-106">Creare un oggetto RuleGroupOverride per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="8fad3-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="8fad3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fad3-107">EXAMPLES</span></span>

### <span data-ttu-id="8fad3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8fad3-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="8fad3-109">Creare un oggetto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8fad3-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="8fad3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fad3-110">PARAMETERS</span></span>

### <span data-ttu-id="8fad3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fad3-111">-DefaultProfile</span></span>
<span data-ttu-id="8fad3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fad3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fad3-113">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="8fad3-113">-Exclusion</span></span>
<span data-ttu-id="8fad3-114">Esclusione</span><span class="sxs-lookup"><span data-stu-id="8fad3-114">Exclusion</span></span>

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

### <span data-ttu-id="8fad3-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8fad3-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="8fad3-116">Elenco di override della regola</span><span class="sxs-lookup"><span data-stu-id="8fad3-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fad3-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="8fad3-117">-RuleGroupName</span></span>
<span data-ttu-id="8fad3-118">Nome del gruppo di regole per cui si applicano queste sostituzioni</span><span class="sxs-lookup"><span data-stu-id="8fad3-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="8fad3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fad3-119">CommonParameters</span></span>
<span data-ttu-id="8fad3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fad3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fad3-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fad3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fad3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fad3-122">INPUTS</span></span>

### <span data-ttu-id="8fad3-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8fad3-123">None</span></span>

## <span data-ttu-id="8fad3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fad3-124">OUTPUTS</span></span>

### <span data-ttu-id="8fad3-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8fad3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="8fad3-126">Note</span><span class="sxs-lookup"><span data-stu-id="8fad3-126">NOTES</span></span>

## <span data-ttu-id="8fad3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fad3-127">RELATED LINKS</span></span>

[<span data-ttu-id="8fad3-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8fad3-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
