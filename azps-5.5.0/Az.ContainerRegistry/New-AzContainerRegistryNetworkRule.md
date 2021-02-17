---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196902"
---
# <span data-ttu-id="e5a46-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e5a46-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="e5a46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a46-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a46-103">Creare una regola di rete.</span><span class="sxs-lookup"><span data-stu-id="e5a46-103">Create a network rule.</span></span>

## <span data-ttu-id="e5a46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5a46-104">SYNTAX</span></span>

### <span data-ttu-id="e5a46-105">ByVirtualNetworkRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5a46-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a46-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="e5a46-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5a46-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5a46-107">DESCRIPTION</span></span>
<span data-ttu-id="e5a46-108">Creare un oggetto regola di rete nella sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="e5a46-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="e5a46-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5a46-109">EXAMPLES</span></span>

### <span data-ttu-id="e5a46-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5a46-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="e5a46-111">Creare un set di regole virtualnetwork.</span><span class="sxs-lookup"><span data-stu-id="e5a46-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="e5a46-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5a46-112">PARAMETERS</span></span>

### <span data-ttu-id="e5a46-113">-Action</span><span class="sxs-lookup"><span data-stu-id="e5a46-113">-Action</span></span>
<span data-ttu-id="e5a46-114">Azione della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="e5a46-114">The action of network rule.</span></span>

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

### <span data-ttu-id="e5a46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a46-115">-DefaultProfile</span></span>
<span data-ttu-id="e5a46-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a46-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e5a46-117">-IPAddressOrRange</span></span>
<span data-ttu-id="e5a46-118">Specifica l'intervallo IP o IP in formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="e5a46-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="e5a46-119">È consentito solo l'indirizzo IPV4.</span><span class="sxs-lookup"><span data-stu-id="e5a46-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a46-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="e5a46-120">-IPRule</span></span>
<span data-ttu-id="e5a46-121">Indicare di creare IPRule.</span><span class="sxs-lookup"><span data-stu-id="e5a46-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a46-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e5a46-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e5a46-123">ID risorsa di una subnet, ad esempio: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="e5a46-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a46-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e5a46-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="e5a46-125">Indicare di creare VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="e5a46-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a46-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a46-126">CommonParameters</span></span>
<span data-ttu-id="e5a46-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a46-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a46-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5a46-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a46-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5a46-129">INPUTS</span></span>

### <span data-ttu-id="e5a46-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e5a46-130">System.String</span></span>

## <span data-ttu-id="e5a46-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5a46-131">OUTPUTS</span></span>

### <span data-ttu-id="e5a46-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e5a46-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="e5a46-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5a46-133">NOTES</span></span>

## <span data-ttu-id="e5a46-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5a46-134">RELATED LINKS</span></span>
