---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190184"
---
# <span data-ttu-id="2d89e-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="2d89e-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="2d89e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d89e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d89e-103">Crea un'app di funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-103">Creates a function app.</span></span>

## <span data-ttu-id="2d89e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d89e-104">SYNTAX</span></span>

### <span data-ttu-id="2d89e-105">Consumo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2d89e-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d89e-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d89e-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d89e-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="2d89e-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d89e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d89e-108">DESCRIPTION</span></span>
<span data-ttu-id="2d89e-109">Crea un'app di funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-109">Creates a function app.</span></span>

## <span data-ttu-id="2d89e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d89e-110">EXAMPLES</span></span>

### <span data-ttu-id="2d89e-111">Esempio 1: creare un'app per la funzione consumer PowerShell in Central US.</span><span class="sxs-lookup"><span data-stu-id="2d89e-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="2d89e-112">Questo comando crea un'app per la funzione consumer PowerShell in Central US.</span><span class="sxs-lookup"><span data-stu-id="2d89e-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="2d89e-113">Esempio 2: creare un'app di funzione di PowerShell che verrà ospitata in un piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="2d89e-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="2d89e-114">Questo comando crea un'app di funzione di PowerShell che verrà ospitata in un piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="2d89e-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="2d89e-115">Esempio 3: creare un'app funzione usando un'immagine di ACR privata.</span><span class="sxs-lookup"><span data-stu-id="2d89e-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="2d89e-116">Questo comando crea un'app di funzione usando un'immagine di ACR privata.</span><span class="sxs-lookup"><span data-stu-id="2d89e-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="2d89e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d89e-117">PARAMETERS</span></span>

### <span data-ttu-id="2d89e-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="2d89e-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="2d89e-119">Chiave di strumentazione degli Insight per l'app da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="2d89e-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="2d89e-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="2d89e-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="2d89e-121">Nome del progetto Insights app esistente da aggiungere all'app funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="2d89e-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="2d89e-122">-AppSetting</span></span>
<span data-ttu-id="2d89e-123">Impostazioni dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-123">Function app settings.</span></span>

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

### <span data-ttu-id="2d89e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d89e-124">-AsJob</span></span>
<span data-ttu-id="2d89e-125">Esegue il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="2d89e-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="2d89e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d89e-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="2d89e-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d89e-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="2d89e-128">Disabilitare la creazione di risorse di Insight per l'applicazione durante la creazione di App funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="2d89e-129">Nessun log sarà disponibile.</span><span class="sxs-lookup"><span data-stu-id="2d89e-129">No logs will be available.</span></span>

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

### <span data-ttu-id="2d89e-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="2d89e-130">-DockerImageName</span></span>
<span data-ttu-id="2d89e-131">Solo Linux.</span><span class="sxs-lookup"><span data-stu-id="2d89e-131">Linux only.</span></span>
<span data-ttu-id="2d89e-132">Nome immagine contenitore da registro di sistema mobile, ad esempio Publisher/nome immagine: Tag.</span><span class="sxs-lookup"><span data-stu-id="2d89e-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="2d89e-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="2d89e-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="2d89e-134">Nome utente e password del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="2d89e-134">The container registry user name and password.</span></span>
<span data-ttu-id="2d89e-135">Obbligatorio per i registri privati.</span><span class="sxs-lookup"><span data-stu-id="2d89e-135">Required for private registries.</span></span>

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

### <span data-ttu-id="2d89e-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="2d89e-136">-FunctionsVersion</span></span>
<span data-ttu-id="2d89e-137">La versione delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="2d89e-137">The Functions version.</span></span>

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

### <span data-ttu-id="2d89e-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="2d89e-138">-IdentityID</span></span>
<span data-ttu-id="2d89e-139">Specifica l'elenco delle identità utente associate all'app funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="2d89e-140">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="2d89e-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2d89e-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2d89e-141">-IdentityType</span></span>
<span data-ttu-id="2d89e-142">Specifica il tipo di identità usata per l'app funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="2d89e-143">I valori accettabili per questo parametro sono:-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="2d89e-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="2d89e-144">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2d89e-144">-Location</span></span>
<span data-ttu-id="2d89e-145">Posizione per il piano di consumo.</span><span class="sxs-lookup"><span data-stu-id="2d89e-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="2d89e-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d89e-146">-Name</span></span>
<span data-ttu-id="2d89e-147">Nome dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-147">The name of the function app.</span></span>

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

### <span data-ttu-id="2d89e-148">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2d89e-148">-NoWait</span></span>
<span data-ttu-id="2d89e-149">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="2d89e-150">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="2d89e-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2d89e-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="2d89e-151">-OSType</span></span>
<span data-ttu-id="2d89e-152">Il sistema operativo per ospitare l'app funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="2d89e-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d89e-153">-PassThru</span></span>
<span data-ttu-id="2d89e-154">Restituisce vero quando il comando riesce.</span><span class="sxs-lookup"><span data-stu-id="2d89e-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="2d89e-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2d89e-155">-PlanName</span></span>
<span data-ttu-id="2d89e-156">Nome del piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="2d89e-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="2d89e-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d89e-157">-ResourceGroupName</span></span>
<span data-ttu-id="2d89e-158">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2d89e-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d89e-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="2d89e-159">-Runtime</span></span>
<span data-ttu-id="2d89e-160">Runtime della funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-160">The function runtime.</span></span>

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

### <span data-ttu-id="2d89e-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="2d89e-161">-RuntimeVersion</span></span>
<span data-ttu-id="2d89e-162">Runtime della funzione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-162">The function runtime.</span></span>

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

### <span data-ttu-id="2d89e-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2d89e-163">-StorageAccountName</span></span>
<span data-ttu-id="2d89e-164">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2d89e-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="2d89e-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d89e-165">-SubscriptionId</span></span>
<span data-ttu-id="2d89e-166">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d89e-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="2d89e-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d89e-167">-Tag</span></span>
<span data-ttu-id="2d89e-168">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2d89e-168">Resource tags.</span></span>

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

### <span data-ttu-id="2d89e-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d89e-169">-Confirm</span></span>
<span data-ttu-id="2d89e-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d89e-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d89e-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d89e-171">-WhatIf</span></span>
<span data-ttu-id="2d89e-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d89e-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d89e-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d89e-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d89e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d89e-174">CommonParameters</span></span>
<span data-ttu-id="2d89e-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d89e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d89e-176">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d89e-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d89e-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d89e-177">INPUTS</span></span>

## <span data-ttu-id="2d89e-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d89e-178">OUTPUTS</span></span>

### <span data-ttu-id="2d89e-179">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="2d89e-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="2d89e-180">Note</span><span class="sxs-lookup"><span data-stu-id="2d89e-180">NOTES</span></span>

<span data-ttu-id="2d89e-181">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2d89e-181">ALIASES</span></span>

## <span data-ttu-id="2d89e-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d89e-182">RELATED LINKS</span></span>

