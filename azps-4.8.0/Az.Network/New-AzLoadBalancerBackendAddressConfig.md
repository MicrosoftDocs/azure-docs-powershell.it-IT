---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192791"
---
# <span data-ttu-id="6177b-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="6177b-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="6177b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6177b-102">SYNOPSIS</span></span>
<span data-ttu-id="6177b-103">Restituisce una configurazione dell'indirizzo backend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6177b-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="6177b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6177b-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6177b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6177b-105">DESCRIPTION</span></span>
<span data-ttu-id="6177b-106">Restituisce una configurazione dell'indirizzo backend del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6177b-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="6177b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6177b-107">EXAMPLES</span></span>

### <span data-ttu-id="6177b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6177b-108">Example 1</span></span>
### <span data-ttu-id="6177b-109">Esempio 2: nuova configurazione dell'indirizzo LoadBalancer con riferimento alla rete virtuale</span><span class="sxs-lookup"><span data-stu-id="6177b-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="6177b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6177b-110">PARAMETERS</span></span>

### <span data-ttu-id="6177b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6177b-111">-DefaultProfile</span></span>
<span data-ttu-id="6177b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6177b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6177b-113">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6177b-113">-IpAddress</span></span>
<span data-ttu-id="6177b-114">IPAddress da aggiungere al pool back-end</span><span class="sxs-lookup"><span data-stu-id="6177b-114">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6177b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6177b-115">-Name</span></span>
<span data-ttu-id="6177b-116">Nome della configurazione dell'indirizzo back-end</span><span class="sxs-lookup"><span data-stu-id="6177b-116">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6177b-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6177b-117">-VirtualNetworkId</span></span>
<span data-ttu-id="6177b-118">Rete virtuale associata alla configurazione dell'indirizzo backend</span><span class="sxs-lookup"><span data-stu-id="6177b-118">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6177b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6177b-119">-Confirm</span></span>
<span data-ttu-id="6177b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6177b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6177b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6177b-121">-WhatIf</span></span>
<span data-ttu-id="6177b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6177b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6177b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6177b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6177b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6177b-124">CommonParameters</span></span>
<span data-ttu-id="6177b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6177b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6177b-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6177b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6177b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6177b-127">INPUTS</span></span>

### <span data-ttu-id="6177b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6177b-128">System.String</span></span>

### <span data-ttu-id="6177b-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6177b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6177b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6177b-130">OUTPUTS</span></span>

### <span data-ttu-id="6177b-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="6177b-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="6177b-132">Note</span><span class="sxs-lookup"><span data-stu-id="6177b-132">NOTES</span></span>

## <span data-ttu-id="6177b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6177b-133">RELATED LINKS</span></span>
