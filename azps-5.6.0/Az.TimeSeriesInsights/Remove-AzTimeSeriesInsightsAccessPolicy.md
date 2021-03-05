---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2fe9a418f135471e18f469bf0dcf5ce515de1c2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963406"
---
# <span data-ttu-id="78f8b-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78f8b-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="78f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="78f8b-103">Elimina i criteri di accesso con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="78f8b-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="78f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78f8b-104">SYNTAX</span></span>

### <span data-ttu-id="78f8b-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78f8b-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="78f8b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="78f8b-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78f8b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78f8b-107">DESCRIPTION</span></span>
<span data-ttu-id="78f8b-108">Elimina i criteri di accesso con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati</span><span class="sxs-lookup"><span data-stu-id="78f8b-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="78f8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78f8b-109">EXAMPLES</span></span>

### <span data-ttu-id="78f8b-110">Esempio 1: Rimuovere un criterio di accesso specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="78f8b-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="78f8b-111">Questo comando rimuove un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="78f8b-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="78f8b-112">Esempio 2: Rimuovere un criterio di accesso specificato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="78f8b-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="78f8b-113">Questo comando rimuove un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="78f8b-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="78f8b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78f8b-114">PARAMETERS</span></span>

### <span data-ttu-id="78f8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f8b-115">-DefaultProfile</span></span>
<span data-ttu-id="78f8b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f8b-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="78f8b-117">-EnvironmentName</span></span>
<span data-ttu-id="78f8b-118">Nome dell'ambiente Approfondimenti serie temporale associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="78f8b-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="78f8b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f8b-119">-InputObject</span></span>
<span data-ttu-id="78f8b-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="78f8b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="78f8b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78f8b-121">-Name</span></span>
<span data-ttu-id="78f8b-122">Nome dei criteri di accesso Time Series Insights associati all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="78f8b-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="78f8b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78f8b-123">-PassThru</span></span>
<span data-ttu-id="78f8b-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="78f8b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="78f8b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f8b-125">-ResourceGroupName</span></span>
<span data-ttu-id="78f8b-126">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8b-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="78f8b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78f8b-127">-SubscriptionId</span></span>
<span data-ttu-id="78f8b-128">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8b-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="78f8b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78f8b-129">-Confirm</span></span>
<span data-ttu-id="78f8b-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f8b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f8b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f8b-131">-WhatIf</span></span>
<span data-ttu-id="78f8b-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78f8b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f8b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78f8b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f8b-134">CommonParameters</span></span>
<span data-ttu-id="78f8b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f8b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78f8b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f8b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="78f8b-137">INPUTS</span></span>

### <span data-ttu-id="78f8b-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="78f8b-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="78f8b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78f8b-139">OUTPUTS</span></span>

### <span data-ttu-id="78f8b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78f8b-140">System.Boolean</span></span>

## <span data-ttu-id="78f8b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="78f8b-141">NOTES</span></span>

<span data-ttu-id="78f8b-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="78f8b-142">ALIASES</span></span>

<span data-ttu-id="78f8b-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="78f8b-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78f8b-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="78f8b-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78f8b-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78f8b-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78f8b-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="78f8b-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78f8b-147">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="78f8b-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="78f8b-148">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="78f8b-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="78f8b-149">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="78f8b-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="78f8b-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="78f8b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78f8b-151">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="78f8b-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="78f8b-152">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8b-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="78f8b-153">`[SubscriptionId <String>]`: ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="78f8b-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="78f8b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78f8b-154">RELATED LINKS</span></span>

