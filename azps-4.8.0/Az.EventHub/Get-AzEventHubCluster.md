---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192493"
---
# <span data-ttu-id="1dbb9-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="1dbb9-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="1dbb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dbb9-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbb9-103">Ottiene i dettagli di un singolo cluster di hub eventi o restituisce un elenco di cluster di hub eventi.</span><span class="sxs-lookup"><span data-stu-id="1dbb9-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="1dbb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dbb9-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbb9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dbb9-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbb9-106">Il cmdlet Get-AzEventHubCluster restituisce i dettagli di un cluster di hub eventi o un elenco di tutti i cluster di hub eventi in un gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="1dbb9-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="1dbb9-107">Se viene fornito il nome del cluster, vengono restituiti i dettagli di un singolo cluster.</span><span class="sxs-lookup"><span data-stu-id="1dbb9-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="1dbb9-108">Se non viene specificato un nome di cluster, viene restituito un elenco di tutti i cluster nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1dbb9-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="1dbb9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dbb9-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbb9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dbb9-110">Example 1</span></span>
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

<span data-ttu-id="1dbb9-111">Restituisce il detials del cluster "Eventhub-cluster-5557" dal gruppo di risorse "RSG-Cluster27651"</span><span class="sxs-lookup"><span data-stu-id="1dbb9-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="1dbb9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dbb9-112">PARAMETERS</span></span>

### <span data-ttu-id="1dbb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbb9-113">-DefaultProfile</span></span>
<span data-ttu-id="1dbb9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbb9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dbb9-115">-Name</span></span>
<span data-ttu-id="1dbb9-116">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="1dbb9-116">Cluster Name</span></span>

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

### <span data-ttu-id="1dbb9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbb9-117">-ResourceGroupName</span></span>
<span data-ttu-id="1dbb9-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1dbb9-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1dbb9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbb9-119">CommonParameters</span></span>
<span data-ttu-id="1dbb9-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbb9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbb9-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dbb9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbb9-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dbb9-122">INPUTS</span></span>

### <span data-ttu-id="1dbb9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1dbb9-123">System.String</span></span>

## <span data-ttu-id="1dbb9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dbb9-124">OUTPUTS</span></span>

### <span data-ttu-id="1dbb9-125">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="1dbb9-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="1dbb9-126">Note</span><span class="sxs-lookup"><span data-stu-id="1dbb9-126">NOTES</span></span>

## <span data-ttu-id="1dbb9-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dbb9-127">RELATED LINKS</span></span>
