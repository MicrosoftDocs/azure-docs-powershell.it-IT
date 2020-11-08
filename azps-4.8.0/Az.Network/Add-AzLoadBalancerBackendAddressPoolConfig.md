---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192855"
---
# <span data-ttu-id="50ff0-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="50ff0-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="50ff0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="50ff0-103">Aggiunge una configurazione del pool di indirizzi back-end a un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="50ff0-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="50ff0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50ff0-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50ff0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="50ff0-106">Il cmdlet **Add-AzLoadBalancerBackend** aggiunge un pool di indirizzi back-end a un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="50ff0-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="50ff0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50ff0-107">EXAMPLES</span></span>

### <span data-ttu-id="50ff0-108">Esempio 1: aggiungere una configurazione del pool di indirizzi back-end a un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="50ff0-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="50ff0-109">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer, aggiunge il pool di indirizzi back-end denominato BackendAddressPool02 a MyLoadBalancer e quindi usa il cmdlet **set-AzLoadBalancer** per aggiornare MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="50ff0-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="50ff0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50ff0-110">PARAMETERS</span></span>

### <span data-ttu-id="50ff0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ff0-111">-DefaultProfile</span></span>
<span data-ttu-id="50ff0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50ff0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50ff0-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50ff0-113">-LoadBalancer</span></span>
<span data-ttu-id="50ff0-114">Specifica un oggetto **LoadBalancer** .</span><span class="sxs-lookup"><span data-stu-id="50ff0-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="50ff0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="50ff0-115">-Name</span></span>
<span data-ttu-id="50ff0-116">Specifica il nome della configurazione del pool di indirizzi back-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="50ff0-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ff0-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50ff0-117">-Confirm</span></span>
<span data-ttu-id="50ff0-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50ff0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ff0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50ff0-119">-WhatIf</span></span>
<span data-ttu-id="50ff0-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50ff0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50ff0-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50ff0-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ff0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ff0-122">CommonParameters</span></span>
<span data-ttu-id="50ff0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ff0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ff0-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ff0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ff0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50ff0-125">INPUTS</span></span>

### <span data-ttu-id="50ff0-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50ff0-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="50ff0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50ff0-127">OUTPUTS</span></span>

### <span data-ttu-id="50ff0-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50ff0-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="50ff0-129">Note</span><span class="sxs-lookup"><span data-stu-id="50ff0-129">NOTES</span></span>

## <span data-ttu-id="50ff0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50ff0-130">RELATED LINKS</span></span>

[<span data-ttu-id="50ff0-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50ff0-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="50ff0-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="50ff0-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="50ff0-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="50ff0-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="50ff0-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="50ff0-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="50ff0-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="50ff0-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


