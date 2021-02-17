---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190535"
---
# <span data-ttu-id="a6c5a-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6c5a-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="a6c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c5a-103">Elimina l'ambiente con il nome specificato nella sottoscrizione e nel gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a6c5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6c5a-104">SYNTAX</span></span>

### <span data-ttu-id="a6c5a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6c5a-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6c5a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c5a-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6c5a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="a6c5a-108">Elimina l'ambiente con il nome specificato nella sottoscrizione e nel gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a6c5a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="a6c5a-110">Esempio 1: Rimuovere un ambiente approfondimenti della serie temporale in base al nome</span><span class="sxs-lookup"><span data-stu-id="a6c5a-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="a6c5a-111">Questo comando rimuove un ambiente approfondimenti della serie temporale.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="a6c5a-112">Esempio 2: Rimuovere un ambiente approfondimenti della serie temporale in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="a6c5a-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="a6c5a-113">Questo comando rimuove un ambiente approfondimenti della serie temporale.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="a6c5a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6c5a-114">PARAMETERS</span></span>

### <span data-ttu-id="a6c5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c5a-115">-DefaultProfile</span></span>
<span data-ttu-id="a6c5a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c5a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c5a-117">-InputObject</span></span>
<span data-ttu-id="a6c5a-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6c5a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a6c5a-119">-Name</span></span>
<span data-ttu-id="a6c5a-120">Nome dell'ambiente Time Series Insights associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c5a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6c5a-121">-PassThru</span></span>
<span data-ttu-id="a6c5a-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="a6c5a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6c5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6c5a-124">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a6c5a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6c5a-125">-SubscriptionId</span></span>
<span data-ttu-id="a6c5a-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a6c5a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6c5a-127">-Confirm</span></span>
<span data-ttu-id="a6c5a-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c5a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c5a-129">-WhatIf</span></span>
<span data-ttu-id="a6c5a-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c5a-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c5a-132">CommonParameters</span></span>
<span data-ttu-id="a6c5a-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c5a-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c5a-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6c5a-135">INPUTS</span></span>

### <span data-ttu-id="a6c5a-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a6c5a-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a6c5a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6c5a-137">OUTPUTS</span></span>

### <span data-ttu-id="a6c5a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6c5a-138">System.Boolean</span></span>

## <span data-ttu-id="a6c5a-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6c5a-139">NOTES</span></span>

<span data-ttu-id="a6c5a-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6c5a-140">ALIASES</span></span>

<span data-ttu-id="a6c5a-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a6c5a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6c5a-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6c5a-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6c5a-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="a6c5a-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6c5a-145">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a6c5a-146">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="a6c5a-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a6c5a-147">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a6c5a-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a6c5a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6c5a-149">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a6c5a-150">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a6c5a-151">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c5a-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a6c5a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6c5a-152">RELATED LINKS</span></span>

