---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199958"
---
# <span data-ttu-id="a1af3-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1af3-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="a1af3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1af3-102">SYNOPSIS</span></span>
<span data-ttu-id="a1af3-103">Elimina i criteri di accesso con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="a1af3-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a1af3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1af3-104">SYNTAX</span></span>

### <span data-ttu-id="a1af3-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1af3-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1af3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1af3-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1af3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1af3-107">DESCRIPTION</span></span>
<span data-ttu-id="a1af3-108">Elimina i criteri di accesso con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="a1af3-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a1af3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1af3-109">EXAMPLES</span></span>

### <span data-ttu-id="a1af3-110">Esempio 1: rimuovere un criterio di accesso specificato per nome</span><span class="sxs-lookup"><span data-stu-id="a1af3-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="a1af3-111">Questo comando rimuove un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="a1af3-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="a1af3-112">Esempio 2: rimuovere un criterio di accesso specificato per oggetto</span><span class="sxs-lookup"><span data-stu-id="a1af3-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="a1af3-113">Questo comando rimuove un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="a1af3-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="a1af3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1af3-114">PARAMETERS</span></span>

### <span data-ttu-id="a1af3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1af3-115">-DefaultProfile</span></span>
<span data-ttu-id="a1af3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1af3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1af3-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a1af3-117">-EnvironmentName</span></span>
<span data-ttu-id="a1af3-118">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a1af3-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a1af3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1af3-119">-InputObject</span></span>
<span data-ttu-id="a1af3-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a1af3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1af3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1af3-121">-Name</span></span>
<span data-ttu-id="a1af3-122">Il nome della serie temporale approfondisce i criteri di accesso associati all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a1af3-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1af3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1af3-123">-PassThru</span></span>
<span data-ttu-id="a1af3-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="a1af3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a1af3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1af3-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1af3-126">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a1af3-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a1af3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1af3-127">-SubscriptionId</span></span>
<span data-ttu-id="a1af3-128">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1af3-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a1af3-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1af3-129">-Confirm</span></span>
<span data-ttu-id="a1af3-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1af3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1af3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1af3-131">-WhatIf</span></span>
<span data-ttu-id="a1af3-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1af3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1af3-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1af3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1af3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1af3-134">CommonParameters</span></span>
<span data-ttu-id="a1af3-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1af3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1af3-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1af3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1af3-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1af3-137">INPUTS</span></span>

### <span data-ttu-id="a1af3-138">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a1af3-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a1af3-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1af3-139">OUTPUTS</span></span>

### <span data-ttu-id="a1af3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1af3-140">System.Boolean</span></span>

## <span data-ttu-id="a1af3-141">Note</span><span class="sxs-lookup"><span data-stu-id="a1af3-141">NOTES</span></span>

<span data-ttu-id="a1af3-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a1af3-142">ALIASES</span></span>

<span data-ttu-id="a1af3-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1af3-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1af3-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a1af3-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1af3-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1af3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1af3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a1af3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1af3-147">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="a1af3-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a1af3-148">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="a1af3-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a1af3-149">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a1af3-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a1af3-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a1af3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1af3-151">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a1af3-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a1af3-152">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="a1af3-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a1af3-153">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="a1af3-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a1af3-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1af3-154">RELATED LINKS</span></span>
