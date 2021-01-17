---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331663"
---
# <span data-ttu-id="795d5-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="795d5-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="795d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="795d5-102">SYNOPSIS</span></span>
<span data-ttu-id="795d5-103">Aggiorna i criteri di accesso con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="795d5-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="795d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="795d5-104">SYNTAX</span></span>

### <span data-ttu-id="795d5-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="795d5-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="795d5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="795d5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="795d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="795d5-107">DESCRIPTION</span></span>
<span data-ttu-id="795d5-108">Aggiorna i criteri di accesso con il nome specificato nell'abbonamento, nel gruppo di risorse e nell'ambiente specificati.</span><span class="sxs-lookup"><span data-stu-id="795d5-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="795d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="795d5-109">EXAMPLES</span></span>

### <span data-ttu-id="795d5-110">Esempio 1: aggiornare un criterio di accesso specificato per nome</span><span class="sxs-lookup"><span data-stu-id="795d5-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="795d5-111">Questo comando aggiorna un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="795d5-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="795d5-112">Esempio 2: aggiornare un criterio di accesso specificato per oggetto</span><span class="sxs-lookup"><span data-stu-id="795d5-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="795d5-113">Questo comando aggiorna un criterio di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="795d5-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="795d5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="795d5-114">PARAMETERS</span></span>

### <span data-ttu-id="795d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795d5-115">-DefaultProfile</span></span>
<span data-ttu-id="795d5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="795d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795d5-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="795d5-117">-Description</span></span>
<span data-ttu-id="795d5-118">Descrizione dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="795d5-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="795d5-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="795d5-119">-EnvironmentName</span></span>
<span data-ttu-id="795d5-120">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="795d5-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="795d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="795d5-121">-InputObject</span></span>
<span data-ttu-id="795d5-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="795d5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="795d5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="795d5-123">-Name</span></span>
<span data-ttu-id="795d5-124">Il nome della serie temporale approfondisce i criteri di accesso associati all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="795d5-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="795d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="795d5-126">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="795d5-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="795d5-127">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="795d5-127">-Role</span></span>
<span data-ttu-id="795d5-128">Elenco dei ruoli assegnati all'oggetto Principal nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="795d5-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="795d5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="795d5-129">-SubscriptionId</span></span>
<span data-ttu-id="795d5-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="795d5-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="795d5-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="795d5-131">-Confirm</span></span>
<span data-ttu-id="795d5-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="795d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795d5-133">-WhatIf</span></span>
<span data-ttu-id="795d5-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="795d5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795d5-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="795d5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795d5-136">CommonParameters</span></span>
<span data-ttu-id="795d5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795d5-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="795d5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795d5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="795d5-139">INPUTS</span></span>

### <span data-ttu-id="795d5-140">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="795d5-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="795d5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="795d5-141">OUTPUTS</span></span>

### <span data-ttu-id="795d5-142">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="795d5-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="795d5-143">Note</span><span class="sxs-lookup"><span data-stu-id="795d5-143">NOTES</span></span>

<span data-ttu-id="795d5-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="795d5-144">ALIASES</span></span>

<span data-ttu-id="795d5-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="795d5-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="795d5-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="795d5-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="795d5-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="795d5-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="795d5-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="795d5-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="795d5-149">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="795d5-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="795d5-150">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="795d5-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="795d5-151">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="795d5-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="795d5-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="795d5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="795d5-153">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="795d5-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="795d5-154">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="795d5-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="795d5-155">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="795d5-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="795d5-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="795d5-156">RELATED LINKS</span></span>

