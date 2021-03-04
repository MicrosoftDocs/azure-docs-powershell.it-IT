---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 3feb6a9cfa06e06a4759c34e3c0b2cd624559d2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955646"
---
# <span data-ttu-id="c5c06-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="c5c06-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="c5c06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c06-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c06-103">Aggiornare una risposta automatica (azione regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="c5c06-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="c5c06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5c06-104">SYNTAX</span></span>

### <span data-ttu-id="c5c06-105">ActionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5c06-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c06-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c5c06-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5c06-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c06-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5c06-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5c06-108">DESCRIPTION</span></span>
<span data-ttu-id="c5c06-109">Il cmdlet **Update-AzSentinelAlertRuleAction** aggiorna il segnalibro nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c5c06-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="c5c06-110">È possibile passare un **oggetto AlertRuleAction** come parametro o usando l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *AlertRuleId* *e ActionId.*</span><span class="sxs-lookup"><span data-stu-id="c5c06-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="c5c06-111">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c5c06-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c5c06-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5c06-112">EXAMPLES</span></span>

### <span data-ttu-id="c5c06-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5c06-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="c5c06-114">Questo esempio aggiorna **un'azione AlertRuleAction** sostituendo un'azione *esistente* con nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5c06-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="c5c06-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c5c06-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="c5c06-116">Questo esempio aggiorna **un oggetto AlertRuleAction** usando un oggetto InputObject sostituendo un'azione *esistente* con nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5c06-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="c5c06-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5c06-117">PARAMETERS</span></span>

### <span data-ttu-id="c5c06-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="c5c06-118">-ActionId</span></span>
<span data-ttu-id="c5c06-119">ID azione.</span><span class="sxs-lookup"><span data-stu-id="c5c06-119">Action Id.</span></span>

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

### <span data-ttu-id="c5c06-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c5c06-120">-AlertRuleId</span></span>
<span data-ttu-id="c5c06-121">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="c5c06-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="c5c06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c06-122">-DefaultProfile</span></span>
<span data-ttu-id="c5c06-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c06-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5c06-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5c06-124">-InputObject</span></span>
<span data-ttu-id="c5c06-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="c5c06-125">InputObject.</span></span>

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

### <span data-ttu-id="c5c06-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c06-126">-LogicAppResourceId</span></span>
<span data-ttu-id="c5c06-127">ID risorsa app logica azione.</span><span class="sxs-lookup"><span data-stu-id="c5c06-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="c5c06-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c06-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5c06-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5c06-129">Resource group name.</span></span>

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

### <span data-ttu-id="c5c06-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c06-130">-ResourceId</span></span>
<span data-ttu-id="c5c06-131">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5c06-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c06-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="c5c06-132">-TriggerUri</span></span>
<span data-ttu-id="c5c06-133">Uri del trigger dell'app per la logica di azione.</span><span class="sxs-lookup"><span data-stu-id="c5c06-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="c5c06-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5c06-134">-WorkspaceName</span></span>
<span data-ttu-id="c5c06-135">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c5c06-135">Workspace Name.</span></span>

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

### <span data-ttu-id="c5c06-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5c06-136">-Confirm</span></span>
<span data-ttu-id="c5c06-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5c06-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c06-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c06-138">-WhatIf</span></span>
<span data-ttu-id="c5c06-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5c06-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c06-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5c06-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5c06-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c06-141">CommonParameters</span></span>
<span data-ttu-id="c5c06-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c06-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c06-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5c06-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c06-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5c06-144">INPUTS</span></span>

### <span data-ttu-id="c5c06-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5c06-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="c5c06-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="c5c06-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="c5c06-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c5c06-147">System.String</span></span>

## <span data-ttu-id="c5c06-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5c06-148">OUTPUTS</span></span>

### <span data-ttu-id="c5c06-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="c5c06-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="c5c06-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5c06-150">NOTES</span></span>

## <span data-ttu-id="c5c06-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5c06-151">RELATED LINKS</span></span>
