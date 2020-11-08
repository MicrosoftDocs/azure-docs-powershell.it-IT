---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191109"
---
# <span data-ttu-id="34e57-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="34e57-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="34e57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34e57-102">SYNOPSIS</span></span>
<span data-ttu-id="34e57-103">Creare o aggiornare un set di dati di riferimento nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="34e57-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="34e57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e57-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34e57-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e57-105">DESCRIPTION</span></span>
<span data-ttu-id="34e57-106">Creare o aggiornare un set di dati di riferimento nell'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="34e57-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="34e57-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e57-107">EXAMPLES</span></span>

### <span data-ttu-id="34e57-108">Esempio 1: creare un set di dati di riferimento per un ambiente specificato</span><span class="sxs-lookup"><span data-stu-id="34e57-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="34e57-109">Questo comando crea un set di dati di riferimento per un ambiente specifico.</span><span class="sxs-lookup"><span data-stu-id="34e57-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="34e57-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34e57-110">PARAMETERS</span></span>

### <span data-ttu-id="34e57-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="34e57-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="34e57-112">Il comportamento di confronto delle chiavi del set di dati di riferimento può essere impostato tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e57-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="34e57-113">Per impostazione predefinita, il valore è' Ordinal '-il che significa che il confronto tra maiuscole e minuscole verrà eseguito durante l'Unione di dati di riferimento con eventi o durante l'aggiunta di nuovi dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="34e57-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="34e57-114">Quando ' OrdinalIgnoreCase ' è impostato, verrà usato il confronto senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="34e57-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e57-115">-DefaultProfile</span></span>
<span data-ttu-id="34e57-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34e57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34e57-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="34e57-117">-EnvironmentName</span></span>
<span data-ttu-id="34e57-118">Nome dell'ambiente Insights serie temporali associato al gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="34e57-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-119">-Proprietà Property</span><span class="sxs-lookup"><span data-stu-id="34e57-119">-KeyProperty</span></span>
<span data-ttu-id="34e57-120">Elenco delle proprietà chiave per il set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="34e57-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="34e57-121">Per creare una tabella hash, vedere la sezione Note per le proprietà della proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e57-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="34e57-122">-Location</span></span>
<span data-ttu-id="34e57-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34e57-123">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="34e57-124">-Name</span></span>
<span data-ttu-id="34e57-125">Nome del set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="34e57-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e57-126">-ResourceGroupName</span></span>
<span data-ttu-id="34e57-127">Nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="34e57-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34e57-128">-SubscriptionId</span></span>
<span data-ttu-id="34e57-129">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="34e57-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="34e57-130">-Tag</span></span>
<span data-ttu-id="34e57-131">Coppie chiave-valore di proprietà aggiuntive per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="34e57-131">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e57-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34e57-132">-Confirm</span></span>
<span data-ttu-id="34e57-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e57-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e57-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e57-134">-WhatIf</span></span>
<span data-ttu-id="34e57-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e57-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e57-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e57-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e57-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e57-137">CommonParameters</span></span>
<span data-ttu-id="34e57-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e57-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e57-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34e57-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e57-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34e57-140">INPUTS</span></span>

## <span data-ttu-id="34e57-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e57-141">OUTPUTS</span></span>

### <span data-ttu-id="34e57-142">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="34e57-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="34e57-143">Note</span><span class="sxs-lookup"><span data-stu-id="34e57-143">NOTES</span></span>

<span data-ttu-id="34e57-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="34e57-144">ALIASES</span></span>

<span data-ttu-id="34e57-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34e57-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34e57-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="34e57-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34e57-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34e57-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34e57-148">Proprietà Key <IReferenceDataSetKeyProperty [] >: elenco delle proprietà chiave per il set di dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="34e57-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="34e57-149">`[Name <String>]`: Nome della proprietà Key.</span><span class="sxs-lookup"><span data-stu-id="34e57-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="34e57-150">`[Type <ReferenceDataKeyPropertyType?>]`: Il tipo della proprietà Key.</span><span class="sxs-lookup"><span data-stu-id="34e57-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="34e57-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e57-151">RELATED LINKS</span></span>
