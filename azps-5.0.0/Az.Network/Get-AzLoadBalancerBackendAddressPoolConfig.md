---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199691"
---
# <span data-ttu-id="4f43f-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f43f-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4f43f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f43f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f43f-103">Ottiene una configurazione del pool di indirizzi back-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="4f43f-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="4f43f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f43f-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f43f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f43f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f43f-106">Il cmdlet **Get-AzLoadBalancerBackendAddressPoolConfig** ottiene un singolo pool di indirizzi back-end o un elenco di pool di indirizzi backend all'interno di un gruppo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="4f43f-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="4f43f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f43f-107">EXAMPLES</span></span>

### <span data-ttu-id="4f43f-108">Esempio 1: ottenere il pool di indirizzi back-end</span><span class="sxs-lookup"><span data-stu-id="4f43f-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4f43f-109">Il primo comando ottiene un bilanciamento del carico esistente denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4f43f-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="4f43f-110">Il secondo comando ottiene la configurazione del pool di indirizzi back-end associata denominata BackendAddressPool02 per il bilanciamento del carico in $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4f43f-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4f43f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f43f-111">PARAMETERS</span></span>

### <span data-ttu-id="4f43f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f43f-112">-DefaultProfile</span></span>
<span data-ttu-id="4f43f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f43f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f43f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4f43f-114">-LoadBalancer</span></span>
<span data-ttu-id="4f43f-115">Specifica il bilanciamento del carico associato al pool di indirizzi back-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4f43f-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f43f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f43f-116">-Name</span></span>
<span data-ttu-id="4f43f-117">Specifica il nome del bilanciamento del carico che contiene il pool di indirizzi di backend da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4f43f-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="4f43f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f43f-118">CommonParameters</span></span>
<span data-ttu-id="4f43f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f43f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f43f-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f43f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f43f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f43f-121">INPUTS</span></span>

### <span data-ttu-id="4f43f-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4f43f-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4f43f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f43f-123">OUTPUTS</span></span>

### <span data-ttu-id="4f43f-124">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f43f-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="4f43f-125">Note</span><span class="sxs-lookup"><span data-stu-id="4f43f-125">NOTES</span></span>

## <span data-ttu-id="4f43f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f43f-126">RELATED LINKS</span></span>

[<span data-ttu-id="4f43f-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f43f-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4f43f-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4f43f-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4f43f-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f43f-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4f43f-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f43f-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)

