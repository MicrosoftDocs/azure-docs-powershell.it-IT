---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191407"
---
# <span data-ttu-id="7b5ef-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="7b5ef-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="7b5ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b5ef-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5ef-103">Ottiene il set di dati di riferimento con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="7b5ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b5ef-104">SYNTAX</span></span>

### <span data-ttu-id="7b5ef-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b5ef-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7b5ef-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7b5ef-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7b5ef-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b5ef-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7b5ef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b5ef-108">DESCRIPTION</span></span>
<span data-ttu-id="7b5ef-109">Ottiene il set di dati di riferimento con il nome specificato nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="7b5ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b5ef-110">EXAMPLES</span></span>

### <span data-ttu-id="7b5ef-111">Esempio 1: elenca tutti i set di dati di riferimento nell'ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="7b5ef-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="7b5ef-112">Questo comando elenca tutti i set di dati di riferimento nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="7b5ef-113">Esempio 2: ottenere i dati di riferimento specificati impostati per nome</span><span class="sxs-lookup"><span data-stu-id="7b5ef-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="7b5ef-114">Questo comando ottiene un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="7b5ef-115">Esempio 3: ottenere un set di dati di riferimento specificato dall'oggetto</span><span class="sxs-lookup"><span data-stu-id="7b5ef-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="7b5ef-116">Questo comando ottiene un set di dati di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="7b5ef-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b5ef-117">PARAMETERS</span></span>

### <span data-ttu-id="7b5ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5ef-118">-DefaultProfile</span></span>
<span data-ttu-id="7b5ef-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5ef-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="7b5ef-120">-EnvironmentName</span></span>
<span data-ttu-id="7b5ef-121">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="7b5ef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b5ef-122">-InputObject</span></span>
<span data-ttu-id="7b5ef-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b5ef-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b5ef-124">-Name</span></span>
<span data-ttu-id="7b5ef-125">Nome del set di dati di riferimento per gli approfondimenti della serie temporale associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="7b5ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b5ef-127">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="7b5ef-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b5ef-128">-SubscriptionId</span></span>
<span data-ttu-id="7b5ef-129">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7b5ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5ef-130">CommonParameters</span></span>
<span data-ttu-id="7b5ef-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5ef-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b5ef-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5ef-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b5ef-133">INPUTS</span></span>

### <span data-ttu-id="7b5ef-134">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="7b5ef-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="7b5ef-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b5ef-135">OUTPUTS</span></span>

### <span data-ttu-id="7b5ef-136">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="7b5ef-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="7b5ef-137">Note</span><span class="sxs-lookup"><span data-stu-id="7b5ef-137">NOTES</span></span>

<span data-ttu-id="7b5ef-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7b5ef-138">ALIASES</span></span>

<span data-ttu-id="7b5ef-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b5ef-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b5ef-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b5ef-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b5ef-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7b5ef-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b5ef-143">`[AccessPolicyName <String>]`: Nome del criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="7b5ef-144">`[EnvironmentName <String>]`: Nome dell'ambiente</span><span class="sxs-lookup"><span data-stu-id="7b5ef-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="7b5ef-145">`[EventSourceName <String>]`: Il nome dell'origine dell'evento Insights serie temporali associato all'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="7b5ef-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7b5ef-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b5ef-147">`[ReferenceDataSetName <String>]`: Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="7b5ef-148">`[ResourceGroupName <String>]`: Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="7b5ef-149">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5ef-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7b5ef-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b5ef-150">RELATED LINKS</span></span>
