---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860989"
---
# <span data-ttu-id="3f4c4-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3f4c4-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3f4c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4c4-103">Aggiunge una configurazione del pool di indirizzi back-end a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="3f4c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f4c4-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f4c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f4c4-105">DESCRIPTION</span></span>
<span data-ttu-id="3f4c4-106">Il cmdlet **Add-AzLoadBalancerBackend** aggiunge un pool di indirizzi back-end a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="3f4c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f4c4-107">EXAMPLES</span></span>

### <span data-ttu-id="3f4c4-108">Esempio 1 aggiungere una configurazione del pool di indirizzi back-end a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="3f4c4-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="3f4c4-109">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer, aggiunge il pool di indirizzi back-end denominato BackendAddressPool02 a MyLoadBalancer e quindi usa il cmdlet **set-AzLoadBalancer** per aggiornare MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="3f4c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f4c4-110">PARAMETERS</span></span>

### <span data-ttu-id="3f4c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4c4-111">-DefaultProfile</span></span>
<span data-ttu-id="3f4c4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f4c4-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f4c4-113">-LoadBalancer</span></span>
<span data-ttu-id="3f4c4-114">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="3f4c4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f4c4-115">-Name</span></span>
<span data-ttu-id="3f4c4-116">Specifica il nome della configurazione del pool di indirizzi back-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="3f4c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4c4-117">CommonParameters</span></span>
<span data-ttu-id="3f4c4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4c4-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4c4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f4c4-120">INPUTS</span></span>

### <span data-ttu-id="3f4c4-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f4c4-121">PSLoadBalancer</span></span>
<span data-ttu-id="3f4c4-122">Il parametro ' LoadBalancer ' accetta il valore di tipo ' PSLoadBalancer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3f4c4-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3f4c4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f4c4-123">OUTPUTS</span></span>

### <span data-ttu-id="3f4c4-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f4c4-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3f4c4-125">Note</span><span class="sxs-lookup"><span data-stu-id="3f4c4-125">NOTES</span></span>

## <span data-ttu-id="3f4c4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f4c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="3f4c4-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f4c4-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3f4c4-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f4c4-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="3f4c4-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3f4c4-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3f4c4-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3f4c4-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3f4c4-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3f4c4-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


