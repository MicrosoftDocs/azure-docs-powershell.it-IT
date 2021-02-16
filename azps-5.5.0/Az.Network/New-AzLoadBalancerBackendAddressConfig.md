---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179670"
---
# <span data-ttu-id="c5714-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="c5714-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="c5714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5714-102">SYNOPSIS</span></span>
<span data-ttu-id="c5714-103">Restituisce una configurazione di indirizzo back-end di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c5714-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="c5714-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5714-104">SYNTAX</span></span>

### <span data-ttu-id="c5714-105">SetByResourcePublicIpAddress (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5714-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5714-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5714-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5714-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5714-107">DESCRIPTION</span></span>
<span data-ttu-id="c5714-108">Restituisce una configurazione di indirizzo back-end di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c5714-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="c5714-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5714-109">EXAMPLES</span></span>

### <span data-ttu-id="c5714-110">Esempio 1: Nuova configurazione dell'indirizzo caricore con riferimento alla rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c5714-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="c5714-111">Esempio 2: Nuova configurazione dell'indirizzo caricore con riferimento alla configurazione ip di loadbalancer frontend</span><span class="sxs-lookup"><span data-stu-id="c5714-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="c5714-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5714-112">PARAMETERS</span></span>

### <span data-ttu-id="c5714-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5714-113">-DefaultProfile</span></span>
<span data-ttu-id="c5714-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5714-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5714-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c5714-115">-IpAddress</span></span>
<span data-ttu-id="c5714-116">IPAddress da aggiungere al pool back-end</span><span class="sxs-lookup"><span data-stu-id="c5714-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5714-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c5714-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="c5714-118">Configurazione IP frontend della bilanciamento del carico associata alla configurazione dell'indirizzo Backend</span><span class="sxs-lookup"><span data-stu-id="c5714-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5714-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5714-119">-Name</span></span>
<span data-ttu-id="c5714-120">Nome della configurazione dell'indirizzo back-end</span><span class="sxs-lookup"><span data-stu-id="c5714-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="c5714-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c5714-121">-VirtualNetworkId</span></span>
<span data-ttu-id="c5714-122">Rete virtuale associata alla configurazione dell'indirizzo back-end</span><span class="sxs-lookup"><span data-stu-id="c5714-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5714-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5714-123">-Confirm</span></span>
<span data-ttu-id="c5714-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5714-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5714-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5714-125">-WhatIf</span></span>
<span data-ttu-id="c5714-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5714-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5714-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5714-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5714-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5714-128">CommonParameters</span></span>
<span data-ttu-id="c5714-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5714-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5714-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5714-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5714-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5714-131">INPUTS</span></span>

### <span data-ttu-id="c5714-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c5714-132">System.String</span></span>

### <span data-ttu-id="c5714-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c5714-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c5714-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5714-134">OUTPUTS</span></span>

### <span data-ttu-id="c5714-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c5714-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="c5714-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5714-136">NOTES</span></span>

## <span data-ttu-id="c5714-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5714-137">RELATED LINKS</span></span>
