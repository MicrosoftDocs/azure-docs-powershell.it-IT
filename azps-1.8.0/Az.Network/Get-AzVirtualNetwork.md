---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: da0dde546d5875c1a29bd02805f40c7f12a68188
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678446"
---
# <span data-ttu-id="82862-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82862-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="82862-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82862-102">SYNOPSIS</span></span>
<span data-ttu-id="82862-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82862-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="82862-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82862-104">SYNTAX</span></span>

### <span data-ttu-id="82862-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="82862-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82862-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="82862-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82862-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82862-107">DESCRIPTION</span></span>
<span data-ttu-id="82862-108">Il cmdlet **Get-AzVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82862-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="82862-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82862-109">EXAMPLES</span></span>

### <span data-ttu-id="82862-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="82862-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="82862-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="82862-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="82862-112">2: elencare reti virtuali tramite filtro</span><span class="sxs-lookup"><span data-stu-id="82862-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="82862-113">Questo comando consente di ottenere tutte le reti virtuali che iniziano con "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="82862-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="82862-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82862-114">PARAMETERS</span></span>

### <span data-ttu-id="82862-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82862-115">-DefaultProfile</span></span>
<span data-ttu-id="82862-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82862-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82862-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="82862-117">-ExpandResource</span></span>
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

### <span data-ttu-id="82862-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="82862-118">-Name</span></span>
<span data-ttu-id="82862-119">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82862-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="82862-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82862-120">-ResourceGroupName</span></span>
<span data-ttu-id="82862-121">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="82862-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="82862-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82862-122">CommonParameters</span></span>
<span data-ttu-id="82862-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82862-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82862-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82862-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82862-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82862-125">INPUTS</span></span>

### <span data-ttu-id="82862-126">System. String</span><span class="sxs-lookup"><span data-stu-id="82862-126">System.String</span></span>

## <span data-ttu-id="82862-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82862-127">OUTPUTS</span></span>

### <span data-ttu-id="82862-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82862-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="82862-129">Note</span><span class="sxs-lookup"><span data-stu-id="82862-129">NOTES</span></span>

## <span data-ttu-id="82862-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82862-130">RELATED LINKS</span></span>

[<span data-ttu-id="82862-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82862-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="82862-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82862-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="82862-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82862-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


