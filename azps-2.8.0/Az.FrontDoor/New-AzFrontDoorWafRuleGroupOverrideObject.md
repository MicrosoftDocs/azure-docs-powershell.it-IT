---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: c55be8e72e3c5bb5418d3be4b74555eb20168113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674363"
---
# <span data-ttu-id="2b32e-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="2b32e-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="2b32e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b32e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b32e-103">Creare un oggetto RuleGroupOverride per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="2b32e-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="2b32e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b32e-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b32e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b32e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b32e-106">Creare un oggetto RuleGroupOverride per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="2b32e-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="2b32e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b32e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b32e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b32e-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="2b32e-109">Creare un oggetto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2b32e-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="2b32e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b32e-110">PARAMETERS</span></span>

### <span data-ttu-id="2b32e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b32e-111">-DefaultProfile</span></span>
<span data-ttu-id="2b32e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b32e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b32e-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2b32e-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="2b32e-114">Elenco di override della regola</span><span class="sxs-lookup"><span data-stu-id="2b32e-114">Rule override list</span></span>

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

### <span data-ttu-id="2b32e-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="2b32e-115">-RuleGroupName</span></span>
<span data-ttu-id="2b32e-116">Nome del gruppo di regole per cui si applicano queste sostituzioni</span><span class="sxs-lookup"><span data-stu-id="2b32e-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="2b32e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b32e-117">CommonParameters</span></span>
<span data-ttu-id="2b32e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b32e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b32e-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b32e-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b32e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b32e-120">INPUTS</span></span>

### <span data-ttu-id="2b32e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b32e-121">None</span></span>

## <span data-ttu-id="2b32e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b32e-122">OUTPUTS</span></span>

### <span data-ttu-id="2b32e-123">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2b32e-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="2b32e-124">Note</span><span class="sxs-lookup"><span data-stu-id="2b32e-124">NOTES</span></span>

## <span data-ttu-id="2b32e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b32e-125">RELATED LINKS</span></span>

[<span data-ttu-id="2b32e-126">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2b32e-126">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
