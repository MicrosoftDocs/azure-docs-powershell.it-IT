---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 858578d36f2f913f903f86b9c556a93d30e2e3b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019072"
---
# <span data-ttu-id="5264f-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5264f-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="5264f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5264f-102">SYNOPSIS</span></span>
<span data-ttu-id="5264f-103">Aggiornare un database di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="5264f-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="5264f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5264f-104">SYNTAX</span></span>

### <span data-ttu-id="5264f-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5264f-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5264f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5264f-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5264f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5264f-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5264f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5264f-108">DESCRIPTION</span></span>
<span data-ttu-id="5264f-109">Aggiornare un database di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="5264f-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="5264f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5264f-110">EXAMPLES</span></span>

### <span data-ttu-id="5264f-111">Esempio 1-aggiornare un database esistente per nome</span><span class="sxs-lookup"><span data-stu-id="5264f-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5264f-112">Il comando precedente aggiorna il periodo di cancellazione soft del database kusto "mykustodatabase" nel cluster "mykustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="5264f-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="5264f-113">Esempio 2-aggiornare un database esistente tramite pipe</span><span class="sxs-lookup"><span data-stu-id="5264f-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="5264f-114">Il comando precedente restituisce il database kusto "mykustodatabase" nel cluster "mykustocluster" trovato nel gruppo di risorse "testrg" con il `Get-AzKustoDatabase` cmdlet e quindi convoglia il risultato in per `Update-AzKustoDatabase` aggiornare il periodo di eliminazione morbida del database a cinque giorni.</span><span class="sxs-lookup"><span data-stu-id="5264f-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="5264f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5264f-115">PARAMETERS</span></span>

### <span data-ttu-id="5264f-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="5264f-116">-ClusterName</span></span>
<span data-ttu-id="5264f-117">Nome del cluster in cui è presente il database</span><span class="sxs-lookup"><span data-stu-id="5264f-117">Name of cluster under which the database exists</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5264f-118">-DefaultProfile</span></span>
<span data-ttu-id="5264f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5264f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5264f-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="5264f-121">Numero di giorni in cui i dati devono essere conservati nella cache per le query veloci</span><span class="sxs-lookup"><span data-stu-id="5264f-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5264f-122">-InputObject</span></span>
<span data-ttu-id="5264f-123">Oggetto di database kusto.</span><span class="sxs-lookup"><span data-stu-id="5264f-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5264f-124">-Name</span></span>
<span data-ttu-id="5264f-125">Nome del database da aggiornare</span><span class="sxs-lookup"><span data-stu-id="5264f-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5264f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5264f-127">Nome del gruppo di risorse in cui è presente il cluster.</span><span class="sxs-lookup"><span data-stu-id="5264f-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5264f-128">-ResourceId</span></span>
<span data-ttu-id="5264f-129">ResourceID database kusto.</span><span class="sxs-lookup"><span data-stu-id="5264f-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5264f-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="5264f-131">Numero di giorni di permanenza dei dati prima che venga impedito l'accessibilità alle query</span><span class="sxs-lookup"><span data-stu-id="5264f-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5264f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5264f-132">-Confirm</span></span>
<span data-ttu-id="5264f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5264f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5264f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5264f-134">-WhatIf</span></span>
<span data-ttu-id="5264f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5264f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5264f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5264f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5264f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5264f-137">CommonParameters</span></span>
<span data-ttu-id="5264f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5264f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5264f-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5264f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5264f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5264f-140">INPUTS</span></span>

### <span data-ttu-id="5264f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5264f-141">System.String</span></span>

### <span data-ttu-id="5264f-142">Microsoft. Azure. Commands. kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5264f-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="5264f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5264f-143">OUTPUTS</span></span>

### <span data-ttu-id="5264f-144">Microsoft. Azure. Commands. kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5264f-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="5264f-145">Note</span><span class="sxs-lookup"><span data-stu-id="5264f-145">NOTES</span></span>

## <span data-ttu-id="5264f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5264f-146">RELATED LINKS</span></span>
