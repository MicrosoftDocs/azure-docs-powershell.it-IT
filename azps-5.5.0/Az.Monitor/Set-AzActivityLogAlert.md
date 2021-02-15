---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 2ce25f0881fff9ee684bcf234d13d847b7f28850
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190095"
---
# <span data-ttu-id="8fe87-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8fe87-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="8fe87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe87-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe87-103">Crea un nuovo avviso del log attività o lo imposta.</span><span class="sxs-lookup"><span data-stu-id="8fe87-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="8fe87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fe87-104">SYNTAX</span></span>

### <span data-ttu-id="8fe87-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8fe87-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fe87-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe87-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fe87-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8fe87-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fe87-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8fe87-108">DESCRIPTION</span></span>
<span data-ttu-id="8fe87-109">Il cmdlet **Set-AzActivityLogAlert** crea una nuova azione o imposta un avviso del log attività esistente.</span><span class="sxs-lookup"><span data-stu-id="8fe87-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="8fe87-110">Per tag, condizioni e azioni, gli oggetti devono essere creati in anticipo e passati come parametri in questa chiamata come valori separati da virgola (vedere l'esempio seguente).</span><span class="sxs-lookup"><span data-stu-id="8fe87-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="8fe87-111">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare o modificare effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8fe87-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="8fe87-112">**NOTA:** questo cmdlet e quelli correlati sostituiscono **add-AzLogAlertRule** deprecato (novembre 2017).</span><span class="sxs-lookup"><span data-stu-id="8fe87-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="8fe87-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fe87-113">EXAMPLES</span></span>

### <span data-ttu-id="8fe87-114">Esempio 1: Creare un avviso di log attività</span><span class="sxs-lookup"><span data-stu-id="8fe87-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="8fe87-115">I primi quattro comandi creano una condizione foglia e un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8fe87-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="8fe87-116">Il comando finale crea un avviso del log attività usando la condizione e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8fe87-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="8fe87-117">Esempio 2: Creare un avviso di log attività disabilitato</span><span class="sxs-lookup"><span data-stu-id="8fe87-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="8fe87-118">I primi quattro comandi creano una condizione foglia e un gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="8fe87-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="8fe87-119">Il comando finale crea un avviso del log attività usando la condizione e il gruppo di azioni, ma crea l'avviso disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8fe87-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="8fe87-120">Esempio 3: Impostare un avviso del log attività in base a un valore della barra verticale o al parametro InputObject</span><span class="sxs-lookup"><span data-stu-id="8fe87-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="8fe87-121">Il primo comando è simile a nop, imposta l'avviso con gli stessi valori che conteneva Già Gli altri comandi recuperano la regola di avviso, modificano la descrizione e la disabilitano, quindi usano il parametro InputObject per rendere persistenti le modifiche</span><span class="sxs-lookup"><span data-stu-id="8fe87-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="8fe87-122">Esempio 4: Impostare un avviso del log attività in base al valore ResourceId della barra verticale</span><span class="sxs-lookup"><span data-stu-id="8fe87-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="8fe87-123">Se esiste una determinata regola di avviso per il log, questo comando la disabilita.</span><span class="sxs-lookup"><span data-stu-id="8fe87-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="8fe87-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fe87-124">PARAMETERS</span></span>

### <span data-ttu-id="8fe87-125">-Action</span><span class="sxs-lookup"><span data-stu-id="8fe87-125">-Action</span></span>
<span data-ttu-id="8fe87-126">Elenco di gruppi di azioni per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8fe87-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-127">-Condizione</span><span class="sxs-lookup"><span data-stu-id="8fe87-127">-Condition</span></span>
<span data-ttu-id="8fe87-128">Elenco di condizioni per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8fe87-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="8fe87-129">**NOTA:** nell'elenco delle condizioni deve esserci almeno un campo il cui campo è uguale a "Categoria".</span><span class="sxs-lookup"><span data-stu-id="8fe87-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="8fe87-130">Il back-end risponde con 400 (BadRequest) se questa condizione non è presente.</span><span class="sxs-lookup"><span data-stu-id="8fe87-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe87-131">-DefaultProfile</span></span>
<span data-ttu-id="8fe87-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8fe87-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fe87-133">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe87-133">-Description</span></span>
<span data-ttu-id="8fe87-134">Descrizione della risorsa avviso.</span><span class="sxs-lookup"><span data-stu-id="8fe87-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="8fe87-135">-DisableAlert</span></span>
<span data-ttu-id="8fe87-136">Consente all'utente di creare un avviso nel log attività disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8fe87-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="8fe87-137">Se non viene specificato, gli avvisi vengono creati abilitati.</span><span class="sxs-lookup"><span data-stu-id="8fe87-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fe87-138">-InputObject</span></span>
<span data-ttu-id="8fe87-139">Imposta la proprietà tag InputObject della chiamata per estrarre il nome richiesto e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8fe87-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-140">-Location</span><span class="sxs-lookup"><span data-stu-id="8fe87-140">-Location</span></span>
<span data-ttu-id="8fe87-141">Posizione in cui verrà visualizzato l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8fe87-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-142">-Name</span><span class="sxs-lookup"><span data-stu-id="8fe87-142">-Name</span></span>
<span data-ttu-id="8fe87-143">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8fe87-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe87-144">-ResourceGroupName</span></span>
<span data-ttu-id="8fe87-145">Nome del gruppo di risorse in cui si trova la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="8fe87-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe87-146">-ResourceId</span></span>
<span data-ttu-id="8fe87-147">Imposta la proprietà tag ResourceId della chiamata per estrarre il nome richiesto e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8fe87-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="8fe87-148">-Scope</span></span>
<span data-ttu-id="8fe87-149">Elenco degli ambiti per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8fe87-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="8fe87-150">-Tag</span></span>
<span data-ttu-id="8fe87-151">Imposta la proprietà tag della risorsa avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="8fe87-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe87-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fe87-152">-Confirm</span></span>
<span data-ttu-id="8fe87-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fe87-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fe87-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fe87-154">-WhatIf</span></span>
<span data-ttu-id="8fe87-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fe87-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fe87-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fe87-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fe87-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe87-157">CommonParameters</span></span>
<span data-ttu-id="8fe87-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe87-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe87-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8fe87-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe87-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="8fe87-160">INPUTS</span></span>

### <span data-ttu-id="8fe87-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8fe87-161">System.String</span></span>

### <span data-ttu-id="8fe87-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8fe87-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8fe87-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8fe87-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8fe87-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8fe87-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8fe87-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8fe87-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8fe87-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8fe87-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8fe87-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fe87-167">OUTPUTS</span></span>

### <span data-ttu-id="8fe87-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8fe87-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8fe87-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="8fe87-169">NOTES</span></span>

## <span data-ttu-id="8fe87-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fe87-170">RELATED LINKS</span></span>

[<span data-ttu-id="8fe87-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8fe87-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="8fe87-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8fe87-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="8fe87-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8fe87-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="8fe87-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8fe87-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8fe87-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8fe87-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="8fe87-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="8fe87-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
