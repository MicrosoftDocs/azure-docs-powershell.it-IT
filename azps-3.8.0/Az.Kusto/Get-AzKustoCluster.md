---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 6e24eaee77e8965ea34cbfcd8c169d675bce56d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019092"
---
# <span data-ttu-id="d1bc0-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d1bc0-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="d1bc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bc0-103">Elencare tutti i cluster di Kusto in un gruppo di risorse o ottenere uno specifico cluster di Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="d1bc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1bc0-104">SYNTAX</span></span>

### <span data-ttu-id="d1bc0-105">ByClusterOrResourceGroupOrSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1bc0-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1bc0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1bc0-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1bc0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="d1bc0-108">Elencare tutti i cluster di Kusto in un gruppo di risorse o ottenere uno specifico cluster di Kusto.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="d1bc0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1bc0-109">EXAMPLES</span></span>

### <span data-ttu-id="d1bc0-110">Esempio 1-elenca tutti i cluster di Kusto in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d1bc0-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="d1bc0-111">Digitare: Microsoft. kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg Name: mykustocluster1 location: Central US Capacity: 3 SKU: D13_v2 ProvisioningState: succeeded state: in corso Tag: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="d1bc0-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="d1bc0-112">Digitare: Microsoft. kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg nome: mykustocluster2 posizione: centrale US capacità: 5 SKU: D13_v2 ProvisioningState: stato riuscito: in corso Tag: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="d1bc0-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="d1bc0-113">Il comando precedente elenca tutti i cluster kusto nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="d1bc0-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="d1bc0-114">Esempio 2-ottenere un cluster specifico di Kusto per nome</span><span class="sxs-lookup"><span data-stu-id="d1bc0-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="d1bc0-115">Il comando precedente restituisce il cluster kusto denominato "mykustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="d1bc0-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="d1bc0-116">Esempio 3-ottenere un cluster kusto specifico per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="d1bc0-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="d1bc0-117">Il comando precedente restituisce il cluster kusto denominato "mykustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="d1bc0-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="d1bc0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1bc0-118">PARAMETERS</span></span>

### <span data-ttu-id="d1bc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bc0-119">-DefaultProfile</span></span>
<span data-ttu-id="d1bc0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1bc0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1bc0-121">-Name</span></span>
<span data-ttu-id="d1bc0-122">Nome di un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1bc0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bc0-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1bc0-124">Nome del gruppo di risorse in cui l'utente vuole recuperare il cluster.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="d1bc0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1bc0-125">-ResourceId</span></span>
<span data-ttu-id="d1bc0-126">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="d1bc0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bc0-127">CommonParameters</span></span>
<span data-ttu-id="d1bc0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bc0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bc0-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bc0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bc0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1bc0-130">INPUTS</span></span>

### <span data-ttu-id="d1bc0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d1bc0-131">System.String</span></span>

## <span data-ttu-id="d1bc0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1bc0-132">OUTPUTS</span></span>

### <span data-ttu-id="d1bc0-133">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d1bc0-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d1bc0-134">Note</span><span class="sxs-lookup"><span data-stu-id="d1bc0-134">NOTES</span></span>

## <span data-ttu-id="d1bc0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1bc0-135">RELATED LINKS</span></span>
