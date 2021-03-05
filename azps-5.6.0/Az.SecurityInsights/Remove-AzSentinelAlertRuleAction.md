---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 0828961a534a6f98d52cdf8c4e2a134cc2975df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963630"
---
# <span data-ttu-id="c38e3-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="c38e3-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="c38e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c38e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c38e3-103">Rimuovere una risposta automatica da un'analisi analitica.</span><span class="sxs-lookup"><span data-stu-id="c38e3-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="c38e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c38e3-104">SYNTAX</span></span>

### <span data-ttu-id="c38e3-105">ActionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c38e3-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c38e3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c38e3-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c38e3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c38e3-107">DESCRIPTION</span></span>
<span data-ttu-id="c38e3-108">Il cmdlet **Remove-AzSentinelAlertRuleAction** elimina definitivamente una risposta automatica dalla regola di avviso in un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c38e3-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="c38e3-109">È possibile passare un **oggetto AlertRuleAction usando** l'operatore della pipeline oppure in alternativa è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="c38e3-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="c38e3-110">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c38e3-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c38e3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c38e3-111">EXAMPLES</span></span>

### <span data-ttu-id="c38e3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c38e3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="c38e3-113">Questo comando rimuove la regola di avviso dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c38e3-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="c38e3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c38e3-114">PARAMETERS</span></span>

### <span data-ttu-id="c38e3-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="c38e3-115">-ActionId</span></span>
<span data-ttu-id="c38e3-116">ID azione.</span><span class="sxs-lookup"><span data-stu-id="c38e3-116">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38e3-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c38e3-117">-AlertRuleId</span></span>
<span data-ttu-id="c38e3-118">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="c38e3-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38e3-119">-DefaultProfile</span></span>
<span data-ttu-id="c38e3-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c38e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c38e3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c38e3-121">-InputObject</span></span>
<span data-ttu-id="c38e3-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="c38e3-122">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c38e3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c38e3-123">-PassThru</span></span>
<span data-ttu-id="c38e3-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="c38e3-124">PassThru</span></span>

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

### <span data-ttu-id="c38e3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38e3-125">-ResourceGroupName</span></span>
<span data-ttu-id="c38e3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c38e3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38e3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c38e3-127">-WorkspaceName</span></span>
<span data-ttu-id="c38e3-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c38e3-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38e3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c38e3-129">-Confirm</span></span>
<span data-ttu-id="c38e3-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38e3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c38e3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38e3-131">-WhatIf</span></span>
<span data-ttu-id="c38e3-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c38e3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c38e3-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c38e3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c38e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38e3-134">CommonParameters</span></span>
<span data-ttu-id="c38e3-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38e3-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c38e3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38e3-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="c38e3-137">INPUTS</span></span>

### <span data-ttu-id="c38e3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c38e3-138">System.String</span></span>
### <span data-ttu-id="c38e3-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="c38e3-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="c38e3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c38e3-140">OUTPUTS</span></span>

### <span data-ttu-id="c38e3-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="c38e3-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="c38e3-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="c38e3-142">NOTES</span></span>

## <span data-ttu-id="c38e3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c38e3-143">RELATED LINKS</span></span>
