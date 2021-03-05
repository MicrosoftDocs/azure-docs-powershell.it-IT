---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 3ef56e9c554b7efbd762b4b373806aad649e0449
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987446"
---
# <span data-ttu-id="1f99f-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1f99f-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="1f99f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f99f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f99f-103">Aggiorna i criteri di accesso con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="1f99f-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="1f99f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f99f-104">SYNTAX</span></span>

### <span data-ttu-id="1f99f-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f99f-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f99f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1f99f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f99f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f99f-107">DESCRIPTION</span></span>
<span data-ttu-id="1f99f-108">Aggiorna i criteri di accesso con il nome specificato nella sottoscrizione, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="1f99f-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="1f99f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f99f-109">EXAMPLES</span></span>

### <span data-ttu-id="1f99f-110">Esempio 1: Aggiornare un criterio di accesso specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="1f99f-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="1f99f-111">Questo comando aggiorna i criteri di accesso specificati.</span><span class="sxs-lookup"><span data-stu-id="1f99f-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="1f99f-112">Esempio 2: Aggiornare un criterio di accesso specificato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="1f99f-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="1f99f-113">Questo comando aggiorna i criteri di accesso specificati.</span><span class="sxs-lookup"><span data-stu-id="1f99f-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="1f99f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f99f-114">PARAMETERS</span></span>

### <span data-ttu-id="1f99f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f99f-115">-DefaultProfile</span></span>
<span data-ttu-id="1f99f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f99f-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f99f-117">-Description</span></span>
<span data-ttu-id="1f99f-118">Descrizione dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="1f99f-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="1f99f-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1f99f-119">-EnvironmentName</span></span>
<span data-ttu-id="1f99f-120">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1f99f-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1f99f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f99f-121">-InputObject</span></span>
<span data-ttu-id="1f99f-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1f99f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f99f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f99f-123">-Name</span></span>
<span data-ttu-id="1f99f-124">Nome dei criteri di accesso Time Series Insights associati all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="1f99f-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f99f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f99f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f99f-126">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1f99f-127">-Role</span><span class="sxs-lookup"><span data-stu-id="1f99f-127">-Role</span></span>
<span data-ttu-id="1f99f-128">Elenco dei ruoli assegnati all'entità nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="1f99f-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f99f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f99f-129">-SubscriptionId</span></span>
<span data-ttu-id="1f99f-130">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1f99f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f99f-131">-Confirm</span></span>
<span data-ttu-id="1f99f-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f99f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f99f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f99f-133">-WhatIf</span></span>
<span data-ttu-id="1f99f-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f99f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f99f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f99f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f99f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f99f-136">CommonParameters</span></span>
<span data-ttu-id="1f99f-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f99f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f99f-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f99f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f99f-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f99f-139">INPUTS</span></span>

### <span data-ttu-id="1f99f-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="1f99f-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="1f99f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f99f-141">OUTPUTS</span></span>

### <span data-ttu-id="1f99f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="1f99f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="1f99f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f99f-143">NOTES</span></span>

<span data-ttu-id="1f99f-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1f99f-144">ALIASES</span></span>

<span data-ttu-id="1f99f-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1f99f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f99f-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1f99f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f99f-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f99f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f99f-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1f99f-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f99f-149">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="1f99f-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="1f99f-150">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="1f99f-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="1f99f-151">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="1f99f-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="1f99f-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="1f99f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f99f-153">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="1f99f-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="1f99f-154">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="1f99f-155">`[SubscriptionId <String>]`: ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1f99f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f99f-156">RELATED LINKS</span></span>

