---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994235"
---
# <span data-ttu-id="82c50-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="82c50-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="82c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c50-102">SYNOPSIS</span></span>
<span data-ttu-id="82c50-103">Elimina un piano dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="82c50-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="82c50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82c50-104">SYNTAX</span></span>

### <span data-ttu-id="82c50-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82c50-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="82c50-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="82c50-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82c50-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82c50-107">DESCRIPTION</span></span>
<span data-ttu-id="82c50-108">Elimina un piano dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="82c50-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="82c50-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82c50-109">EXAMPLES</span></span>

### <span data-ttu-id="82c50-110">Esempio 1: Ottenere un piano dell'app per le funzioni in base al nome ed eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="82c50-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="82c50-111">Questo comando recupera un piano dell'app per le funzioni in base al nome ed lo elimina.</span><span class="sxs-lookup"><span data-stu-id="82c50-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="82c50-112">Esempio 2: Eliminare il piano di un'app per le funzioni in base al nome.</span><span class="sxs-lookup"><span data-stu-id="82c50-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="82c50-113">Questo comando elimina il piano di un'app per le funzioni in base al nome.</span><span class="sxs-lookup"><span data-stu-id="82c50-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="82c50-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c50-114">PARAMETERS</span></span>

### <span data-ttu-id="82c50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c50-115">-DefaultProfile</span></span>
<span data-ttu-id="82c50-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82c50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c50-117">-Force</span><span class="sxs-lookup"><span data-stu-id="82c50-117">-Force</span></span>
<span data-ttu-id="82c50-118">Forza il cmdlet a rimuovere il piano dell'app per le funzioni senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="82c50-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="82c50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82c50-119">-InputObject</span></span>
<span data-ttu-id="82c50-120">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="82c50-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="82c50-121">-Name</span><span class="sxs-lookup"><span data-stu-id="82c50-121">-Name</span></span>
<span data-ttu-id="82c50-122">Nome dell'app per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="82c50-122">The name of function app.</span></span>

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

### <span data-ttu-id="82c50-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82c50-123">-PassThru</span></span>
<span data-ttu-id="82c50-124">Restituisce true quando il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="82c50-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="82c50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c50-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="82c50-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82c50-126">-SubscriptionId</span></span>
<span data-ttu-id="82c50-127">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="82c50-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="82c50-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82c50-128">-Confirm</span></span>
<span data-ttu-id="82c50-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82c50-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82c50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c50-130">-WhatIf</span></span>
<span data-ttu-id="82c50-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82c50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c50-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82c50-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82c50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c50-133">CommonParameters</span></span>
<span data-ttu-id="82c50-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c50-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82c50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c50-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="82c50-136">INPUTS</span></span>

### <span data-ttu-id="82c50-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="82c50-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="82c50-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82c50-138">OUTPUTS</span></span>

### <span data-ttu-id="82c50-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82c50-139">System.Boolean</span></span>

## <span data-ttu-id="82c50-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="82c50-140">NOTES</span></span>

<span data-ttu-id="82c50-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="82c50-141">ALIASES</span></span>

<span data-ttu-id="82c50-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="82c50-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82c50-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="82c50-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82c50-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82c50-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82c50-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="82c50-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="82c50-146">`Location <String>`: Posizione risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="82c50-147">`[Kind <String>]`: tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="82c50-148">`[Tag <IResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="82c50-149">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="82c50-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82c50-150">`[Capacity <Int32?>]`: numero corrente di istanze assegnate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="82c50-151">`[FreeOfferExpirationTime <DateTime?>]`: il tempo in cui scade l'offerta gratuita della server farm.</span><span class="sxs-lookup"><span data-stu-id="82c50-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="82c50-152">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="82c50-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="82c50-153">`[HyperV <Boolean?>]`: se il piano di servizio app contenitore Hyper-V, <code>true</code> in <code>false</code> caso contrario.</span><span class="sxs-lookup"><span data-stu-id="82c50-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="82c50-154">`[IsSpot <Boolean?>]`: se <code>true</code> , questo piano di servizio dell'app è proprietario di istanze spot.</span><span class="sxs-lookup"><span data-stu-id="82c50-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="82c50-155">`[IsXenon <Boolean?>]`: Obsoleta: se il piano di servizio delle app contenitore Hyper-V, <code>true</code> in <code>false</code> caso contrario.</span><span class="sxs-lookup"><span data-stu-id="82c50-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="82c50-156">`[MaximumElasticWorkerCount <Int32?>]`: numero massimo di persone totali consentite per questo piano di servizio app ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="82c50-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="82c50-157">`[PerSiteScaling <Boolean?>]`: se <code>true</code> , le app assegnate a questo piano di servizio app possono essere ridimensionate in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="82c50-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="82c50-158">Se <code>false</code> , le app assegnate a questo piano di servizio app verranno ridimensionate in base a tutte le istanze del piano.</span><span class="sxs-lookup"><span data-stu-id="82c50-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="82c50-159">`[Reserved <Boolean?>]`: se il piano di servizio dell'app <code>true</code> Linux, in <code>false</code> caso contrario.</span><span class="sxs-lookup"><span data-stu-id="82c50-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="82c50-160">`[SkuCapability <ICapability[]>]`: Le funzionalità dello SKU, ad esempio, sono abilitate da Gestione traffico?</span><span class="sxs-lookup"><span data-stu-id="82c50-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="82c50-161">`[Name <String>]`: nome della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="82c50-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="82c50-162">`[Reason <String>]`: motivo della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="82c50-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="82c50-163">`[Value <String>]`: valore della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="82c50-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="82c50-164">`[SkuCapacityDefault <Int32?>]`: numero predefinito di dipendenti per questo SKU del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="82c50-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="82c50-165">`[SkuCapacityMaximum <Int32?>]`: numero massimo di persone per questo SKU del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="82c50-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="82c50-166">`[SkuCapacityMinimum <Int32?>]`: numero minimo di dipendenti per questo SKU del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="82c50-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="82c50-167">`[SkuCapacityScaleType <String>]`: configurazioni di scala disponibili per un piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="82c50-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="82c50-168">`[SkuFamily <String>]`: codice famiglia dello SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="82c50-169">`[SkuLocation <String[]>]`: posizione dello SKU.</span><span class="sxs-lookup"><span data-stu-id="82c50-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="82c50-170">`[SkuName <String>]`: nome della SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="82c50-171">`[SkuSize <String>]`: specificatore di dimensione dello SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="82c50-172">`[SkuTier <String>]`: livello di servizio della SKU della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82c50-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="82c50-173">`[SpotExpirationTime <DateTime?>]`: ora di scadenza della server farm.</span><span class="sxs-lookup"><span data-stu-id="82c50-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="82c50-174">Valido solo se si tratta di una server farm spot.</span><span class="sxs-lookup"><span data-stu-id="82c50-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="82c50-175">`[TargetWorkerCount <Int32?>]`: per ridimensionare il numero di lavoratori.</span><span class="sxs-lookup"><span data-stu-id="82c50-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="82c50-176">`[TargetWorkerSizeId <Int32?>]`: per ridimensionare l'ID delle dimensioni dei lavoratori.</span><span class="sxs-lookup"><span data-stu-id="82c50-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="82c50-177">`[WorkerTierName <String>]`: livello di utente di destinazione assegnato al piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="82c50-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="82c50-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82c50-178">RELATED LINKS</span></span>

