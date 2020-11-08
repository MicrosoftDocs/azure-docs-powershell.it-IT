---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021236"
---
# <span data-ttu-id="68206-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68206-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="68206-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68206-102">SYNOPSIS</span></span>
<span data-ttu-id="68206-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68206-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="68206-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68206-104">SYNTAX</span></span>

### <span data-ttu-id="68206-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="68206-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68206-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="68206-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68206-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68206-107">DESCRIPTION</span></span>
<span data-ttu-id="68206-108">Il cmdlet **Get-AzVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68206-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="68206-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68206-109">EXAMPLES</span></span>

### <span data-ttu-id="68206-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="68206-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="68206-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68206-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="68206-112">2: elencare reti virtuali tramite filtro</span><span class="sxs-lookup"><span data-stu-id="68206-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="68206-113">Questo comando consente di ottenere tutte le reti virtuali che iniziano con "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="68206-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="68206-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68206-114">PARAMETERS</span></span>

### <span data-ttu-id="68206-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68206-115">-DefaultProfile</span></span>
<span data-ttu-id="68206-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68206-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68206-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="68206-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68206-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="68206-118">-Name</span></span>
<span data-ttu-id="68206-119">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68206-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="68206-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68206-120">-ResourceGroupName</span></span>
<span data-ttu-id="68206-121">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="68206-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="68206-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68206-122">CommonParameters</span></span>
<span data-ttu-id="68206-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68206-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68206-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68206-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68206-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68206-125">INPUTS</span></span>

### <span data-ttu-id="68206-126">System. String</span><span class="sxs-lookup"><span data-stu-id="68206-126">System.String</span></span>

## <span data-ttu-id="68206-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68206-127">OUTPUTS</span></span>

### <span data-ttu-id="68206-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68206-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="68206-129">Note</span><span class="sxs-lookup"><span data-stu-id="68206-129">NOTES</span></span>

## <span data-ttu-id="68206-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68206-130">RELATED LINKS</span></span>

[<span data-ttu-id="68206-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68206-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="68206-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68206-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="68206-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68206-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


