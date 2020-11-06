---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 66c127e701432604654cacb556d71588d9786dbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509859"
---
# <span data-ttu-id="bb774-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bb774-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="bb774-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb774-102">SYNOPSIS</span></span>
<span data-ttu-id="bb774-103">Crea un nuovo o imposta un avviso del log attività esistente.</span><span class="sxs-lookup"><span data-stu-id="bb774-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb774-104">SYNTAX</span></span>

### <span data-ttu-id="bb774-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb774-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb774-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb774-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb774-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb774-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb774-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb774-108">DESCRIPTION</span></span>
<span data-ttu-id="bb774-109">Il cmdlet **set-AzureRmActivityLogAlert** crea un nuovo o imposta un avviso del log attività esistente.</span><span class="sxs-lookup"><span data-stu-id="bb774-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="bb774-110">Per tag, condizioni e azioni gli oggetti devono essere creati in anticipo e passati come parametri in questa chiamata come separati da virgola (Vedi l'esempio seguente).</span><span class="sxs-lookup"><span data-stu-id="bb774-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="bb774-111">Questo cmdlet implementa il modello ShouldProcess, ossia potrebbe richiedere la conferma da parte dell'utente prima di creare o modificare effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bb774-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

<span data-ttu-id="bb774-112">**Nota** : questo cmdlet e i relativi correlati sostituiscono il **componente aggiuntivo** deprecato (2017 novembre) AzureRmLogAlertRule.</span><span class="sxs-lookup"><span data-stu-id="bb774-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="bb774-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb774-113">EXAMPLES</span></span>

### <span data-ttu-id="bb774-114">Esempio 1: creare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="bb774-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="bb774-115">I primi quattro comandi creano la condizione foglia e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="bb774-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="bb774-116">Il comando finale crea un avviso del log attività usando la condizione e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="bb774-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="bb774-117">Esempio 2: creare un avviso del log attività disabilitato</span><span class="sxs-lookup"><span data-stu-id="bb774-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="bb774-118">I primi quattro comandi creano la condizione foglia e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="bb774-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="bb774-119">Il comando finale crea un avviso del log attività usando la condizione e il gruppo di azioni, ma crea l'avviso disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bb774-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="bb774-120">Esempio 3: impostare un avviso del log attività basato su un valore della pipe o del parametro InputObject</span><span class="sxs-lookup"><span data-stu-id="bb774-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="bb774-121">Il primo comando è simile a un NOP, imposta l'avviso con gli stessi valori già contenuta nel resto dei comandi recupera la regola di avviso, modifica la descrizione e la Disabilita, quindi usa il parametro InputObject per rendere persistenti tali modifiche.</span><span class="sxs-lookup"><span data-stu-id="bb774-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="bb774-122">Esempio 4: impostare un avviso del log attività basato sul valore ResourceId della pipe</span><span class="sxs-lookup"><span data-stu-id="bb774-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="bb774-123">Se la regola di avviso del log specificata esiste, questo comando lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="bb774-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="bb774-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb774-124">PARAMETERS</span></span>

### <span data-ttu-id="bb774-125">-Azione</span><span class="sxs-lookup"><span data-stu-id="bb774-125">-Action</span></span>
<span data-ttu-id="bb774-126">Elenco di gruppi di azioni per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="bb774-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="bb774-127">-Condition</span><span class="sxs-lookup"><span data-stu-id="bb774-127">-Condition</span></span>
<span data-ttu-id="bb774-128">Elenco delle condizioni per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="bb774-128">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="bb774-129">**Nota** : nell'elenco delle condizioni deve essere presente almeno uno con il campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="bb774-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="bb774-130">Il backend risponde con 400 (BadRequest) se questa condizione non è presente.</span><span class="sxs-lookup"><span data-stu-id="bb774-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="bb774-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb774-131">-DefaultProfile</span></span>
<span data-ttu-id="bb774-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb774-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-133">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb774-133">-Description</span></span>
<span data-ttu-id="bb774-134">Descrizione della risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="bb774-134">The description of the alert resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="bb774-135">-DisableAlert</span></span>
<span data-ttu-id="bb774-136">Consente all'utente di creare un avviso di registro attività disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bb774-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="bb774-137">Se non viene assegnato, gli avvisi vengono creati abilitati.</span><span class="sxs-lookup"><span data-stu-id="bb774-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb774-138">-InputObject</span></span>
<span data-ttu-id="bb774-139">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb774-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-140">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bb774-140">-Location</span></span>
<span data-ttu-id="bb774-141">Posizione in cui è presente l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="bb774-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb774-142">-Name</span></span>
<span data-ttu-id="bb774-143">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="bb774-143">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb774-144">-ResourceGroupName</span></span>
<span data-ttu-id="bb774-145">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="bb774-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb774-146">-ResourceId</span></span>
<span data-ttu-id="bb774-147">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="bb774-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-148">-Ambito</span><span class="sxs-lookup"><span data-stu-id="bb774-148">-Scope</span></span>
<span data-ttu-id="bb774-149">Elenco di ambiti per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="bb774-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="bb774-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb774-150">-Tag</span></span>
<span data-ttu-id="bb774-151">Imposta la proprietà Tags della risorsa di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="bb774-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="bb774-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb774-152">-Confirm</span></span>
<span data-ttu-id="bb774-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb774-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb774-154">-WhatIf</span></span>
<span data-ttu-id="bb774-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb774-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb774-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb774-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb774-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb774-157">CommonParameters</span></span>
<span data-ttu-id="bb774-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb774-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb774-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb774-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb774-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb774-160">INPUTS</span></span>

### <span data-ttu-id="bb774-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bb774-161">None</span></span>
<span data-ttu-id="bb774-162">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bb774-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb774-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb774-163">OUTPUTS</span></span>

### <span data-ttu-id="bb774-164">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="bb774-164">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="bb774-165">Note</span><span class="sxs-lookup"><span data-stu-id="bb774-165">NOTES</span></span>

## <span data-ttu-id="bb774-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb774-166">RELATED LINKS</span></span>

[<span data-ttu-id="bb774-167">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bb774-167">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bb774-168">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bb774-168">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bb774-169">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bb774-169">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bb774-170">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bb774-170">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bb774-171">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="bb774-171">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="bb774-172">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="bb774-172">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
