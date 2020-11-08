---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031729"
---
# <span data-ttu-id="8bad6-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="8bad6-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="8bad6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bad6-102">SYNOPSIS</span></span>
<span data-ttu-id="8bad6-103">Aggiorna un piano di servizio App funzione.</span><span class="sxs-lookup"><span data-stu-id="8bad6-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="8bad6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bad6-104">SYNTAX</span></span>

### <span data-ttu-id="8bad6-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8bad6-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8bad6-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="8bad6-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8bad6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bad6-107">DESCRIPTION</span></span>
<span data-ttu-id="8bad6-108">Aggiorna un piano di servizio App funzione.</span><span class="sxs-lookup"><span data-stu-id="8bad6-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="8bad6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bad6-109">EXAMPLES</span></span>

### <span data-ttu-id="8bad6-110">Esempio 1: aggiornare un piano di servizio app alla SKU EP2 con venti dipendenti massimi.</span><span class="sxs-lookup"><span data-stu-id="8bad6-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="8bad6-111">Questo comando aggiorna un piano di servizio app per EP2 SKU con venti dipendenti massimi.</span><span class="sxs-lookup"><span data-stu-id="8bad6-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="8bad6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bad6-112">PARAMETERS</span></span>

### <span data-ttu-id="8bad6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bad6-113">-AsJob</span></span>
<span data-ttu-id="8bad6-114">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="8bad6-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="8bad6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bad6-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="8bad6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bad6-116">-InputObject</span></span>
<span data-ttu-id="8bad6-117">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8bad6-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bad6-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="8bad6-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="8bad6-119">Numero massimo di dipendenti per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="8bad6-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="8bad6-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="8bad6-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="8bad6-121">Il numero minimo di lavoratori per il piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="8bad6-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="8bad6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bad6-122">-Name</span></span>
<span data-ttu-id="8bad6-123">Nome del piano del servizio app.</span><span class="sxs-lookup"><span data-stu-id="8bad6-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="8bad6-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="8bad6-124">-NoWait</span></span>
<span data-ttu-id="8bad6-125">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="8bad6-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8bad6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bad6-126">-ResourceGroupName</span></span>
<span data-ttu-id="8bad6-127">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8bad6-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="8bad6-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="8bad6-128">-Sku</span></span>
<span data-ttu-id="8bad6-129">SKU piano.</span><span class="sxs-lookup"><span data-stu-id="8bad6-129">The plan sku.</span></span>
<span data-ttu-id="8bad6-130">Gli input validi sono: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="8bad6-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="8bad6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bad6-131">-SubscriptionId</span></span>
<span data-ttu-id="8bad6-132">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="8bad6-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="8bad6-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="8bad6-133">-Tag</span></span>
<span data-ttu-id="8bad6-134">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-134">Resource tags.</span></span>

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

### <span data-ttu-id="8bad6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bad6-135">-Confirm</span></span>
<span data-ttu-id="8bad6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bad6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bad6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bad6-137">-WhatIf</span></span>
<span data-ttu-id="8bad6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bad6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bad6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bad6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bad6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bad6-140">CommonParameters</span></span>
<span data-ttu-id="8bad6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bad6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bad6-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bad6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bad6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bad6-143">INPUTS</span></span>

### <span data-ttu-id="8bad6-144">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8bad6-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="8bad6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bad6-145">OUTPUTS</span></span>

### <span data-ttu-id="8bad6-146">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8bad6-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="8bad6-147">Note</span><span class="sxs-lookup"><span data-stu-id="8bad6-147">NOTES</span></span>

<span data-ttu-id="8bad6-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8bad6-148">ALIASES</span></span>

<span data-ttu-id="8bad6-149">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bad6-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8bad6-150">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8bad6-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bad6-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8bad6-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8bad6-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="8bad6-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="8bad6-153">`Location <String>`: Percorso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="8bad6-154">`[Kind <String>]`: Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="8bad6-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="8bad6-155">`[Tag <IResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8bad6-156">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8bad6-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8bad6-157">`[Capacity <Int32?>]`: Numero corrente di istanze assegnate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="8bad6-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="8bad6-158">`[FreeOfferExpirationTime <DateTime?>]`: Il momento in cui l'offerta gratuita della server farm scade.</span><span class="sxs-lookup"><span data-stu-id="8bad6-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="8bad6-159">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente di servizio app.</span><span class="sxs-lookup"><span data-stu-id="8bad6-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="8bad6-160">`[HyperV <Boolean?>]`: Se il piano di servizio app contenitore Hyper-V <code>true</code> , <code>false</code> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8bad6-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="8bad6-161">`[IsSpot <Boolean?>]`: Se <code>true</code> , questo piano di servizio app possiede istanze di spot.</span><span class="sxs-lookup"><span data-stu-id="8bad6-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="8bad6-162">`[IsXenon <Boolean?>]`: Obsolete: se piano di servizio app contenitore Hyper-V <code>true</code> , <code>false</code> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8bad6-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="8bad6-163">`[MaximumElasticWorkerCount <Int32?>]`: Numero massimo di lavoratori totali consentiti per il piano di servizio app ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="8bad6-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="8bad6-164">`[PerSiteScaling <Boolean?>]`: Se le <code>true</code> app assegnate a questo piano di servizio app possono essere ridimensionate in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="8bad6-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="8bad6-165">Se <code>false</code> , le app assegnate al piano del servizio app verranno ridimensionate in tutte le istanze del piano.</span><span class="sxs-lookup"><span data-stu-id="8bad6-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="8bad6-166">`[Reserved <Boolean?>]`: Se piano di servizio app Linux <code>true</code> , <code>false</code> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8bad6-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="8bad6-167">`[SkuCapability <ICapability[]>]`: Le funzionalità dell'USK, ad esempio, sono abilitate per Traffic Manager?</span><span class="sxs-lookup"><span data-stu-id="8bad6-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="8bad6-168">`[Name <String>]`: Nome della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="8bad6-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="8bad6-169">`[Reason <String>]`: Motivo della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="8bad6-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="8bad6-170">`[Value <String>]`: Valore della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="8bad6-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="8bad6-171">`[SkuCapacityDefault <Int32?>]`: Numero predefinito di Worker per questo piano di servizio App SKU.</span><span class="sxs-lookup"><span data-stu-id="8bad6-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="8bad6-172">`[SkuCapacityMaximum <Int32?>]`: Numero massimo di dipendenti per questo piano di servizio App SKU.</span><span class="sxs-lookup"><span data-stu-id="8bad6-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="8bad6-173">`[SkuCapacityMinimum <Int32?>]`: Numero minimo di dipendenti per questo piano di servizio App SKU.</span><span class="sxs-lookup"><span data-stu-id="8bad6-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="8bad6-174">`[SkuCapacityScaleType <String>]`: Configurazioni di scala disponibili per un piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="8bad6-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="8bad6-175">`[SkuFamily <String>]`: Codice famiglia della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="8bad6-176">`[SkuLocation <String[]>]`: Posizioni dell'USK.</span><span class="sxs-lookup"><span data-stu-id="8bad6-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="8bad6-177">`[SkuName <String>]`: Nome della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="8bad6-178">`[SkuSize <String>]`: Specificatore di dimensioni della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="8bad6-179">`[SkuTier <String>]`: Livello di servizio della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bad6-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="8bad6-180">`[SpotExpirationTime <DateTime?>]`: L'ora in cui scade la server farm.</span><span class="sxs-lookup"><span data-stu-id="8bad6-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="8bad6-181">Valido solo se si tratta di una farm di server di punti.</span><span class="sxs-lookup"><span data-stu-id="8bad6-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="8bad6-182">`[TargetWorkerCount <Int32?>]`: Ridimensionamento del conteggio lavoratori.</span><span class="sxs-lookup"><span data-stu-id="8bad6-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="8bad6-183">`[TargetWorkerSizeId <Int32?>]`: Ridimensionamento ID dimensione lavoratore.</span><span class="sxs-lookup"><span data-stu-id="8bad6-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="8bad6-184">`[WorkerTierName <String>]`: Livello di lavoro di destinazione assegnato al piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="8bad6-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="8bad6-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bad6-185">RELATED LINKS</span></span>

