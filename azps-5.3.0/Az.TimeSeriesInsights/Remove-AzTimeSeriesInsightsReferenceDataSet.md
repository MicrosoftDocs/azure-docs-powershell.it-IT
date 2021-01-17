---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474813"
---
# <span data-ttu-id="d8f26-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="d8f26-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="d8f26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8f26-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f26-103">Elimina il set di dati di riferimento con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="d8f26-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="d8f26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8f26-104">SYNTAX</span></span>

### <span data-ttu-id="d8f26-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8f26-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8f26-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8f26-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8f26-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8f26-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f26-108">Elimina il set di dati di riferimento con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="d8f26-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="d8f26-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8f26-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f26-110">Esempio 1: rimuovere i dati di riferimento specificati impostati per nome</span><span class="sxs-lookup"><span data-stu-id="d8f26-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="d8f26-111">Questo comando rimuove un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="d8f26-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="d8f26-112">Esempio 2: rimuovere un set di dati di riferimento specificato da un oggetto</span><span class="sxs-lookup"><span data-stu-id="d8f26-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="d8f26-113">Questo comando rimuove un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="d8f26-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="d8f26-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8f26-114">PARAMETERS</span></span>

### <span data-ttu-id="d8f26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f26-115">-DefaultProfile</span></span>
<span data-ttu-id="d8f26-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f26-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d8f26-117">-EnvironmentName</span></span>
<span data-ttu-id="d8f26-118">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d8f26-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="d8f26-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f26-119">-InputObject</span></span>
<span data-ttu-id="d8f26-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d8f26-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8f26-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8f26-121">-Name</span></span>
<span data-ttu-id="d8f26-122">Nome del set di dati di riferimento per gli approfondimenti della serie temporale associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="d8f26-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f26-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8f26-123">-PassThru</span></span>
<span data-ttu-id="d8f26-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="d8f26-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d8f26-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f26-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8f26-126">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d8f26-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8f26-127">-SubscriptionId</span></span>
<span data-ttu-id="d8f26-128">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d8f26-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8f26-129">-Confirm</span></span>
<span data-ttu-id="d8f26-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f26-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f26-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f26-131">-WhatIf</span></span>
<span data-ttu-id="d8f26-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8f26-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f26-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8f26-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f26-134">CommonParameters</span></span>
<span data-ttu-id="d8f26-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f26-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8f26-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f26-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8f26-137">INPUTS</span></span>

### <span data-ttu-id="d8f26-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="d8f26-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="d8f26-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8f26-139">OUTPUTS</span></span>

### <span data-ttu-id="d8f26-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8f26-140">System.Boolean</span></span>

## <span data-ttu-id="d8f26-141">Note</span><span class="sxs-lookup"><span data-stu-id="d8f26-141">NOTES</span></span>

<span data-ttu-id="d8f26-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d8f26-142">ALIASES</span></span>

<span data-ttu-id="d8f26-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8f26-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8f26-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d8f26-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8f26-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8f26-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8f26-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d8f26-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8f26-147">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="d8f26-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="d8f26-148">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="d8f26-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="d8f26-149">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="d8f26-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="d8f26-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d8f26-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8f26-151">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d8f26-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="d8f26-152">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="d8f26-153">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f26-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d8f26-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8f26-154">RELATED LINKS</span></span>

