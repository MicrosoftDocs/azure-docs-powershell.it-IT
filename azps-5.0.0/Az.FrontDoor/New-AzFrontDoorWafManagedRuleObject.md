---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200860"
---
# <span data-ttu-id="b1e79-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b1e79-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="b1e79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1e79-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e79-103">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="b1e79-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b1e79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1e79-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1e79-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1e79-105">DESCRIPTION</span></span>
<span data-ttu-id="b1e79-106">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="b1e79-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b1e79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1e79-107">EXAMPLES</span></span>

### <span data-ttu-id="b1e79-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1e79-108">Example 1</span></span>
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

<span data-ttu-id="b1e79-109">Creare un oggetto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b1e79-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="b1e79-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1e79-110">PARAMETERS</span></span>

### <span data-ttu-id="b1e79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e79-111">-DefaultProfile</span></span>
<span data-ttu-id="b1e79-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e79-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e79-113">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="b1e79-113">-Exclusion</span></span>
<span data-ttu-id="b1e79-114">Esclusione</span><span class="sxs-lookup"><span data-stu-id="b1e79-114">Exclusion</span></span>

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

### <span data-ttu-id="b1e79-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b1e79-115">-RuleGroupOverride</span></span>
<span data-ttu-id="b1e79-116">Elenco della configurazione di override di Azure Managed provider</span><span class="sxs-lookup"><span data-stu-id="b1e79-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="b1e79-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="b1e79-117">-Type</span></span>
<span data-ttu-id="b1e79-118">Tipo di RuleSet</span><span class="sxs-lookup"><span data-stu-id="b1e79-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="b1e79-119">-Versione</span><span class="sxs-lookup"><span data-stu-id="b1e79-119">-Version</span></span>
<span data-ttu-id="b1e79-120">Versione del set di regole</span><span class="sxs-lookup"><span data-stu-id="b1e79-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="b1e79-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e79-121">CommonParameters</span></span>
<span data-ttu-id="b1e79-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1e79-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e79-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1e79-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e79-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1e79-124">INPUTS</span></span>

### <span data-ttu-id="b1e79-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1e79-125">None</span></span>

## <span data-ttu-id="b1e79-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1e79-126">OUTPUTS</span></span>

### <span data-ttu-id="b1e79-127">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="b1e79-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="b1e79-128">Note</span><span class="sxs-lookup"><span data-stu-id="b1e79-128">NOTES</span></span>

## <span data-ttu-id="b1e79-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1e79-129">RELATED LINKS</span></span>

<span data-ttu-id="b1e79-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="b1e79-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
