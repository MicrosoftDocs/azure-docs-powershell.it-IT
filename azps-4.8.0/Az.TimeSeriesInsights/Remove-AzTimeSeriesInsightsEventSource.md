---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94030917"
---
# <span data-ttu-id="1c9bf-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="1c9bf-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="1c9bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9bf-103">Elimina l'origine eventi con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="1c9bf-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="1c9bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c9bf-104">SYNTAX</span></span>

### <span data-ttu-id="1c9bf-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c9bf-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c9bf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c9bf-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c9bf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c9bf-107">DESCRIPTION</span></span>
<span data-ttu-id="1c9bf-108">Elimina l'origine eventi con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="1c9bf-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="1c9bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c9bf-109">EXAMPLES</span></span>

### <span data-ttu-id="1c9bf-110">Esempio 1: rimuovere un'origine eventi specificata per nome</span><span class="sxs-lookup"><span data-stu-id="1c9bf-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="1c9bf-111">In questo modo viene rimossa una specifica origine eventi.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-111">This removes a specific event source.</span></span>

### <span data-ttu-id="1c9bf-112">Esempio 2: rimuovere un'origine eventi specificata per oggetto</span><span class="sxs-lookup"><span data-stu-id="1c9bf-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="1c9bf-113">In questo modo viene rimossa una specifica origine eventi.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-113">This removes a specific event source.</span></span>

## <span data-ttu-id="1c9bf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c9bf-114">PARAMETERS</span></span>

### <span data-ttu-id="1c9bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9bf-115">-DefaultProfile</span></span>
<span data-ttu-id="1c9bf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9bf-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1c9bf-117">-EnvironmentName</span></span>
<span data-ttu-id="1c9bf-118">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1c9bf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c9bf-119">-InputObject</span></span>
<span data-ttu-id="1c9bf-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c9bf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c9bf-121">-Name</span></span>
<span data-ttu-id="1c9bf-122">Nome dell'origine dell'evento Insights Series associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="1c9bf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c9bf-123">-PassThru</span></span>
<span data-ttu-id="1c9bf-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="1c9bf-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c9bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c9bf-126">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1c9bf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c9bf-127">-SubscriptionId</span></span>
<span data-ttu-id="1c9bf-128">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1c9bf-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c9bf-129">-Confirm</span></span>
<span data-ttu-id="1c9bf-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9bf-131">-WhatIf</span></span>
<span data-ttu-id="1c9bf-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9bf-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9bf-134">CommonParameters</span></span>
<span data-ttu-id="1c9bf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9bf-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c9bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9bf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c9bf-137">INPUTS</span></span>

### <span data-ttu-id="1c9bf-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="1c9bf-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="1c9bf-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c9bf-139">OUTPUTS</span></span>

### <span data-ttu-id="1c9bf-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c9bf-140">System.Boolean</span></span>

## <span data-ttu-id="1c9bf-141">Note</span><span class="sxs-lookup"><span data-stu-id="1c9bf-141">NOTES</span></span>

<span data-ttu-id="1c9bf-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c9bf-142">ALIASES</span></span>

<span data-ttu-id="1c9bf-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c9bf-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c9bf-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c9bf-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c9bf-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1c9bf-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c9bf-147">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="1c9bf-148">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="1c9bf-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="1c9bf-149">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="1c9bf-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1c9bf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c9bf-151">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="1c9bf-152">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="1c9bf-153">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9bf-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1c9bf-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c9bf-154">RELATED LINKS</span></span>

