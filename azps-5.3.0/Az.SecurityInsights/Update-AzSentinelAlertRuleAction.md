---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486155"
---
# <span data-ttu-id="7856a-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="7856a-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="7856a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7856a-102">SYNOPSIS</span></span>
<span data-ttu-id="7856a-103">Aggiornare una risposta automatica (azione regola di avviso).</span><span class="sxs-lookup"><span data-stu-id="7856a-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="7856a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7856a-104">SYNTAX</span></span>

### <span data-ttu-id="7856a-105">ActionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7856a-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7856a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7856a-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7856a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7856a-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7856a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7856a-108">DESCRIPTION</span></span>
<span data-ttu-id="7856a-109">Il cmdlet **Update-AzSentinelAlertRuleAction** aggiorna il segnalibro nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="7856a-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="7856a-110">Puoi passare un oggetto **AlertRuleAction** come parametro o usando l'operatore pipeline o in alternativa puoi specificare i parametri *AlertRuleId* e *ActionId* .</span><span class="sxs-lookup"><span data-stu-id="7856a-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="7856a-111">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="7856a-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7856a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7856a-112">EXAMPLES</span></span>

### <span data-ttu-id="7856a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7856a-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="7856a-114">Questo esempio aggiorna un **AlertRuleAction** che sostituisce un' *azione* esistente con nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="7856a-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="7856a-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7856a-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="7856a-116">Questo esempio aggiorna un **AlertRuleAction** usando un InputObject che sostituisce un' *azione* esistente con nuove proprietà.</span><span class="sxs-lookup"><span data-stu-id="7856a-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="7856a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7856a-117">PARAMETERS</span></span>

### <span data-ttu-id="7856a-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="7856a-118">-ActionId</span></span>
<span data-ttu-id="7856a-119">ID azione.</span><span class="sxs-lookup"><span data-stu-id="7856a-119">Action Id.</span></span>

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

### <span data-ttu-id="7856a-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="7856a-120">-AlertRuleId</span></span>
<span data-ttu-id="7856a-121">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="7856a-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="7856a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7856a-122">-DefaultProfile</span></span>
<span data-ttu-id="7856a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7856a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7856a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7856a-124">-InputObject</span></span>
<span data-ttu-id="7856a-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="7856a-125">InputObject.</span></span>

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

### <span data-ttu-id="7856a-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="7856a-126">-LogicAppResourceId</span></span>
<span data-ttu-id="7856a-127">ID risorsa delle app logiche di azione.</span><span class="sxs-lookup"><span data-stu-id="7856a-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="7856a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7856a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7856a-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7856a-129">Resource group name.</span></span>

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

### <span data-ttu-id="7856a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7856a-130">-ResourceId</span></span>
<span data-ttu-id="7856a-131">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7856a-131">Resource Id.</span></span>

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

### <span data-ttu-id="7856a-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="7856a-132">-TriggerUri</span></span>
<span data-ttu-id="7856a-133">URI trigger dell'app logica di azione.</span><span class="sxs-lookup"><span data-stu-id="7856a-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="7856a-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7856a-134">-WorkspaceName</span></span>
<span data-ttu-id="7856a-135">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7856a-135">Workspace Name.</span></span>

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

### <span data-ttu-id="7856a-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7856a-136">-Confirm</span></span>
<span data-ttu-id="7856a-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7856a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7856a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7856a-138">-WhatIf</span></span>
<span data-ttu-id="7856a-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7856a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7856a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7856a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7856a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7856a-141">CommonParameters</span></span>
<span data-ttu-id="7856a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7856a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7856a-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7856a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7856a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7856a-144">INPUTS</span></span>

### <span data-ttu-id="7856a-145">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="7856a-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="7856a-146">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="7856a-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="7856a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7856a-147">System.String</span></span>

## <span data-ttu-id="7856a-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7856a-148">OUTPUTS</span></span>

### <span data-ttu-id="7856a-149">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="7856a-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="7856a-150">Note</span><span class="sxs-lookup"><span data-stu-id="7856a-150">NOTES</span></span>

## <span data-ttu-id="7856a-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7856a-151">RELATED LINKS</span></span>
