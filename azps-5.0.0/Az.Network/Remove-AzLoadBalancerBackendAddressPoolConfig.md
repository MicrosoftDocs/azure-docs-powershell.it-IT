---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199541"
---
# <span data-ttu-id="a67e7-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a67e7-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a67e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a67e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a67e7-103">Rimuove una configurazione del pool di indirizzi back-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a67e7-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="a67e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a67e7-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a67e7-105">DESCRIPTION</span></span>
<span data-ttu-id="a67e7-106">Il cmdlet **Remove-AzLoadBalancerBackendAddressPoolConfig** rimuove un pool di indirizzi back-end da un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a67e7-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="a67e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a67e7-107">EXAMPLES</span></span>

### <span data-ttu-id="a67e7-108">Esempio 1: rimuovere una configurazione del pool di indirizzi back-end da un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="a67e7-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="a67e7-109">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer e lo passa a **Remove-AzLoadBalancerBackendAddressPoolConfig** , che rimuove la configurazione di BackendAddressPool02 da MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a67e7-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="a67e7-110">Infine, il cmdlet Set-AzLoadBalancer Aggiorna MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a67e7-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="a67e7-111">Tieni presente che la configurazione del pool di indirizzi di backend deve esistere prima di poterla eliminare.</span><span class="sxs-lookup"><span data-stu-id="a67e7-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="a67e7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a67e7-112">PARAMETERS</span></span>

### <span data-ttu-id="a67e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67e7-113">-DefaultProfile</span></span>
<span data-ttu-id="a67e7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a67e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a67e7-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a67e7-115">-LoadBalancer</span></span>
<span data-ttu-id="a67e7-116">Specifica il bilanciamento del carico che contiene il pool di indirizzi back-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a67e7-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="a67e7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a67e7-117">-Name</span></span>
<span data-ttu-id="a67e7-118">Specifica il nome del pool di indirizzi back-end rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67e7-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a67e7-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a67e7-119">-Confirm</span></span>
<span data-ttu-id="a67e7-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67e7-121">-WhatIf</span></span>
<span data-ttu-id="a67e7-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a67e7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a67e7-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a67e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67e7-124">CommonParameters</span></span>
<span data-ttu-id="a67e7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67e7-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a67e7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67e7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a67e7-127">INPUTS</span></span>

### <span data-ttu-id="a67e7-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a67e7-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a67e7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a67e7-129">OUTPUTS</span></span>

### <span data-ttu-id="a67e7-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a67e7-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a67e7-131">Note</span><span class="sxs-lookup"><span data-stu-id="a67e7-131">NOTES</span></span>

## <span data-ttu-id="a67e7-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a67e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="a67e7-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a67e7-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a67e7-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a67e7-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a67e7-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a67e7-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a67e7-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a67e7-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

