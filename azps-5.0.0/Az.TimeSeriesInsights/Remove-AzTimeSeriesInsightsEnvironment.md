---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203204"
---
# <span data-ttu-id="c8a47-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8a47-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="c8a47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8a47-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a47-103">Elimina l'ambiente con il nome specificato nel gruppo di sottoscrizioni e risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c8a47-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="c8a47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8a47-104">SYNTAX</span></span>

### <span data-ttu-id="c8a47-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8a47-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8a47-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8a47-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8a47-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8a47-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a47-108">Elimina l'ambiente con il nome specificato nel gruppo di sottoscrizioni e risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c8a47-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="c8a47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8a47-109">EXAMPLES</span></span>

### <span data-ttu-id="c8a47-110">Esempio 1: rimuovere un ambiente Insights serie temporali per nome</span><span class="sxs-lookup"><span data-stu-id="c8a47-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="c8a47-111">Questo comando rimuove un ambiente Insights serie temporali.</span><span class="sxs-lookup"><span data-stu-id="c8a47-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="c8a47-112">Esempio 2: rimuovere un ambiente Insights serie temporali per oggetto</span><span class="sxs-lookup"><span data-stu-id="c8a47-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="c8a47-113">Questo comando rimuove un ambiente Insights serie temporali.</span><span class="sxs-lookup"><span data-stu-id="c8a47-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="c8a47-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8a47-114">PARAMETERS</span></span>

### <span data-ttu-id="c8a47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a47-115">-DefaultProfile</span></span>
<span data-ttu-id="c8a47-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a47-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8a47-117">-InputObject</span></span>
<span data-ttu-id="c8a47-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c8a47-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8a47-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8a47-119">-Name</span></span>
<span data-ttu-id="c8a47-120">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c8a47-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="c8a47-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8a47-121">-PassThru</span></span>
<span data-ttu-id="c8a47-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="c8a47-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c8a47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a47-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8a47-124">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a47-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c8a47-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8a47-125">-SubscriptionId</span></span>
<span data-ttu-id="c8a47-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a47-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c8a47-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8a47-127">-Confirm</span></span>
<span data-ttu-id="c8a47-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a47-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a47-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a47-129">-WhatIf</span></span>
<span data-ttu-id="c8a47-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8a47-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a47-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8a47-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a47-132">CommonParameters</span></span>
<span data-ttu-id="c8a47-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a47-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8a47-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a47-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8a47-135">INPUTS</span></span>

### <span data-ttu-id="c8a47-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="c8a47-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="c8a47-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8a47-137">OUTPUTS</span></span>

### <span data-ttu-id="c8a47-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8a47-138">System.Boolean</span></span>

## <span data-ttu-id="c8a47-139">Note</span><span class="sxs-lookup"><span data-stu-id="c8a47-139">NOTES</span></span>

<span data-ttu-id="c8a47-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c8a47-140">ALIASES</span></span>

<span data-ttu-id="c8a47-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8a47-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8a47-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c8a47-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8a47-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8a47-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8a47-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c8a47-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8a47-145">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="c8a47-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="c8a47-146">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="c8a47-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="c8a47-147">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="c8a47-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="c8a47-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c8a47-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8a47-149">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="c8a47-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="c8a47-150">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a47-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="c8a47-151">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a47-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c8a47-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8a47-152">RELATED LINKS</span></span>

