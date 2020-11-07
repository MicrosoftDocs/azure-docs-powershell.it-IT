---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 3538a74b2ac638270d5487039faf9f8268d6efa8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866312"
---
# <span data-ttu-id="623d8-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="623d8-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="623d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="623d8-102">SYNOPSIS</span></span>
<span data-ttu-id="623d8-103">Aggiunge una configurazione del pool di indirizzi back-end a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="623d8-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="623d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="623d8-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="623d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="623d8-105">DESCRIPTION</span></span>
<span data-ttu-id="623d8-106">Il cmdlet **Add-AzureRmLoadBalancerBackend** aggiunge un pool di indirizzi back-end a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="623d8-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="623d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="623d8-107">EXAMPLES</span></span>

### <span data-ttu-id="623d8-108">Esempio 1 aggiungere una configurazione del pool di indirizzi back-end a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="623d8-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="623d8-109">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer, aggiunge il pool di indirizzi back-end denominato BackendAddressPool02 a MyLoadBalancer e quindi usa il cmdlet **set-AzureRmLoadBalancer** per aggiornare MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="623d8-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="623d8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="623d8-110">PARAMETERS</span></span>

### <span data-ttu-id="623d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623d8-111">-DefaultProfile</span></span>
<span data-ttu-id="623d8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="623d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623d8-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="623d8-113">-LoadBalancer</span></span>
<span data-ttu-id="623d8-114">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="623d8-114">Specifies a **LoadBalancer** object.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623d8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="623d8-115">-Name</span></span>
<span data-ttu-id="623d8-116">Specifica il nome della configurazione del pool di indirizzi back-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="623d8-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="623d8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623d8-117">CommonParameters</span></span>
<span data-ttu-id="623d8-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623d8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623d8-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="623d8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623d8-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="623d8-120">INPUTS</span></span>

### <span data-ttu-id="623d8-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="623d8-121">PSLoadBalancer</span></span>
<span data-ttu-id="623d8-122">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="623d8-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="623d8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="623d8-123">OUTPUTS</span></span>

### <span data-ttu-id="623d8-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="623d8-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="623d8-125">Note</span><span class="sxs-lookup"><span data-stu-id="623d8-125">NOTES</span></span>

## <span data-ttu-id="623d8-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="623d8-126">RELATED LINKS</span></span>

[<span data-ttu-id="623d8-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="623d8-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="623d8-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="623d8-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="623d8-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="623d8-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="623d8-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="623d8-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="623d8-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="623d8-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


