---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203189"
---
# <span data-ttu-id="9fce9-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9fce9-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="9fce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fce9-102">SYNOPSIS</span></span>
<span data-ttu-id="9fce9-103">Aggiunge una configurazione del pool di indirizzi back-end a un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9fce9-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="9fce9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fce9-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fce9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9fce9-105">DESCRIPTION</span></span>
<span data-ttu-id="9fce9-106">Il cmdlet **Add-AzLoadBalancerBackend aggiunge** un pool di indirizzi back-end a una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="9fce9-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="9fce9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fce9-107">EXAMPLES</span></span>

### <span data-ttu-id="9fce9-108">Esempio 1: Aggiungere una configurazione del pool di indirizzi back-end a una bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="9fce9-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="9fce9-109">Questo comando recupera la bilanciamento del carico denominata MyLoadBalancer, aggiunge il pool di indirizzi back-end denominato BackendAddressPool02 a MyLoadBalancer e quindi usa il cmdlet **Set-AzLoadBalancer** per aggiornare MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="9fce9-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="9fce9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fce9-110">PARAMETERS</span></span>

### <span data-ttu-id="9fce9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fce9-111">-DefaultProfile</span></span>
<span data-ttu-id="9fce9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fce9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fce9-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fce9-113">-LoadBalancer</span></span>
<span data-ttu-id="9fce9-114">Specifica un **oggetto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="9fce9-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="9fce9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9fce9-115">-Name</span></span>
<span data-ttu-id="9fce9-116">Specifica il nome della configurazione del pool di indirizzi back-end da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9fce9-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="9fce9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fce9-117">-Confirm</span></span>
<span data-ttu-id="9fce9-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fce9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fce9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fce9-119">-WhatIf</span></span>
<span data-ttu-id="9fce9-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fce9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fce9-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fce9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fce9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fce9-122">CommonParameters</span></span>
<span data-ttu-id="9fce9-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fce9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fce9-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fce9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fce9-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="9fce9-125">INPUTS</span></span>

### <span data-ttu-id="9fce9-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fce9-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9fce9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fce9-127">OUTPUTS</span></span>

### <span data-ttu-id="9fce9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fce9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9fce9-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="9fce9-129">NOTES</span></span>

## <span data-ttu-id="9fce9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fce9-130">RELATED LINKS</span></span>

[<span data-ttu-id="9fce9-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fce9-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9fce9-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9fce9-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="9fce9-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9fce9-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9fce9-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9fce9-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="9fce9-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9fce9-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


