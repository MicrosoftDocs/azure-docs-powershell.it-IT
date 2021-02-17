---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207547"
---
# <span data-ttu-id="a3744-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a3744-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a3744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3744-102">SYNOPSIS</span></span>
<span data-ttu-id="a3744-103">Aggiorna il set di dati di riferimento con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="a3744-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a3744-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3744-104">SYNTAX</span></span>

### <span data-ttu-id="a3744-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3744-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3744-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a3744-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3744-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3744-107">DESCRIPTION</span></span>
<span data-ttu-id="a3744-108">Aggiorna il set di dati di riferimento con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="a3744-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a3744-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3744-109">EXAMPLES</span></span>

### <span data-ttu-id="a3744-110">Esempio 1: Aggiornare un set di dati di riferimento specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="a3744-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a3744-111">Questo comando aggiorna un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="a3744-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="a3744-112">Esempio 2: Aggiornare un set di dati di riferimento specificato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="a3744-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a3744-113">Questo comando aggiorna un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="a3744-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="a3744-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3744-114">PARAMETERS</span></span>

### <span data-ttu-id="a3744-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3744-115">-DefaultProfile</span></span>
<span data-ttu-id="a3744-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3744-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3744-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a3744-117">-EnvironmentName</span></span>
<span data-ttu-id="a3744-118">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a3744-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a3744-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3744-119">-InputObject</span></span>
<span data-ttu-id="a3744-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a3744-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3744-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3744-121">-Name</span></span>
<span data-ttu-id="a3744-122">Nome del set di dati di riferimento Approfondimenti serie temporale associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a3744-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="a3744-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3744-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3744-124">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3744-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a3744-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3744-125">-SubscriptionId</span></span>
<span data-ttu-id="a3744-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="a3744-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a3744-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3744-127">-Tag</span></span>
<span data-ttu-id="a3744-128">Coppie chiave-valore di proprietà aggiuntive per il set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a3744-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="a3744-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3744-129">-Confirm</span></span>
<span data-ttu-id="a3744-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3744-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3744-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3744-131">-WhatIf</span></span>
<span data-ttu-id="a3744-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3744-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3744-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3744-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3744-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3744-134">CommonParameters</span></span>
<span data-ttu-id="a3744-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3744-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3744-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3744-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3744-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3744-137">INPUTS</span></span>

### <span data-ttu-id="a3744-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a3744-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a3744-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3744-139">OUTPUTS</span></span>

### <span data-ttu-id="a3744-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="a3744-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="a3744-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3744-141">NOTES</span></span>

<span data-ttu-id="a3744-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a3744-142">ALIASES</span></span>

<span data-ttu-id="a3744-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a3744-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3744-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a3744-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3744-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3744-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3744-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="a3744-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3744-147">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="a3744-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a3744-148">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="a3744-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a3744-149">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a3744-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a3744-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a3744-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3744-151">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a3744-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a3744-152">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3744-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a3744-153">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3744-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a3744-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3744-154">RELATED LINKS</span></span>

