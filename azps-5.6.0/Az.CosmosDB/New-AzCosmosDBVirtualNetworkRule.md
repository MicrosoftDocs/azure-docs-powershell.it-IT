---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: abc97b0473353a0bc71aae59386bc5b5770b730b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980797"
---
# <span data-ttu-id="7b082-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7b082-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="7b082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b082-102">SYNOPSIS</span></span>
<span data-ttu-id="7b082-103">Creare un nuovo oggettoDb VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="7b082-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="7b082-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b082-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b082-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b082-105">DESCRIPTION</span></span>
<span data-ttu-id="7b082-106">Creare un nuovo oggettoDb VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="7b082-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="7b082-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b082-107">EXAMPLES</span></span>

### <span data-ttu-id="7b082-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b082-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="7b082-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b082-109">PARAMETERS</span></span>

### <span data-ttu-id="7b082-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b082-110">-DefaultProfile</span></span>
<span data-ttu-id="7b082-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b082-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b082-112">-Id</span><span class="sxs-lookup"><span data-stu-id="7b082-112">-Id</span></span>
<span data-ttu-id="7b082-113">ID risorsa di una subnet, ad esempio: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="7b082-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="7b082-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b082-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="7b082-115">Booleano per indicare se creare una regola del firewall prima che la rete virtuale abbia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="7b082-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="7b082-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b082-116">CommonParameters</span></span>
<span data-ttu-id="7b082-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b082-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b082-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b082-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b082-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b082-119">INPUTS</span></span>

### <span data-ttu-id="7b082-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b082-120">None</span></span>

## <span data-ttu-id="7b082-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b082-121">OUTPUTS</span></span>

### <span data-ttu-id="7b082-122">Microsoft.Azure.Commands.CartelDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7b082-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="7b082-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b082-123">NOTES</span></span>

## <span data-ttu-id="7b082-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b082-124">RELATED LINKS</span></span>
