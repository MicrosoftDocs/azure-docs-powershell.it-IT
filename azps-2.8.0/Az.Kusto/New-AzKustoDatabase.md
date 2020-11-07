---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: 33272012d81160a055bcd5d1eb0ef617787eed1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674070"
---
# <span data-ttu-id="c2ef9-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c2ef9-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="c2ef9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ef9-103">Crea un nuovo database di Kusto in un cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="c2ef9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2ef9-104">SYNTAX</span></span>

### <span data-ttu-id="c2ef9-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2ef9-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ef9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ef9-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ef9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2ef9-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ef9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2ef9-108">DESCRIPTION</span></span>
<span data-ttu-id="c2ef9-109">Crea un nuovo database di Kusto in un cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="c2ef9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2ef9-110">EXAMPLES</span></span>

### <span data-ttu-id="c2ef9-111">Esempio 1-creare un nuovo database di Kusto in base al nome</span><span class="sxs-lookup"><span data-stu-id="c2ef9-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="c2ef9-112">Il comando precedente crea un nuovo database di Kusto denominato "mykustodatabase" nel cluster esistente "mykustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="c2ef9-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c2ef9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2ef9-113">PARAMETERS</span></span>

### <span data-ttu-id="c2ef9-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c2ef9-114">-ClusterName</span></span>
<span data-ttu-id="c2ef9-115">Nome del cluster in cui si vuole creare il database.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-115">Name of cluster under which you want to create the database.</span></span>

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

### <span data-ttu-id="c2ef9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ef9-116">-DefaultProfile</span></span>
<span data-ttu-id="c2ef9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ef9-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c2ef9-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="c2ef9-119">Numero di giorni di dati che devono essere conservati nella cache per le query veloci.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2ef9-120">-InputObject</span></span>
<span data-ttu-id="c2ef9-121">Oggetto cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2ef9-122">-Name</span></span>
<span data-ttu-id="c2ef9-123">Nome del database da creare.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="c2ef9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ef9-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2ef9-125">Nome del gruppo di risorse in cui è presente il cluster.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="c2ef9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ef9-126">-ResourceId</span></span>
<span data-ttu-id="c2ef9-127">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="c2ef9-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c2ef9-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="c2ef9-129">Il numero di giorni di dati deve essere mantenuto prima che smetta di essere accessibile alle query.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ef9-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2ef9-130">-Confirm</span></span>
<span data-ttu-id="c2ef9-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ef9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ef9-132">-WhatIf</span></span>
<span data-ttu-id="c2ef9-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ef9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ef9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ef9-135">CommonParameters</span></span>
<span data-ttu-id="c2ef9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ef9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ef9-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ef9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ef9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2ef9-138">INPUTS</span></span>

### <span data-ttu-id="c2ef9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ef9-139">System.String</span></span>

### <span data-ttu-id="c2ef9-140">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="c2ef9-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="c2ef9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2ef9-141">OUTPUTS</span></span>

### <span data-ttu-id="c2ef9-142">Microsoft. Azure. Commands. kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c2ef9-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="c2ef9-143">Note</span><span class="sxs-lookup"><span data-stu-id="c2ef9-143">NOTES</span></span>

## <span data-ttu-id="c2ef9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2ef9-144">RELATED LINKS</span></span>
