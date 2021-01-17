---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357797"
---
# <span data-ttu-id="38f7f-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="38f7f-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="38f7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="38f7f-103">Creare una regola di rete.</span><span class="sxs-lookup"><span data-stu-id="38f7f-103">Create a network rule.</span></span>

## <span data-ttu-id="38f7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38f7f-104">SYNTAX</span></span>

### <span data-ttu-id="38f7f-105">ByVirtualNetworkRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38f7f-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38f7f-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="38f7f-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f7f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38f7f-107">DESCRIPTION</span></span>
<span data-ttu-id="38f7f-108">Creare un oggetto regola di rete nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38f7f-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="38f7f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38f7f-109">EXAMPLES</span></span>

### <span data-ttu-id="38f7f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38f7f-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="38f7f-111">Creare un set di regole virtualnetwork.</span><span class="sxs-lookup"><span data-stu-id="38f7f-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="38f7f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38f7f-112">PARAMETERS</span></span>

### <span data-ttu-id="38f7f-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="38f7f-113">-Action</span></span>
<span data-ttu-id="38f7f-114">Azione della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="38f7f-114">The action of network rule.</span></span>

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

### <span data-ttu-id="38f7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f7f-115">-DefaultProfile</span></span>
<span data-ttu-id="38f7f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38f7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38f7f-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="38f7f-117">-IPAddressOrRange</span></span>
<span data-ttu-id="38f7f-118">Specifica l'intervallo IP o IP in formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="38f7f-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="38f7f-119">È consentito solo l'indirizzo IPV4.</span><span class="sxs-lookup"><span data-stu-id="38f7f-119">Only IPV4 address is allowed.</span></span>

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

### <span data-ttu-id="38f7f-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="38f7f-120">-IPRule</span></span>
<span data-ttu-id="38f7f-121">Indicare per creare IPRule.</span><span class="sxs-lookup"><span data-stu-id="38f7f-121">Indicate to create IPRule.</span></span>

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

### <span data-ttu-id="38f7f-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="38f7f-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="38f7f-123">ID risorsa di una subnet, ad esempio:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="38f7f-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

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

### <span data-ttu-id="38f7f-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="38f7f-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="38f7f-125">Indicare per creare VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="38f7f-125">Indicate to create VirtualNetworkRule.</span></span>

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

### <span data-ttu-id="38f7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f7f-126">CommonParameters</span></span>
<span data-ttu-id="38f7f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f7f-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38f7f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f7f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38f7f-129">INPUTS</span></span>

### <span data-ttu-id="38f7f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="38f7f-130">System.String</span></span>

## <span data-ttu-id="38f7f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38f7f-131">OUTPUTS</span></span>

### <span data-ttu-id="38f7f-132">Microsoft. Azure. Commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="38f7f-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="38f7f-133">Note</span><span class="sxs-lookup"><span data-stu-id="38f7f-133">NOTES</span></span>

## <span data-ttu-id="38f7f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38f7f-134">RELATED LINKS</span></span>
