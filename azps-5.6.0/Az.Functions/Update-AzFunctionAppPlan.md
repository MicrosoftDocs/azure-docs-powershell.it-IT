---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963038"
---
# <span data-ttu-id="9c04e-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="9c04e-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="9c04e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c04e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c04e-103">Aggiorna un piano di servizio app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9c04e-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="9c04e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c04e-104">SYNTAX</span></span>

### <span data-ttu-id="9c04e-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c04e-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c04e-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="9c04e-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c04e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c04e-107">DESCRIPTION</span></span>
<span data-ttu-id="9c04e-108">Aggiorna un piano di servizio app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="9c04e-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="9c04e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c04e-109">EXAMPLES</span></span>

### <span data-ttu-id="9c04e-110">Esempio 1: Aggiornare un piano di servizio app alla SKU EP2 con venti massime lavorate.</span><span class="sxs-lookup"><span data-stu-id="9c04e-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="9c04e-111">Questo comando aggiorna un piano di servizio app alle SKU EP2 con venti utenti massimi.</span><span class="sxs-lookup"><span data-stu-id="9c04e-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="9c04e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c04e-112">PARAMETERS</span></span>

### <span data-ttu-id="9c04e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c04e-113">-AsJob</span></span>
<span data-ttu-id="9c04e-114">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="9c04e-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="9c04e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c04e-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="9c04e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c04e-116">-InputObject</span></span>
<span data-ttu-id="9c04e-117">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9c04e-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="9c04e-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="9c04e-119">Il numero massimo di persone per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="9c04e-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="9c04e-121">Il numero minimo di persone per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9c04e-122">-Name</span></span>
<span data-ttu-id="9c04e-123">Nome del piano di servizio dell'app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9c04e-124">-NoWait</span></span>
<span data-ttu-id="9c04e-125">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="9c04e-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="9c04e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c04e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c04e-127">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="9c04e-128">-Sku</span></span>
<span data-ttu-id="9c04e-129">SKU del piano.</span><span class="sxs-lookup"><span data-stu-id="9c04e-129">The plan sku.</span></span>
<span data-ttu-id="9c04e-130">Gli input validi sono: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="9c04e-130">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c04e-131">-SubscriptionId</span></span>
<span data-ttu-id="9c04e-132">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c04e-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c04e-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c04e-133">-Tag</span></span>
<span data-ttu-id="9c04e-134">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c04e-134">Resource tags.</span></span>

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

### <span data-ttu-id="9c04e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c04e-135">-Confirm</span></span>
<span data-ttu-id="9c04e-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c04e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c04e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c04e-137">-WhatIf</span></span>
<span data-ttu-id="9c04e-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c04e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c04e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c04e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c04e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c04e-140">CommonParameters</span></span>
<span data-ttu-id="9c04e-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c04e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c04e-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c04e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c04e-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c04e-143">INPUTS</span></span>

### <span data-ttu-id="9c04e-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9c04e-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="9c04e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c04e-145">OUTPUTS</span></span>

### <span data-ttu-id="9c04e-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9c04e-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="9c04e-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c04e-147">NOTES</span></span>

<span data-ttu-id="9c04e-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c04e-148">ALIASES</span></span>

<span data-ttu-id="9c04e-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9c04e-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c04e-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9c04e-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c04e-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c04e-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c04e-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="9c04e-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="9c04e-153">`Location <String>`: Posizione risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="9c04e-154">`[Kind <String>]`: tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="9c04e-155">`[Tag <IResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="9c04e-156">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c04e-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9c04e-157">`[Capacity <Int32?>]`: numero corrente di istanze assegnate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="9c04e-158">`[FreeOfferExpirationTime <DateTime?>]`: il tempo in cui scade l'offerta gratuita della server farm.</span><span class="sxs-lookup"><span data-stu-id="9c04e-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="9c04e-159">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="9c04e-160">`[HyperV <Boolean?>]`: se il piano di servizio app contenitore Hyper-V, <code>true</code> in <code>false</code> caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c04e-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="9c04e-161">`[IsSpot <Boolean?>]`: se <code>true</code> , questo piano di servizio dell'app è proprietario di istanze spot.</span><span class="sxs-lookup"><span data-stu-id="9c04e-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="9c04e-162">`[IsXenon <Boolean?>]`: Obsoleta: se il piano di servizio delle app contenitore Hyper-V, <code>true</code> in <code>false</code> caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c04e-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="9c04e-163">`[MaximumElasticWorkerCount <Int32?>]`: numero massimo di persone totali consentite per questo piano di servizio app ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="9c04e-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="9c04e-164">`[PerSiteScaling <Boolean?>]`: se <code>true</code> , le app assegnate a questo piano di servizio app possono essere ridimensionate in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="9c04e-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="9c04e-165">Se <code>false</code> , le app assegnate a questo piano di servizio app verranno ridimensionate in base a tutte le istanze del piano.</span><span class="sxs-lookup"><span data-stu-id="9c04e-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="9c04e-166">`[Reserved <Boolean?>]`: se il piano di servizio dell'app <code>true</code> Linux, in <code>false</code> caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c04e-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="9c04e-167">`[SkuCapability <ICapability[]>]`: Le funzionalità dello SKU, ad esempio, sono abilitate da Gestione traffico?</span><span class="sxs-lookup"><span data-stu-id="9c04e-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="9c04e-168">`[Name <String>]`: nome della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="9c04e-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="9c04e-169">`[Reason <String>]`: motivo della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="9c04e-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="9c04e-170">`[Value <String>]`: valore della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="9c04e-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="9c04e-171">`[SkuCapacityDefault <Int32?>]`: numero predefinito di dipendenti per questo SKU del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="9c04e-172">`[SkuCapacityMaximum <Int32?>]`: numero massimo di persone per questo SKU del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="9c04e-173">`[SkuCapacityMinimum <Int32?>]`: numero minimo di dipendenti per questo SKU del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="9c04e-174">`[SkuCapacityScaleType <String>]`: configurazioni di scala disponibili per un piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="9c04e-175">`[SkuFamily <String>]`: codice famiglia dello SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="9c04e-176">`[SkuLocation <String[]>]`: posizione dello SKU.</span><span class="sxs-lookup"><span data-stu-id="9c04e-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="9c04e-177">`[SkuName <String>]`: nome della SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="9c04e-178">`[SkuSize <String>]`: specificatore di dimensioni dello SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="9c04e-179">`[SkuTier <String>]`: livello di servizio della SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c04e-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="9c04e-180">`[SpotExpirationTime <DateTime?>]`: ora di scadenza della server farm.</span><span class="sxs-lookup"><span data-stu-id="9c04e-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="9c04e-181">Valido solo se si tratta di una server farm spot.</span><span class="sxs-lookup"><span data-stu-id="9c04e-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="9c04e-182">`[TargetWorkerCount <Int32?>]`: per ridimensionare il numero di lavoratori.</span><span class="sxs-lookup"><span data-stu-id="9c04e-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="9c04e-183">`[TargetWorkerSizeId <Int32?>]`: per ridimensionare l'ID delle dimensioni dei lavoratori.</span><span class="sxs-lookup"><span data-stu-id="9c04e-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="9c04e-184">`[WorkerTierName <String>]`: livello di utente di destinazione assegnato al piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="9c04e-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="9c04e-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c04e-185">RELATED LINKS</span></span>

