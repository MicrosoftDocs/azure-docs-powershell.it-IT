---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190337"
---
# <span data-ttu-id="ce293-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce293-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="ce293-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce293-102">SYNOPSIS</span></span>
<span data-ttu-id="ce293-103">Crea un nuovo oggetto CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="ce293-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="ce293-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce293-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce293-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce293-105">DESCRIPTION</span></span>
<span data-ttu-id="ce293-106">Crea un nuovo oggetto CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="ce293-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="ce293-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce293-107">EXAMPLES</span></span>

### <span data-ttu-id="ce293-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce293-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="ce293-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce293-109">PARAMETERS</span></span>

### <span data-ttu-id="ce293-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce293-110">-DefaultProfile</span></span>
<span data-ttu-id="ce293-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce293-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce293-112">-ID</span><span class="sxs-lookup"><span data-stu-id="ce293-112">-Id</span></span>
<span data-ttu-id="ce293-113">ID risorsa di una subnet, ad esempio:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="ce293-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce293-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce293-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="ce293-115">Booleano per indicare se creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="ce293-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce293-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce293-116">CommonParameters</span></span>
<span data-ttu-id="ce293-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce293-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce293-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce293-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce293-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce293-119">INPUTS</span></span>

### <span data-ttu-id="ce293-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ce293-120">None</span></span>

## <span data-ttu-id="ce293-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce293-121">OUTPUTS</span></span>

### <span data-ttu-id="ce293-122">Microsoft. Azure. Commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce293-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="ce293-123">Note</span><span class="sxs-lookup"><span data-stu-id="ce293-123">NOTES</span></span>

## <span data-ttu-id="ce293-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce293-124">RELATED LINKS</span></span>