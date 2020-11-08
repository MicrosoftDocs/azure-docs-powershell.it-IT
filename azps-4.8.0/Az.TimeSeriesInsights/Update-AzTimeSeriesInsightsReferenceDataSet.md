---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188674"
---
# <span data-ttu-id="8996c-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="8996c-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="8996c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8996c-102">SYNOPSIS</span></span>
<span data-ttu-id="8996c-103">Aggiorna il set di dati di riferimento con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="8996c-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="8996c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8996c-104">SYNTAX</span></span>

### <span data-ttu-id="8996c-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8996c-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8996c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8996c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8996c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8996c-107">DESCRIPTION</span></span>
<span data-ttu-id="8996c-108">Aggiorna il set di dati di riferimento con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="8996c-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="8996c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8996c-109">EXAMPLES</span></span>

### <span data-ttu-id="8996c-110">Esempio 1: aggiornare i dati di riferimento specificati impostati per nome</span><span class="sxs-lookup"><span data-stu-id="8996c-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8996c-111">Questo comando aggiorna un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="8996c-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="8996c-112">Esempio 2: aggiornare un set di dati di riferimento specificato da un oggetto</span><span class="sxs-lookup"><span data-stu-id="8996c-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8996c-113">Questo comando aggiorna un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="8996c-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="8996c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8996c-114">PARAMETERS</span></span>

### <span data-ttu-id="8996c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8996c-115">-DefaultProfile</span></span>
<span data-ttu-id="8996c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8996c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8996c-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="8996c-117">-EnvironmentName</span></span>
<span data-ttu-id="8996c-118">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8996c-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8996c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8996c-119">-InputObject</span></span>
<span data-ttu-id="8996c-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8996c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8996c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8996c-121">-Name</span></span>
<span data-ttu-id="8996c-122">Nome del set di dati di riferimento per gli approfondimenti della serie temporale associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="8996c-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8996c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8996c-123">-ResourceGroupName</span></span>
<span data-ttu-id="8996c-124">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="8996c-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8996c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8996c-125">-SubscriptionId</span></span>
<span data-ttu-id="8996c-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="8996c-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8996c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="8996c-127">-Tag</span></span>
<span data-ttu-id="8996c-128">Coppie chiave-valore di proprietà aggiuntive per il set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="8996c-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="8996c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8996c-129">-Confirm</span></span>
<span data-ttu-id="8996c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8996c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8996c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8996c-131">-WhatIf</span></span>
<span data-ttu-id="8996c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8996c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8996c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8996c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8996c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8996c-134">CommonParameters</span></span>
<span data-ttu-id="8996c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8996c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8996c-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8996c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8996c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8996c-137">INPUTS</span></span>

### <span data-ttu-id="8996c-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="8996c-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="8996c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8996c-139">OUTPUTS</span></span>

### <span data-ttu-id="8996c-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="8996c-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="8996c-141">Note</span><span class="sxs-lookup"><span data-stu-id="8996c-141">NOTES</span></span>

<span data-ttu-id="8996c-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8996c-142">ALIASES</span></span>

<span data-ttu-id="8996c-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8996c-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8996c-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8996c-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8996c-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8996c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8996c-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8996c-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8996c-147">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="8996c-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="8996c-148">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="8996c-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="8996c-149">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="8996c-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="8996c-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8996c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8996c-151">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="8996c-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="8996c-152">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="8996c-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="8996c-153">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="8996c-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8996c-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8996c-154">RELATED LINKS</span></span>

