---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 97a1fa7aa5488034fa1f0147ae5a06ff639ecc06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969054"
---
# <span data-ttu-id="9b96c-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="9b96c-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="9b96c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b96c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b96c-103">Crea un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-103">Creates a function app.</span></span>

## <span data-ttu-id="9b96c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b96c-104">SYNTAX</span></span>

### <span data-ttu-id="9b96c-105">Consumo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b96c-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9b96c-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b96c-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9b96c-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="9b96c-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9b96c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b96c-108">DESCRIPTION</span></span>
<span data-ttu-id="9b96c-109">Crea un'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-109">Creates a function app.</span></span>

## <span data-ttu-id="9b96c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b96c-110">EXAMPLES</span></span>

### <span data-ttu-id="9b96c-111">Esempio 1: Creare un'app funzione di PowerShell a consumo negli Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="9b96c-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="9b96c-112">Questo comando crea un'app funzione di PowerShell a consumo negli Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="9b96c-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="9b96c-113">Esempio 2: Creare un'app con funzioni di PowerShell che verrà ospitata in un piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="9b96c-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="9b96c-114">Questo comando crea un'app funzione di PowerShell che verrà ospitata in un piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="9b96c-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="9b96c-115">Esempio 3: Creare un'app function usando un'immagine ACR privata.</span><span class="sxs-lookup"><span data-stu-id="9b96c-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="9b96c-116">Questo comando crea un'app function usando un'immagine ACR privata.</span><span class="sxs-lookup"><span data-stu-id="9b96c-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="9b96c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b96c-117">PARAMETERS</span></span>

### <span data-ttu-id="9b96c-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="9b96c-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="9b96c-119">Chiave univoca di Approfondimenti app da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9b96c-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="9b96c-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="9b96c-121">Nome del progetto Approfondimenti app esistente da aggiungere all'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="9b96c-122">-AppSetting</span></span>
<span data-ttu-id="9b96c-123">Impostazioni delle app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-123">Function app settings.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b96c-124">-AsJob</span></span>
<span data-ttu-id="9b96c-125">Esegue il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="9b96c-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="9b96c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b96c-126">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9b96c-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="9b96c-128">Disabilitare la creazione di informazioni dettagliate sull'applicazione durante la creazione dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="9b96c-129">Non saranno disponibili log.</span><span class="sxs-lookup"><span data-stu-id="9b96c-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="9b96c-130">-DockerImageName</span></span>
<span data-ttu-id="9b96c-131">Solo Linux.</span><span class="sxs-lookup"><span data-stu-id="9b96c-131">Linux only.</span></span>
<span data-ttu-id="9b96c-132">Nome dell'immagine contenitore del Registro di sistema di Docker, ad esempio publisher/image-name:tag.</span><span class="sxs-lookup"><span data-stu-id="9b96c-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9b96c-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="9b96c-134">Nome utente e password del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="9b96c-134">The container registry user name and password.</span></span>
<span data-ttu-id="9b96c-135">Obbligatorio per i registri privati.</span><span class="sxs-lookup"><span data-stu-id="9b96c-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="9b96c-136">-FunctionsVersion</span></span>
<span data-ttu-id="9b96c-137">Versione di Funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="9b96c-138">-IdentityID</span></span>
<span data-ttu-id="9b96c-139">Specifica l'elenco di identità utente associate all'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="9b96c-140">I riferimenti di identità utente ARM id risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="9b96c-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9b96c-141">-IdentityType</span></span>
<span data-ttu-id="9b96c-142">Specifica il tipo di identità usato per l'app function.</span><span class="sxs-lookup"><span data-stu-id="9b96c-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="9b96c-143">I valori accettabili per questo parametro sono: - SystemAssigned - UserAssigned</span><span class="sxs-lookup"><span data-stu-id="9b96c-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-144">-Location</span><span class="sxs-lookup"><span data-stu-id="9b96c-144">-Location</span></span>
<span data-ttu-id="9b96c-145">Posizione del piano di consumo.</span><span class="sxs-lookup"><span data-stu-id="9b96c-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-146">-Name</span><span class="sxs-lookup"><span data-stu-id="9b96c-146">-Name</span></span>
<span data-ttu-id="9b96c-147">Nome dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-147">The name of the function app.</span></span>

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

### <span data-ttu-id="9b96c-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9b96c-148">-NoWait</span></span>
<span data-ttu-id="9b96c-149">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9b96c-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="9b96c-150">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="9b96c-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9b96c-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="9b96c-151">-OSType</span></span>
<span data-ttu-id="9b96c-152">Sistema operativo per ospitare l'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b96c-153">-PassThru</span></span>
<span data-ttu-id="9b96c-154">Restituisce true quando il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9b96c-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="9b96c-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9b96c-155">-PlanName</span></span>
<span data-ttu-id="9b96c-156">Nome del piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="9b96c-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b96c-157">-ResourceGroupName</span></span>
<span data-ttu-id="9b96c-158">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b96c-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b96c-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="9b96c-159">-Runtime</span></span>
<span data-ttu-id="9b96c-160">Runtime delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="9b96c-161">-RuntimeVersion</span></span>
<span data-ttu-id="9b96c-162">Runtime delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="9b96c-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b96c-163">-StorageAccountName</span></span>
<span data-ttu-id="9b96c-164">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9b96c-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="9b96c-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b96c-165">-SubscriptionId</span></span>
<span data-ttu-id="9b96c-166">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b96c-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b96c-167">-Tag</span></span>
<span data-ttu-id="9b96c-168">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b96c-168">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b96c-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b96c-169">-Confirm</span></span>
<span data-ttu-id="9b96c-170">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b96c-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b96c-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b96c-171">-WhatIf</span></span>
<span data-ttu-id="9b96c-172">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b96c-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b96c-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b96c-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b96c-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b96c-174">CommonParameters</span></span>
<span data-ttu-id="9b96c-175">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b96c-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b96c-176">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b96c-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b96c-177">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b96c-177">INPUTS</span></span>

## <span data-ttu-id="9b96c-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b96c-178">OUTPUTS</span></span>

### <span data-ttu-id="9b96c-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="9b96c-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="9b96c-180">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b96c-180">NOTES</span></span>

<span data-ttu-id="9b96c-181">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9b96c-181">ALIASES</span></span>

## <span data-ttu-id="9b96c-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b96c-182">RELATED LINKS</span></span>

