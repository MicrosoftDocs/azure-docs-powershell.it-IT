---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: f78dd41283312434f8a3ea833f9c96df6527cb95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019091"
---
# <span data-ttu-id="3f0be-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="3f0be-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="3f0be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f0be-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0be-103">Elencare tutti i database di Kusto in un cluster o ottenere uno specifico database di Kusto.</span><span class="sxs-lookup"><span data-stu-id="3f0be-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="3f0be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f0be-104">SYNTAX</span></span>

### <span data-ttu-id="3f0be-105">ByClusterOrResourceGroupOrSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f0be-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f0be-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f0be-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f0be-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f0be-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f0be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f0be-108">DESCRIPTION</span></span>
<span data-ttu-id="3f0be-109">Elencare tutti i database di Kusto in un cluster o ottenere uno specifico database di Kusto.</span><span class="sxs-lookup"><span data-stu-id="3f0be-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="3f0be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f0be-110">EXAMPLES</span></span>

### <span data-ttu-id="3f0be-111">Esempio 1-elencare tutti i database di Kusto in un cluster per nome</span><span class="sxs-lookup"><span data-stu-id="3f0be-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f0be-112">Il comando precedente restituisce tutti i database di Kusto nel cluster "mykustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="3f0be-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3f0be-113">Esempio 2-elencare tutti i database di Kusto in un cluster tramite piping</span><span class="sxs-lookup"><span data-stu-id="3f0be-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f0be-114">Il comando precedente otterrà il cluster kusto denominato "mykustocluster" nel gruppo di risorse "testrg" che usa il `Get-AzKustoCluster` cmdlet e consente di inviare il risultato al `Get-AzKustoDatabase` cmdlet per elencare tutti i database del cluster.</span><span class="sxs-lookup"><span data-stu-id="3f0be-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="3f0be-115">Esempio 3-ottenere un database di Kusto specifico per nome</span><span class="sxs-lookup"><span data-stu-id="3f0be-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f0be-116">Il comando precedente restituisce il database di Kusto denominato "mykustodatabase" nel cluster "mykustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="3f0be-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="3f0be-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f0be-117">PARAMETERS</span></span>

### <span data-ttu-id="3f0be-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3f0be-118">-ClusterName</span></span>
<span data-ttu-id="3f0be-119">Nome del cluster in cui è presente il database.</span><span class="sxs-lookup"><span data-stu-id="3f0be-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0be-120">-DefaultProfile</span></span>
<span data-ttu-id="3f0be-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f0be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f0be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f0be-122">-InputObject</span></span>
<span data-ttu-id="3f0be-123">Oggetto cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="3f0be-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0be-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f0be-124">-Name</span></span>
<span data-ttu-id="3f0be-125">nome del database.</span><span class="sxs-lookup"><span data-stu-id="3f0be-125">the name of the database.</span></span>

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

### <span data-ttu-id="3f0be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f0be-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f0be-127">Nome del gruppo di risorse in cui l'utente vuole recuperare il cluster.</span><span class="sxs-lookup"><span data-stu-id="3f0be-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0be-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f0be-128">-ResourceId</span></span>
<span data-ttu-id="3f0be-129">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="3f0be-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0be-130">CommonParameters</span></span>
<span data-ttu-id="3f0be-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f0be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0be-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f0be-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0be-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f0be-133">INPUTS</span></span>

### <span data-ttu-id="3f0be-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3f0be-134">System.String</span></span>

### <span data-ttu-id="3f0be-135">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3f0be-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="3f0be-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f0be-136">OUTPUTS</span></span>

### <span data-ttu-id="3f0be-137">Microsoft. Azure. Commands. kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="3f0be-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="3f0be-138">Note</span><span class="sxs-lookup"><span data-stu-id="3f0be-138">NOTES</span></span>

## <span data-ttu-id="3f0be-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f0be-139">RELATED LINKS</span></span>
