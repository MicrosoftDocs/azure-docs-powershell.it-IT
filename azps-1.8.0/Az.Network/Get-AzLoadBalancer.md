---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 38a8083b96915ad40aafcb4437b88d9266cae1bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678520"
---
# <span data-ttu-id="5ae65-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ae65-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="5ae65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ae65-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae65-103">Ottiene un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5ae65-103">Gets a load balancer.</span></span>

## <span data-ttu-id="5ae65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ae65-104">SYNTAX</span></span>

### <span data-ttu-id="5ae65-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ae65-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ae65-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="5ae65-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ae65-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ae65-107">DESCRIPTION</span></span>
<span data-ttu-id="5ae65-108">Il cmdlet **Get-AzLoadBalancer** ottiene uno o più gruppi di bilanciamento del carico di Azure contenuti in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ae65-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="5ae65-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ae65-109">EXAMPLES</span></span>

### <span data-ttu-id="5ae65-110">Esempio 1: ottenere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="5ae65-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="5ae65-111">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="5ae65-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="5ae65-112">Prima di poter eseguire questo cmdlet deve esistere un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5ae65-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="5ae65-113">Esempio 2: elenco di bilanciamento del carico tramite filtro</span><span class="sxs-lookup"><span data-stu-id="5ae65-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="5ae65-114">Questo comando ottiene tutti i bilanciatori di carico con un nome che inizia con "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="5ae65-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="5ae65-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ae65-115">PARAMETERS</span></span>

### <span data-ttu-id="5ae65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae65-116">-DefaultProfile</span></span>
<span data-ttu-id="5ae65-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ae65-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ae65-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5ae65-118">-ExpandResource</span></span>
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

### <span data-ttu-id="5ae65-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ae65-119">-Name</span></span>
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

### <span data-ttu-id="5ae65-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae65-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5ae65-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae65-121">CommonParameters</span></span>
<span data-ttu-id="5ae65-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae65-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae65-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ae65-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae65-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ae65-124">INPUTS</span></span>

### <span data-ttu-id="5ae65-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5ae65-125">System.String</span></span>

## <span data-ttu-id="5ae65-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ae65-126">OUTPUTS</span></span>

### <span data-ttu-id="5ae65-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ae65-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5ae65-128">Note</span><span class="sxs-lookup"><span data-stu-id="5ae65-128">NOTES</span></span>

## <span data-ttu-id="5ae65-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ae65-129">RELATED LINKS</span></span>

[<span data-ttu-id="5ae65-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ae65-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="5ae65-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ae65-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="5ae65-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5ae65-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


