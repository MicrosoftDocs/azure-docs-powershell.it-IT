---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182598"
---
# <span data-ttu-id="64326-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="64326-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="64326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64326-102">SYNOPSIS</span></span>
<span data-ttu-id="64326-103">Elimina l'origine evento con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="64326-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="64326-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64326-104">SYNTAX</span></span>

### <span data-ttu-id="64326-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64326-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64326-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64326-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64326-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64326-107">DESCRIPTION</span></span>
<span data-ttu-id="64326-108">Elimina l'origine evento con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="64326-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="64326-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64326-109">EXAMPLES</span></span>

### <span data-ttu-id="64326-110">Esempio 1: Rimuovere un'origine evento specificata in base al nome</span><span class="sxs-lookup"><span data-stu-id="64326-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="64326-111">In questo modo viene rimossa un'origine evento specifica.</span><span class="sxs-lookup"><span data-stu-id="64326-111">This removes a specific event source.</span></span>

### <span data-ttu-id="64326-112">Esempio 2: Rimuovere un'origine evento specificata in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="64326-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="64326-113">In questo modo viene rimossa un'origine evento specifica.</span><span class="sxs-lookup"><span data-stu-id="64326-113">This removes a specific event source.</span></span>

## <span data-ttu-id="64326-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64326-114">PARAMETERS</span></span>

### <span data-ttu-id="64326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64326-115">-DefaultProfile</span></span>
<span data-ttu-id="64326-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64326-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64326-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="64326-117">-EnvironmentName</span></span>
<span data-ttu-id="64326-118">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="64326-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64326-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64326-119">-InputObject</span></span>
<span data-ttu-id="64326-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64326-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64326-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64326-121">-Name</span></span>
<span data-ttu-id="64326-122">Nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="64326-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64326-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64326-123">-PassThru</span></span>
<span data-ttu-id="64326-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="64326-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64326-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64326-125">-ResourceGroupName</span></span>
<span data-ttu-id="64326-126">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="64326-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64326-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64326-127">-SubscriptionId</span></span>
<span data-ttu-id="64326-128">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="64326-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64326-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64326-129">-Confirm</span></span>
<span data-ttu-id="64326-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64326-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64326-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64326-131">-WhatIf</span></span>
<span data-ttu-id="64326-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64326-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64326-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64326-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64326-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64326-134">CommonParameters</span></span>
<span data-ttu-id="64326-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64326-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64326-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64326-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64326-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="64326-137">INPUTS</span></span>

### <span data-ttu-id="64326-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="64326-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="64326-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64326-139">OUTPUTS</span></span>

### <span data-ttu-id="64326-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64326-140">System.Boolean</span></span>

## <span data-ttu-id="64326-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="64326-141">NOTES</span></span>

<span data-ttu-id="64326-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="64326-142">ALIASES</span></span>

<span data-ttu-id="64326-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="64326-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64326-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="64326-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64326-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64326-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64326-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="64326-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64326-147">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="64326-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="64326-148">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="64326-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="64326-149">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="64326-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="64326-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="64326-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64326-151">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="64326-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="64326-152">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="64326-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="64326-153">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="64326-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="64326-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64326-154">RELATED LINKS</span></span>

