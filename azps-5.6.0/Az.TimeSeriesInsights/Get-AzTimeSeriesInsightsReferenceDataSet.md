---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1fef5f018791fba9369ce7ab18a4b0c3a2440cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950829"
---
# <span data-ttu-id="a7537-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a7537-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a7537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7537-102">SYNOPSIS</span></span>
<span data-ttu-id="a7537-103">Ottiene il set di dati di riferimento con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="a7537-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7537-104">SYNTAX</span></span>

### <span data-ttu-id="a7537-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7537-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7537-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a7537-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7537-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7537-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a7537-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7537-108">DESCRIPTION</span></span>
<span data-ttu-id="a7537-109">Ottiene il set di dati di riferimento con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="a7537-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7537-110">EXAMPLES</span></span>

### <span data-ttu-id="a7537-111">Esempio 1: Elencare tutti i set di dati di riferimento nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="a7537-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a7537-112">Questo comando elenca tutti i set di dati di riferimento nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="a7537-113">Esempio 2: Ottenere un set di dati di riferimento specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="a7537-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a7537-114">Questo comando ottiene un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="a7537-115">Esempio 3: Ottenere un set di dati di riferimento specificato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="a7537-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a7537-116">Questo comando ottiene un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="a7537-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7537-117">PARAMETERS</span></span>

### <span data-ttu-id="a7537-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7537-118">-DefaultProfile</span></span>
<span data-ttu-id="a7537-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7537-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7537-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a7537-120">-EnvironmentName</span></span>
<span data-ttu-id="a7537-121">Nome dell'ambiente Approfondimenti serie temporale associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7537-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7537-122">-InputObject</span></span>
<span data-ttu-id="a7537-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a7537-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7537-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a7537-124">-Name</span></span>
<span data-ttu-id="a7537-125">Nome del set di dati di riferimento Approfondimenti serie temporale associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7537-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7537-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7537-127">Nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7537-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7537-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7537-128">-SubscriptionId</span></span>
<span data-ttu-id="a7537-129">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="a7537-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7537-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7537-130">CommonParameters</span></span>
<span data-ttu-id="a7537-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7537-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7537-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7537-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7537-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7537-133">INPUTS</span></span>

### <span data-ttu-id="a7537-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a7537-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a7537-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7537-135">OUTPUTS</span></span>

### <span data-ttu-id="a7537-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="a7537-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="a7537-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7537-137">NOTES</span></span>

<span data-ttu-id="a7537-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a7537-138">ALIASES</span></span>

<span data-ttu-id="a7537-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a7537-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7537-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a7537-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7537-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7537-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7537-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a7537-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7537-143">`[AccessPolicyName <String>]`: nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="a7537-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a7537-144">`[EnvironmentName <String>]`: nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="a7537-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a7537-145">`[EventSourceName <String>]`: nome dell'origine evento Time Series Insights associata all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="a7537-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a7537-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a7537-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7537-147">`[ReferenceDataSetName <String>]`: nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a7537-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a7537-148">`[ResourceGroupName <String>]`: nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7537-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a7537-149">`[SubscriptionId <String>]`: ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="a7537-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a7537-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7537-150">RELATED LINKS</span></span>

