---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181302"
---
# <span data-ttu-id="61a8d-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61a8d-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="61a8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="61a8d-103">Creare un nuovo oggettoDb VirtualNetworkRule(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="61a8d-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="61a8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61a8d-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a8d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="61a8d-106">Creare un nuovo oggettoDb VirtualNetworkRule(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="61a8d-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="61a8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61a8d-107">EXAMPLES</span></span>

### <span data-ttu-id="61a8d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61a8d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="61a8d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61a8d-109">PARAMETERS</span></span>

### <span data-ttu-id="61a8d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a8d-110">-DefaultProfile</span></span>
<span data-ttu-id="61a8d-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61a8d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a8d-112">-Id</span><span class="sxs-lookup"><span data-stu-id="61a8d-112">-Id</span></span>
<span data-ttu-id="61a8d-113">ID risorsa di una subnet, ad esempio: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="61a8d-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="61a8d-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="61a8d-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="61a8d-115">Booleano per indicare se creare una regola del firewall prima che la rete virtuale abbia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="61a8d-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="61a8d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a8d-116">CommonParameters</span></span>
<span data-ttu-id="61a8d-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a8d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a8d-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61a8d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a8d-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="61a8d-119">INPUTS</span></span>

### <span data-ttu-id="61a8d-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61a8d-120">None</span></span>

## <span data-ttu-id="61a8d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61a8d-121">OUTPUTS</span></span>

### <span data-ttu-id="61a8d-122">Microsoft.Azure.Commands.EnterpriseDb.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="61a8d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="61a8d-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="61a8d-123">NOTES</span></span>

## <span data-ttu-id="61a8d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61a8d-124">RELATED LINKS</span></span>
