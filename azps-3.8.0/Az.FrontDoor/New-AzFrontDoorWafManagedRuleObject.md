---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403953"
---
# <span data-ttu-id="41dfc-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="41dfc-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="41dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="41dfc-103">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="41dfc-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="41dfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41dfc-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41dfc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="41dfc-106">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="41dfc-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="41dfc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="41dfc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41dfc-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="41dfc-109">Creare un oggetto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="41dfc-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="41dfc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="41dfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41dfc-111">-DefaultProfile</span></span>
<span data-ttu-id="41dfc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41dfc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41dfc-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="41dfc-113">-Exclusion</span></span>
<span data-ttu-id="41dfc-114">Esclusione</span><span class="sxs-lookup"><span data-stu-id="41dfc-114">Exclusion</span></span>

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

### <span data-ttu-id="41dfc-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="41dfc-115">-RuleGroupOverride</span></span>
<span data-ttu-id="41dfc-116">Elenco della configurazione override del provider gestito da Azure</span><span class="sxs-lookup"><span data-stu-id="41dfc-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41dfc-117">-Type</span><span class="sxs-lookup"><span data-stu-id="41dfc-117">-Type</span></span>
<span data-ttu-id="41dfc-118">Tipo del set di regole</span><span class="sxs-lookup"><span data-stu-id="41dfc-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="41dfc-119">-Version</span><span class="sxs-lookup"><span data-stu-id="41dfc-119">-Version</span></span>
<span data-ttu-id="41dfc-120">Versione del set di regole</span><span class="sxs-lookup"><span data-stu-id="41dfc-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="41dfc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41dfc-121">CommonParameters</span></span>
<span data-ttu-id="41dfc-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41dfc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41dfc-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41dfc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41dfc-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="41dfc-124">INPUTS</span></span>

### <span data-ttu-id="41dfc-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="41dfc-125">None</span></span>

## <span data-ttu-id="41dfc-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41dfc-126">OUTPUTS</span></span>

### <span data-ttu-id="41dfc-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="41dfc-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="41dfc-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="41dfc-128">NOTES</span></span>

## <span data-ttu-id="41dfc-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41dfc-129">RELATED LINKS</span></span>

<span data-ttu-id="41dfc-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="41dfc-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
