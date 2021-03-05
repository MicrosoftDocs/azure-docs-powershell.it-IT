---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 22bbbb79f8662f1e1e70785489187e68e5b38813
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983133"
---
# <span data-ttu-id="75db2-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="75db2-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="75db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75db2-102">SYNOPSIS</span></span>
<span data-ttu-id="75db2-103">Recupera i dettagli di un singolo cluster di hub eventi o ottiene un elenco di cluster di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="75db2-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="75db2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75db2-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75db2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75db2-105">DESCRIPTION</span></span>
<span data-ttu-id="75db2-106">Il Get-AzEventHubCluster cmdlet restituisce i dettagli di un cluster di hub eventi o un elenco di tutti i cluster di hub eventi in un determinato gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75db2-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="75db2-107">Se viene specificato il nome del cluster, vengono restituiti i dettagli di un singolo cluster.</span><span class="sxs-lookup"><span data-stu-id="75db2-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="75db2-108">Se non viene fornito il nome di un cluster, viene restituito un elenco di tutti i cluster nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="75db2-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="75db2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75db2-109">EXAMPLES</span></span>

### <span data-ttu-id="75db2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75db2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="75db2-111">Restituisce i detial del cluster 'Eventhub-Cluster-5557' dal gruppo di risorse 'RSG-Cluster27651'</span><span class="sxs-lookup"><span data-stu-id="75db2-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="75db2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75db2-112">PARAMETERS</span></span>

### <span data-ttu-id="75db2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75db2-113">-DefaultProfile</span></span>
<span data-ttu-id="75db2-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75db2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75db2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="75db2-115">-Name</span></span>
<span data-ttu-id="75db2-116">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="75db2-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75db2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75db2-117">-ResourceGroupName</span></span>
<span data-ttu-id="75db2-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="75db2-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75db2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75db2-119">CommonParameters</span></span>
<span data-ttu-id="75db2-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75db2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75db2-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75db2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75db2-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="75db2-122">INPUTS</span></span>

### <span data-ttu-id="75db2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="75db2-123">System.String</span></span>

## <span data-ttu-id="75db2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75db2-124">OUTPUTS</span></span>

### <span data-ttu-id="75db2-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="75db2-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="75db2-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="75db2-126">NOTES</span></span>

## <span data-ttu-id="75db2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75db2-127">RELATED LINKS</span></span>
