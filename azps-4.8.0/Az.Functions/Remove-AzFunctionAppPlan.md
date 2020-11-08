---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192900"
---
# <span data-ttu-id="d43c4-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="d43c4-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="d43c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d43c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d43c4-103">Elimina un piano dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="d43c4-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="d43c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d43c4-104">SYNTAX</span></span>

### <span data-ttu-id="d43c4-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d43c4-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d43c4-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="d43c4-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d43c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d43c4-107">DESCRIPTION</span></span>
<span data-ttu-id="d43c4-108">Elimina un piano dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="d43c4-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="d43c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d43c4-109">EXAMPLES</span></span>

### <span data-ttu-id="d43c4-110">Esempio 1: ottenere un piano per l'app di funzioni per nome ed eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="d43c4-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="d43c4-111">Questo comando consente di ottenere un piano per l'app di funzioni per nome ed eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="d43c4-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="d43c4-112">Esempio 2: eliminare un piano dell'app funzione per nome.</span><span class="sxs-lookup"><span data-stu-id="d43c4-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="d43c4-113">Questo comando Elimina un piano per nome dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="d43c4-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="d43c4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d43c4-114">PARAMETERS</span></span>

### <span data-ttu-id="d43c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43c4-115">-DefaultProfile</span></span>
<span data-ttu-id="d43c4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d43c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d43c4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d43c4-117">-Force</span></span>
<span data-ttu-id="d43c4-118">Impone al cmdlet di rimuovere il piano dell'app funzione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d43c4-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d43c4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d43c4-119">-InputObject</span></span>
<span data-ttu-id="d43c4-120">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d43c4-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d43c4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d43c4-121">-Name</span></span>
<span data-ttu-id="d43c4-122">Nome dell'app funzione.</span><span class="sxs-lookup"><span data-stu-id="d43c4-122">The name of function app.</span></span>

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

### <span data-ttu-id="d43c4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d43c4-123">-PassThru</span></span>
<span data-ttu-id="d43c4-124">Restituisce vero quando il comando riesce.</span><span class="sxs-lookup"><span data-stu-id="d43c4-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="d43c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43c4-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="d43c4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d43c4-126">-SubscriptionId</span></span>
<span data-ttu-id="d43c4-127">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="d43c4-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d43c4-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d43c4-128">-Confirm</span></span>
<span data-ttu-id="d43c4-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d43c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43c4-130">-WhatIf</span></span>
<span data-ttu-id="d43c4-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d43c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d43c4-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d43c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43c4-133">CommonParameters</span></span>
<span data-ttu-id="d43c4-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43c4-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d43c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43c4-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d43c4-136">INPUTS</span></span>

### <span data-ttu-id="d43c4-137">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d43c4-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d43c4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d43c4-138">OUTPUTS</span></span>

### <span data-ttu-id="d43c4-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d43c4-139">System.Boolean</span></span>

## <span data-ttu-id="d43c4-140">Note</span><span class="sxs-lookup"><span data-stu-id="d43c4-140">NOTES</span></span>

<span data-ttu-id="d43c4-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d43c4-141">ALIASES</span></span>

<span data-ttu-id="d43c4-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d43c4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d43c4-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d43c4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d43c4-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d43c4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d43c4-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="d43c4-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="d43c4-146">`Location <String>`: Percorso delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d43c4-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="d43c4-147">`[Kind <String>]`: Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d43c4-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="d43c4-148">`[Tag <IResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d43c4-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d43c4-149">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d43c4-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d43c4-150">`[Capacity <Int32?>]`: Numero corrente di istanze assegnate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="d43c4-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="d43c4-151">`[FreeOfferExpirationTime <DateTime?>]`: Il momento in cui l'offerta gratuita della server farm scade.</span><span class="sxs-lookup"><span data-stu-id="d43c4-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="d43c4-152">`[HostingEnvironmentProfileId <String>]`: ID risorsa dell'ambiente di servizio app.</span><span class="sxs-lookup"><span data-stu-id="d43c4-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="d43c4-153">`[HyperV <Boolean?>]`: Se il piano di servizio app contenitore Hyper-V <code>true</code> , <code>false</code> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d43c4-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d43c4-154">`[IsSpot <Boolean?>]`: Se <code>true</code> , questo piano di servizio app possiede istanze di spot.</span><span class="sxs-lookup"><span data-stu-id="d43c4-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="d43c4-155">`[IsXenon <Boolean?>]`: Obsolete: se piano di servizio app contenitore Hyper-V <code>true</code> , <code>false</code> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d43c4-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d43c4-156">`[MaximumElasticWorkerCount <Int32?>]`: Numero massimo di lavoratori totali consentiti per il piano di servizio app ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="d43c4-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="d43c4-157">`[PerSiteScaling <Boolean?>]`: Se le <code>true</code> app assegnate a questo piano di servizio app possono essere ridimensionate in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="d43c4-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="d43c4-158">Se <code>false</code> , le app assegnate al piano del servizio app verranno ridimensionate in tutte le istanze del piano.</span><span class="sxs-lookup"><span data-stu-id="d43c4-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="d43c4-159">`[Reserved <Boolean?>]`: Se piano di servizio app Linux <code>true</code> , <code>false</code> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d43c4-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="d43c4-160">`[SkuCapability <ICapability[]>]`: Le funzionalità dell'USK, ad esempio, sono abilitate per Traffic Manager?</span><span class="sxs-lookup"><span data-stu-id="d43c4-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="d43c4-161">`[Name <String>]`: Nome della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="d43c4-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="d43c4-162">`[Reason <String>]`: Motivo della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="d43c4-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="d43c4-163">`[Value <String>]`: Valore della funzionalità SKU.</span><span class="sxs-lookup"><span data-stu-id="d43c4-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="d43c4-164">`[SkuCapacityDefault <Int32?>]`: Numero predefinito di Worker per questo piano di servizio App SKU.</span><span class="sxs-lookup"><span data-stu-id="d43c4-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d43c4-165">`[SkuCapacityMaximum <Int32?>]`: Numero massimo di dipendenti per questo piano di servizio App SKU.</span><span class="sxs-lookup"><span data-stu-id="d43c4-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d43c4-166">`[SkuCapacityMinimum <Int32?>]`: Numero minimo di dipendenti per questo piano di servizio App SKU.</span><span class="sxs-lookup"><span data-stu-id="d43c4-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="d43c4-167">`[SkuCapacityScaleType <String>]`: Configurazioni di scala disponibili per un piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="d43c4-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="d43c4-168">`[SkuFamily <String>]`: Codice famiglia della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="d43c4-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="d43c4-169">`[SkuLocation <String[]>]`: Posizioni dell'USK.</span><span class="sxs-lookup"><span data-stu-id="d43c4-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="d43c4-170">`[SkuName <String>]`: Nome della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="d43c4-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="d43c4-171">`[SkuSize <String>]`: Specificatore di dimensioni della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="d43c4-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="d43c4-172">`[SkuTier <String>]`: Livello di servizio della SKU di risorse.</span><span class="sxs-lookup"><span data-stu-id="d43c4-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="d43c4-173">`[SpotExpirationTime <DateTime?>]`: L'ora in cui scade la server farm.</span><span class="sxs-lookup"><span data-stu-id="d43c4-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="d43c4-174">Valido solo se si tratta di una farm di server di punti.</span><span class="sxs-lookup"><span data-stu-id="d43c4-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="d43c4-175">`[TargetWorkerCount <Int32?>]`: Ridimensionamento del conteggio lavoratori.</span><span class="sxs-lookup"><span data-stu-id="d43c4-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="d43c4-176">`[TargetWorkerSizeId <Int32?>]`: Ridimensionamento ID dimensione lavoratore.</span><span class="sxs-lookup"><span data-stu-id="d43c4-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="d43c4-177">`[WorkerTierName <String>]`: Livello di lavoro di destinazione assegnato al piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="d43c4-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="d43c4-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d43c4-178">RELATED LINKS</span></span>

