---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: af63ecd604f6ea7e475fcc8034a4e4b6d532069e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963646"
---
# <span data-ttu-id="fc468-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fc468-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="fc468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc468-102">SYNOPSIS</span></span>
<span data-ttu-id="fc468-103">Eliminare un'analisi.</span><span class="sxs-lookup"><span data-stu-id="fc468-103">Delete an Analytic.</span></span>

## <span data-ttu-id="fc468-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc468-104">SYNTAX</span></span>

### <span data-ttu-id="fc468-105">AlertRuleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc468-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc468-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc468-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc468-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc468-107">DESCRIPTION</span></span>
<span data-ttu-id="fc468-108">Il cmdlet **Remove-AzSentinelAlertRule** elimina definitivamente una regola di avviso da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="fc468-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="fc468-109">È possibile passare un **oggetto AlertRule** usando l'operatore della pipeline oppure è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="fc468-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="fc468-110">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="fc468-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="fc468-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc468-111">EXAMPLES</span></span>

### <span data-ttu-id="fc468-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc468-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="fc468-113">Questo comando rimuove la regola di avviso dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fc468-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="fc468-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc468-114">PARAMETERS</span></span>

### <span data-ttu-id="fc468-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fc468-115">-AlertRuleId</span></span>
<span data-ttu-id="fc468-116">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="fc468-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc468-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc468-117">-DefaultProfile</span></span>
<span data-ttu-id="fc468-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc468-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc468-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc468-119">-InputObject</span></span>
<span data-ttu-id="fc468-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="fc468-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc468-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc468-121">-PassThru</span></span>
<span data-ttu-id="fc468-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="fc468-122">PassThru</span></span>

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

### <span data-ttu-id="fc468-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc468-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc468-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc468-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc468-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fc468-125">-WorkspaceName</span></span>
<span data-ttu-id="fc468-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fc468-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc468-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc468-127">-Confirm</span></span>
<span data-ttu-id="fc468-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc468-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc468-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc468-129">-WhatIf</span></span>
<span data-ttu-id="fc468-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc468-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc468-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc468-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc468-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc468-132">CommonParameters</span></span>
<span data-ttu-id="fc468-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc468-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc468-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc468-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc468-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc468-135">INPUTS</span></span>

### <span data-ttu-id="fc468-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fc468-136">System.String</span></span>
### <span data-ttu-id="fc468-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fc468-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="fc468-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc468-138">OUTPUTS</span></span>

### <span data-ttu-id="fc468-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fc468-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="fc468-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc468-140">NOTES</span></span>

## <span data-ttu-id="fc468-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc468-141">RELATED LINKS</span></span>
