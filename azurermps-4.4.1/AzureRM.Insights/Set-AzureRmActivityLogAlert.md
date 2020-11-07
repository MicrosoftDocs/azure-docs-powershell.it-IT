---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686830"
---
# <span data-ttu-id="12135-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12135-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="12135-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12135-102">SYNOPSIS</span></span>
<span data-ttu-id="12135-103">Crea un nuovo o imposta un avviso del log attività esistente.</span><span class="sxs-lookup"><span data-stu-id="12135-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12135-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12135-104">SYNTAX</span></span>

### <span data-ttu-id="12135-105">Parametri predefiniti per l'avviso imposta log attività</span><span class="sxs-lookup"><span data-stu-id="12135-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12135-106">Parametri per impostare gli avvisi del log attività che impiegano il valore di ResourceId dalla pipe</span><span class="sxs-lookup"><span data-stu-id="12135-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12135-107">Parametri per impostare gli avvisi del log attività che prendono valore dalla pipe</span><span class="sxs-lookup"><span data-stu-id="12135-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12135-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12135-108">DESCRIPTION</span></span>
<span data-ttu-id="12135-109">Il cmdlet **set-AzureRmActivityLogAlert** crea un nuovo o imposta un avviso del log attività esistente.</span><span class="sxs-lookup"><span data-stu-id="12135-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="12135-110">Per tag, condizioni e azioni gli oggetti devono essere creati in anticipo e passati come parametri in questa chiamata come separati da virgola (Vedi l'esempio seguente).</span><span class="sxs-lookup"><span data-stu-id="12135-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="12135-111">Questo cmdlet implementa il modello ShouldProcess, ossia potrebbe richiedere la conferma da parte dell'utente prima di creare o modificare effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="12135-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="12135-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12135-112">EXAMPLES</span></span>

### <span data-ttu-id="12135-113">Esempio 1: creare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="12135-113">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="12135-114">I primi quattro comandi creano la condizione foglia e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="12135-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="12135-115">Il comando finale crea un avviso del log attività usando la condizione e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="12135-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="12135-116">Esempio 2: creare un avviso del log attività disabilitato</span><span class="sxs-lookup"><span data-stu-id="12135-116">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="12135-117">I primi quattro comandi creano la condizione foglia e il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="12135-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="12135-118">Il comando finale crea un avviso del log attività usando la condizione e il gruppo di azioni, ma crea l'avviso disabilitato.</span><span class="sxs-lookup"><span data-stu-id="12135-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="12135-119">Esempio 3: impostare un avviso del log attività basato su un valore della pipe o del parametro InputObject</span><span class="sxs-lookup"><span data-stu-id="12135-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="12135-120">Il primo comando è simile a un NOP, imposta l'avviso con gli stessi valori già contenuta nel resto dei comandi recupera la regola di avviso, modifica la descrizione e la Disabilita, quindi usa il parametro InputObject per rendere persistenti tali modifiche.</span><span class="sxs-lookup"><span data-stu-id="12135-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="12135-121">Esempio 4: impostare un avviso del log attività basato sul valore ResourceId della pipe</span><span class="sxs-lookup"><span data-stu-id="12135-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="12135-122">Se la regola di avviso del log specificata esiste, questo comando lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="12135-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="12135-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12135-123">PARAMETERS</span></span>

### <span data-ttu-id="12135-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="12135-124">-Location</span></span>
<span data-ttu-id="12135-125">Posizione in cui è presente l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="12135-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="12135-126">-Name</span></span>
<span data-ttu-id="12135-127">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="12135-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12135-128">-ResourceGroupName</span></span>
<span data-ttu-id="12135-129">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="12135-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-130">-Ambito</span><span class="sxs-lookup"><span data-stu-id="12135-130">-Scope</span></span>
<span data-ttu-id="12135-131">Elenco di ambiti per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="12135-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-132">-Condition</span><span class="sxs-lookup"><span data-stu-id="12135-132">-Condition</span></span>
<span data-ttu-id="12135-133">Elenco delle condizioni per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="12135-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="12135-134">**Nota** : nell'elenco delle condizioni deve essere presente almeno uno con il campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="12135-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="12135-135">Il backend risponde con 400 (BadRequest) se questa condizione non è presente.</span><span class="sxs-lookup"><span data-stu-id="12135-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-136">-Azione</span><span class="sxs-lookup"><span data-stu-id="12135-136">-Action</span></span>
<span data-ttu-id="12135-137">Elenco di gruppi di azioni per l'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="12135-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="12135-138">-DisableAlert</span></span>
<span data-ttu-id="12135-139">Consente all'utente di creare un avviso di registro attività disabilitato.</span><span class="sxs-lookup"><span data-stu-id="12135-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="12135-140">Se non viene assegnato, gli avvisi vengono creati abilitati.</span><span class="sxs-lookup"><span data-stu-id="12135-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12135-141">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="12135-141">-Description</span></span>
<span data-ttu-id="12135-142">Descrizione della risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="12135-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="12135-143">-Tag</span></span>
<span data-ttu-id="12135-144">Imposta la proprietà Tags della risorsa di avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="12135-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12135-145">-InputObject</span></span>
<span data-ttu-id="12135-146">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12135-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12135-147">-ResourceId</span></span>
<span data-ttu-id="12135-148">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="12135-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12135-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12135-149">-Confirm</span></span>
<span data-ttu-id="12135-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12135-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12135-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12135-151">-DefaultProfile</span></span>
<span data-ttu-id="12135-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12135-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12135-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12135-153">-WhatIf</span></span>
<span data-ttu-id="12135-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12135-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12135-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12135-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12135-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12135-156">CommonParameters</span></span>
<span data-ttu-id="12135-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12135-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12135-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12135-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12135-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12135-159">INPUTS</span></span>

## <span data-ttu-id="12135-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12135-160">OUTPUTS</span></span>

### <span data-ttu-id="12135-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="12135-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="12135-162">Note</span><span class="sxs-lookup"><span data-stu-id="12135-162">NOTES</span></span>

## <span data-ttu-id="12135-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12135-163">RELATED LINKS</span></span>

[<span data-ttu-id="12135-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12135-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12135-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12135-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12135-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12135-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12135-167">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12135-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12135-168">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="12135-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="12135-169">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="12135-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
